# Nyxor Download Manager

Nyxor is a download manager for Windows. It keeps track of which parts of a file have reached disk, so you can close the app and pick up where you left off. The same queue handles direct links, torrents, videos, and live recordings.

**[Download the latest release for Windows](https://github.com/UacoderSYS/Nyxor-Download-Manager/releases/latest)** · [Official website](https://nyxorlabs.com) · [Changelog](https://nyxorlabs.com/changelog)

![Nyxor’s main window with the download queue and completion controls](https://github.com/user-attachments/assets/63913aa4-91e1-47db-8723-95221073a098)

## Getting started

1. Open the [latest release](https://github.com/UacoderSYS/Nyxor-Download-Manager/releases/latest) and download `NyxorDM.exe` from **Assets**.
2. Launch Nyxor on Windows 10 or 11 (64-bit) with .NET Framework 4.8 or newer.
3. Press **Ctrl+N** to add a download link, or **Ctrl+B** to add several at once.

The full app is available for a 14-day trial without a credit card. A lifetime license costs $15 as a one-time purchase.

<details>
<summary>Verify a download with PowerShell</summary>

Open PowerShell in the folder containing the downloaded file and run:

```powershell
Get-FileHash -Algorithm SHA256 .\NyxorDM.exe
```

If the release includes a SHA-256 checksum, compare it with the value in the `Hash` column. Use the checksum for the exact file and release you downloaded.

</details>

## Download engine

For servers that support byte ranges, Nyxor splits a file into segments and adjusts the connection count according to measured throughput, up to 128 parallel streams. Near the end of a transfer, idle connections can take on part of a slow segment. The live monitor shows progress per segment and lets you set a speed limit.

When a connection drops, Nyxor checks the returned byte range and expected length before resuming. It checks each segment’s size and position again before assembling the file. If disk space allows, Nyxor keeps the segments until it has written and verified the output. On drives with less free space, it assembles the file progressively.

![Live monitor showing individual download segments and the speed limiter](https://github.com/user-attachments/assets/a6d8e414-7df7-4237-954b-31d1f18492b4)

## Media capture and live recording

Paste a video or playlist link into **Media Grabber** to see the formats the source offers. Select a resolution up to 8K at 60 fps, or choose an audio-only download. When a video has multiple audio tracks, the selector lists the original and available dubs, including Arabic where offered.

Nyxor supports sources including YouTube, Facebook, Instagram, TikTok, Twitch, Reddit, and X. For live broadcasts, the recorder handles HLS, DASH, and FLV streams, with a stop timer and ad-break filtering on supported sources. If a media link expires during a download, **Auto-Healing** tries to obtain a fresh link and continue from the saved position.

![Media Grabber with quality and audio track selection](https://github.com/user-attachments/assets/2c5b519c-b80d-453a-a196-ed5218e8086e)

## BitTorrent

Open a torrent file or magnet link to see its contents before downloading. Choose individual files, set their priorities, or use sequential downloading to start watching a video while the remaining pieces arrive. Nyxor verifies pieces as they arrive and can stop seeding when the download finishes. The swarm inspector shows peers, seeds, and tracker status, with controls to add trackers or block a peer.

## Browser integration

The Chrome and Edge extension adds a download control to supported videos. Use it to send a video to Nyxor, extract audio, save a gallery image, or capture a frame. You can dismiss the control for an individual video. The extension connects to the desktop app on your machine at `127.0.0.1` and shows when the app is offline.

[Chrome Web Store](https://chromewebstore.google.com/detail/nyxor-browser-integration/fmbpmhpahecfneoanghjcdnoiipgagon) · [Microsoft Edge Add-ons](https://microsoftedge.microsoft.com/addons/detail/nyxor-browser-integration/dlnncpfaaejjbdgkfabhjjnnjhhboapp)

## Working with downloaded files

| Tool | What you can do |
| --- | --- |
| LAN Warp | Scan a QR code and enter a PIN to copy a file to a phone or another computer over Wi-Fi. Use the optional tunnel to share across networks. |
| Media Studio | Trim a clip, normalize audio to EBU R128, add MP3 cover art, or prepare an MP4 for fast-start playback. Export to MP4, MKV, WebM, MOV, AVI, GIF, MP3, M4A, WAV, or FLAC. Supported encoders can use NVIDIA NVENC, Intel Quick Sync, or AMD AMF. |
| Site Grabber | Browse a page’s videos, images, documents, and archives in a file tree, then queue the items you want. |
| Checksum verifier | Calculate MD5, SHA-1, and SHA-256 hashes from within the app. |

## Desktop and network settings

Nyxor includes light and dark themes and supports Arabic, English, Spanish, French, German, Portuguese, and Russian, with a right-to-left layout for Arabic. Proxy settings support HTTP, HTTPS, SOCKS4, and SOCKS5 and include a latency test.

<details>
<summary>Keyboard shortcuts</summary>

| Shortcut | Action |
| --- | --- |
| Ctrl+N | Add a download link |
| Ctrl+B | Add links in bulk |
| Space | Pause or resume the selected task |
| Delete | Open the deletion prompt |
| Ctrl+A | Select all tasks |
| Ctrl+, | Open settings |

</details>

## Implementation

The Windows interface uses .NET Framework and GDI+. A native Rust library, `nyxor_core.dll`, handles segmented HTTP and HTTPS transfers and BitTorrent networking. For media tasks, Nyxor can use [yt-dlp](https://github.com/yt-dlp/yt-dlp) to resolve manifests and discover audio tracks, and [FFmpeg](https://ffmpeg.org/) to combine audio and video, remux recordings, and convert files.

## Support

For download, extension, or licensing questions, email [info@nyxorlabs.com](mailto:info@nyxorlabs.com) or [nyxorlabs@gmail.com](mailto:nyxorlabs@gmail.com).

[Telegram community](https://t.me/nyxorglobal) · [Nyxor Labs on YouTube](https://www.youtube.com/@nyxorlabs)

Developed by Uacoder. © 2026 Nyxor Labs. All rights reserved.
