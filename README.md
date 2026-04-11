<div align="center">

```
██████╗  ██████╗      ██████╗██╗      █████╗ ███████╗███████╗
██╔══██╗██╔═══██╗    ██╔════╝██║     ██╔══██╗██╔════╝██╔════╝
██████╔╝██║   ██║    ██║     ██║     ███████║█████╗  ███████╗
██╔══██╗██║   ██║    ██║     ██║     ██╔══██║██╔══╝  ╚════██║
██████╔╝╚██████╔╝    ╚██████╗███████╗██║  ██║███████╗███████║
╚═════╝  ╚═════╝      ╚═════╝╚══════╝╚═╝  ╚═╝╚══════╝╚══════╝
```

**Full-stack developer · IoT engineer · Cybersecurity analyst**

[thedeepspaceproject.be](https://thedeepspaceproject.be) · [boclaes102@gmail.com](mailto:boclaes102@gmail.com) · [linkedin.com/in/bo-claes-a20695233](https://linkedin.com/in/bo-claes-a20695233)

</div>

---

## About me

Full-stack developer, IoT engineer, and cybersecurity analyst based in Belgium. I build complete systems from the ground up — hardware to application.

At MyPitch, I was the sole engineer for an AI-powered soccer analytics platform: installing cameras at facilities, routing footage through AWS S3 and SQS to a custom Linux VM, and writing Python/OpenCV pipelines that extracted per-player performance metrics by jersey number from match footage. At Agilica, I built a Three.js drone fleet management tool with real-time GPS tracking, rebuilt the company website with a full analytics pipeline, and assembled custom embedded hardware including PCB soldering for drone systems. In 2026, I independently arranged and executed a 3-month security engagement at a public safety facility — running OpenVAS/Nessus scans, auditing Active Directory, conducting an authorised penetration test, and delivering remediation reports.

Currently completing a Cybersecurity Analyst & Engineer programme at Syntra alongside active project work.

- Based in Langdorp, Belgium
- Background: web development, IoT, embedded systems, offensive security
- Open to roles in: full-stack development, data engineering, cybersecurity
- Languages: Dutch (native), English (professional)

---

## Projects

### [Deep Space — Interactive 3D Portfolio](https://github.com/boclaes102-eng/Personal-web-page)
> A Three.js space scene where every floating object is a real, working application

A retro PC with 10 hacking tools, a TV showing live news/weather/markets, a multiplayer arcade cabinet, a procedurally synthesized jukebox, and a British phone booth — all floating in 3D space. Built with zero npm dependencies shipped to the browser.

`Three.js` `Vanilla JS` `Supabase` `Web Audio API` `GSAP` `Groq AI` `GLSL`

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
| **Languages** | Python · JavaScript (ES2022) · PHP · C# · SQL · Bash |
| **Backend** | FastAPI · asyncio · WebSockets · SQLite · REST · AWS |
| **Frontend** | Three.js · Vanilla JS · Chart.js · HTML/CSS · GLSL |
| **ML / Data** | XGBoost · scikit-learn · OpenCV · pandas · Streamlit |
| **Security** | Scapy · YARA · MITRE ATT&CK · OpenVAS · Nessus · Burp Suite · Metasploit · Wireshark |
| **IoT / Hardware** | Raspberry Pi · Arduino · PCB Design · Soldering · Firmware · Node-RED |
| **AI / APIs** | Anthropic Claude · Groq (Llama 3.1) · Supabase |
| **Tooling** | Git · Linux · PyInstaller · pytest · Node test runner |

---

<div align="center">
<sub>All projects are MIT licensed · Open to work · Belgium</sub>
</div>
