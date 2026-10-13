# Changelog — Recon SDLC Agentic Tool

All notable release versions for the Recon SDLC Agentic Tool are documented below.

---

## [1.0.0] — 2026-10-13

### Initial Public GA Release
Recon v1.0.0 represents the general availability release of the local-first autonomous SDLC desktop command center.

#### Core Engine & Multi-Agent Orchestration
- **25 Specialized Agent Brains**: Deployed end-to-end agent orchestration covering Discovery, Architecture, Coding, Database, Security, Testing, DevOps, and Continuous Learning.
- **Fail-Closed Contract Governance**: Enforced declarative contracts ensuring strict input/output boundaries and permission gates across all agent executions.
- **Sandboxed Worktree Verification**: Automatic compilation and test verification within ephemeral Git worktrees with atomic rollback protection.
- **Embedded Persistence**: Zero-dependency local storage utilizing an embedded pure-Go SQLite database and SHA-256 content-addressed artifact store.

#### Desktop Cockpit & Visual Quality
- **Obsidian Aerospace UI**: High-density engineering command center interface designed for technical developers.
- **25-Brain Live Telemetry Strip**: Instant visual feedback on agent lifecycle states (*active pulse, completed, blocked gates, skipped, failed*).
- **Live Reasoning Stream**: Real-time SSE streaming of agent thoughts and model tokens directly into the terminal inspector.
- **Colorized Patch Review**: Side-by-side and unified git diff review with syntax tinting, line numbers, and per-finding verdict controls.
- **Interactive Findings Browser**: Multi-severity filtering and evidence exploration with direct drill-down into source code lines.
- **One-Click Audit Reports**: Standalone offline HTML/PDF compliance reports featuring executive summaries, gate statuses, and evidence chains.

#### Security & Hardware Protection
- **Windows DPAPI Credential Storage**: Hardware-level encryption for LLM gateway API keys at rest.
- **Model Policy Verification**: Automatic checking of data retention policies on configured remote endpoints with required operator consent.
- **Local LLM Compatibility**: Full support for air-gapped local inference via Ollama and LM Studio (`http://localhost:11434/v1`).
- **Portable Distribution**: Single self-contained Windows executable (`recon-sdlc.exe`) with embedded UI assets and native icon resource.
