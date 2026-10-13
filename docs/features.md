# Product Features — Recon SDLC Agentic Tool

## 1. Multi-Agent SDLC Orchestration

Recon deploys 25 purpose-built, collaborative agent brains across five stages of engineering delivery:

### Discovery & Strategic Planning
- **`idea`**: Explores problem spaces, analyzes functional feasibility, and flags potential security and architectural risks early.
- **`discovery`**: Performs deep workspace scanning, framework detection, AST structure parsing, and repository fingerprinting.
- **`requirements`**: Translates project objectives into structured user stories, acceptance criteria, and traceable quality gates.

### Architecture & System Design
- **`architecture`**: Defines system boundaries, microservice topologies, API contracts, and Architecture Decision Records (ADRs).
- **`planning`**: Compiles dependency task graphs, resource allocations, and milestone execution schedules.
- **`ux-design`**: Validates interaction patterns, component hierarchies, and WCAG accessibility specifications.

### Implementation & Verified Coding
- **`coding-orchestrator`**: Coordinates multi-file tasks and allocates coding assignments across isolated Git worktrees.
- **`frontend-coding`**: Generates responsive, accessible UI components, design tokens, and state management logic.
- **`backend-coding`**: Implements domain models, REST/gRPC endpoints, service logic, and input validation.
- **`database`**: Generates zero-downtime database migrations, schema constraints, index optimizations, and query plans.
- **`refactoring-debt`**: Scans for cyclomatic complexity hotspots, code smells, and safely refactors legacy components.

### Quality, Security & Assurance
- **`testing`**: Synthesizes comprehensive unit, integration, property-based, and regression test suites.
- **`security`**: Executes static application security testing (SAST), secret detection, and CVE vulnerability mitigation.
- **`compliance`**: Audits open-source licenses, software inventory, and privacy policy conformance.
- **`performance`**: Identifies computational bottlenecks, memory allocation leaks, and query execution overhead.
- **`accessibility-i18n`**: Audits WCAG 2.1 AA accessibility, keyboard navigation, color contrast, and localization readiness.
- **`code-review`**: Conducts multi-discipline peer reviews against architectural contracts and code standards.

### DevOps, Operations & Continuous Improvement
- **`documentation`**: Synchronizes OpenAPI specifications, architecture diagrams, and release changelogs.
- **`devops-cicd`**: Crafts production-ready Dockerfiles, CI/CD pipeline definitions, and deployment health checks.
- **`finops`**: Models infrastructure resource allocation, network egress, and cloud cost optimization.
- **`observability`**: Instruments OpenTelemetry tracing, Prometheus metrics, and structured log emitters.
- **`incident-triage`**: Correlates runtime telemetry alerts with Git commits for accelerated root-cause analysis (RCA).
- **`release`**: Validates release candidate packages, semantic versioning, and build integrity checklists.
- **`learning` & `continuous-improvement`**: Captures verified project heuristics to recommend systemic architectural improvements.

---

## 2. Desktop Command Center Cockpit

- **Obsidian Aerospace Visual Theme**: High-contrast, dense engineering dashboard designed for professional development monitors.
- **Live 25-Brain Telemetry Strip**: Instant visual feedback for each brain's operational state (*pulsing electric cyan for active scanning, emerald for passed, amber for quality gates, orange for skipped, ruby for failures*).
- **Real-Time Streaming Reasoning Terminal**: Live streaming of model reasoning tokens via Server-Sent Events (SSE), keeping developers informed during complex reasoning tasks.
- **Virtualized Live Event Log**: High-performance log stream capable of rendering thousands of runtime events without UI degradation, with instant case-insensitive filtering (`/` shortcut).

---

## 3. Sandboxed Patch Review & Safety Gates

- **Ephemeral Git Worktrees**: Automated code modifications take place in isolated worktrees, completely shielding your primary working directory.
- **Compile-Before-Show Guarantee**: If an agent generates code that fails compilation or breaks existing test suites, the change is atomically discarded.
- **Visual Diff Inspection**: Side-by-side and unified git-style diff viewer with syntax tinting, line gutters, `+added`/`-removed` metric badges, and one-click clipboard copying.
- **Per-Finding Human Verdicts**: Engineers can selectively accept or reject individual findings and patch hunks with full decision persistence.

---

## 4. Security & Privacy Hardening

- **Local-First Architecture**: Source code stays on your physical machine. No background telemetry or code telemetry is transmitted.
- **Windows DPAPI Credential Protection**: API keys entered into the UI are encrypted at rest using Windows Data Protection API (DPAPI). Keys are masked in the UI and never exposed to the frontend renderer.
- **Model Privacy Gating**: Recon verifies the privacy and retention policies of configured LLM gateways. Endpoints with trial data-retention require explicit developer acknowledgment before receiving context.
- **Air-Gapped Local LLM Compatibility**: Seamless integration with local inference engines (Ollama, LM Studio, vLLM) for completely air-gapped environments.

---

## 5. Reporting & Evidence Lineage

- **Content-Addressed Evidence Store**: All analysis findings and test results are stored in an embedded SQLite database backed by SHA-256 content-addressed artifacts.
- **One-Click Offline Reports**: Export branded, offline-ready HTML/PDF audit reports summarizing executive health scores, quality gates, findings breakdown, and evidence chains.
