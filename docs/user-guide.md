# User Guide — Recon SDLC Agentic Tool

Welcome to the **Recon SDLC Agentic Tool** user guide. This document provides step-by-step instructions for launching, configuring, and operating the Recon desktop command center.

---

## 1. System Requirements

- **Operating System**: Windows 10 or Windows 11 (64-bit)
- **Memory**: 4 GB RAM minimum (8 GB+ recommended)
- **Disk Space**: 100 MB for executable + local project storage
- **Dependencies**: Git 2.30+ installed on your system PATH

---

## 2. Getting Started

Recon is distributed as a self-contained portable executable. No installers, runtime frameworks, or database setups are required.

### Step 1: Download & Integrity Verification
1. Download `recon-sdlc.exe` from the official [GitHub Releases](https://github.com/chandrahotha/Recon_SDLC_Agentic_Tool-P/releases) page.
2. Verify the SHA-256 hash in PowerShell:
   ```powershell
   Get-FileHash -Path .\recon-sdlc.exe -Algorithm SHA256
   ```
3. Confirm that the calculated hash matches the published checksum:
   ```text
   AC96AA010C3FF8052514B4A6FD257DAE88FC43D721FBB6FE1B3722882B76C40C
   ```

### Step 2: Launch the Cockpit
Double-click `recon-sdlc.exe`. The native desktop cockpit window will launch immediately.

---

## 3. Registering Your Project

1. In the upper-left **PROJECT** panel:
   - **Project Name**: Enter a descriptive name for your application.
   - **Workspace Path**: Enter the absolute filesystem path to your local Git repository (e.g., `C:\Work\my-project`).
2. Click **Register & Connect**.
3. Once verified, the connection status chip will turn green (`✓ PROJECT CONNECTED`).

---

## 4. Configuring Model Gateways

Recon operates completely offline for repo analysis and scanning. To enable autonomous reasoning for the 25 agent brains, configure an LLM gateway in **Settings → Provider Credentials**:

### Option A: 100% Offline via Local Ollama / LM Studio (Recommended for maximum privacy)
1. Ensure Ollama is running locally:
   ```bash
   ollama run llama3.3
   ```
2. In the cockpit's Model Picker, select custom endpoint: `http://localhost:11434/v1`.
3. Select your local model. Source code never leaves your local workstation.

### Option B: Cloud Provider Gateways (OpenAI, NVIDIA NIM, Google Gemini)
1. Select your desired provider from the **Gateway / Provider** dropdown.
2. In the **Provider Credentials** card, paste your API key.
3. Click **Save key**.
   - *Security Note*: Keys are encrypted at rest using Windows DPAPI (bound to your Windows account) and only ever displayed masked (`first-4...last-4`).
4. If selecting a model with trial terms or retention policies, review and check the data policy acknowledgement.
5. Click **Save model selection**.

---

## 5. Running the Autonomous SDLC Pipeline

1. In the **LAUNCH CONTROL** panel, click **Start Autonomous SDLC Run**.
2. **25-Brain Telemetry Strip**:
   - The horizontal agent rail displays all 25 brains in true execution order.
   - **Pulsing Cyan**: Currently executing brain.
   - **Emerald Green**: Brain completed successfully with passing quality gates.
   - **Amber**: Brain identified a quality gate or requires operator input.
   - **Orange**: Agent skipped according to project configuration.
   - **Ruby Red**: Gate failure or critical error.
3. **Live Reasoning Stream**:
   - Watch the active agent's thoughts and reasoning stream live into the reasoning terminal via Server-Sent Events (SSE).

---

## 6. Reviewing Findings & Applying Patches

### Reviewing Findings
1. Click the **FINDINGS** tab in the dock.
2. Filter findings by severity (*CRITICAL, HIGH, MEDIUM, LOW*).
3. Click any finding to inspect evidence, line references, and remediation guidance.

### Reviewing and Approving Code Patches
1. When an implementation or security agent proposes a code fix, the **PATCH REVIEW** panel highlights the staged changes.
2. Review the colorized diff:
   - Green rows indicate additions (`+`).
   - Red rows indicate removals (`−`).
   - Line gutters reflect exact file positions.
3. Click **ACCEPT PATCH** to apply the changes to your working tree, or **REJECT PATCH** to discard.

---

## 7. Exporting Compliance & Audit Reports

1. Navigate to the **EVIDENCE** tab in the dock.
2. View the language breakdown bars and finding severity donut chart.
3. Click **⬇ Export HTML Report**.
4. A self-contained, print-to-PDF ready HTML report will be generated and saved to `.sdlc/artifacts/`, containing executive verdicts, gate results, full findings with evidence IDs, and timestamps.

---

## 8. Keyboard Shortcuts

| Shortcut | Action |
| :--- | :--- |
| `1` | Switch to **LOGS** dock tab |
| `2` | Switch to **EVIDENCE** dock tab |
| `3` | Switch to **FINDINGS** dock tab |
| `4` | Switch to **FILES** dock tab |
| `5` | Switch to **SETTINGS** dock tab |
| `/` | Focus the live log search filter |
| `Esc` | Clear log search filter and return focus |
