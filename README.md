<div align="center">

```
██████╗  ██████╗      ██████╗██╗      █████╗ ███████╗███████╗
██╔══██╗██╔═══██╗    ██╔════╝██║     ██╔══██╗██╔════╝██╔════╝
██████╔╝██║   ██║    ██║     ██║     ███████║█████╗  ███████╗
██╔══██╗██║   ██║    ██║     ██║     ██╔══██║██╔══╝  ╚════██║
██████╔╝╚██████╔╝    ╚██████╗███████╗██║  ██║███████╗███████║
╚═════╝  ╚═════╝      ╚═════╝╚══════╝╚═╝  ╚═╝╚══════╝╚══════╝
```

**Full-stack developer** · Python · JavaScript · Security · ML

[thedeepspaceproject.be](https://thedeepspaceproject.be) · [boclaes102@gmail.com](mailto:boclaes102@gmail.com)

</div>

---

## About me

I build things that actually work — a 3D browser portfolio, a real-time data pipeline, a cybersecurity toolkit, and tools powered by AI APIs. I'm interested in the full stack: from WebSocket servers and ML model training to 3D rendering and network packet analysis.

- Based in Belgium
- Currently building and shipping personal projects
- Interested in: data engineering, cybersecurity, AI tooling, creative coding
- Ask me about: FastAPI, Three.js, async Python, or WebSockets

---

## Projects

### [Deep Space — Interactive 3D Portfolio](https://github.com/boclaes102-eng/Personal-web-page)
> A Three.js space scene where every floating object is a real, working application

A retro PC with 10 hacking tools, a TV showing live news/weather/markets, a multiplayer arcade cabinet, a procedurally synthesized jukebox, and a British phone booth — all floating in 3D space. Built with zero npm dependencies shipped to the browser.

`Three.js` `Vanilla JS` `Supabase` `Web Audio API` `GSAP` `Groq AI`

Live: [thedeepspaceproject.be](https://thedeepspaceproject.be)

---

### [Real-Time Data Pipeline](https://github.com/boclaes102-eng/Real-time-data-pipeline)
> Production-style streaming pipeline with a live browser dashboard

3 async producers (stocks, crypto, Reddit) → topic-based message broker (Kafka-compatible interface) → SQLite → WebSocket fan-out → Chart.js dashboard. Graceful degradation with Gaussian simulation when markets are closed.

`FastAPI` `asyncio` `WebSockets` `SQLite` `yfinance` `CoinGecko API`

---

### [CyberSuite Pro](https://github.com/boclaes102-eng/Cybersecurity-software)
> Three professional security tools — one unified dark-themed GUI launcher

**NIDS** — real-time packet capture with 6 attack detectors (Port Scan, SYN Flood, DNS Tunneling, ARP Poisoning, ICMP Amplification, Statistical Anomaly)  
**PAS** — offline hash cracking, entropy scoring, HIBP breach check  
**SMA** — PE/ELF static analysis mapped to 18 MITRE ATT&CK behavioral rules, YARA scanning, VirusTotal lookup

147 unit tests. Builds to a single portable `.exe`.

`Python` `CustomTkinter` `Scapy` `PyInstaller` `MITRE ATT&CK` `pytest`

---

### [Telecom Churn Predictor](https://github.com/boclaes102-eng/ML-coding-project)
> XGBoost classifier with a live Streamlit UI — ROC-AUC 0.84

Trained on IBM Telco dataset (7,043 customers, 20 features). Real-time prediction with gauge chart, risk verdict, churn driver bullets, and feature importances.

Live: [telecom-churn-predictor.streamlit.app](https://telecom-churn-predictor.streamlit.app)

`XGBoost` `Streamlit` `scikit-learn` `pandas`

---

### [PyMind — Python AI Assistant](https://github.com/boclaes102-eng/ML-python-tool)
> Claude-powered CLI that reads your actual files, runs code, and fixes real problems

Filesystem tools, code execution, cross-platform path resolution, and an agentic loop that chains tool calls until the answer is complete. Uses Anthropic's prompt caching to reduce cost on every request.

`Python` `Anthropic Claude API` `Tool use` `Prompt caching`

---

### [Sub-Checker](https://github.com/boclaes102-eng/Sub-checker)
> Scans your Gmail inbox and shows everything you're subscribed to

Detects active, likely active, inactive, and cancelled subscriptions from 2 years of billing emails. Read-only Gmail API — nothing ever leaves your machine. Built after finding 4 forgotten subscriptions still charging me every month.

`Python` `Gmail API` `OAuth2`

---

## Tech

| | |
|---|---|
| **Languages** | Python · JavaScript (ES2022) · SQL · Bash |
| **Backend** | FastAPI · asyncio · WebSockets · SQLite · REST |
| **Frontend** | Three.js · Vanilla JS · Chart.js · HTML/CSS |
| **ML / Data** | XGBoost · scikit-learn · pandas · Streamlit |
| **Security** | Scapy · YARA · MITRE ATT&CK · HIBP · VirusTotal |
| **AI / APIs** | Anthropic Claude · Groq (Llama 3.1) · Supabase |
| **Tooling** | Git · PyInstaller · pytest · Node test runner |

---

<div align="center">
<sub>All projects are MIT licensed · Open to work · Belgium</sub>
</div>
