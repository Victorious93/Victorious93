<div align="center">

<img src="assets/victorious-framework-logo.png" alt="Victorious Framework" width="900" />

<p align="center">
  <a href="https://preview.victorious-framework.pages.dev/"><img src="https://img.shields.io/badge/Victorious_Framework-Website-FFB000?style=for-the-badge&labelColor=0A0F1F&color=FFB000" alt="Victorious Framework website" /></a>
  <a href="https://victorious-designs.pages.dev"><img src="https://img.shields.io/badge/Victorious_Designs-Website-FF2E97?style=for-the-badge&labelColor=0A0F1F&color=FF2E97" alt="Victorious Designs website" /></a>
  <!-- Instagram badge goes here, e.g.:
  <a href="https://instagram.com/HANDLE"><img src="https://img.shields.io/badge/Instagram-Follow-00F0FF?style=for-the-badge&logo=instagram&logoColor=00F0FF&labelColor=0A0F1F&color=00F0FF" alt="Instagram" /></a>
  -->
</p>

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

<p align="center"><img src="assets/logos/victorious-framework-hoodie-brand.png" alt="Victorious Framework" width="280"></p>

## 🛰️ Victorious fleet

Grouped by how each app connects to the hub. Package IDs are shown where the project defines one. Private repos are listed by name only.

**Controller / Hub**

### <img src="assets/logos/droidcommand-logo.jpg" alt="droidcommand-AI" width="64" valign="middle"> droidcommand-AI

- **Repo:** [Victorious93/droidcommand-AI](https://github.com/Victorious93/droidcommand-AI)
- **Package id:** `ai.droidcommand.app`
- **Purpose:** The fleet controller/brain — remote command and orchestration of every app in the fleet.

### <img src="assets/logos/pyraclaw-logo.jpg" alt="Pyra Claw" width="64" valign="middle"> Pyra Claw

- **Repo:** pyra-claw *(private)*
- **Package id:** *(hub / hardware — not an Android package)*
- **Purpose:** Raspberry Pi 5 + ESP32 command hub that bridges the phone controller to physical devices.

### <img src="assets/logos/victormodem-logo.jpg" alt="VictorModem" width="64" valign="middle"> VictorModem *(in planning)*

- **Repo:** victormodem *(private)*
- **Package id:** *(in planning / hardware — no confirmed package id yet)*
- **Purpose:** ESP32-S3 + cellular modem board that gives the fleet an independent second line.

**Bound Companions**

### <img src="assets/logos/hackerai-logo.jpg" alt="HackerAI-Commander" width="64" valign="middle"> HackerAI-Commander

- **Repo:** [Victorious93/HackerAI-Commander](https://github.com/Victorious93/HackerAI-Commander)
- **Package id:** `ai.hackerai.companion`
- **Purpose:** Companion to the `hackeraiETC` fork — an AI hacking assistant.

### <img src="assets/logos/pentest-swarm-logo.png" alt="Pentest-Swarm-AI" width="64" valign="middle"> Pentest-Swarm-AI

- **Repo:** [Victorious93/Pentest-Swarm-AI](https://github.com/Victorious93/Pentest-Swarm-AI)
- **Package id:** `ai.pentestswarm.companion`
- **Purpose:** Multi-agent pentest swarm companion.

### <img src="assets/logos/edl-commander-logo.png" alt="EDL-Commander" width="64" valign="middle"> EDL-Commander

- **Repo:** [Victorious93/EDL-Commander](https://github.com/Victorious93/EDL-Commander)
- **Package id:** `ai.edlcommander.companion`
- **Purpose:** Safety-first Qualcomm EDL (Emergency Download mode) framework/tool companion.

**External Nodes**

### <img src="assets/logos/rootforge-logo.jpg" alt="rootforge-os" width="64" valign="middle"> rootforge-os

- **Repo:** [Victorious93/rootforge-os](https://github.com/Victorious93/rootforge-os)
- **Package id:** `ai.rootforge.os`
- **Purpose:** Android rooting / root-management app.

### <img src="assets/logos/file-manager-logo.png" alt="File-Manager" width="64" valign="middle"> File-Manager

- **Repo:** [Victorious93/File-Manager](https://github.com/Victorious93/File-Manager)
- **Package id:** `ai.victorious.filemanager` (debug: `ai.victorious.filemanager.debug`) *(rename in progress — repo still uses `ai.victorious.victorfiles`)*
- **Purpose:** Dual-pane power-user file manager aiming to beat MT Manager VIP.

#### Victorious-Keyboard *(logo pending)*

- **Repo:** [Victorious93/Victorious-Keyboard](https://github.com/Victorious93/Victorious-Keyboard)
- **Package id:** `com.victorious.keyboard` *(code namespace still `dev.patrickgold.florisboard` — rename queued)*
- **Purpose:** Custom Android keyboard with integrated media controls.

### <img src="assets/logos/victorious-flash-logo.png" alt="Victorious Flash (Distro Installer)" width="64" valign="middle"> Victorious Flash (Distro Installer)

- **Repo:** [Victorious93/victorious-flash](https://github.com/Victorious93/victorious-flash) *(desktop app)*
- **Package id:** `com.victorious.flash.android` *(desktop app — not an APK)*
- **Purpose:** Desktop app to pick a Linux distro, download its official ISO, and write it to USB.

### <img src="assets/logos/victorious-mesh-logo.jpg" alt="Victorious Mesh" width="64" valign="middle"> Victorious Mesh

- **Repo:** [Victorious93/victorious-mesh](https://github.com/Victorious93/victorious-mesh)
- **Package id:** `com.victorious.mesh`
- **Purpose:** Secure mesh-networking / VPN Android app.

### <img src="assets/logos/victorious-browser-logo.jpg" alt="Victorious Browser" width="64" valign="middle"> Victorious Browser

- **Repo:** [Victorious93/victorious-browser](https://github.com/Victorious93/victorious-browser)
- **Package id:** `com.victorious.browser`
- **Purpose:** Fleet security / recon browser with web interception.

### <img src="assets/logos/victorsms-logo.jpg" alt="VictorSMS" width="64" valign="middle"> VictorSMS

- **Repo:** victorsms *(private)*
- **Package id:** `com.victorious.sms`
- **Purpose:** Universal messaging app (Matrix-based) with voice cloning and persona learning.

### <img src="assets/logos/victorlaunch-logo.jpg" alt="VictorLaunch" width="64" valign="middle"> VictorLaunch

- **Repo:** victorlaunch *(private)*
- **Package id:** `com.victorious.launch`
- **Purpose:** Nova-class, Lawnchair-based fleet home-screen launcher.

### <img src="assets/logos/victorspoof-logo.jpg" alt="VictorSpoof" width="64" valign="middle"> VictorSpoof

- **Repo:** victorspoof *(private)*
- **Package id:** `com.victorious.spoof`
- **Purpose:** Legal novelty / prank caller-ID app with strict compliance guardrails.

### <img src="assets/logos/victorlink64-logo.png" alt="VictorLink64" width="64" valign="middle"> VictorLink64

- **Repo:** [Victorious93/VictorLink64](https://github.com/Victorious93/VictorLink64)
- **Package id:** `org.victoriousframework.victorlink64` *(Kotlin / Jetpack Compose; Android 9+)*
- **Purpose:** Multi-game emulator + play hub — play N64 and SNES games, built-in chess, and multiplayer with friends — in one Android app.

### <img src="assets/logos/victorcam-logo.jpg" alt="VictorCam" width="64" valign="middle"> VictorCam

- **Repo:** VictorCam *(not public)*
- **Package id:** `com.victorious.cam`
- **Purpose:** OBS-style virtual camera APK.

**Termux / Host**

### <img src="assets/logos/victorsuite-logo.png" alt="VictorSuite" width="64" valign="middle"> VictorSuite

- **Repo:** [Victorious93/VictorSuite](https://github.com/Victorious93/VictorSuite)
- **Package id:** `com.termux` (lineage; `TERMUX_IPC`)
- **Purpose:** Termux-based Android Linux suite — the fleet home for container-style workloads.

### <img src="assets/logos/kyc-auditlab-logo.png" alt="KYC-AuditLab / IdentityShield" width="64" valign="middle"> KYC-AuditLab / IdentityShield

- **Repo:** [Victorious93/KYC-AuditLab](https://github.com/Victorious93/KYC-AuditLab)
- **Package id:** `com.identityshield.companion`
- **Purpose:** Local KYC / identity audit lab.

### <img src="assets/logos/bakerpi-logo.jpg" alt="BakerPi-Installer" width="64" valign="middle"> BakerPi-Installer

- **Repo:** [Victorious93/BakerPi-Installer](https://github.com/Victorious93/BakerPi-Installer)
- **Package id:** *(cross-platform tool — n/a)*
- **Purpose:** Cross-platform tool that installs/flashes in Raspberry Pi imaging style.

**Social / Marketplace Apps**

### <img src="assets/logos/matchvictorious-logo.jpg" alt="MatchVictorious" width="64" valign="middle"> MatchVictorious

- **Repo:** [Victorious93/matchvictorious](https://github.com/Victorious93/matchvictorious)
- **Package id:** `com.victorious.match`
- **Purpose:** Dating app.

### <img src="assets/logos/victorpedigree-logo.jpg" alt="VictoryPed" width="64" valign="middle"> VictoryPed

- **Repo:** VictoryPed *(private)*
- **Package id:** `com.victorious.victoryped`
- **Purpose:** Social network and marketplace for bully breeders.

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
