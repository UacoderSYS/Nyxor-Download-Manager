<div align="center">

# ⚡ Nyxor Download Manager

### Multi-Threaded Rust Download Engine, BitTorrent Client, Media Studio & LAN Warp for Windows

[![Latest Release](https://img.shields.io/github/v/release/UacoderSYS/Nyxor-Download-Manager?style=for-the-badge&logo=github&color=38BDF8)](https://github.com/UacoderSYS/Nyxor-Download-Manager/releases)
[![Website](https://img.shields.io/badge/Website-nyxorlabs.com-10B981?style=for-the-badge&logo=googlechrome&logoColor=white)](https://nyxorlabs.com)
[![License](https://img.shields.io/badge/License-Lifetime%20%2415-2563EB?style=for-the-badge)](https://nyxorlabs.com)
[![VirusTotal](https://img.shields.io/badge/VirusTotal-Scan%20Report-EF4444?style=for-the-badge&logo=virustotal&logoColor=white)](https://www.virustotal.com/gui/file/001ba4a6e06aa480da08d355a0941df972285fcd2257b3a60bec2ee59316df98?nocache=1)

<p align="center">
  <a href="#-overview"><b>Overview</b></a> •
  <a href="#️-architecture"><b>Architecture</b></a> •
  <a href="#-why-nyxor"><b>Why Nyxor?</b></a> •
  <a href="#-key-features"><b>Features</b></a> •
  <a href="#-screenshots"><b>Screenshots</b></a> •
  <a href="#-browser-integration"><b>Extension</b></a> •
  <a href="#-quick-start--verification"><b>Quick Start</b></a> •
  <a href="#-community--support"><b>Support</b></a>
</p>

---

</div>

## 📌 Overview

**Nyxor Download Manager (NDM)** is a native 64-bit Windows desktop suite built for fast file transfers, torrenting, media capture, format conversion, and instant local file sharing — all inside one lightweight application.

Instead of relying on a single browser connection or juggling separate tools for torrents, video downloads, and media conversion, Nyxor pairs a **.NET Framework 4.8** double-buffered GDI+ interface with a native **Rust core library (`nyxor_core.dll`)** to handle multi-segmented HTTP/HTTPS transfers (up to 128 streams), P2P BitTorrent swarms, adaptive 4K/8K media streams, and direct LAN/QR device sharing.

---

## 🏗️ Architecture

```mermaid
flowchart LR
    subgraph Input["1. Ingestion Layer"]
        A1["🌐 Browser HUD (127.0.0.1)"]
        A2["🔗 HTTP / HTTPS & Site Grabber"]
        A3["🧲 BitTorrent & Magnet P2P"]
        A4["🎥 4K/8K Media & Live DVR"]
    end

    subgraph Engine["2. Hybrid Core (.NET 4.8 + Rust)"]
        B1["⚡ Adaptive Multi-Segment Engine<br/>Up to 128 Parallel Streams"]
        B2["🛡️ Strict HTTP 206/416 Guard<br/>& DASH Segment Rollback"]
        B3["🦀 Native Rust Core<br/>High-Speed I/O & Asset Scanner"]
    end

    subgraph Output["3. Assembly, Studio & Sharing"]
        C1["💾 Disk-Aware Crash-Safe<br/>File Assembler"]
        C2["🎛️ Nyxor Media Studio<br/>10-Format GPU Converter"]
        C3["📡 Nyxor LAN Warp<br/>Wi-Fi QR & Global Tunnel"]
    end

    Input --> Engine --> Output

    style A1 fill:#111625,stroke:#38BDF8,stroke-width:1.4px,color:#F8FAFC
    style A2 fill:#111625,stroke:#38BDF8,stroke-width:1.4px,color:#F8FAFC
    style A3 fill:#111625,stroke:#38BDF8,stroke-width:1.4px,color:#F8FAFC
    style A4 fill:#111625,stroke:#38BDF8,stroke-width:1.4px,color:#F8FAFC
    style B1 fill:#161B2E,stroke:#2563EB,stroke-width:1.6px,color:#F8FAFC
    style B2 fill:#161B2E,stroke:#2563EB,stroke-width:1.6px,color:#F8FAFC
    style B3 fill:#161B2E,stroke:#E65100,stroke-width:1.6px,color:#F8FAFC
    style C1 fill:#111D1B,stroke:#10B981,stroke-width:1.5px,color:#F8FAFC
    style C2 fill:#111D1B,stroke:#10B981,stroke-width:1.5px,color:#F8FAFC
    style C3 fill:#111D1B,stroke:#10B981,stroke-width:1.5px,color:#F8FAFC

📊 Why Nyxor?
Capability	Nyxor Download Manager	Conventional Accelerators	Standard Web Browsers
Max Concurrent Streams	Up to 128 (Adaptive Scaling)	8 – 32 Streams	1 Stream
Resume & Assembly Safety	Strict Range Checks + Crash-Safe Staging	⚠️ Basic Resume	❌ Limited
BitTorrent & Magnet Client	Built-in (File Tree + Sequential Play)	❌ Not Supported	❌ Not Supported
4K/8K Media & Live DVR	Built-in (Multi-Audio + Ad-Skip DVR)	⚠️ Limited / Breaks on DASH	❌ Not Supported
Media Studio Converter	Built-in (10 Formats + GPU + EBU R128)	❌ Not Supported	❌ Not Supported
LAN / Phone File Sharing	Built-in Nyxor LAN Warp (QR + Tunnel)	❌ Not Supported	❌ Not Supported
Interface & Themes	Dual Theme (Light & Dark GDI+) • 7 Languages	Legacy Win32 UI	Standard Tab UI
Privacy Model	100% Local Processing (127.0.0.1)	Varies	Cloud-Synced
⚡ Key Features
🚀 Adaptive Multi-Segment Engine & Crash-Safe Assembly
Up to 128 Parallel Streams: Splits large downloads dynamically across concurrent connections and scales workers up based on real measured throughput, avoiding unnecessary server throttling.

Live Work Stealing (EndGame): Automatically slices remaining byte ranges from slow or stalled connections and hands them to faster idle workers.

Strict Resume Integrity: Validates byte ranges, Content-Length, and premature stream closures so dropped connections near the end of a file never shrink expected sizes or mark incomplete files as finished.

Disk-Aware Crash-Safe Merging: Verifies chunk presence, ordering, and exact sizes before assembly. When free disk space allows, original chunks remain intact until the final file is flushed and verified; on tight drives, it automatically switches to zero-extra-space rolling assembly.

Reliable Session Persistence: Saves active, paused, and empty download states cleanly across restarts and unexpected shutdowns.

🧲 Built-in BitTorrent & Magnet Engine
Direct .torrent & magnet: Support: Open torrent files or magnet links directly in Nyxor with a pre-download file tree to pick specific files and set per-file priorities.

Sequential Streaming & Piece Verification: Stream video files while downloading, verify pieces with SHA-1/v2 checks, and optionally stop seeding automatically at 100%.

Live Swarm & Tracker Inspector: View connected peers, seed counts, tracker status, custom tracker injection, and IP ban controls in real time.

📡 Nyxor LAN Warp — Local & Cross-Network File Sharing
Instant Wi-Fi & QR Transfer: Share completed downloads directly to your phone, tablet, or nearby PC over local Wi-Fi using a scannable QR code and PIN — with no cloud upload limits.

One-Click Global Tunnel: Share across different networks when devices aren't on the same Wi-Fi, with automatic link readiness checks and clean background process teardown on app exit.

🎥 4K/8K Media Grabber, Multi-Language Audio & Live DVR
Universal Media Capture: Extracts video, audio, and playlists up to 4K / 8K 60fps from YouTube, Facebook (Reels/VOD), X/Twitter, TikTok, Instagram, Reddit, and Twitch.

Multi-Language Audio & Fast DASH: Choose between original and dubbed audio tracks (including Arabic and international tracks), backed by 4–6 parallel DASH audio lanes with automatic byte rollback if a segment drops.

Live Stream DVR: Records HLS (.m3u8), DASH (.mpd), and FLV live broadcasts in real time with automatic ad-pod filtering and stop timers.

Auto-Healing Links: Detects expired stream tokens mid-transfer and refreshes them automatically without restarting from zero.

🎛️ Nyxor Media Studio & Site Grabber
10-Format GPU Converter: Convert media across MP4 (H.264), MKV, WebM (VP9), MOV, AVI, GIF, MP3, M4A, WAV, and FLAC with hardware acceleration (NVENC / QSV / AMF).

Audio Mastering & Lossless Tools: FastStart MP4 remuxing, EBU R128 loudness normalization, MP3 cover-art tagging, and precision video trimming.

Deep Site Grabber: Scans web pages (including relative asset links via the native Rust scanner) into an interactive tree of videos, images, documents, and archives for batch queuing.

🎨 Dual Theme Engine (Light & Dark) & 7 Built-in Languages
Soft Alabaster Light & Fluent Dark: Custom double-buffered GDI+ rendering with consistent contrast across the main window, Settings, Site Grabber, Media Grabber, dropdowns, scrollbars, and toast notifications.

7 Native Languages: Full RTL and LTR interface support for Arabic, English, Spanish, French, German, Portuguese, and Russian.

Built-in Checksum Verifier & Proxy Diagnostics: Verify MD5, SHA-1, and SHA-256 hashes directly in-app, and configure HTTP, HTTPS, SOCKS4, and SOCKS5 proxies with live latency testing.

📸 Screenshots
<div align="center">
1. Main Workspace & Completion Center
Double-buffered GDI+ workspace with automatic category routing and interactive completion cards.


<img width="1095" height="615" alt="Main Workspace & Completion Center" src="https://github.com/user-attachments/assets/f066a5c3-7ff2-47c0-897b-2d6212ae9482" />




2. Multi-Segment Live Monitor & Speed Limiter
Real-time socket telemetry, adaptive connection scaling, and per-chunk progress tracking.


<img width="600" height="665" alt="Multi-Segment Live Monitor" src="https://github.com/user-attachments/assets/eb5008ed-92b5-45d5-96b5-7ea7cbc58f7c" />




3. Media Grabber & Quality Selector
4K/8K DASH stream parser with multi-language audio selection and instant metadata caching.


<img width="640" height="520" alt="Media Grabber Dialog" src="https://github.com/user-attachments/assets/c3df4a84-1215-40c2-a6b3-6b261ddbf307" />




4. Desktop Notification Toast
Clean completion alerts with quick folder and file launch actions.


<img width="390" height="96" alt="Fluent Notification Toast" src="https://github.com/user-attachments/assets/d2cde3a3-0bb2-47be-b12e-54695321ec07" />

</div>
🧩 Browser Integration
Nyxor pairs with the official Nyxor Browser Integration extension (Manifest V3) for Google Chrome and Microsoft Edge:

Floating Media HUD: Displays resolution badges (4K, 2K, FHD, HD, LIVE) directly over web videos with 1-click download, MP3 extraction, gallery image saving, and frame snapshots.

Inline Dismiss (✕) & Offline Awareness: Hide the overlay per video when not needed, and see immediate visual status when Nyxor Desktop is closed.

Strict Local Privacy: Communicates only with 127.0.0.1 on your machine — browsing history is never sent to external servers.

Official Store Links:

Google Chrome Web Store

Microsoft Edge Add-ons

🚀 Quick Start & Verification
System Requirements
OS: Windows 10 / Windows 11 (64-bit)

Runtime: .NET Framework 4.8 or newer

Storage: SSD recommended for high-concurrency multi-segment assembly

Download & Verify (v2.1.5.0)
File	Platform	Size	SHA-256 Checksum
NyxorDM.exe	Windows 10 / 11 (x64)	32 MB	1c38e0078dc1faaf3d2a137804293c271a6f07cdd009a6af71cc0418c76ae65e
Download: Grab NyxorDM.exe from GitHub Releases or nyxorlabs.com.

Security Scan: Official VirusTotal Report

Trial & Licensing: Includes a full-featured 14-day free trial (no credit card required), followed by a $15 one-time lifetime license.

<details> <summary><b>⌨️ Keyboard Shortcuts</b></summary>
Shortcut	Action
<kbd>Ctrl</kbd> + <kbd>N</kbd>	Add New Download URL
<kbd>Ctrl</kbd> + <kbd>B</kbd>	Batch Add Downloads
<kbd>Space</kbd>	Pause / Resume Selected Task
<kbd>Delete</kbd>	Open Smart Deletion Prompt
<kbd>Ctrl</kbd> + <kbd>A</kbd>	Select All Tasks
<kbd>Ctrl</kbd> + <kbd>,</kbd>	Open Settings
</details>
🔧 Optional Auxiliary Tools
Nyxor's core networking, multi-segment downloading, BitTorrent swarm engine, LAN Warp sharing, and file assembly run natively in Nyxor (.NET + Rust). Two optional open-source utilities are used strictly for specialized media tasks:

yt-dlp: Optional manifest resolver used for restricted YouTube streams and dubbed multi-language track discovery. All actual high-speed segmented downloading and assembly remain handled by Nyxor's own engine.

FFmpeg: Used for lossless DASH audio/video muxing, Live DVR remuxing, and Media Studio format conversions.

💬 Community & Support
🌐 Official Website: nyxorlabs.com · Changelog

📢 Telegram Community: @nyxorglobal

▶️ YouTube Channel: @nyxorlabs

📧 Support & Inquiries: info@nyxorlabs.com | nyxorlabs@gmail.com

<div align="center"> <sub>Developed by <b>Uacoder</b> • Copyright © 2026 <b>Nyxor Labs</b>. All rights reserved.</sub> </div> ```
