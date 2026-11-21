Nyxor Download Manager

A Windows download manager for large files, torrents, and live streams.

￼ ￼ 

Official website · Changelog · Browser extension · Support 

Close Nyxor halfway through a large download and it remembers which parts are already on disk. You can pick up the transfer when you reopen the app, set a speed limit while you’re on a call, or send the finished file to your phone with a QR code.
�

📥 Get started
Open the latest release and download NyxorDM.exe from Assets.
Launch Nyxor on Windows 10 or 11 (64-bit) with .NET Framework 4.8 or newer.
Press Ctrl+N to add a download link, or Ctrl+B to add several at once.
Trial and license. Try the full app for 14 days without a credit card. A lifetime license is a one-time $15 purchase.
Verify a download with PowerShell
Open PowerShell in the folder containing the downloaded file and run:
Get-FileHash -Algorithm SHA256 .\NyxorDM.exe
If the release includes a SHA-256 checksum, compare it with the value in the Hash column. Use the checksum for the exact file and release you downloaded.

⚡ Downloads and recovery
Use the live monitor to see how much of a file each connection has received. If you need bandwidth for something else, set a limit while the transfer is running.
Connection scaling. On servers that support byte ranges, Nyxor adjusts the number of connections to measured throughput, up to 128 parallel streams. Toward the end of a download, idle connections can take over part of a slow segment.
Resume checks. After an interruption, Nyxor checks the server’s returned range and expected length before continuing. It checks the size and position of each segment again before joining the file.
Disk space. When space allows, Nyxor keeps the segments until it has written and verified the output. On a nearly full drive, it assembles the file progressively.
�
🎬 Video, audio, and live recording
Paste a video or playlist link into Media Grabber to see the formats the source offers. Select a resolution up to 8K at 60 fps, or choose an audio-only download. When a video has multiple audio tracks, the selector lists the original and available dubs, including Arabic where offered.
Supported sources include YouTube, Facebook, Instagram, TikTok, Twitch, Reddit, and X.
For live broadcasts, the recorder handles HLS, DASH, and FLV streams, with a stop timer and ad-break filtering on supported sources. If a media link expires during a download, Auto-Healing tries to obtain a fresh link and continue from the saved position.
�
🧲 Torrents and magnet links
Open a torrent file or magnet link to see its contents before downloading. Choose individual files, set their priorities, or use sequential downloading to start watching a video while the remaining pieces arrive. Nyxor verifies pieces as they arrive and can stop seeding when the download finishes. The swarm inspector shows peers, seeds, and tracker status, with controls to add trackers or block a peer.

🌐 Browser extension
The Chrome and Edge extension adds a download control to supported videos. Use it to send a video to Nyxor, extract audio, save a gallery image, or capture a frame. You can dismiss the control for an individual video. The extension connects to the desktop app on your machine at 127.0.0.1 and shows when the app is offline.
￼ ￼ 

🧰 Built-in tools
Tool
What you can do
LAN Warp
Scan a QR code and enter a PIN to copy a file to a phone or another computer over Wi-Fi. Use the optional tunnel to share across networks.
Media Studio
Trim a clip, convert it for another device, normalize audio to EBU R128, add MP3 cover art, or prepare an MP4 for fast-start playback.
Site Grabber
Browse a page’s videos, images, documents, and archives in a file tree, then queue the items you want.
Checksum verifier
Calculate MD5, SHA-1, and SHA-256 hashes from within the app.
Media Studio exports to MP4, MKV, WebM, MOV, AVI, GIF, MP3, M4A, WAV, and FLAC. Hardware encoding is available with NVIDIA NVENC, Intel Quick Sync, or AMD AMF on supported hardware and formats.
⚙️ Desktop and network settings
Nyxor includes light and dark themes and supports Arabic, English, Spanish, French, German, Portuguese, and Russian, with a right-to-left layout for Arabic. Proxy settings support HTTP, HTTPS, SOCKS4, and SOCKS5 and include a latency test.
Keyboard shortcuts
Shortcut
Action
Ctrl+N
Add a download link
Ctrl+B
Add links in bulk
Space
Pause or resume the selected task
Delete
Open the deletion prompt
Ctrl+A
Select all tasks
Ctrl+,
Open settings

Under the hood
The Windows interface uses .NET Framework and GDI+. A native Rust library, nyxor_core.dll, handles segmented HTTP and HTTPS transfers and BitTorrent networking. For media tasks, Nyxor can use yt-dlp to resolve manifests and discover audio tracks, and FFmpeg to combine audio and video, remux recordings, and convert files.

💬 Support
For download, extension, or licensing questions, email info@nyxorlabs.com or nyxorlabs@gmail.com.
Telegram community · Nyxor Labs on YouTube
Developed by Uacoder. © 2026 Nyxor Labs. All rights reserved.