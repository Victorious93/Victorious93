<div align="center">

<img src="assets/banner.png" alt="VICTORIOUS93 — Victorious Framework: Android tooling, rooting and flashing, AI agents, Linux installers" width="100%" />

<br />

[![Follow on GitHub](https://img.shields.io/github/followers/Victorious93?label=Follow&style=for-the-badge&logo=github&color=0A0F1F&labelColor=FF2E97&logoColor=00F0FF)](https://github.com/Victorious93)
```text
>_ victorious-framework --whoami
```

**[About](#-about)** · **[Featured](#-featured-projects)** · **[More](#-more-projects)** · **[Architecture](#-how-the-fleet-connects)** · **[Stack](#-tech-stack)**

</div>

## ⚡ About

I'm Don, and I build the **Victorious Framework**: a set of Android, Linux and security tools that run as separate apps and connect to one hub app.

| | Focus | What it covers |
|:-:|:--|:--|
| 📱 | **Android & Termux tooling** | Root modules, boot-image work, Linux-on-Android, a keyboard and a file manager. |
| 🧠 | **AI agent hub** | [droidcommand-AI](https://github.com/Victorious93/droidcommand-AI) is the controller. The other apps stay standalone and connect to it. |
| 🔧 | **Recovery & installers** | Qualcomm EDL recovery, Linux ISO flashing, and Raspberry Pi Zero tool installs. |
| 🛡️ | **Security labs** | AI pentest assistants and a KYC test lab that only targets its own simulator. |

> [!NOTE]
> Most of these projects are in **early development**. Each repo's README says what has and hasn't been tested on real hardware.

<img src="assets/divider.png" width="100%" alt="" />

## 🛰️ Featured projects

| Project | What it is |
|:--|:--|
| [**droidcommand-AI**](https://github.com/Victorious93/droidcommand-AI) <br/> `Kotlin` `Compose` | The hub of the fleet. You chat with it, and it calls tools under a security policy, runs “Forge” build workflows, and sends commands to member apps. The JVM engine is CI-tested. |
| [**rootforge-os**](https://github.com/Victorious93/rootforge-os) <br/> `Debian` `Termux` | A Debian live distro and Termux rootfs toolkit for Magisk/KernelSU module and boot-image work, with phone and desktop apps. |
| [**Victorious Keyboard**](https://github.com/Victorious93/Victorious-Keyboard) <br/> `Android` | An Android keyboard based on FlorisBoard, with an AES-256-GCM encrypted clipboard, a terminal key row, snippets and offline dictionary packs. Nothing leaves the device. |
| [**VictorSuite**](https://github.com/Victorious93/VictorSuite) <br/> `Termux` `proot` | A Termux/ZeroTermux-based Android Linux suite with proot containers, backup/restore, a plugin framework, X11 and automation. |
| [**VictorLink64**](https://github.com/Victorious93/VictorLink64) <br/> `Early beta` | Plays N64 (Mupen64Plus) and SNES (bsnes) games from your own files, with built-in chess and online, Wi-Fi or Bluetooth rooms. |
| [**HackerAI-Commander**](https://github.com/Victorious93/HackerAI-Commander) <br/> `Fork` `AIDL` | A fork of `hackerai-tech/hackerai`, the AI pentest assistant, plus a Kotlin/Compose Android companion that DroidCommand controls over AIDL. |

<img src="assets/divider.png" width="100%" alt="" />

## 🧰 More projects

| Project | Status / scope | What it is |
|:--|:--|:--|
| [**Pentest-Swarm-AI**](https://github.com/Victorious93/Pentest-Swarm-AI) | AGPL fork | Armur-Ai's Go multi-agent pentest CLI, with an Android companion APK for the fleet. |
| [**BakerPi-Installer**](https://github.com/Victorious93/BakerPi-Installer) | FastAPI | Installs tools on a Raspberry Pi Zero 1.3 over USB OTG or SSH, from a browser or native UI. |
| [**victorious-mesh**](https://github.com/Victorious93/victorious-mesh) | tailscale-android fork | An Android VPN/mesh node for a self-hosted Headscale network. |
| [**KYC-AuditLab**](https://github.com/Victorious93/KYC-AuditLab) | Simulator only | IdentityShield, a local-first KYC security test lab that runs against its own bundled simulator. |
| [**Victorious Flash**](https://github.com/Victorious93/victorious-flash) | Tauri v2 | A desktop app that downloads Linux ISOs, checks them against checksums and flashes them to USB or SD. |
| [**EDL-Commander**](https://github.com/Victorious93/EDL-Commander) | ⚠️ Not hardware-tested | A safety-first Rust framework for Qualcomm EDL recovery, with a Sahara core and a simulator. |
| [**File-Manager**](https://github.com/Victorious93/File-Manager) | Standalone | An Android file manager with dual panes, tabs, and a copy/move queue with undo. |
| [**DreamOS-Victorious**](https://github.com/Victorious93/DreamOS-Victorious) | ⚠️ Not flashable | Phase 1 groundwork for pulling Android ROM source together: profile validator, reproducible source bundle, SHA-256 integrity check. |
| [**MT-Manager-VIP**](https://github.com/Victorious93/MT-Manager-VIP) *(FileForge)* | Skeleton (M0) | The skeleton of a clean-room Compose file manager. |

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
  subgraph BC["BOUND_COMPANION"]
    HAI["HackerAI-Commander"]
    PSA["Pentest-Swarm-AI"]
    EDL["EDL-Commander"]
  end
  subgraph EN["EXTERNAL_NODE"]
    RF["rootforge-os"]
    FM["File-Manager"]
    VK["Victorious Keyboard"]
    VF["Victorious Flash"]
    VM["victorious-mesh"]
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
> This shows how the apps are *meant* to connect. Not every link is wired up yet. VictorLink64 isn't part of the fleet.

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
  <img src="https://img.shields.io/badge/Termux-0A0F1F?style=for-the-badge&logo=gnometerminal&logoColor=FF2E97" alt="Termux" />
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
