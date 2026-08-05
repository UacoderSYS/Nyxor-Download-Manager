# Nyxor Download Manager 

![Version](https://img.shields.io/badge/Version-v1.2.0.0-0080FF?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011-121212?style=for-the-badge)
![Architecture](https://img.shields.io/badge/Architecture-x64%20Only-8B0000?style=for-the-badge)
![Core](https://img.shields.io/badge/Core-.NET%20%2B%20Rust-E65100?style=for-the-badge)
![UI](https://img.shields.io/badge/UI-Custom%20GDI%2B-1E1E1E?style=for-the-badge)

**Nyxor Download Manager** is an advanced, high-concurrency desktop download executive engineered to push network bandwidth to its absolute limits. Built on a hybrid **.NET and Rust** architecture, Nyxor discards standard download mechanics in favor of aggressive multi-threading, real-time stream capturing, and dynamic network recovery.

This tool is strictly compiled for power users demanding raw speed, stability with massive files, and unrestricted media extraction.

---

## ⚡ Ultra-Speed Engine & File Management

Compiled exclusively for **64-bit (x64)** systems, Nyxor easily handles massive multi-gigabyte file streams without memory bloat.

* **Aggressive Concurrency:** Dynamically splits files into parallel streams (up to 128 chunks) based on payload size, maximizing your internet speed.
* **Smart Auto-Healing & Resume:** Broken link? Network failure? Nyxor's Auto-Healing engine automatically detects expired tokens and fetches fresh connection links in the background, allowing downloads to resume without user intervention.
* **Bandwidth Control:** Built-in precision throttle limits to balance network load without completely choking the application.

## 📡 Real-Time Live Stream Capture & Ad-Blocking

Nyxor is uniquely equipped to handle complex, fragmented live broadcasting environments. The core engine captures, buffers, and compiles live streams instantly.

* **Broad Platform Support:** Natively latches onto live broadcasts from platforms like **YouTube, Twitch, Kick, and TikTok**, capturing data packet-by-packet as it happens.
* **Native Twitch Ad-Blocking:** Features an integrated filter that automatically detects and skips commercial/ad nodes (`weaver_ad`) during live Twitch captures, ensuring your final video is ad-free.
* **HLS/M3U8 & DASH Processing:** Seamlessly processes varying stream resolutions and dynamic segments without corruption.

## 🎬 4K/8K Media Muxing & Formats

Standard file downloading is trivial; Nyxor excels in pulling multi-layered media.

* **Highest Quality Variants:** Automatically analyzes media platforms and extracts the absolute highest available quality (up to 4K/8K UHD).
* **On-the-Fly DASH Muxing:** Synchronously merges detached video and high-bitrate audio streams during the download phase via an integrated FFmpeg engine, eliminating post-processing latency.
* **Format Conversion:** Features native options to extract direct Audio (MP3/M4A) from any supported media link.

## 📅 Task Scheduling & Automation

Nyxor operates completely hands-free when needed via its built-in Scheduler Engine.
* Set strict start/stop times for off-peak bandwidth usage.
* Configure post-download automated actions, including system Sleep, Hibernate, or forced Shutdown once the queue is clear.

## 🎨 Zero WinForms Clutter: Pure GDI+ UI

We discarded default Windows controls. Nyxor’s interface is a precision-engineered frontend, rendered entirely from scratch using a double-buffered **GDI+** engine.

* **Executive Aesthetics:** Built on a strict 8/16px spatial grid, enforcing absolute proportion and structural harmony across all elements.
* **Fluent Dark Identity:** Driven by a `#121212` base layered with `#1E1E1E` surfaces, accented by precision 8px rounded corners and a strict 1px inner-glow for depth.
* **High-Performance Rendering:** 100% flicker-free, high-DPI aware, and fully anti-aliased. It looks and responds like a native, premium application.

## ⚙️ Core Dependencies

To maintain high-speed extraction and media compilation, Nyxor integrates with heavily customized open-source utilities:
* **[yt-dlp](https://github.com/yt-dlp/yt-dlp):** Leveraged for dynamic metadata extraction, format mapping, and token generation.
* **[FFmpeg](https://ffmpeg.org/):** Utilized as the backend engine for high-speed A/V muxing and raw stream compilation.

## 🔑 Activation & Getting Started

To initialize the local environment and bypass speed restrictions, launch the application and click **"Start Free Trial"**. This standard procedure authenticates the session and immediately unlocks the high-concurrency extraction engine.

---

## 🔗 Connect & Support

Nyxor is an actively maintained, closed-source project. For binary updates, feature requests, or technical reports, reach out through our official channels:

* 🌐 **Official Website:** [nyxorlabs.com](https://nyxorlabs.com)
* 💬 **Telegram Community:** [Nyxor Global](https://t.me/nyxorglobal)
* 📧 **Direct Contact:** [nyxorlabs@gmail.com](mailto:nyxorlabs@gmail.com)

---
*Architected and developed by **Uacoder** | NyxorLabs.*
