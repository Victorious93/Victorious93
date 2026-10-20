<div align="center">

<img src="assets/victorious-framework-logo.png" alt="Victorious Framework" width="900" />

<br />

<img src="assets/banner.png" alt="VICTORIOUS93 — Victorious Framework: Android tooling, rooting and flashing, AI agents, Linux installers" width="100%" />

<br />

[![Follow on GitHub](https://img.shields.io/github/followers/Victorious93?label=Follow&style=for-the-badge&logo=github&color=0A0F1F&labelColor=FF2E97&logoColor=00F0FF)](https://github.com/Victorious93)
```text
>_ victorious-framework --whoami
```

**[About](#-about)** · **[Fleet](#-victorious-fleet)** · **[More](#-more-apps--tools)** · **[Architecture](#-how-the-fleet-connects)** · **[Stack](#-tech-stack)**

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

## 🛰️ Victorious fleet

Grouped by how each app connects to the hub. Package IDs are shown where the project defines one.

### Controllers / hub

| | Project | Package | What it is |
|:--:|:--|:--|:--|
| <img src="assets/icons/droidcommand-AI.png" height="28" align="center" alt="" /> | [**droidcommand-AI**](https://github.com/Victorious93/droidcommand-AI) | `ai.droidcommand.app` | Android AI agent hub: JVM-tested tool engine, Forge builds, and fleet IPC to Termux/security companions. |
| <img src="assets/icons/pyra-claw.png" height="28" align="center" alt="" /> | **Pyra Claw** *(private, in development)* | — | Pi 5 + ESP32 command hub that bridges the phone controller to physical devices. |

### Bound companions

| | Project | Package | What it is |
|:--:|:--|:--|:--|
| <img src="assets/icons/HackerAI-Commander.png" height="28" align="center" alt="" /> | [**HackerAI-Commander**](https://github.com/Victorious93/HackerAI-Commander) | `ai.hackerai.companion` | Fork of `hackerai-tech/hackerai` — AI pentest assistant with a Kotlin/Compose Android companion for the fleet. |
| <img src="assets/icons/Pentest-Swarm-AI.png" height="28" align="center" alt="" /> | [**Pentest-Swarm-AI**](https://github.com/Victorious93/Pentest-Swarm-AI) | `ai.pentestswarm.companion` | AGPL fork of Armur Pentest Swarm AI with an Android companion APK for the DroidCommand fleet. |
| <img src="assets/icons/EDL-Commander.png" height="28" align="center" alt="" /> | [**EDL-Commander**](https://github.com/Victorious93/EDL-Commander) | `ai.edlcommander.companion` | Safety-first Rust framework for Qualcomm EDL recovery — Phase 1 Sahara core + simulator (no USB yet). |

### External nodes

| | Project | Package | What it is |
|:--:|:--|:--|:--|
| <img src="assets/icons/rootforge-os.png" height="28" align="center" alt="" /> | [**rootforge-os**](https://github.com/Victorious93/rootforge-os) | — | Debian live distro + Termux rootfs toolkit for Magisk/KernelSU module and boot-image work. |
| <img src="assets/icons/File-Manager.png" height="28" align="center" alt="" /> | [**File-Manager**](https://github.com/Victorious93/File-Manager) *(VictorFiles)* | `ai.victorious.filemanager` | Standalone Android file manager with dual panes, tabs, copy/move queue with undo, and optional fleet stub. |
| <img src="assets/icons/Victorious-Keyboard.png" height="28" align="center" alt="" /> | [**Victorious-Keyboard**](https://github.com/Victorious93/Victorious-Keyboard) | — | Android IME based on FlorisBoard: encrypted clipboard, developer row, snippets, offline dictionary packs. |
| <img src="assets/icons/victorious-flash.png" height="28" align="center" alt="" /> | [**victorious-flash**](https://github.com/Victorious93/victorious-flash) | — | Download, verify and flash Linux ISOs to USB (Tauri v2). |
| <img src="assets/icons/victorious-mesh.png" height="28" align="center" alt="" /> | [**victorious-mesh**](https://github.com/Victorious93/victorious-mesh) | — | Android VPN/mesh node for the droidcommand-AI fleet (self-hosted Headscale). |
| <img src="assets/icons/victorious-browser.png" height="28" align="center" alt="" /> | [**victorious-browser**](https://github.com/Victorious93/victorious-browser) | — | Fleet security/recon browser: WebView shell, on-device HTTP(S) inspection, and Messenger fleet bridge. |
| <img src="assets/icons/victorsms.png" height="28" align="center" alt="" /> | **victorsms** *(private, in development)* | `com.victorious.sms` | Fleet universal messaging APK (Matrix + bridges; EXTERNAL_NODE for droidcommand-AI). |
| <img src="assets/icons/victorlaunch.png" height="28" align="center" alt="" /> | **victorlaunch** *(private, in development)* | `com.victorious.launch` | Fleet-native Android home launcher (Lawnchair-based EXTERNAL_NODE for droidcommand-AI). |
| <img src="assets/icons/victorspoof.png" height="28" align="center" alt="" /> | **victorspoof** *(private, in development)* | `com.victorious.spoof` | Fleet novelty/prank caller-ID Android app (owned-number pool + Twilio; EXTERNAL_NODE). |
| <img src="assets/icons/VictorLink64.png" height="28" align="center" alt="" /> | [**VictorLink64**](https://github.com/Victorious93/VictorLink64) | — | N64 (Mupen64Plus) and SNES (bsnes) from your own files, plus built-in chess and online / Wi-Fi / Bluetooth rooms. |

### Termux / host

| | Project | Package | What it is |
|:--:|:--|:--|:--|
| <img src="assets/icons/VictorSuite.png" height="28" align="center" alt="" /> | [**VictorSuite**](https://github.com/Victorious93/VictorSuite) | — | Termux-based Android Linux suite: proot containers, backup/restore, plugins, X11, and automation tools. |
| <img src="assets/icons/KYC-AuditLab.png" height="28" align="center" alt="" /> | [**KYC-AuditLab**](https://github.com/Victorious93/KYC-AuditLab) | `com.identityshield.companion` | IdentityShield: local-first KYC security test lab against a bundled simulator (Phase 1). |
| <img src="assets/icons/BakerPi-Installer.png" height="28" align="center" alt="" /> | [**BakerPi-Installer**](https://github.com/Victorious93/BakerPi-Installer) | — | Cross-platform tool installer for Pi Zero 1.3 — browser/native UI over USB OTG or SSH. |

<img src="assets/divider.png" width="100%" alt="" />

## 🧰 More apps & tools

Projects by Don that are not (yet) wired into the fleet connection model above.

| | Project | What it is |
|:--:|:--|:--|
| | [**DreamOS-Victorious**](https://github.com/Victorious93/DreamOS-Victorious) | Phase 1 groundwork for Android ROM source integration: profile validator, reproducible source bundle, SHA-256 integrity check (not flashable). |
| <img src="assets/icons/droidpilot.png" height="28" align="center" alt="" /> | [**droidpilot**](https://github.com/Victorious93/droidpilot) *(DroidPilot Forge)* | Stable Android device automation for AI agents via Accessibility Service + MCP — no ADB, no OCR; enhanced fork for agentic control. |

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
  Hub --- PHY["Pyra Claw<br/>Pi5+ESP32<br/>(private)"]
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
    VSMS["victorsms (private)"]
    VLC["victorlaunch (private)"]
    VSP["victorspoof (private)"]
    VL64["VictorLink64"]
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
> This shows how the apps are *meant* to connect. Not every link is wired up yet. Private repos are listed by name only until they are public.

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
