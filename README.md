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

### Three-platform cybersecurity ecosystem

Three separate applications sharing a live PostgreSQL backend — recon results gathered in the web dashboard flow into a shared database and load directly into the desktop attack tool with one click.

```
CyberOps Dashboard  (Next.js · Vercel)
  56 recon/intel tools
  "Save to Workspace" → POST /api/v1/recon-sessions
        │
        │ HTTPS · X-API-Key (server-side proxy, never in browser)
        ▼
Threat Intel Platform  (Fastify · PostgreSQL · BullMQ · Redis · Railway)
  CVE feed sync · IOC enrichment · asset monitoring · recon session store
        │
        │ X-API-Key
        ▼
CyberSuite Pro Desktop  (Python · CustomTkinter · Windows)
  Load saved recon → one click → active target → 15 attack modules
```

---

#### [CyberOps Dashboard](https://github.com/boclaes102-eng/Online-Cyber-dashboard)
> 56 integrated security tools — Next.js 15, TypeScript strict, deployed on Vercel

OSINT, recon, threat intelligence, web analysis, forensics, automation, asset monitoring, and reporting in one interface. Every algorithm implemented from scratch — no chart libraries, no HTTP clients, no utility belts. Zero `any` escapes in TypeScript strict mode throughout.

From-scratch implementations: Wagner-Fischer edit distance (SSDEEP fuzzy hash scoring), MurmurHash3 (Shodan favicon pivoting), CVSS v3.1 base score formula, DataView multi-format byte interpretation (int8–int64, float32/64, BE/LE), sliding-window rate limiter running at Vercel Edge before any serverless function is invoked.

All backend API keys stay server-side — a Next.js catch-all proxy route injects credentials before forwarding to Railway, making CORS structurally impossible.

`Next.js 15` `TypeScript` `Tailwind CSS` `Edge Middleware` `Vercel`

---

#### [Threat Intel Platform](https://github.com/boclaes102-eng/threat-intel-platform)
> Production backend API — the shared data layer for the three-platform ecosystem

Live API: [threat-intel-platform-production-eb1b.up.railway.app](https://threat-intel-platform-production-eb1b.up.railway.app)

Fastify API backed by PostgreSQL 16 and Redis 7. Runs three BullMQ background workers: a CVE feed worker that pages the full NIST NVD API every 6 hours with exponential backoff and jitter, an IOC enrichment worker that fans out to AbuseIPDB, VirusTotal, and AlienVault OTX in parallel with Redis TTL caching, and an asset-scan worker that correlates CPE strings against known CVEs entirely database-side. Ships as two separate Docker targets (API + Worker) on a single Railway project.

10-table PostgreSQL schema with full relational integrity — bcrypt passwords, SHA-256 hashed tokens, cursor-based pagination, TTL-based stale-while-revalidate for IOC records, and a complete remediation lifecycle on the asset_vulnerabilities join table.

CI pipeline: type check → security audit → unit + integration tests (real Postgres + Redis service containers) → Codecov coverage upload.

`Fastify` `TypeScript` `PostgreSQL` `Redis` `BullMQ` `Drizzle ORM` `Docker` `Railway` `Vitest`

---

#### [CyberSuite Pro](https://github.com/boclaes102-eng/Cybersecurity-software)
> 15-module penetration testing toolkit — the desktop attack layer of the ecosystem

A full offensive security workflow in one dark-themed GUI launcher, covering every phase from network discovery to client report delivery. Auto-elevates to admin via UAC on launch.

**Network & Discovery** — Network Map (ARP scan + nmap deep scan + SNMP router query, interactive 2D canvas with draggable nodes), NIDS (real-time packet capture, 6 attack detectors), WiFi Recon (WPA2 handshake capture + deauth attack)

**Attack** — MITM/ARP Spoof (MAC changer + bidirectional ARP poisoning), SSL Interceptor (mitmproxy transparent mode, full request/response inspection), Credential Harvester (HTTP/Basic Auth/NTLM sniffing, hashcat export), Metasploit Bridge (CVE→module map, pre-fills all options, launches msfconsole), Payload Generator (reverse/bind/web shells, 10+ languages)

**Post-Exploitation** — AD Enumeration (pure-Python LDAP, Kerberoastable/AS-REP roastable/unconstrained delegation/stale accounts), Password Auditing, Static Malware Analyzer (18 MITRE ATT&CK rules, YARA, VirusTotal), Web App Tester, CVE & Exploit Helper

**Reporting** — Report Generator (persistent findings tracker, auto-imports high-risk hosts from NetMap, exports styled HTML → PDF), Recon Workspace (loads saved dashboard sessions, one click sets active target across all tools)

Tools run in-process via `importlib`, stdout intercepted per-thread with `threading.local()` without modifying tool source, threads stopped by injecting `KeyboardInterrupt` at the C level via `ctypes.PyThreadState_SetAsyncExc`. Builds to a portable single-file `.exe`.

`Python` `CustomTkinter` `Scapy` `Nmap` `mitmproxy` `ldap3` `YARA` `MITRE ATT&CK` `PyInstaller`

---

### [Deep Space — Interactive 3D Portfolio](https://github.com/boclaes102-eng/Personal-web-page)
> A Three.js space scene where every floating object is a real, working application

A retro PC with 10 hacking tools, a TV showing live news/weather/markets, a multiplayer arcade cabinet, a procedurally synthesized jukebox, and a British phone booth — all floating in 3D space. Zero npm dependencies shipped to the browser. Multiplayer Pong via Supabase Realtime with authoritative host physics and lerp interpolation for the guest.

`Three.js` `Vanilla JS` `Supabase` `Web Audio API` `GSAP` `Groq AI` `GLSL`

Live: [thedeepspaceproject.be](https://thedeepspaceproject.be)

---

### [Real-Time Data Pipeline](https://github.com/boclaes102-eng/Real-time-data-pipeline)
> Production-style streaming pipeline with a live browser dashboard

3 async producers (stocks, crypto, Reddit) → topic-based message broker (Kafka-compatible interface) → SQLite → WebSocket fan-out → Chart.js dashboard. Swapping in real Confluent Kafka requires changing only one file.

`FastAPI` `asyncio` `WebSockets` `SQLite` `yfinance` `CoinGecko API`

---

### [Telecom Churn Predictor](https://github.com/boclaes102-eng/ML-coding-project)
> XGBoost classifier with a live Streamlit UI — ROC-AUC 0.84

Trained on IBM Telco dataset (7,043 customers, 20 features). Real-time prediction with gauge chart, risk verdict, churn driver bullets, and feature importances.

Live: [telecom-churn-predictor.streamlit.app](https://telecom-churn-predictor.streamlit.app)

`XGBoost` `Streamlit` `scikit-learn` `pandas`

---

### [PyMind — Python AI Assistant](https://github.com/boclaes102-eng/ML-python-tool)
> Claude-powered CLI that reads your actual files, runs code, and fixes real problems

Agentic loop with tool use and prompt caching — reads codebases, searches code, and runs Python snippets before responding. Supports Windows and Linux path conventions transparently.

`Python` `Anthropic Claude API` `Tool use` `Prompt caching`

---

### [Sub-Checker](https://github.com/boclaes102-eng/Sub-checker)
> Scans your Gmail inbox and shows everything you're subscribed to

Detects active, likely active, inactive, and cancelled subscriptions from 2 years of billing emails. Fully local — nothing leaves your machine. Built after finding 4 forgotten subscriptions still charging me every month.

`Python` `Gmail API` `OAuth2`

---

## Tech

| | |
|---|---|
| **Languages** | Python · TypeScript · JavaScript (ES2022) · PHP · C# · SQL · Bash |
| **Backend** | Fastify · Next.js 15 · FastAPI · asyncio · WebSockets · REST · PostgreSQL · Redis · AWS |
| **Frontend** | Three.js · React · Tailwind CSS · Vanilla JS · Chart.js · HTML/CSS · GLSL |
| **ML / Data** | XGBoost · scikit-learn · OpenCV · pandas · Streamlit |
| **Security** | Scapy · Nmap · mitmproxy · ldap3 · YARA · MITRE ATT&CK · OpenVAS · Nessus · Burp Suite · Metasploit · Wireshark |
| **IoT / Hardware** | Raspberry Pi · Arduino · PCB Design · Soldering · Firmware · Node-RED |
| **Infra / DevOps** | Docker · Railway · Vercel · BullMQ · GitHub Actions · Prometheus · Grafana |
| **AI / APIs** | Anthropic Claude · Groq (Llama 3.1) · Supabase · VirusTotal · Shodan · AbuseIPDB |
| **Tooling** | Git · Linux · Drizzle ORM · PyInstaller · pytest · Vitest · Node test runner |

---

<div align="center">
<sub>All projects are MIT licensed · Open to work · Belgium</sub>
</div>
