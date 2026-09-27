# 🎯 Open Source Contribution Targets

This document tracks selected open-source issues aligned with your technical stack (Python, FastAPI, SQLite, and Data Engineering). No development has started yet—use this as a reference when you are ready to propose fixes and submit PRs.

---

## 1. 📊 `ibis-project/ibis` — MSSQL Sample vs. Population Stddev Mismatch

- **Repository**: [ibis-project/ibis](https://github.com/ibis-project/ibis) (12k+ ⭐ | Modern Python Data Portability Layer)
- **Issue**: [#12057 — bug: MSSQL dialect rewrites STDEV (sample) to STDEVP (population) when round-tripping SQL through Backend.sql()](https://github.com/ibis-project/ibis/issues/12057)
- **Status**: Open • Unassigned • 0 Comments • 0 PRs

### Summary & Root Cause
In `ibis.backends.sql.dialects.MSSQL`, the AST node `sge.Stddev` is mapped to `stdevp`:
```python
sge.Stddev: rename_func("stdevp")
```
In T-SQL (MSSQL), `STDEV` computes the **sample standard deviation**, while `STDEVP` computes the **population standard deviation**. Round-tripping T-SQL through `Backend.sql()` alters the statistical semantics of the query.

### Reproduction
```python
import sqlglot
from ibis.backends.sql.dialects import MSSQL

# Currently outputs SELECT STDEVP([x]) AS [s] FROM [t] (incorrect)
print(sqlglot.transpile("SELECT STDEV([x]) AS [s] FROM [t]", read=MSSQL, write=MSSQL)[0])
```

### Proposed Fix
1. In `ibis/backends/sql/dialects/mssql.py`, change `rename_func("stdevp")` to `rename_func("stdev")`.
2. Add a regression test in `tests/dialects/test_mssql.py` verifying that `STDEV([x])` preserves `STDEV`.

---

## 2. ⚡ `encode/databases` — SQLite Connection Lock on Commit Failure

- **Repository**: [encode/databases](https://github.com/encode/databases) (3.8k+ ⭐ | Async SQL database support for Python/FastAPI)
- **Issue**: [#594 — Handle errors in transaction.commit() (for sqlite)](https://github.com/encode/databases/issues/594)
- **Status**: Open • Unassigned • 0 Comments • 0 PRs

### Summary & Root Cause
In `databases/core.py` within `Transaction.commit()`:
```python
class Transaction:
    async def commit(self) -> None:
        async with self._connection._transaction_lock:
            assert self._connection._transaction_stack[-1] is self
            self._connection._transaction_stack.pop()  # <--- Pops BEFORE commit execution
            assert self._transaction is not None
            await self._transaction.commit()
            await self._connection.__aexit__()
            self._transaction = None
```
In SQLite, deferred foreign key and constraint checks are validated at `COMMIT` time. Because `pop()` executes before `await self._transaction.commit()`, if `commit()` raises, the transaction is already lost from the stack. The caller cannot roll back, leaving the SQLite database in a locked state.

### Reproduction
```sql
PRAGMA foreign_keys = ON;
BEGIN TRANSACTION;
INSERT INTO "follow" ("user_id", "target_id") VALUES (0, 0); -- fails FK
COMMIT; -- Error raised here, transaction popped prematurely
```

### Proposed Fix
1. Only pop `self._connection._transaction_stack.pop()` after `await self._transaction.commit()` completes successfully.
2. In `Transaction.__aexit__`, wrap the `commit()` call in a `try...except` block so that any error triggers `await self.rollback()` before re-raising.
3. Add a unit test simulating a SQLite commit-time constraint failure.

---

## 3. 🌐 `encode/starlette` — Leading `//` Path Netloc Parsing without Host Header

- **Repository**: [encode/starlette](https://github.com/encode/starlette) (11k+ ⭐ | The ASGI engine behind FastAPI)
- **Issue**: [#3579 — Request.url turns a // path into an authority when the scope has no host](https://github.com/encode/starlette/issues/3579)
- **Status**: Open • Unassigned • 0 Comments • 0 PRs

### Summary & Root Cause
When an ASGI request scope contains neither a `Host` header nor a `server` entry (which is legal under the ASGI HTTP specification), `Request.url` places `scope["path"]` directly after the scheme:
```python
scope = {
    "type": "http",
    "scheme": "http",
    "path": "//evil.example/x",
    "query_string": b"a=1",
    "headers": [],
    "server": None,
}
url = Request(scope).url
# Parses evil.example as url.netloc (authority)
```
If an application constructs a `RedirectResponse(request.url)`, it inadvertently redirects the client to `http://evil.example/x?a=1` (open redirect vulnerability).

### Proposed Fix
1. In `starlette/requests.py` / `starlette/datastructures.py`, ensure that when building the URL without origin/host metadata, leading double slashes (`//`) in the path are normalized or escaped so they cannot be parsed into an authority/netloc.
2. Add a test in `tests/test_requests.py` verifying `Request(scope).url` behavior when `headers=[]` and `path="//evil.example/x"`.

---

## 🛠️ Contributor Workflow Reference

When you decide to tackle one of these:

```bash
# 1. Fork and clone the target repository
gh repo fork <owner/repo> --clone

# 2. Enforce your personal git identity locally
git config --local user.name "joseamair"
git config --local user.email "joseamair@gmail.com"

# 3. Create a feature branch
git checkout -b fix/<short-description>

# 4. Run tests with uv / pytest
uv run pytest -v

# 5. Push using strict token isolation
$token = (gh auth token --user joseamair)
$b64 = [Convert]::ToBase64String([Text.Encoding]::ASCII.GetBytes("x-access-token:$token"))
git -c http.extraheader="Authorization: Basic $b64" push -u origin fix/<short-description>

# 6. Create the pull request
$env:GH_TOKEN = (gh auth token --user joseamair)
gh pr create --title "fix: ..." --body "Fixes #<issue-number>..."
```
