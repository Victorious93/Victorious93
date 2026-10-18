<div align="center">

<img src="assets/header.png" alt="Victorious Labs — Android tooling · rooting & flashing · AI agents · Linux installers" width="100%" />

[<img src="assets/tagline.png" alt="Building Android & Linux tooling" width="100%" />](https://github.com/Victorious93)

[![GitHub followers](https://img.shields.io/github/followers/Victorious93?label=Follow&style=for-the-badge&logo=github&color=0D0221&labelColor=BD00FF&logoColor=00F0FF)](https://github.com/Victorious93)

</div>

## ⚡ About

- **Android & Termux tooling** — modules, rootfs work, and on-device apps around Magisk/KernelSU and Linux-on-Android.
- **AI agent hubs** — a phone-side command center with a small fleet of companion apps and tools.
- **Device recovery & installers** — flashing/root workflows and cross-platform Pi Zero tooling.
- **Security labs & experiments** — KYC test labs, swarm-style pentest agents, file managers, and retro multiplayer.

<img src="assets/divider.png" width="100%" alt="" />

## 🟣 The fleet

[**droidcommand-AI**](https://github.com/Victorious93/droidcommand-AI) is the **controller** — the hub I talk to. The other apps are members, grouped by how they connect (not by topic). This is a map, not a claim that every link is live.

```mermaid
flowchart LR
  Hub["droidcommand-AI<br/>CONTROLLER"]

  Hub --- BC
  Hub --- EN
  Hub --- TX
  Hub --- HP

  subgraph BC["BOUND_COMPANION"]
    HAI["HackerAI-Commander"]
    PSA["Pentest-Swarm-AI"]
    EDL["EDL-Commander [planned]"]
  end

  subgraph EN["EXTERNAL_NODE"]
    RF["rootforge-os"]
    FM["File-Manager"]
    VK["Victorious-Keyboard"]
    VF["victorious-flash"]
    VM["victorious-mesh"]
  end

  subgraph TX["TERMUX_IPC"]
    VS["VictorSuite"]
  end

  subgraph HP["HOST_PROCESS_TOOL"]
    KYC["KYC-AuditLab"]
    BPI["BakerPi-Installer [Likely]"]
  end
```

Public repos are linked. Names without a link are **not a public repo** on this account from here (they may still be private or not created yet). VictorLink64 is a separate project — **not** in this fleet.

### Controller (hub)

The app at the center. Members hang off this; they are not folded into it.

- [**droidcommand-AI**](https://github.com/Victorious93/droidcommand-AI) — on-device AI command center: chat, tools, and the place the fleet is reached from.

### BOUND_COMPANION

Tightly bound apps signed with the shared key.

- [**HackerAI-Commander**](https://github.com/Victorious93/HackerAI-Commander) — chat with AI to find and fix security issues; companion in this fleet.
- [**Pentest-Swarm-AI**](https://github.com/Victorious93/Pentest-Swarm-AI) — swarm of specialist agents for authorized pentest work (AGPL fork with an Android companion).
- **EDL-Commander** *[planned]* — Qualcomm EDL recovery helper (Sahara-first, safety-minded). No public repo here yet.

### EXTERNAL_NODE

Separate apps that talk over a small JSON command bridge.

- [**rootforge-os**](https://github.com/Victorious93/rootforge-os) — Debian live toolkit and phone/desktop apps for Magisk/KernelSU module and boot-image work.
- **File-Manager** — standalone Android file manager (dual panes, tabs, copy/move queue, search, trash). No public repo here yet.
- **Victorious-Keyboard** — Android keyboard with encrypted clipboard, a developer row, snippets, and offline dictionaries. No public repo here yet.
- **victorious-flash** — download, verify, and flash Linux ISOs to USB. No public repo here yet.
- [**victorious-mesh**](https://github.com/Victorious93/victorious-mesh) — Android VPN / mesh node for a self-hosted Headscale network.

### TERMUX_IPC

Commands into Termux.

- [**VictorSuite**](https://github.com/Victorious93/VictorSuite) — Termux-based Android Linux suite: proot containers, backup/restore, plugins, X11, and automation.

### HOST_PROCESS_TOOL

A local process / HTTP tool.

- **KYC-AuditLab** — local-first KYC security test lab against a bundled simulator. No public repo here yet.
- [**BakerPi-Installer**](https://github.com/Victorious93/BakerPi-Installer) *[Likely]* — browser or native UI to install tools on a Raspberry Pi Zero 1.3 over USB OTG or SSH.

<img src="assets/divider.png" width="100%" alt="" />

## 🎮 Also (not in the fleet)

| Project | Description |
|:--------|:------------|
| [**VictorLink64**](https://github.com/Victorious93/VictorLink64) | Android app for N64 & Super Nintendo play, built-in chess, and local/online multiplayer (PLAY · CONNECT · CAST). |
| [**MT-Manager-VIP**](https://github.com/Victorious93/MT-Manager-VIP) *(FileForge)* | FileForge: clean-room Android file manager skeleton (Compose) — M0, dual-pane planned. |

<img src="assets/divider.png" width="100%" alt="" />

## 🔷 Tech stack

<p align="center">
  <img src="https://img.shields.io/badge/Kotlin-0D0221?style=for-the-badge&logo=kotlin&logoColor=BD00FF" alt="Kotlin" />
  <img src="https://img.shields.io/badge/Java-0D0221?style=for-the-badge&logo=openjdk&logoColor=FF00E5" alt="Java" />
  <img src="https://img.shields.io/badge/Python-0D0221?style=for-the-badge&logo=python&logoColor=00F0FF" alt="Python" />
  <img src="https://img.shields.io/badge/Rust-0D0221?style=for-the-badge&logo=rust&logoColor=FF00E5" alt="Rust" />
  <img src="https://img.shields.io/badge/Go-0D0221?style=for-the-badge&logo=go&logoColor=00F0FF" alt="Go" />
  <img src="https://img.shields.io/badge/C-0D0221?style=for-the-badge&logo=c&logoColor=BD00FF" alt="C" />
  <img src="https://img.shields.io/badge/Shell-0D0221?style=for-the-badge&logo=gnubash&logoColor=00F0FF" alt="Shell" />
  <img src="https://img.shields.io/badge/HTML-0D0221?style=for-the-badge&logo=html5&logoColor=FF00E5" alt="HTML" />
  <img src="https://img.shields.io/badge/Android-0D0221?style=for-the-badge&logo=android&logoColor=00F0FF" alt="Android" />
  <img src="https://img.shields.io/badge/Jetpack%20Compose-0D0221?style=for-the-badge&logo=jetpackcompose&logoColor=BD00FF" alt="Jetpack Compose" />
</p>

## 📊 Stats

See my activity at **[github.com/Victorious93](https://github.com/Victorious93)**.

<details>
<summary><b>GitHub stats</b> (live cards — may not render in the GitHub mobile app)</summary>
<br />

<div align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=Victorious93&show_icons=true&theme=radical&hide_border=true&count_private=true" alt="Victorious93 GitHub stats" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Victorious93&layout=compact&theme=radical&hide_border=true&langs_count=8" alt="Top languages" />
</div>

<div align="center">
  <img src="https://streak-stats.demolab.com/?user=Victorious93&theme=radical&hide_border=true" alt="GitHub streak stats" />
</div>

</details>

<div align="center">

*Victorious Labs — tools for Android, Linux, and agent-driven workflows.*

<img src="assets/footer.png" alt="" width="100%" />

</div>
