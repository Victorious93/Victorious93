<div align="center">

<img src="assets/victorious-framework-logo.png" alt="Victorious Framework" width="900" />

<p>
  <a href="https://victorious-framework.pages.dev"><img src="https://img.shields.io/badge/Victorious_Framework-Website-FFB000?style=for-the-badge&labelColor=0A0F1F&color=FFB000" alt="Victorious Framework website" /></a>
  <a href="https://victorious-designs.pages.dev"><img src="https://img.shields.io/badge/Victorious_Designs-Website-FF2E97?style=for-the-badge&labelColor=0A0F1F&color=FF2E97" alt="Victorious Designs website" /></a>
  <a href="https://www.instagram.com/sudo.victorious00"><img src="https://img.shields.io/badge/Instagram-@sudo.victorious00-00F0FF?style=for-the-badge&logo=instagram&logoColor=00F0FF&labelColor=0A0F1F&color=00F0FF" alt="Instagram @sudo.victorious00" /></a>
</p>

<br />

<img src="assets/banner.png" alt="VICTORIOUS93 — Victorious Framework: Android tooling, rooting and flashing, AI agents, Linux installers" width="100%" />

<br />

[![Follow on GitHub](https://img.shields.io/github/followers/Victorious93?label=Follow&style=for-the-badge&logo=github&color=0A0F1F&labelColor=FF2E97&logoColor=00F0FF)](https://github.com/Victorious93)

```text
>_ victorious-framework --whoami
```

**Android · Linux · AI agents · security tooling — separate apps, one fleet.**

**[About](#-about)** · **[Fleet](#-victorious-fleet)** · **[More](#-more-apps--tools)** · **[Architecture](#-how-the-fleet-connects)** · **[Stack](#-tech-stack)**

</div>

## ⚡ About

I'm Don, and I build the **Victorious Framework**: Android, Linux, and security tools that ship as separate apps and connect to one hub.

| | Focus | What it covers |
|:-:|:--|:--|
| 📱 | **Android & host tooling** | Root modules, boot-image work, Linux-on-Android, keyboard, file manager |
| 🧠 | **AI agent hub** | [droidcommand-AI](https://github.com/Victorious93/droidcommand-AI) — controller; other apps stay standalone |
| 🔧 | **Recovery & installers** | Qualcomm EDL recovery, Linux ISO flashing, Raspberry Pi tool installs |
| 🛡️ | **Security labs** | AI pentest assistants and a KYC test lab that only targets its own simulator |

> [!NOTE]
> Most projects are in **early development**. Each repo README states what has (and has not) been tested on real hardware.

Monorepo pointers: **[Victorious93/victorious-fleet](https://github.com/Victorious93/victorious-fleet)** · Site: **[victorious-framework.pages.dev](https://victorious-framework.pages.dev)**

<img src="assets/divider.png" width="100%" alt="" />

<p align="center"><img src="assets/logos/victorious-framework-hoodie-brand.png" alt="Victorious Framework" width="280"></p>

## 🛰️ Victorious fleet

Grouped by how each app connects to the hub. Package IDs come from each project’s build files where defined. Private repos are named only (no public link).

### Controller / Hub

| | App | Package | Purpose |
|:-:|:--|:--|:--|
| <img src="assets/logos/droidcommand-logo.jpg" width="44" alt="" /> | [**droidcommand-AI**](https://github.com/Victorious93/droidcommand-AI) | `ai.droidcommand.app` | Fleet controller — remote command & orchestration |
| <img src="assets/logos/pyraclaw-logo.jpg" width="44" alt="" /> | [**Pyra Claw**](https://github.com/Victorious93/pyra-claw) | `com.victorious.pyraclaw` *(companion)* / hardware hub | Pi 5 + ESP32 command hub |
| <img src="assets/logos/victormodem-logo.jpg" width="44" alt="" /> | VictorModem *(private)* | hardware — no Android package yet | ESP32-S3 + cellular second line |

### Bound Companions

| | App | Package | Purpose |
|:-:|:--|:--|:--|
| <img src="assets/logos/hackerai-logo.jpg" width="44" alt="" /> | [**HackerAI-Commander**](https://github.com/Victorious93/HackerAI-Commander) | `ai.hackerai.companion` | Companion to the hackeraiETC fork |
| <img src="assets/logos/pentest-swarm-logo.png" width="44" alt="" /> | [**Pentest-Swarm-AI**](https://github.com/Victorious93/Pentest-Swarm-AI) | `ai.pentestswarm.companion` | Multi-agent pentest swarm companion |
| <img src="assets/logos/edl-commander-logo.png" width="44" alt="" /> | [**EDL-Commander**](https://github.com/Victorious93/EDL-Commander) | `ai.edlcommander.companion` | Safety-first Qualcomm EDL companion |

### External Nodes

| | App | Package | Purpose |
|:-:|:--|:--|:--|
| <img src="assets/logos/rootforge-logo.jpg" width="44" alt="" /> | [**rootforge-os**](https://github.com/Victorious93/rootforge-os) | `ai.rootforge.os` | Rooting / root-management |
| <img src="assets/logos/file-manager-logo.png" width="44" alt="" /> | [**File-Manager**](https://github.com/Victorious93/File-Manager) | `ai.victorious.victorfiles` *(rename → `filemanager` planned)* | Dual-pane power-user file manager |
| <img src="assets/logos/victorious-keyboard-logo.png" width="44" alt="" /> | [**Victorious-Keyboard**](https://github.com/Victorious93/Victorious-Keyboard) | `com.victorious.keyboard` | Custom keyboard + media controls |
| <img src="assets/logos/victorious-flash-logo.png" width="44" alt="" /> | [**Victorious Flash**](https://github.com/Victorious93/victorious-flash) | `com.victorious.flash.android` | Desktop Linux ISO → USB installer |
| <img src="assets/logos/victorious-mesh-logo.jpg" width="44" alt="" /> | [**Victorious Mesh**](https://github.com/Victorious93/victorious-mesh) | `com.victorious.mesh` | Secure mesh / VPN |
| <img src="assets/logos/victorious-browser-logo.jpg" width="44" alt="" /> | [**Victorious Browser**](https://github.com/Victorious93/victorious-browser) | `com.victorious.browser` | Security / recon browser |
| <img src="assets/logos/victorsms-logo.jpg" width="44" alt="" /> | [**VictorSMS**](https://github.com/Victorious93/victorsms) | `com.victorious.sms` | Matrix messaging + persona tools |
| <img src="assets/logos/victorlaunch-logo.jpg" width="44" alt="" /> | [**VictorLaunch**](https://github.com/Victorious93/victorlaunch) | `com.victorious.launch` | Fleet home-screen launcher |
| <img src="assets/logos/victorspoof-logo.jpg" width="44" alt="" /> | [**VictorSpoof**](https://github.com/Victorious93/victorspoof) | `com.victorious.spoof` | Novelty caller-ID with compliance guards |
| <img src="assets/logos/victorlink64-logo.png" width="44" alt="" /> | [**VictorLink64**](https://github.com/Victorious93/VictorLink64) | `org.victoriousframework.victorlink64` | Multi-game emulator hub *(not remote fleet)* |
| <img src="assets/logos/victorcam-logo.jpg" width="44" alt="" /> | [**VictorCam**](https://github.com/Victorious93/victorcam) | `com.victorious.cam` | OBS-style virtual camera *(repo scaffolding)* |

### Host & Shell Tools

| | App | Package | Purpose |
|:-:|:--|:--|:--|
| <img src="assets/logos/victorsuite-logo.png" width="44" alt="" /> | [**VictorSuite**](https://github.com/Victorious93/VictorSuite) | `com.termux` *(TERMUX_IPC lineage)* | Android Linux environment suite for the fleet |
| <img src="assets/logos/kyc-auditlab-logo.png" width="44" alt="" /> | [**KYC-AuditLab**](https://github.com/Victorious93/KYC-AuditLab) | `com.identityshield.companion` | Local KYC / identity audit lab |
| <img src="assets/logos/bakerpi-logo.jpg" width="44" alt="" /> | [**BakerPi-Installer**](https://github.com/Victorious93/BakerPi-Installer) | n/a (host tool) | Pi Zero tool installer (PC / on-device) |
| | [**DreamOS-Victorious**](https://github.com/Victorious93/DreamOS-Victorious) | n/a | Phase 1 ROM source integration foundation |

### Social / Marketplace

| | App | Package | Purpose |
|:-:|:--|:--|:--|
| <img src="assets/logos/matchvictorious-logo.jpg" width="44" alt="" /> | [**MatchVictorious**](https://github.com/Victorious93/matchvictorious) | `com.victorious.match` | Dating hub |
| <img src="assets/logos/victorpedigree-logo.jpg" width="44" alt="" /> | VictoryPed *(private)* | `com.victorious.victoryped` | Social / marketplace for bully breeders |

### Games

| | App | Package | Purpose |
|:-:|:--|:--|:--|
| <img src="assets/logos/victorops-zombies-logo.jpg" width="44" alt="" /> | VictorOps Zombies *(private)* | `com.victorious.zombie` | Wave-survival zombies game (libGDX + Kotlin) |

<img src="assets/divider.png" width="100%" alt="" />

## 🧰 More apps & tools

Projects by Don that are not (yet) wired into the fleet connection model above.

| | Project | What it is |
|:--:|:--|:--|
| <img src="assets/icons/droidpilot.png" height="28" align="center" alt="" /> | [**droidpilot**](https://github.com/Victorious93/droidpilot) *(DroidPilot Forge)* | Stable Android device automation for AI agents via Accessibility Service + MCP — no ADB, no OCR |

<img src="assets/divider.png" width="100%" alt="" />

## 🟣 How the fleet connects

<details open>
<summary><b>Architecture diagram</b>: apps grouped by connection class</summary>
<br />

```mermaid
flowchart LR
  Hub["droidcommand-AI<br/>CONTROLLER"]
  Hub --- BC
  Hub --- EN
  Hub --- TX
  Hub --- HP
  Hub --- PHY["Pyra Claw<br/>Pi5+ESP32"]
  subgraph BC["BOUND_COMPANION"]
    HAI["HackerAI-Commander"]
    PSA["Pentest-Swarm-AI"]
    EDL["EDL-Commander"]
  end
  subgraph EN["EXTERNAL_NODE"]
    RF["rootforge-os"]
    FM["File-Manager"]
    VK["Victorious-Keyboard"]
    VF["victorious-flash"]
    VM["victorious-mesh"]
    VB["victorious-browser"]
    VSMS["victorsms"]
    VLC["victorlaunch"]
    VSP["victorspoof"]
    VL64["VictorLink64"]
    VC["VictorCam"]
  end
  subgraph TX["TERMUX_IPC"]
    VS["VictorSuite"]
  end
  subgraph HP["HOST_PROCESS_TOOL"]
    KYC["KYC-AuditLab"]
    BPI["BakerPi-Installer"]
  end
```

> [!IMPORTANT]
> This shows how the apps are *meant* to connect. Not every link is wired yet. Private repos stay unlinked until public.

</details>

<img src="assets/divider.png" width="100%" alt="" />

## 🔷 Tech stack

<p align="center">
  <img src="https://img.shields.io/badge/Kotlin-0A0F1F?style=for-the-badge&logo=kotlin&logoColor=00F0FF" alt="Kotlin" />
  <img src="https://img.shields.io/badge/Java-0A0F1F?style=for-the-badge&logo=openjdk&logoColor=FF2E97" alt="Java" />
  <img src="https://img.shields.io/badge/Python-0A0F1F?style=for-the-badge&logo=python&logoColor=00F0FF" alt="Python" />
  <img src="https://img.shields.io/badge/Rust-0A0F1F?style=for-the-badge&logo=rust&logoColor=FF2E97" alt="Rust" />
  <img src="https://img.shields.io/badge/Go-0A0F1F?style=for-the-badge&logo=go&logoColor=00F0FF" alt="Go" />
  <img src="https://img.shields.io/badge/TypeScript-0A0F1F?style=for-the-badge&logo=typescript&logoColor=FF2E97" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Shell-0A0F1F?style=for-the-badge&logo=gnubash&logoColor=00F0FF" alt="Shell" />
  <img src="https://img.shields.io/badge/C%2FC%2B%2B-0A0F1F?style=for-the-badge&logo=c&logoColor=FF2E97" alt="C/C++" />
</p>
<p align="center">
  <img src="https://img.shields.io/badge/Android-0A0F1F?style=for-the-badge&logo=android&logoColor=00F0FF" alt="Android" />
  <img src="https://img.shields.io/badge/Jetpack%20Compose-0A0F1F?style=for-the-badge&logo=jetpackcompose&logoColor=FF2E97" alt="Jetpack Compose" />
  <img src="https://img.shields.io/badge/Gradle-0A0F1F?style=for-the-badge&logo=gradle&logoColor=00F0FF" alt="Gradle" />
  <img src="https://img.shields.io/badge/FastAPI-0A0F1F?style=for-the-badge&logo=fastapi&logoColor=FF2E97" alt="FastAPI" />
  <img src="https://img.shields.io/badge/Tauri-0A0F1F?style=for-the-badge&logo=tauri&logoColor=00F0FF" alt="Tauri" />
  <img src="https://img.shields.io/badge/Docker-0A0F1F?style=for-the-badge&logo=docker&logoColor=FF2E97" alt="Docker" />
  <img src="https://img.shields.io/badge/GitHub%20Actions-0A0F1F?style=for-the-badge&logo=githubactions&logoColor=00F0FF" alt="GitHub Actions" />
</p>

<details>
<summary><b>📊 GitHub stats</b> (live cards from third-party services; may not load in the GitHub mobile app)</summary>
<br />

<div align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=Victorious93&show_icons=true&hide_border=true&bg_color=0A0F1F&title_color=FF2E97&text_color=9FB4E8&icon_color=00F0FF&ring_color=FF2E97" alt="Victorious93 GitHub stats" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Victorious93&layout=compact&hide_border=true&langs_count=8&exclude_repo=VictorLink64&bg_color=0A0F1F&title_color=FF2E97&text_color=9FB4E8" alt="Top languages (excluding vendored emulator code)" />
</div>

<div align="center">
  <img src="https://streak-stats.demolab.com/?user=Victorious93&hide_border=true&background=0A0F1F&ring=FF2E97&fire=FF2E97&currStreakNum=00F0FF&currStreakLabel=00F0FF&sideNums=FF2E97&sideLabels=9FB4E8&dates=6B7DB3&stroke=1B2A5C" alt="GitHub streak stats" />
</div>

</details>

<div align="center">

<sub><code>&gt;_</code> Victorious Framework: tools for Android, Linux, and agent-driven workflows.</sub>

<img src="assets/footer.png" alt="" width="100%" />

</div>
