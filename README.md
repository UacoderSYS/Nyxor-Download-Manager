<div align="center">

# Nyxor Download Manager

**High-Throughput Network Engine & Low-Latency Media Ingestion Platform**

[![Release](https://img.shields.io/badge/Release-v1.3.0.0-00C6FF?style=for-the-badge&logo=github&logoColor=white)](https://github.com)
[![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011-121212?style=for-the-badge&logo=windows&logoColor=white)](https://microsoft.com)
[![Architecture](https://img.shields.io/badge/Architecture-x64%20Native-8B0000?style=for-the-badge)](https://github.com)
[![Core](https://img.shields.io/badge/Core-.NET%20%2B%20Rust%20Engine-E65100?style=for-the-badge&logo=rust&logoColor=white)](https://nyxorlabs.com)
[![UI](https://img.shields.io/badge/Interface-Custom%20GDI%2B%20Fluent-1E1E1E?style=for-the-badge)](https://nyxorlabs.com)

<p align="center">
  <a href="#-overview">Overview</a> •
  <a href="#-key-features">Key Features</a> •
  <a href="#-screenshots">Screenshots</a> •
  <a href="#-quick-start">Quick Start</a> •
  <a href="#-browser-integration">Browser Extension</a> •
  <a href="#-optional-plugins--auxiliary-tools">Auxiliary Tools</a> •
  <a href="#-community--support">Community</a>
</p>

---

</div>

## 📌 Overview

**Nyxor Download Manager** is an enterprise-grade desktop accelerator built from the ground up for maximum bandwidth saturation and seamless media archiving on Windows x64. Powered by a hybrid high-concurrency architecture, Nyxor replaces standard single-stream downloading with real-time dynamic segment slicing, automated socket recovery, and native transport stream compilation.

Designed for creators, archiving enthusiasts, and power users who need reliable multi-gigabyte transfers and zero-delay media capture.

---

## ⚡ Key Features

### 🚀 Ultra-Speed Multi-Segment Engine
* **Dynamic Range Slicing:** Fragments downloads into up to **128 parallel streams**, bypassing single-thread server throttles and maximizing connection throughput.
* **Intelligent Work Stealing:** Continuously balances active threads by detecting stalled network connections and dynamically reallocating pending byte-ranges to faster sockets.
* **Instant Pre-Allocation:** Allocates file space instantly on the drive before writing, preventing disk fragmentation and eliminating system freeze on large files.
* **Resilient State Engine:** Atomic write verification ensures downloads resume precisely where they stopped after power cuts or network drops.

### 🎥 Live Stream DVR & Media Extraction
* **Universal Live Capture:** Real-time stream recording for **HLS (`.m3u8`)**, **DASH (`.mpd`)**, and **FLV** live broadcasts across major platforms.
* **Ad-Free Recording:** Intelligent node filtering automatically identifies and bypasses commercial ad segments during stream capture.
* **Zero-Latency Remuxing:** Integrated high-speed pipeline packages segmented streams into standard, ready-to-play **MP4** video containers without quality loss.
* **Ultra HD Formats (4K / 8K):** Automatically extracts and combines separated video and high-bitrate audio streams (up to **8K 60fps** and **192kbps MP3 / AAC**).
* **Auto-Healing Links:** Automatically detects expired media tokens and refreshes bearer links in the background without resetting download progress.

### 🌐 Deep Web Crawler & Site Grabber
* **Recursive Asset Grabber:** Automatically downloads entire websites, media galleries, or document archives with customizable crawl depths.
* **Smart Content Routing:** Organizes incoming files into clean categories (*Videos, Documents, Programs, Music, Compressed*) based on file signatures.
* **Robots & Sitemap Parsing:** Scans XML sitemaps to quickly map and queue entire remote asset libraries.

### 🛡️ Network Tunneling & Proxy Manager
* **Multi-Protocol Proxy Support:** Full native routing for **HTTP, HTTPS, SOCKS4, and SOCKS5** connections with authentication.
* **Integrated Latency Diagnostic:** Test proxy stability, DNS latency, and ping directly inside the settings hub before launching tasks.
* **Rate-Limit Evasion:** Tailored header management and keep-alive handling prevent aggressive connection throttling.

### ⏳ Automation & Task Scheduling
* **Recurring Timetables:** Set operational hours and specific days for off-peak bandwidth usage.
* **Post-Queue Actions:** Automatically trigger PC **Shutdown**, **Sleep**, **Hibernate**, or exit the application once tasks complete.
* **Precision Limiter:** Set global or per-download speed caps to browse or game comfortably while downloading.

### 🎨 Pure GDI+ Fluent-Dark Interface
* **Zero Default WinForms Controls:** Precision-crafted UI rendered via custom double-buffered GDI+ with smooth sub-pixel anti-aliasing.
* **Real-Time Visualizer:** Multi-segment progress visualizer highlights individual connection states, throughput, and disk writes.
* **Integrated Hash Verifier:** Verify file integrity post-download using built-in **MD5** and **SHA-256** checksum verification.

---

## 📸 Screenshots

<div align="center">

### 1. Main Workspace & Transfer Center
<img width="1095" height="615" alt="1" src="https://github.com/user-attachments/assets/03a5ba6e-0c85-408f-aadf-97b93377f961" />

### 2. Multi-Segment Visualizer & Live Monitor
<img width="600" height="665" alt="2" src="https://github.com/user-attachments/assets/999ada56-1684-4389-9b60-dc51ffd82d24" />

</div>

---

## 🚀 Quick Start

### System Requirements
* **Operating System:** Windows 10 / Windows 11 (64-bit strictly required)
* **Runtime:** .NET Framework 4.8 or higher
* **Storage:** High-speed drive recommended for high-concurrency multi-part merging

### Running Nyxor
1. Download the latest release from the **Releases** section.
2. Run `NyxorDM.exe` or extract the standalone archive to your preferred location.
3. Launch the application and click **"Start Free Trial"** to initialize your local session and unlock high-concurrency downloads.
4. Set your default download location under **Settings** (<kbd>⚙️</kbd>).

---

## 🧩 Browser Integration

Nyxor works alongside an official companion extension for **Microsoft Edge** and **Google Chrome** to capture downloads with one click.

* **One-Click Capture:** Captures download dialogs, streaming media, and embedded files across web pages.
* **Pre-Download Caching:** Gathers file metadata the moment you interact with a link for immediate downloads.
* **Local Isolation:** Operates strictly on your local machine with zero external network traffic or browsing telemetry.

> [!TIP]
> Open **Settings -> Add-ons** inside Nyxor to install the companion extension directly into your browser.

---

## 🧩 Optional Plugins & Auxiliary Tools

While **Nyxor Download Manager** relies entirely on its **proprietary native engine (.NET & Rust Core)** for all network streaming, multi-segmented TCP routing (up to 128+ threads), zero-copy kernel disk commits, and direct downloads, it delegates certain dynamic web scraping tasks to auxiliary tools:

* **[yt-dlp](https://github.com/yt-dlp/yt-dlp):** Integrated solely as an optional upstream resolver plugin for parsing dynamic tokens and manifest URLs from social media platforms. *(The actual multi-part network ingestion and chunk assembling remain 100% handled by Nyxor's internal engine).*
* **[FFmpeg](https://ffmpeg.org/):** Utilized strictly as a secondary post-muxing utility when compiling detached adaptive audio/video DASH streams.

*Nyxor is an independent standalone download executive and is not affiliated with or a simple GUI wrapper for these third-party utilities.*

---

## 💬 Community & Support

Need assistance, want to report an issue, or suggest a new feature? Connect through our official channels:

* 🌐 **Website:** [nyxorlabs.com](https://nyxorlabs.com)
* 📢 **Telegram Channel:** [Nyxor Global](https://t.me/nyxorglobal)
* 📧 **Direct Contact:** [nyxorlabs@gmail.com](mailto:nyxorlabs@gmail.com)

---

<div align="center">
  <sub>Architected and engineered by <b>Uacoder</b> • Copyright © 2026 <b>Nyxor Labs</b>. All rights reserved.</sub>
</div>
