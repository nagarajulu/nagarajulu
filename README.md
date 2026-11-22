# Nagarajulu (Naga) Aerakoni

**Senior Software & Distributed Systems Engineer** · **Independent Security Researcher**  
*Seattle, WA · Claude Certified Architect Foundations · Distributed Systems, Runtime Information-Flow Control (IFC) & Model Context Protocol (MCP) Security*

[![GitHub — mcp-cage](https://img.shields.io/badge/Featured%20Project-mcp--cage%20v0.4.1-1f6feb?style=flat-square&logo=github)](https://github.com/nagarajulu/mcp-cage)
[![PyPI — mcp-cage](https://img.shields.io/pypi/v/mcp-cage.svg?style=flat-square)](https://pypi.org/project/mcp-cage/)
[![Live Interactive Sandbox](https://img.shields.io/badge/🌐%20Interactive%20Web%20Sandbox-nagarajulu.github.io%2Fmcp--cage-06b6d4?style=flat-square)](https://nagarajulu.github.io/mcp-cage/)
[![CI Status](https://github.com/nagarajulu/mcp-cage/actions/workflows/ci.yml/badge.svg)](https://github.com/nagarajulu/mcp-cage/actions/workflows/ci.yml)
<!-- Uncomment on Preprint Launch Day: [![ORCID](https://img.shields.io/badge/ORCID-0009--0003--4269--0169-a6ce39?style=flat-square&logo=orcid&logoColor=white)](https://orcid.org/0009-0003-4269-0169) -->
[![LinkedIn](https://img.shields.io/badge/LinkedIn-nagarajulu-0a66c2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nagarajulu/)
[![KineticBloom](https://img.shields.io/badge/🌱%20KineticBloom-kineticbloom.org-10b981?style=flat-square)](https://github.com/nagarajulu/kinetic-bloom)

---

### About Me

I design and build high-assurance distributed systems, deterministic runtime security architectures for autonomous AI agents, and evidence-based assistive applications. My security research and engineering focus on **OS-process-isolated reference monitors**, **decentralized Information-Flow Control (DIFC)**, and **protocol-level security** for the **Model Context Protocol (MCP)** and modern coding agents (**Claude Code**, **Cursor**, **OpenAI Codex CLI**, **Google Gemini CLI**, and **Google Antigravity `agy`**).

---

### Featured Open-Source Projects & Applications

#### 1. 🛡️ [`mcp-cage`](https://github.com/nagarajulu/mcp-cage) (`v0.4.1`) — Zero-Code Wire & Native-Hook Security Firewall for AI Coding Agents & MCP
> *"Gitleaks + Little Snitch for AI Coding Agents"* — **100% Python 3.10+ Standard Library · Zero External Dependencies**  
> 🌐 **Live Interactive Sandbox & Config Generator:** [**`https://nagarajulu.github.io/mcp-cage/`**](https://nagarajulu.github.io/mcp-cage/) · 📦 **PyPI:** [**`pip install mcp-cage`**](https://pypi.org/project/mcp-cage/) · 💻 **GitHub:** [**`https://github.com/nagarajulu/mcp-cage`**](https://github.com/nagarajulu/mcp-cage)

Modern AI coding agents regularly encounter the **Lethal Trifecta** (private credential access + untrusted external content ingestion + external network/shell actuation). **`mcp-cage`** enforces deterministic, non-bypassable security boundaries outside the LLM context window across both **Plane A (`stdio` MCP JSON-RPC 2.0 Wire Proxy)** and **Plane B (Native Agent Lifecycle Hooks)**:

- **Cross-Process Bidirectional Secret Vault & Destination-Bound FPE (`SQLite WAL`):** Scrubs 11+ secret classes on the wire into `<MCP_REDACTED_...>` / format-preserving tokens before they enter the LLM context window, blocking cross-process exfiltration and confused-deputy secret oracles.
- **Dual-Lattice Wire-DIFC, Line-Span WAL Provenance & MELON Attribution:** Tracks monotonic session `(Integrity, Confidentiality)` state via atomic `BEGIN IMMEDIATE` transactions, isolates untrusted line spans in `CLAUDE.md`/`.cursorrules`/`MEMORY.md` (`PersistentLineSpanProvenance`), arrests `OverServe` ($93.88\times$) polling loops (`CausalStateProgressGovernor`), and provides 5-minute scoped workspace edit leases.
- **34-Mechanism Empirical CWE Parameter Firewall:** Zero-config wire guards blocking runtime endpoint repointing (`GHSA-rvjm-7hvp-f868`), embedded POSIX command substitution (`CWE-78`), REST path/delimiter smuggling (`CWE-22`), CLI flag & `git::ext::` transport injection (`CWE-88`), comment-split SQLi/Cypher/NoSQLi (`CWE-89`/`CWE-943`), Python sandbox escapes & SSTI (`CWE-94`/`CWE-1336`), XXE (`CWE-611`), pickle/YAML deserialization (`CWE-502`), and cloud metadata/IPv6-mapped loopback SSRF (`CWE-918`).
- **7-Vector Agent Skill & Rule Static + AST Auditor (`mcp-cage audit-skills`) & Kernel Sandbox Compiler (`mcp-cage compile-sandbox`):** Statically scans `SKILL.md`, `CLAUDE.md`, `AGENTS.md`, `.cursorrules`, and companion `scripts/*.py` (via Python `ast.parse()`) for Unicode Tag smuggling (`CVE-2021-42574`), markdown image beacons, capability drift, and persistence backdoors (`CVE-2025-53773`), and compiles macOS Seatbelt SBPL / Linux Landlock profiles.

---

#### 2. 🌱 [`kinetic-bloom`](https://github.com/nagarajulu/kinetic-bloom) — 10-Minute Home Movement & Primitive Reflex Co-Regulation Companion
> 🌐 **Live Web Application:** [**`https://kineticbloom.org`**](https://kineticbloom.org) · 💻 **GitHub:** [**`https://github.com/nagarajulu/kinetic-bloom`**](https://github.com/nagarajulu/kinetic-bloom)

A privacy-first, offline-capable progressive web application (React 19, TypeScript, TailwindCSS, WCAG 2.2 AA) built for parents, caregivers, and pediatric occupational therapists to support neurodivergent children (Autism Levels 1–3, ADHD, Sensory Processing Differences, and developmental dyspraxia):

- **11 Primitive Reflexes & 51 Evidence-Based Pathways:** Covers Moro, ATNR, STNR, TLR, Spinal Galant, Palmar Grasp, Plantar, Fear Paralysis (FPR), Landau, Amphibian, and Rooting & Sucking across Active Dynamic, Passive Co-Regulation, Isometric, and Rhythmic RMT modalities.
- **Interactive 10-Minute Circuit Runner & Biomechanical Visuals:** Tailors 3-card daily routines to the child's autonomic energy state with 432 Hz interval chimes, metronome pacing, First–Then visual motivators, and Calm Dark Sensory Mode.
- **100% Zero-PII & COPPA-Compliant Local Storage:** Runs entirely in the browser with zero remote telemetry and portable JSON export/import across devices.

---

### Core Technical Domains

| Domain | Focus Areas |
| :--- | :--- |
| **Agentic & LLM Security** | Model Context Protocol (MCP) Firewalls, Indirect Prompt Injection (`XPIA`) Defense, Lethal Trifecta Mitigation, Tool & Skill Poisoning (`MCPTox` / `CurXecute` / `SKILL.md` AST) Prevention, Cryptographic Datamarking (*Spotlighting*) |
| **Systems & Information-Flow Control** | Dual-Lattice Taint Tracking (*FIDES* / *CaMeL* / *HiStar* / *Flume*), Capability-Based Confinement (*Capsicum* / Seatbelt / Landlock), Provenance Attribution (*MELON*), Cross-Process SQLite WAL State Machines |
| **Large-Scale Distributed Systems** | High-Throughput Cloud & Backend Services, Fault-Tolerant Storage & Messaging Pipelines, Zero-Trust Service Architectures |
