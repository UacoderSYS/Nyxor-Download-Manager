<div align="center">

# ⚡ Nyxor Download Manager

### Multi-Threaded Rust Download Engine, BitTorrent Client, Media Studio & LAN Warp for Windows

**[Download for Windows](https://github.com/UacoderSYS/Nyxor-Download-Manager/releases)** · **[Official website](https://nyxorlabs.com)**

<p align="center">
  <a href="#overview"><b>Overview</b></a> •
  <a href="#architecture"><b>Architecture</b></a> •
  <a href="#why-nyxor"><b>Why Nyxor?</b></a> •
  <a href="#key-features"><b>Features</b></a> •
  <a href="#screenshots"><b>Screenshots</b></a> •
  <a href="#browser-integration"><b>Extension</b></a> •
  <a href="#quick-start-verification"><b>Quick Start</b></a> •
  <a href="#community-support"><b>Support</b></a>
</p>

---

</div>

<a name="overview"></a>

## 📌 Overview

**Nyxor Download Manager (NDM)** is a native 64-bit Windows desktop suite built for fast file transfers, torrenting, media capture, format conversion, and instant local file sharing — all inside one lightweight application.

Instead of relying on a single browser connection or juggling separate tools for torrents, video downloads, and media conversion, Nyxor pairs a **.NET Framework 4.8** double-buffered GDI+ interface with a native **Rust core library (`nyxor_core.dll`)** to handle multi-segmented HTTP/HTTPS transfers (up to 128 streams), P2P BitTorrent swarms, adaptive 4K/8K media streams, and direct LAN/QR device sharing.

---

<a name="architecture"></a>

## 🏗️ Architecture

```mermaid
graph LR
    A["🌐 Capture Layer<br/>Browser HUD • HTTP/S<br/>BitTorrent • 4K/8K DVR"] --> B["⚡ Hybrid Core<br/>.NET 4.8 + Rust Engine<br/>Up to 128 Adaptive Streams"]
    B --> C["🛡️ Crash-Safe Assembler<br/>Strict Range Validation<br/>Disk-Aware Staging"]
    C --> D["📡 Studio & LAN Warp<br/>10-Format GPU Converter<br/>Wi-Fi QR & Global Tunnel"]

    style A fill:#111625,stroke:#38BDF8,stroke-width:1.6px,color:#F8FAFC
    style B fill:#161B2E,stroke:#2563EB,stroke-width:1.6px,color:#F8FAFC
    style C fill:#141E28,stroke:#F59E0B,stroke-width:1.6px,color:#F8FAFC
    style D fill:#111D1B,stroke:#10B981,stroke-width:1.6px,color:#F8FAFC
```

---

<a name="why-nyxor"></a>

## 📊 Why Nyxor?

| Capability | Nyxor Download Manager | Conventional Accelerators | Standard Web Browsers |
| :--- | :---: | :---: | :---: |
| **Max Concurrent Streams** | **Up to 128 (Adaptive Scaling)** | 8 – 32 Streams | 1 Stream |
| **Resume & Assembly Safety** | **Strict Range Checks + Crash-Safe Staging** | ⚠️ Basic Resume | ❌ Limited |
| **BitTorrent & Magnet Client** | **Built-in (File Tree + Sequential Play)** | ❌ Not Supported | ❌ Not Supported |
| **4K/8K Media & Live DVR** | **Built-in (Multi-Audio + Ad-Skip DVR)** | ⚠️ Limited / Breaks on DASH | ❌ Not Supported |
| **Media Studio Converter** | **Built-in (10 Formats + GPU + EBU R128)** | ❌ Not Supported | ❌ Not Supported |
| **LAN / Phone File Sharing** | **Built-in Nyxor LAN Warp (QR + Tunnel)** | ❌ Not Supported | ❌ Not Supported |
| **Interface & Themes** | **Dual Theme (Light & Dark GDI+) • 7 Languages** | Legacy Win32 UI | Standard Tab UI |
| **Privacy Model** | **100% Local Processing (`127.0.0.1`)** | Varies | Cloud-Synced |

---

<a name="key-features"></a>

## ⚡ Key Features

### 🚀 Adaptive Multi-Segment Engine & Crash-Safe Assembly

- **Up to 128 Parallel Streams:** Splits large downloads dynamically across concurrent connections and scales workers up based on real measured throughput, avoiding unnecessary server throttling.
- **Live Work Stealing (EndGame):** Automatically slices remaining byte ranges from slow or stalled connections and hands them to faster idle workers.
- **Strict Resume Integrity:** Validates byte ranges, `Content-Length`, and premature stream closures so dropped connections near the end of a file never shrink expected sizes or mark incomplete files as finished.
- **Disk-Aware Crash-Safe Merging:** Verifies chunk presence, ordering, and exact sizes before assembly. When free disk space allows, original chunks remain intact until the final file is flushed and verified; on tight drives, it automatically switches to zero-extra-space rolling assembly.
- **Reliable Session Persistence:** Saves active, paused, and empty download states cleanly across restarts and unexpected shutdowns.

### 🧲 Built-in BitTorrent & Magnet Engine

- **Direct `.torrent` & `magnet:` Support:** Open torrent files or magnet links directly in Nyxor with a pre-download file tree to pick specific files and set per-file priorities.
- **Sequential Streaming & Piece Verification:** Stream video files while downloading, verify pieces with SHA-1/v2 checks, and optionally stop seeding automatically at 100%.
- **Live Swarm & Tracker Inspector:** View connected peers, seed counts, tracker status, custom tracker injection, and IP ban controls in real time.

### 📡 Nyxor LAN Warp — Local & Cross-Network File Sharing

- **Instant Wi-Fi & QR Transfer:** Share completed downloads directly to your phone, tablet, or nearby PC over local Wi-Fi using a scannable QR code and PIN — with no cloud upload limits.
- **One-Click Global Tunnel:** Share across different networks when devices aren't on the same Wi-Fi, with automatic link readiness checks and clean background process teardown on app exit.

### 🎥 4K/8K Media Grabber, Multi-Language Audio & Live DVR

- **Universal Media Capture:** Extracts video, audio, and playlists up to **4K / 8K 60fps** from YouTube, Facebook (Reels/VOD), X/Twitter, TikTok, Instagram, Reddit, and Twitch.
- **Multi-Language Audio & Fast DASH:** Choose between original and dubbed audio tracks (including Arabic and international tracks), backed by 4–6 parallel DASH audio lanes with automatic byte rollback if a segment drops.
- **Live Stream DVR:** Records **HLS (`.m3u8`)**, **DASH (`.mpd`)**, and **FLV** live broadcasts in real time with automatic ad-pod filtering and stop timers.
- **Auto-Healing Links:** Detects expired stream tokens mid-transfer and refreshes them automatically without restarting from zero.

### 🎛️ Nyxor Media Studio & Site Grabber

- **10-Format GPU Converter:** Convert media across **MP4 (H.264), MKV, WebM (VP9), MOV, AVI, GIF, MP3, M4A, WAV, and FLAC** with hardware acceleration (NVENC / QSV / AMF).
- **Audio Mastering & Lossless Tools:** FastStart MP4 remuxing, EBU R128 loudness normalization, MP3 cover-art tagging, and precision video trimming.
- **Deep Site Grabber:** Scans web pages (including relative asset links via the native Rust scanner) into an interactive tree of videos, images, documents, and archives for batch queuing.

### 🎨 Dual Theme Engine (Light & Dark) & 7 Built-in Languages

- **Soft Alabaster Light & Fluent Dark:** Custom double-buffered GDI+ rendering with consistent contrast across the main window, Settings, Site Grabber, Media Grabber, dropdowns, scrollbars, and toast notifications.
- **7 Native Languages:** Full RTL and LTR interface support for **Arabic, English, Spanish, French, German, Portuguese, and Russian**.
- **Built-in Checksum Verifier & Proxy Diagnostics:** Verify **MD5, SHA-1, and SHA-256** hashes directly in-app, and configure **HTTP, HTTPS, SOCKS4, and SOCKS5** proxies with live latency testing.

---

<a name="screenshots"></a>

## 📸 Screenshots

<div align="center">

### 1. Main Workspace & Completion Center

*Double-buffered GDI+ workspace with automatic category routing and interactive completion cards.*

<img width="1095" height="615" alt="Main Workspace &amp; Completion Center" src="https://github.com/user-attachments/assets/f066a5c3-7ff2-47c0-897b-2d6212ae9482" />

### 2. Multi-Segment Live Monitor & Speed Limiter

*Real-time socket telemetry, adaptive connection scaling, and per-chunk progress tracking.*

<img width="600" height="665" alt="Multi-Segment Live Monitor" src="https://github.com/user-attachments/assets/eb5008ed-92b5-45d5-96b5-7ea7cbc58f7c" />

### 3. Media Grabber & Quality Selector

*4K/8K DASH stream parser with multi-language audio selection and instant metadata caching.*

<img width="640" height="520" alt="Media Grabber Dialog" src="https://github.com/user-attachments/assets/c3df4a84-1215-40c2-a6b3-6b261ddbf307" />

### 4. Desktop Notification Toast

*Clean completion alerts with quick folder and file launch actions.*

<img width="390" height="96" alt="Fluent Notification Toast" src="https://github.com/user-attachments/assets/d2cde3a3-0bb2-47be-b12e-54695321ec07" />

</div>

---

<a name="browser-integration"></a>

## 🧩 Browser Integration

Nyxor pairs with the official **Nyxor Browser Integration** extension (Manifest V3) for **Google Chrome** and **Microsoft Edge**:

- **Floating Media HUD:** Displays resolution badges (4K, 2K, FHD, HD, LIVE) directly over web videos with 1-click download, MP3 extraction, gallery image saving, and frame snapshots.
- **Inline Dismiss (`✕`) & Offline Awareness:** Hide the overlay per video when not needed, and see immediate visual status when Nyxor Desktop is closed.
- **Strict Local Privacy:** Communicates only with `127.0.0.1` on your machine — browsing history is never sent to external servers.

**Official Store Links:**

- [Google Chrome Web Store](https://chromewebstore.google.com/detail/nyxor-browser-integration/fmbpmhpahecfneoanghjcdnoiipgagon)
- [Microsoft Edge Add-ons](https://microsoftedge.microsoft.com/addons/detail/nyxor-browser-integration/dlnncpfaaejjbdgkfabhjjnnjhhboapp)

---

<a name="quick-start-verification"></a>

## 🚀 Quick Start & Verification

### System Requirements

- **OS:** Windows 10 / Windows 11 (64-bit)
- **Runtime:** .NET Framework 4.8 or newer
- **Storage:** SSD recommended for high-concurrency multi-segment assembly

### Download & Verify (`v2.1.5.0`)

| File | Platform | Size | SHA-256 Checksum |
| :--- | :--- | :--- | :--- |
| `NyxorDM.exe` | Windows 10 / 11 (x64) | 32 MB | `1c38e0078dc1faaf3d2a137804293c271a6f07cdd009a6af71cc0418c76ae65e` |

- **Download:** Grab `NyxorDM.exe` from **[GitHub Releases](https://github.com/UacoderSYS/Nyxor-Download-Manager/releases)** or **[nyxorlabs.com](https://nyxorlabs.com/#get-started)**.
- **Trial & Licensing:** Includes a full-featured **14-day free trial** (no credit card required), followed by a **$15 one-time lifetime license**.

<details>
<summary><b>⌨️ Keyboard Shortcuts</b></summary>

| Shortcut | Action |
| :--- | :--- |
| <kbd>Ctrl</kbd> + <kbd>N</kbd> | Add New Download URL |
| <kbd>Ctrl</kbd> + <kbd>B</kbd> | Batch Add Downloads |
| <kbd>Space</kbd> | Pause / Resume Selected Task |
| <kbd>Delete</kbd> | Open Smart Deletion Prompt |
| <kbd>Ctrl</kbd> + <kbd>A</kbd> | Select All Tasks |
| <kbd>Ctrl</kbd> + <kbd>,</kbd> | Open Settings |

</details>

---

## 🔧 Optional Auxiliary Tools

Nyxor's core networking, multi-segment downloading, BitTorrent swarm engine, LAN Warp sharing, and file assembly run natively in **Nyxor (.NET + Rust)**. Two optional open-source utilities are used strictly for specialized media tasks:

- **[yt-dlp](https://github.com/yt-dlp/yt-dlp):** Optional manifest resolver used for restricted YouTube streams and dubbed multi-language track discovery. All actual high-speed segmented downloading and assembly remain handled by Nyxor's own engine.
- **[FFmpeg](https://ffmpeg.org/):** Used for lossless DASH audio/video muxing, Live DVR remuxing, and Media Studio format conversions.

---

<a name="community-support"></a>

## 💬 Community & Support

- 🌐 **Official Website:** [nyxorlabs.com](https://nyxorlabs.com) · [Changelog](https://nyxorlabs.com/changelog)
- 📢 **Telegram Community:** [@nyxorglobal](https://t.me/nyxorglobal)
- ▶️ **YouTube Channel:** [@nyxorlabs](https://www.youtube.com/@nyxorlabs)
- 📧 **Support & Inquiries:** `info@nyxorlabs.com` | `nyxorlabs@gmail.com`

---

<div align="center">
  <sub>Developed by <b>Uacoder</b> • Copyright © 2026 <b>Nyxor Labs</b>. All rights reserved.</sub>
</div>
