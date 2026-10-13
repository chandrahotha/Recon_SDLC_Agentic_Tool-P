# Security Policy — Recon SDLC Agentic Tool

## Supported Versions

Only the latest release of the Recon SDLC Agentic Tool receives security updates:

| Version | Supported |
| :--- | :--- |
| 1.0.x | :white_check_mark: Yes |
| < 1.0 | :x: No |

---

## Reporting a Security Vulnerability

Digi Tracks takes the security and privacy of the Recon platform seriously. If you identify a security vulnerability, we request that you report it responsibly through private channels.

### How to Report
Please **do not report security vulnerabilities through public GitHub issues**.

Instead, email your security advisory directly to:  
📧 **[digi.tracks@outlook.com](mailto:digi.tracks@outlook.com)**

### What to Include in Your Report
To help us triage and resolve the issue quickly, please include:
1. A clear description of the vulnerability and its potential impact.
2. Step-by-step reproduction instructions or a minimal proof of concept (PoC).
3. The affected version and operating system environment.
4. Any potential mitigations or workarounds identified.

### Response Timeline
- **Initial Acknowledgment**: Within 48 hours of receipt.
- **Triage & Assessment**: Within 5 business days.
- **Coordinated Disclosure**: We work with reporters to coordinate an appropriate patch release window prior to public disclosure.

---

## Security Architecture Principles

Recon is architected with defensive security as a core tenet:
- **Zero Involuntary Egress**: Source code never leaves your local workstation unless you explicitly configure a remote LLM gateway.
- **Credential Protection**: All API keys are encrypted at rest using Windows DPAPI (bound to the local Windows user profile). Plaintext secrets are never stored in unencrypted configuration files.
- **Sandboxed Execution**: Automated code generation executes in isolated, ephemeral Git worktrees with mandatory compilation checks and atomic rollback protection.
- **Model Privacy Gating**: Recon enforces explicit operator confirmation before transmitting source context to models that retain data for training or evaluation.
