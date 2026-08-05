# Nyxor Download Manager 

![Version](https://img.shields.io/badge/Version-v1.2.0.0-0080FF?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011-121212?style=for-the-badge)
![Architecture](https://img.shields.io/badge/Architecture-x64%20Only-8B0000?style=for-the-badge)
![Core](https://img.shields.io/badge/Core-.NET%20%2B%20Rust-E65100?style=for-the-badge)
![UI](https://img.shields.io/badge/UI-Custom%20GDI%2B-1E1E1E?style=for-the-badge)

**Nyxor Download Manager** is a high-concurrency desktop executive engineered to push network bandwidth to its absolute limits. Built on a hybrid **.NET and Rust** architecture, Nyxor discards legacy download mechanics in favor of aggressive multi-threading, dynamic segmentation, and deep browser integration. 

This is not just another downloader; it is a precision tool built for power users who demand speed, stability, and unrestricted media extraction.

---

## ⚡ Under the Hood: Pure Performance

Nyxor is strictly compiled for **64-bit (x64)** systems. By removing 32-bit memory constraints, the engine effortlessly handles massive multi-gigabyte file streams and CPU-intensive media processing without breaking a sweat.

* **Hybrid Engine (.NET + Rust):** Combines the rapid deployment of .NET with the memory-safe, low-latency execution of Rust for network packet handling and heavy I/O operations.
* **Aggressive Concurrency:** Dynamically splits files into parallel streams with automated connection recovery, ensuring zero data loss during network drops.
* **Manifest V3 Native Integration:** Ships with a lightweight, highly secure JavaScript Manifest V3 browser extension. It intercepts downloads, sniffs complex media streams, and communicates directly with the desktop client via secure native messaging.

## 🎨 Zero WinForms Clutter: The GDI+ Fluent Dark UI

We threw out the default Windows controls. Nyxor’s interface is a masterclass in custom UI engineering, drawn entirely from scratch using a highly optimized, double-buffered **GDI+** rendering engine.

* **Executive Aesthetics:** Built on a strict 8/16px spatial grid ensuring perfect proportion.
* **Fluent Dark Identity:** Features a rich `#121212` base layered with `#1E1E1E` surfaces, accented by precision 8px rounded corners and a subtle 1px inner-glow.
* **Silky Smooth:** 100% flicker-free, high-DPI aware, and fully anti-aliased typography that feels native, responsive, and incredibly premium.

## ⚙️ Advanced Media Acquisition

Nyxor handles standard files with ease, but its true power lies in direct extraction of video and audio streams from complex web platforms, DASH, and M3U8/HLS playlists. 

To achieve seamless media muxing and protocol bypassing, Nyxor proudly integrates the following open-source backbone utilities in its background processes:
* **[yt-dlp](https://github.com/yt-dlp/yt-dlp):** Leveraged for state-of-the-art protocol bypassing, handling dynamic cookies, custom headers, and stream metadata extraction.
* **[FFmpeg](https://ffmpeg.org/):** The industry standard, utilized as our core backend component for high-speed A/V muxing and post-download processing.

---

## 🔗 Connect & Support

Nyxor is an actively maintained, closed-source project. For updates, feature requests, bug reports, or just to hang out with the community, reach out through our official channels:

* 🌐 **Official Website:** [nyxorlabs.com](https://nyxorlabs.com)
* 💬 **Telegram Community:** [Nyxor Global](https://t.me/nyxorglobal)
* 📧 **Direct Contact:** [nyxorlabs@gmail.com](mailto:nyxorlabs@gmail.com)

---
*Architected and developed by **Osama Ghalib (UacoderSA)** | NyxorLabs.*
