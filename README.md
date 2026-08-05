# Nyxor Download Manager 

![Version](https://img.shields.io/badge/Version-v1.2.0.0-0080FF?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011-121212?style=for-the-badge)
![Architecture](https://img.shields.io/badge/Architecture-x64%20Only-8B0000?style=for-the-badge)
![Core](https://img.shields.io/badge/Core-.NET%20%2B%20Rust-E65100?style=for-the-badge)
![UI](https://img.shields.io/badge/UI-Custom%20GDI%2B-1E1E1E?style=for-the-badge)

**Nyxor Download Manager** is a high-concurrency desktop executive engineered to push network bandwidth to its absolute limits. Built on a hybrid **.NET and Rust** architecture, Nyxor discards legacy download mechanics in favor of aggressive multi-threading, dynamic segmentation, and deep browser integration. 

This tool is strictly compiled for power users demanding raw speed and unrestricted media extraction.

---

## ⚡ Under the Hood: Core Architecture

Compiled exclusively for **64-bit (x64)** systems, Nyxor is structured to bypass legacy memory constraints, handling massive multi-gigabyte file streams and CPU-intensive media multiplexing without system bloat.

* **Hybrid Engine (.NET + Rust):** Combines the rapid deployment ecosystem of .NET with the memory-safe, low-latency execution of Rust for heavy I/O operations and low-level network packet handling.
* **Aggressive Concurrency:** Dynamically splits payloads into parallel streams with automated connection recovery, enforcing zero data loss during unstable network conditions.
* **Native Manifest V3 Integration:** Ships with a highly secure JavaScript Manifest V3 browser extension. It intercepts traffic, sniffs raw media streams, and communicates directly with the desktop client via encrypted native messaging.

## 📡 Advanced Decryption & Protocol Bypassing

Standard file downloading is trivial; Nyxor is engineered specifically for complex, fragmented, and heavily restricted media environments. The core engine is optimized to capture, decrypt, and compile live broadcasts on the fly.

* **AES & DRM Decryption:** Features a real-time decryption core capable of handling AES-128/256 protected M3U8 and DASH manifests, instantly resolving and assembling fragmented video chunks.
* **Complex Bypassing Logic:** Built-in token extraction and header spoofing algorithms designed to break through geo-blocks, request-rate limits, and anti-scraping firewalls on strict platforms (including FB, IG, Twitch, and custom CDN nodes).
* **On-the-Fly Muxing:** Automatically merges detached video and audio streams synchronously during the download phase, eliminating post-processing latency.

## 🎨 Zero WinForms Clutter: Pure GDI+ UI

We discarded default Windows controls. Nyxor’s interface is a precision-engineered frontend, rendered entirely from scratch using a double-buffered **GDI+** engine.

* **Executive Aesthetics:** Built on a strict 8/16px spatial grid, enforcing absolute proportion and structural harmony across all elements.
* **Fluent Dark Identity:** Driven by a `#121212` base layered with `#1E1E1E` surfaces, accented by precision 8px rounded corners and a strict 1px inner-glow for depth.
* **High-Performance Rendering:** 100% flicker-free, high-DPI aware, and fully anti-aliased. It looks and responds like a native, premium application.

## ⚙️ Open-Source Backbone Integration

To maintain dominance over edge-case protocol updates and hardware-accelerated processing, Nyxor securely interfaces with heavily customized open-source utilities:
* **[yt-dlp](https://github.com/yt-dlp/yt-dlp):** Leveraged as an underlying dependency for handling dynamic cookie injection, rotating custom headers, and aggressive metadata extraction.
* **[FFmpeg](https://ffmpeg.org/):** Utilized as the backend engine for high-speed A/V muxing and raw stream compilation.

## 🔑 Activation & Getting Started

To initialize the local environment and bypass restrictions, launch the application and click **"Start Free Trial"**. This standard procedure authenticates the session and immediately unlocks the high-concurrency extraction engine.

---

## 🔗 Connect & Support

Nyxor is an actively maintained, closed-source project. For binary updates, feature requests, or technical reports, reach out through our official channels:

* 🌐 **Official Website:** [nyxorlabs.com](https://nyxorlabs.com)
* 💬 **Telegram Community:** [Nyxor Global](https://t.me/nyxorglobal)
* 📧 **Direct Contact:** [nyxorlabs@gmail.com](mailto:nyxorlabs@gmail.com)

---
*Architected and developed by **Uacoder** | NyxorLabs.*
