# Frequently Asked Questions (FAQ) — Recon SDLC Agentic Tool

### Q1: Does Recon send my source code to the cloud?
**No.** Recon is engineered local-first. Repository analysis, AST parsing, secret detection, and diff computation occur locally on your machine via an embedded Go engine. Source code is never sent to third-party services unless you configure a cloud LLM gateway for agent reasoning. Even then, you can use local models (such as Ollama or LM Studio) for 100% air-gapped, zero-egress operation.

---

### Q2: How are the 25 agent brains different from using ChatGPT or Claude directly?
General-purpose LLMs lack project awareness, context isolation, and deterministic validation. Recon breaks down software delivery into 25 role-specialized brains (Architecture, Security, Database, Frontend, QA, etc.). Each brain operates under a strict declarative contract with defined inputs, outputs, and quality gates, collaborating systematically rather than relying on an ambiguous conversational prompt.

---

### Q3: Can an agent make unverified or breaking changes to my repository?
**No.** Automated modifications take place in isolated, ephemeral Git worktrees. Before any proposed code change is shown to you, it must compile and pass existing test suites. If a change breaks the build, it is atomically rolled back. Furthermore, no change is written to your main working branch without explicit developer sign-off in the Patch Review panel.

---

### Q4: How are my API keys and credentials secured?
Recon uses Windows Data Protection API (DPAPI) to encrypt API keys at rest. Keys are encrypted with keys tied directly to your Windows user account, masked in the user interface (showing only the first-4 and last-4 characters), and never stored in plain `.env` files or transmitted back to the browser runtime.

---

### Q5: What programming languages and ecosystems are supported?
Recon's language discovery, AST parsing, and verification sandbox support major development ecosystems, including:
- **Go** (`go build`, `go test`, `go vet`)
- **TypeScript / JavaScript** (Node.js, npm, pnpm, Vite, React, Next.js)
- **Python** (pytest, pip, virtualenv)
- **Rust** (`cargo build`, `cargo test`)
- **Java** (Maven, Gradle)
- **C# / .NET** (`dotnet build`, `dotnet test`)

---

### Q6: Can Recon run completely offline?
**Yes.** You can run Recon in completely offline or air-gapped environments by connecting it to a local inference engine such as Ollama or LM Studio (`http://localhost:11434/v1`). All database storage, artifact caching, and evidence tracking are handled locally by the embedded SQLite database.

---

### Q7: What is the purpose of this public showcase repository?
This public repository (`Recon_SDLC_Agentic_Tool-P`) serves as an official product showcase, public documentation hub, and binary distribution channel for external evaluation. It contains architecture overviews, use cases, and verified binaries without exposing proprietary source code, internal agent schemas, or confidential development workflows.

---

### Q8: How can my organization obtain enterprise licensing or custom integrations?
For enterprise licensing, tailored on-premise agent brains, or commercial pilot programs, contact Digi Tracks directly at **[digi.tracks@outlook.com](mailto:digi.tracks@outlook.com)**.
