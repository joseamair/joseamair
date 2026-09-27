<div align="center">

# Hi there, I'm Jose Gabriel Kordahi Amair 👋

<a href="https://github.com/joseamair">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=38BDF8&center=true&vCenter=true&width=750&lines=Data+%26+Software+Engineer+%289%2B+Years%29%3BLLM-Grounding+Platforms+%26+Evaluation+Tooling%3BPython-Centric+ETL+%26+Dataset+Curation%3BEnterprise+Audio+ML+Pipelines%3BB.Sc.+Systems+Engineering+%7C+Control+%26+Automation" alt="Typing SVG" />
</a>

<p align="center">
  <a href="mailto:joseamair@gmail.com"><img src="https://img.shields.io/badge/Email-joseamair%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  <a href="https://github.com/joseamair"><img src="https://img.shields.io/badge/GitHub-joseamair-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" /></a>
  <a href="https://www.linkedin.com/in/joseamair/"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <img src="https://img.shields.io/badge/Location-Kraków%2C%20Poland%20🇵🇱-334155?style=for-the-badge&logo=googlemaps&logoColor=white" alt="Location" />
</p>

</div>

---

### 👨‍💻 Professional Summary

Data Engineer with **9+ years** in data delivery, annotation, and validation for large-scale audio ML pipelines, now building LLM-grounding data platforms and evaluation tooling. Specialized in Python-centric ETL, dataset curation, and enforcing strict metadata traceability and licensing compliance across global organizations.

- 🚀 **Industry Experience:** 9+ years across **Kedara.care**, **Cisco**, and **BabbleLabs** delivering production audio datasets, ETL pipelines, and knowledge-base ingestion.
- 📊 **Data Engineering & ETL:** Practical experience with Python, SQL, MongoDB, Typesense, Apache Airflow, Kafka, and data quality validation across 200K+ records.
- 🤖 **Applied AI & Tooling:** Building LLM evaluation scenarios (LLM-as-a-Judge, OpenRouter), voice model benchmarking (ElevenLabs, Whisper), and exploring developer CLI tooling.
- 🎓 **Education:** B.Sc. in Systems Engineering from Universidad de Los Andes (Specialization in Control & Automation).

---

### 💼 Professional Journey & Experience

| Period | Company / Institution | Role | Core Focus |
| :--- | :--- | :--- | :--- |
| **Feb 2026 – Present** | **Kedara.care** | Data & Software Engineer | Voice-AI family care platform, Knowledge-Base ETL (Typesense, MongoDB), LLM evaluation harness (LLM-as-a-Judge, OpenRouter), Arize telemetry |
| **Nov 2021 – Nov 2025** | **Cisco** | Data Engineer (Data Processing) | Enterprise-scale audio ML curation pipelines, 100% metadata traceability, distributed survey & collection platforms, sub-team coordination |
| **Jul 2019 – Nov 2021** | **BabbleLabs** *(Acq. by Cisco)* | Software / Data Engineer | Audio preprocessing pipelines (MATLAB/Python), SQL-backed dataset delivery, OS & disk performance benchmarking utilities |
| **2010 – 2017** | **Universidad de Los Andes** | B.Sc. Systems Engineering | Specialization in Control & Automation | Thesis: 18-DoF Hexapod Robot (Grade: 20/20) |

<details>
<summary><b>🔍 Click to expand detailed professional accomplishments & production impact</b></summary>
<br>

#### 🔹 Kedara.care — Data & Software Engineer *(Feb 2026 – Present | Remote)*
- **Knowledge-Base ETL & Data Ingestion:** Built and maintained ETL pipelines grounding LLM/Chat/Agent knowledge bases (Facilities, Services, Benefits), ingesting from web crawlers and government sources with geo-location tracking and LLM-driven metadata extraction using **Typesense**, **MongoDB**, and **Google Drive**.
- **LLM Evaluation Harness:** Designed evaluation scenarios spanning dialogue, resource search, and persona testing against live chat; created evaluation datasets and applied **LLM-as-a-Judge** to validate chat quality across multiple dimensions; orchestrated multi-provider routing (**OpenRouter**) to reduce pipeline costs.
- **Data Quality & Telemetry Dashboards:** Applied LLM-based classification across **200K+** service/facility records; built **Streamlit** dashboards for coverage/quality metrics and LLM performance reporting from post-processed **Arize** traces and spans.
- **Voice & Audio Benchmarking:** Tested audio reliability for the voice assistant, benchmarking candidate TTS voices via the **ElevenLabs API**.
- **Mentorship:** Scoped technical projects and mentored Cornell University software interns.

#### 🔹 Cisco — Data Engineer *(Nov 2021 – Nov 2025 | Kraków, Poland)*
- **Enterprise Audio ML Curation:** Orchestrated audio curation frameworks transforming massive raw datasets into production-grade training sets for global ML models.
- **Traceability & Standardization:** Standardized Python/MATLAB/Bash pipelines for audio and RIR (Room Impulse Response) data with **100% metadata traceability**, enrichment, and regulatory licensing compliance.
- **Distributed Data Collection:** Coordinated and led an engineering sub-team building custom survey and data-collection applications across MTurk, Prolific, and Upwork; implemented anti-cheating mechanisms and strict source validation.

#### 🔹 BabbleLabs (Acquired by Cisco) — Software / Data Engineer *(Jul 2019 – Nov 2021 | Remote)*
- **Audio Processing Pipelines:** Built automated Python/MATLAB pipelines preprocessing audio datasets with CSV/MAT metadata indexing for controlled dataset delivery.
- **System Benchmarking Utilities:** Designed custom ingestion tools and benchmarking utilities for audio quality and Windows/OS resource monitoring.

</details>

---

### 🚀 Featured Systems & Open-Source Engineering

| Project | Description | Stack |
| :--- | :--- | :--- |
| ⚡ **[agent-quota-tracker](https://github.com/joseamair/agent-quota-tracker)** | Autonomous watchdog CLI monitor & live web dashboard tracking 5-hour rolling rate limits, weekly quotas, and smart window priming across Claude Code, OpenAI Codex, and Google Antigravity. | `Python 3.11+` `uv` `FastAPI` `HTML5/CSS` |
| 🤖 **cli-agent-orchestrator** *(Private MVP)* | Autonomous coordination layer multiplexing native vendor CLIs across isolated Git worktrees and WezTerm panes. Features durable state files, keep-alive verify loops, and preemptive quota handoffs. | `Python 3.12+` `WezTerm CLI` `Git Worktrees` |
| 🚴 **VeloMind** *(Private)* | AI-driven endurance coach analyzing biometric telemetry (HRV, sleep, body battery) from Garmin, Strava, and Intervals.icu to generate adaptive training recommendations and fueling strategies. | `FastAPI` `SQLModel` `React` `Vitest` `Playwright` |
| 🎨 **LocalPenServer V2** *(Private)* | Real-time collaborative whiteboard and vector drawing server. Turns tablets into wireless PC drawing pads with infinite canvas zoom/pan, palm rejection, and instant WebSockets sync. | `React` `Vite` `FastAPI` `WebSockets` `Fabric.js` |

---

### 🛠️ Tech Stack & Tooling

<div align="center">

#### 💻 Programming Languages & Runtimes
<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white" alt="SQL" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
  <img src="https://img.shields.io/badge/Bash-4EAA25?style=for-the-badge&logo=gnubash&logoColor=white" alt="Bash" />
  <img src="https://img.shields.io/badge/PowerShell-5391FE?style=for-the-badge&logo=powershell&logoColor=white" alt="PowerShell" />
  <img src="https://img.shields.io/badge/MATLAB-0076A8?style=for-the-badge&logo=mathworks&logoColor=white" alt="MATLAB" />
  <img src="https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" alt="C++" />
</p>

#### ⚡ Data Engineering, Databases & Search
<p>
  <img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB" />
  <img src="https://img.shields.io/badge/Typesense-D32F2F?style=for-the-badge&logo=search&logoColor=white" alt="Typesense" />
  <img src="https://img.shields.io/badge/Snowflake-29B5E8?style=for-the-badge&logo=snowflake&logoColor=white" alt="Snowflake" />
  <img src="https://img.shields.io/badge/Apache_Airflow-017CEE?style=for-the-badge&logo=apacheairflow&logoColor=white" alt="Apache Airflow" />
  <img src="https://img.shields.io/badge/Apache_Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white" alt="Apache Kafka" />
  <img src="https://img.shields.io/badge/PySpark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white" alt="PySpark" />
  <img src="https://img.shields.io/badge/dbt-FF694B?style=for-the-badge&logo=dbt&logoColor=white" alt="dbt" />
  <img src="https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white" alt="SQLite" />
</p>

#### 🤖 AI, LLM-Ops & Voice Tech
<p>
  <img src="https://img.shields.io/badge/Multi--Agent%20Systems-7C3AED?style=for-the-badge&logo=openai&logoColor=white" alt="Multi-Agent Systems" />
  <img src="https://img.shields.io/badge/LLM--as--a--Judge-10A37F?style=for-the-badge&logo=openai&logoColor=white" alt="LLM-as-a-Judge" />
  <img src="https://img.shields.io/badge/OpenRouter-000000?style=for-the-badge&logo=openai&logoColor=white" alt="OpenRouter" />
  <img src="https://img.shields.io/badge/Arize%20Phoenix-FF6F00?style=for-the-badge&logo=datadog&logoColor=white" alt="Arize Phoenix" />
  <img src="https://img.shields.io/badge/ElevenLabs-000000?style=for-the-badge&logo=waveform&logoColor=white" alt="ElevenLabs" />
  <img src="https://img.shields.io/badge/OpenAI%20Whisper-00A67E?style=for-the-badge&logo=openai&logoColor=white" alt="Whisper" />
  <img src="https://img.shields.io/badge/Claude%20Code-D97706?style=for-the-badge&logo=anthropic&logoColor=white" alt="Claude Code" />
  <img src="https://img.shields.io/badge/Google%20Gemini-4285F4?style=for-the-badge&logo=google&logoColor=white" alt="Google Gemini" />
</p>

#### 🛠️ Backends, Web & Testing
<p>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI" />
  <img src="https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white" alt="Django" />
  <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" alt="Streamlit" />
  <img src="https://img.shields.io/badge/WebSockets-010101?style=for-the-badge&logo=socketdotio&logoColor=white" alt="WebSockets" />
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React" />
  <img src="https://img.shields.io/badge/Playwright-2EAD33?style=for-the-badge&logo=playwright&logoColor=white" alt="Playwright" />
  <img src="https://img.shields.io/badge/Pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white" alt="Pytest" />
</p>

#### ⚙️ DevOps & Cloud Infrastructure
<p>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" alt="Kubernetes" />
  <img src="https://img.shields.io/badge/UV_Manager-DE5FE9?style=for-the-badge&logo=python&logoColor=white" alt="UV" />
  <img src="https://img.shields.io/badge/Linux_%2F_WSL2-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux" />
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git" />
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" alt="GitHub Actions" />
</p>

</div>

---

### 📊 GitHub Activity & Real-Time Telemetry

<div align="center">
  <table border="0">
    <tr>
      <td align="center" width="50%">
        <img src="https://github-readme-stats-eight-theta.vercel.app/api?username=joseamair&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=38bdf8&icon_color=38bdf8&text_color=c9d1d9" alt="GitHub Stats" width="100%" />
      </td>
      <td align="center" width="50%">
        <img src="https://github-readme-stats-eight-theta.vercel.app/api/top-langs/?username=joseamair&layout=compact&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=38bdf8&text_color=c9d1d9" alt="Top Languages" width="100%" />
      </td>
    </tr>
    <tr>
      <td colspan="2" align="center">
        <img src="https://streak-stats.demolab.com/?user=joseamair&theme=tokyonight&hide_border=true&background=0d1117&ring=38bdf8&fire=f59e0b&currStreakLabel=38bdf8" alt="GitHub Streak" width="95%" />
      </td>
    </tr>
  </table>
</div>

---

<div align="center">
  <sub>Engineered with precision • Constantly iterating • Feel free to connect or open an issue!</sub>
</div>
