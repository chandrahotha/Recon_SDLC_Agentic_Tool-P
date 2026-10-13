<div align="center">

<img width="712" height="174" alt="Recon Banner" src="https://github.com/user-attachments/assets/7fb9c87b-6872-423b-a724-8affc76eee69" />

<br />

<img src="./assets/recon-logo.png" alt="Recon Logo" width="130" />

# Recon — Autonomous SDLC Agentic Tool

### *The local-first engineering command center powered by 25 specialized agent brains.*

**Zero Code Egress • Fail-Closed Governance • Sandboxed Verification • Single Portable .exe**

<br />

[![Version](https://img.shields.io/badge/version-1.0.0-0ea5e9?style=for-the-badge&logo=semver&logoColor=white)](./CHANGELOG.md)
[![Platform](https://img.shields.io/badge/platform-Windows_x64-0078D6?style=for-the-badge&logo=windows&logoColor=white)](./docs/user-guide.md)
[![Security](https://img.shields.io/badge/security-fail--closed-10b981?style=for-the-badge&logo=shield&logoColor=white)](./SECURITY.md)
[![Architecture](https://img.shields.io/badge/runtime-local--first-8b5cf6?style=for-the-badge)](./docs/product-overview.md)
[![License](https://img.shields.io/badge/license-Digi_Tracks-64748b?style=for-the-badge)](mailto:digi.tracks@outlook.com)

<br />

<img width="1902" height="672" alt="Recon Desktop Cockpit" src="https://github.com/user-attachments/assets/1469e22b-ff26-4c8d-9f33-d172f7e7ecbe" />
<img width="1886" height="665" alt="Recon Real-Time Stream and Findings" src="https://github.com/user-attachments/assets/b3021360-ef52-4c8a-8351-b3167ff13e27" />

<br />

[Product Overview](./docs/product-overview.md) • [Features](./docs/features.md) • [Use Cases](./docs/use-cases.md) • [User Guide](./docs/user-guide.md) • [FAQ](./docs/faq.md) • [Changelog](./CHANGELOG.md) • [Security](./SECURITY.md)

</div>

---

## ⚡ What is Recon?

**Recon** is an autonomous, local-first desktop command center for engineering teams. It orchestrates **25 specialized AI agent brains** across every phase of the Software Development Life Cycle (SDLC)—from architecture and security static analysis to verified automated patch generation and release readiness.

Built as a single, self-contained desktop executable, Recon runs directly on your workstation without transmitting source code to third-party cloud services.

### Core Architectural Pillars

- 🔒 **100% Local-First & Zero Code Egress**  
  Source code parsing, AST indexing, security analysis, and diff generation execute locally. Code never leaves your machine unless you explicitly connect an external LLM endpoint.

- 🧠 **25 Dedicated Agent Brains**  
  Specialized, role-based agents collaborate across distinct lifecycle phases rather than relying on generic, monolithic prompts.

- 🛡️ **Fail-Closed Governance & Contracts**  
  Every agent operates under declarative contract constraints. Undeclared outputs, unauthorized writes, or missing validations immediately halt execution.

- 🧪 **Sandboxed Worktree Verification**  
  Code modifications are isolated within temporary Git worktrees. Every proposed change is compiled and validated prior to human presentation, with atomic rollback on failure.

- 👨‍💻 **Human-in-the-Loop Decision Gates**  
  Developers retain total control. Inspect syntax-tinted line-by-line diffs, evaluate categorized findings, and approve or reject changes with a single click.

---

## 🧭 The 25 Agent Lifecycle Matrix

```mermaid
flowchart LR
    A["1. Discovery & Strategy"] --> B["2. Architecture & Design"]
    B --> C["3. Implementation & Patches"]
    C --> D["4. Quality & Security"]
    D --> E["5. DevOps & Release"]
```

| Lifecycle Stage | Agent Brain | Core Responsibility |
| :--- | :--- | :--- |
| **1. Discovery & Strategy** | `idea` | Explores problem domain, architectural constraints, and risk factors |
| | `discovery` | Scans workspace, detects frameworks, extracts AST and dependency maps |
| | `requirements` | Formulates structured user stories, acceptance criteria, and quality gates |
| **2. Architecture & Design** | `architecture` | Establishes component topologies, system boundaries, and ADR records |
| | `planning` | Generates dependency task graphs and milestone sequencing |
| | `ux-design` | Validates interaction flows, layout systems, and accessibility guidelines |
| **3. Implementation** | `coding-orchestrator`| Distributes implementation tasks across isolated Git worktrees |
| | `frontend-coding` | Develops responsive UI components, state management, and design systems |
| | `backend-coding` | Implements domain models, API endpoints, business logic, and validation |
| | `database` | Generates safe zero-downtime migrations, schema indexes, and query plans |
| | `refactoring-debt` | Identifies code complexity hotspots, technical debt, and safe refactoring paths |
| **4. Quality & Security** | `testing` | Creates comprehensive unit, integration, property, and regression suites |
| | `security` | Performs static analysis (SAST), secret detection, and vulnerability audit |
| | `compliance` | Validates open-source license governance, headers, and privacy rules |
| | `performance` | Analyzes execution bottlenecks, memory footprint, and query complexity |
| | `accessibility-i18n` | Audits WCAG 2.1 AA compliance, screen reader support, and localization |
| | `code-review` | Executes cross-discipline peer review against architectural contracts |
| **5. DevOps & Release** | `documentation` | Generates OpenAPI specifications, developer guides, and changelogs |
| | `devops-cicd` | Produces production Dockerfiles, CI/CD pipelines, and infrastructure checks |
| | `finops` | Models cloud infrastructure costs and rightsizing recommendations |
| | `observability` | Instruments OpenTelemetry tracing, Prometheus metrics, and structured logs |
| | `incident-triage` | Correlates error telemetry with git revisions for root-cause analysis |
| | `release` | Verifies release artifacts, semantic versioning, and build checklists |
| **Continuous Learning** | `learning` | Synthesizes project-specific heuristics from successful patch cycles |
| | `continuous-improvement`| Recommends systemic architectural enhancements over time |

---

## 🖥️ Command Center Cockpit

The Recon interface delivers a high-density, aerospace-inspired desktop cockpit engineered for professional developer workflows:

- **25-Brain Telemetry Strip**: Instant visual recognition of agent status (*cyan pulse = scanning, emerald = passed, amber = blocked, orange = skipped, ruby = failed*).
- **Live Reasoning Stream**: Watch agent thoughts and model reasoning stream in real time via Server-Sent Events (SSE).
- **Interactive Patch Review**: View real git-diff comparisons with line numbers, `+added`/`-removed` badges, and one-click copy.
- **Findings & Evidence Browser**: Filter security advisories, code smells, and quality issues with direct drill-down into source lines.
- **One-Click Audit Reports**: Export standalone, offline-ready HTML/PDF audit summaries complete with executive scores, quality gates, and evidence chains.
- **Hardware-Encrypted Keys**: Sensitive credentials are encrypted via Windows DPAPI—never saved in plaintext or transmitted to the frontend.

---

## 🚀 Quickstart Guide

Recon is distributed as a single self-contained desktop executable for Windows.

### 1. Download & Launch
1. Download `recon-sdlc.exe` from the [Releases](https://github.com/chandrahotha/Recon_SDLC_Agentic_Tool-P/releases) section.
2. Verify the SHA-256 checksum against our published release notes.
3. Launch `recon-sdlc.exe` directly (no installer required).

### 2. Connect Your Project
In the **PROJECT** panel:
- Enter your project name.
- Provide the local directory path of your repository.
- Click **Register & Connect**.

### 3. Configure Your LLM Endpoint
Recon supports both local air-gapped models and cloud providers:
- **Local (100% Offline)**: Ollama / LM Studio (`http://localhost:11434/v1`) — zero data leaves your PC.
- **Cloud Gateways**: NVIDIA NIM, OpenAI, OpenRouter, Google Gemini (credentials stored via Windows DPAPI).

For detailed walkthroughs, see the [User Guide](./docs/user-guide.md).

---

## 📦 Verified Binary Distribution

| Binary Name | Platform | Type | SHA-256 Checksum |
| :--- | :--- | :--- | :--- |
| `recon-sdlc.exe` | Windows x64 (10/11) | Portable Executable | `AC96AA010C3FF8052514B4A6FD257DAE88FC43D721FBB6FE1B3722882B76C40C` |

*Note: Pre-compiled binaries are officially published through [GitHub Releases](https://github.com/chandrahotha/Recon_SDLC_Agentic_Tool-P/releases).*

---

## 📄 License & Commercial Inquiries

**Proprietary — © 2026 Digi Tracks. All rights reserved.**

Recon — SDLC Agentic Tool is proprietary software developed by **Digi Tracks**. This public showcase repository is provided strictly for product evaluation, architectural transparency, and commercial demonstration purposes.

For enterprise licensing, commercial trials, or bespoke agent integrations:  
📧 **[digi.tracks@outlook.com](mailto:digi.tracks@outlook.com)**

<div align="center">
<br />
<sub>Built by <strong>Digi Tracks</strong> — Engineering intelligence delivered directly to your desktop.</sub>
</div>
