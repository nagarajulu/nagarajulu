# Nagarajulu (Naga) Aerakoni

**Senior Software Engineer @ Amazon** · **AI & Agentic Systems Security Researcher & Architect**  
*Seattle, WA · Claude Certified Architect Foundations · Distributed Systems, Runtime Information-Flow Control (IFC) & Model Context Protocol (MCP) Security*

[![GitHub — mcp-cage](https://img.shields.io/badge/Featured%20Project-mcp--cage%20v0.2.2-1f6feb?style=flat-square&logo=github)](https://github.com/nagarajulu/mcp-cage)
[![CI Status](https://github.com/nagarajulu/mcp-cage/actions/workflows/ci.yml/badge.svg)](https://github.com/nagarajulu/mcp-cage/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/Open%20Source-MIT-success?style=flat-square)](https://github.com/nagarajulu/mcp-cage/blob/main/LICENSE)

---

### About Me

I design and build high-assurance distributed systems and deterministic runtime security architectures for autonomous AI agents. My research and engineering focus on **OS-process-isolated reference monitors**, **decentralized Information-Flow Control (IFC)**, and **protocol-level security** for the **Model Context Protocol (MCP)** and modern coding agents (**Claude Code**, **Cursor**, **OpenAI Codex CLI**, **Google Gemini CLI**, and **Google Antigravity `agy`**).

---

### Featured Open-Source Project

#### 🛡️ [`mcp-cage`](https://github.com/nagarajulu/mcp-cage) — Zero-Code Wire & Native-Hook Security Firewall for AI Coding Agents & MCP
> *"Gitleaks + Little Snitch for AI Coding Agents"* — **100% Python 3.10+ Standard Library · Zero External Dependencies**

Modern AI coding agents regularly encounter the **Lethal Trifecta** (private credential access + untrusted external content ingestion + external network/shell actuation). **`mcp-cage`** enforces deterministic, non-bypassable security boundaries outside the LLM context window across both **Plane A (`stdio` MCP JSON-RPC 2.0 Wire Proxy)** and **Plane B (Native Agent Lifecycle Hooks)**:

- **Cross-Process Bidirectional Secret Vault (`SQLite WAL`):** Scrubs 11+ secret classes (OpenAI, Anthropic, AWS, GitHub PATs, Stripe, Slack, PEM keys, DB URIs, `.env` secrets) on the wire into `<MCP_REDACTED_...>` tokens before they enter the LLM context window, blocking cross-process exfiltration across separate MCP servers.
- **Lethal-Trifecta Circuit Breaker & MELON Provenance Attribution:** Tracks monotonic session `(Integrity, Confidentiality)` state via atomic `BEGIN IMMEDIATE` transactions, blocks sink/mutator arguments derived from untrusted external entities, and provides 5-minute scoped workspace edit leases to eliminate approval fatigue.
- **SSRF (`169.254.169.254`), Path Confinement & High-Entropy DNS Exfiltration Firewall:** Deterministically blocks cloud metadata endpoints (AWS/GCP/Alibaba/IPv6 IMDS), RFC 1918 private networks, dangerous URI schemes (`file://`, `gopher://`, `dict://`), symlink/dotfile escapes (`.git/hooks/`, `.vscode/settings.json`, `.cursor/mcp.json`), and high-entropy/hex DNS exfiltration subdomains.
- **`CurXecute` Config Linter (`mcp-cage audit-config`) & `MCPTox` Schema Lockfile (`mcp-lock.json`):** Strips hidden prompt-injection tags and cross-server shadowing directives from `tools/list` prior to SHA-256 pinning, and audits workspace MCP configs for RCE and plaintext secrets.

---

### Core Technical Domains

| Domain | Focus Areas |
| :--- | :--- |
| **Agentic & LLM Security** | Model Context Protocol (MCP) Firewalls, Indirect Prompt Injection (`XPIA`) Defense, Lethal Trifecta Mitigation, Tool Poisoning (`MCPTox` / `CurXecute`) Prevention, Cryptographic Datamarking (*Spotlighting*) |
| **Systems & Information-Flow Control** | Dual-Lattice Taint Tracking (*FIDES* / *CaMeL* / *HiStar* / *Flume*), Capability-Based Confinement (*Capsicum*), Provenance Attribution (*MELON*), Cross-Process SQLite WAL State Machines |
| **Large-Scale Distributed Systems** | High-Throughput Cloud Services @ Amazon, Fault-Tolerant Storage & Messaging Pipelines, Zero-Trust Service Architectures |
