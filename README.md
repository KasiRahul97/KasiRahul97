<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:6366F1,100:22D3EE&height=200&section=header&text=Kasi%20Rahul%20M&fontSize=52&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=AI%20Engineering%20%C2%B7%20Data%20Engineering%20%C2%B7%20Cloud&descAlignY=58&descSize=18" width="100%"/>

<a href="https://github.com/KasiRahul97">
  <img src="https://readme-typing-svg.demolab.com/?font=Fira+Code&weight=600&size=22&pause=1200&color=6366F1&center=true&vCenter=true&width=680&lines=CSE+Undergraduate+%40+VIT+Vellore;Data+Engineering+Intern+%40+FedEx+Dataworks;I+build+pipelines%2C+models%2C+and+the+odd+3+AM+bug+fix;Currently%3A+diagnosing+why+R%C2%B2+went+negative" alt="Typing SVG" />
</a>

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/kasi-rahul-m-738ab428a/)
[![Email](https://img.shields.io/badge/Email-Reach_out-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:rahulmkofficial97@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/KasiRahul97)
[![Resume](https://img.shields.io/badge/Resume-View-6366F1?style=for-the-badge&logo=readdotcv&logoColor=white)](https://drive.google.com/drive/folders/1iapGQnaXT4tG8y6_tYtZL2LZfZJNbPLn?usp=drive_link)

</div>

---

## About

I'm a Computer Science undergraduate at **VIT Vellore** (CGPA **8.74/10.0**, 2023–2027) with hands-on experience across software development, data engineering, and AI. I like building systems that hold up under real data — most recently that meant ingesting and transforming logistics data at scale at **FedEx Dataworks**, and before that, chasing a data-leakage bug that was quietly wrecking a forecasting model's accuracy.

```yaml
role:        CSE Undergraduate, VIT Vellore
focus:       AI Engineering · Data Engineering · Cloud
currently:   Data Engineering Intern @ FedEx Dataworks
strong_in:   [Python, PySpark, Databricks, SQL]
based_in:    Chennai, Tamil Nadu, India
```

---

## Experience

<table>
<tr>
<td width="100%">

**Data Engineering Intern · FedEx Dataworks** — *May 2026 – Jul 2026*
`Python` `SQL` `PySpark` `Databricks`

- Ingested and transformed logistics datasets using PySpark on Databricks, enabling downstream analytics for shipment operations
- Engineered SQL-based analytical workflows generating ULD container-level shipment insights
- Developed SLA-driven shipment prioritization logic (Hot / Cold / Past Due) to support operations reporting
- Built scalable data processing workflows for logistics analytics using PySpark, SQL, and Databricks

</td>
</tr>
</table>

---

## Tech I build with

<div align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Java](https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=openjdk&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)
![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=databricks&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
<br/>
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![scikit--learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

</div>

---

## Featured Projects

### [CloudSense](https://github.com/KasiRahul97/CloudSense) — Leakage-Free Cloud CPU Forecasting Benchmark
`Python` `PyTorch` `FastAPI` `Docker` `AWS`

A causal, leakage-free benchmark of CPU-utilization forecasters for proactive cloud autoscaling, served behind a live FastAPI + Docker stack whose online forecasts reproduce the offline test accuracy exactly.

- Compared a **CEEMDAN + CNN-BiLSTM** ensemble against 4 deep-learning baselines and 2 naive baselines on real AWS/Numenta NAB telemetry, at the 4-hour-ahead horizon reaching **R² 0.73 / MAE 5.7%**
- Found and fixed a data-leakage + scaling bug that had collapsed a baseline to **R² ≈ −1.7**, recovering it to **≈ 0.70** via physical-range scaling and per-window RevIN normalization
- Kept the decomposition **causal** — it only ever sees the past window, using the same code at train and serving time, so the benchmark number is one the live model can actually reproduce
- Reported naive persistence/EMA baselines alongside the learned models and let the honest result stand — persistence wins at both horizons, which the README says out loud instead of hiding
- 30 passing tests, GitHub Actions CI, Dockerized inference API with a live demo dashboard

### [PAXA AI Assistant](https://github.com/KasiRahul97/PAXA-AI-Assistant) — Multi-Agent AI Assistant Platform
`Python`

A modular AI assistant built around a multi-agent architecture, separating orchestration from execution.

- `core/` orchestration layer coordinating specialized `agents/` and backend `services/`
- Persistent memory and enterprise-context stores (`paxa_memory.db`, `paxa_enterprise.db`) so the assistant retains context across sessions
- Includes a dedicated `frontend/` for user interaction on top of the agent backend
- 100% Python end to end, from agent logic to service layer

---

## Education

**B.Tech, Computer Science & Engineering — VIT Vellore**
CGPA: 8.74 / 10.0 · 2023 – 2027
Relevant coursework: Data Structures & Algorithms, Machine Learning, Deep Learning, DBMS, Operating Systems, Computer Architecture

---

## Certifications

- **Oracle Cloud Infrastructure 2024 Generative AI Certified Professional** — LLM fundamentals, prompt engineering, RAG

---

## Leadership & Achievements

- **Student Manager, Publicity & Marketing — GRAVITAS '25 (VIT Flagship Fest)**: led nationwide outreach driving 1,200+ external registrations through cold calling, email campaigns, and institutional engagement
- **Management Head, Geospatial Club, VIT**: served on the executive board, planning and executing technical events and workshops

---

<div align="center">

*Building things that hold up when the data gets messy and the metrics stop cooperating.*

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:22D3EE,100:6366F1&height=100&section=footer" width="100%"/>

</div>
