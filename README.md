# Flow — AirDrop-style continuity for Windows, Mac & Android

**[Download Flow →](https://platiniumtermite.github.io)**

Flow is a free, open alternative to AirDrop, LocalSend, KDE Connect, Snapdrop and AirDroid. Devices on the same Wi-Fi discover each other automatically, pair only with approval, and share everything wirelessly between Mac, Windows PC and Android:

- **AirDrop-style file sharing** — files, folders, text and links in both directions, with progress, resume and multiple recipients
- **Universal clipboard sync** — copied text and images move instantly between desktops, like Apple's Universal Clipboard
- **Screen sharing** — view another computer's screen after explicit approval
- **Extended display** — use a second computer as an extra monitor over Wi-Fi (experimental)
- **Keyboard & mouse link** — drive a connected computer from either side, like Universal Control
- **Menu-bar / system-tray agent** — discovery and sharing keep working without a window open
- iPhone and iPad join through Safari; a native iOS app is planned

Flow uses direct WebRTC when reachable. On isolated networks, Internet invitations use a public HTTPS tunnel and data can fall back to the signaling relay. Screen video still requires a working WebRTC media route. No account is required.

## Downloads

**[Windows 0.6.16 installer](https://github.com/PlatiniumTermite/flow-downloads/releases/download/v0.6.16/Flow-0.6.16-Windows-x64-Setup.exe)** — connection update for isolated Wi-Fi. Install, reopen Flow, then share **Connect a device → Internet invitation**. [Release notes](https://github.com/PlatiniumTermite/flow-downloads/releases/tag/v0.6.16).

[Download the latest release directly from GitHub](https://github.com/PlatiniumTermite/flow-downloads/releases/latest).

- `Flow-*-Windows-x64-Setup.exe` — Windows x64 installer
- `Flow-*-Mac-arm64.dmg` — Apple silicon Mac disk image
- `Flow-*-Mac-x64.dmg` — Intel Mac disk image
- `Flow-*-Android.apk` — Android app
- `INSTALL.md` — full install and pairing guide
- `SHA256SUMS.txt` — integrity checksums

Unsigned alpha builds: your OS may warn on first launch — see INSTALL.md in the latest release for the exact clicks. Source code: [PlatiniumTermite/flow](https://github.com/PlatiniumTermite/flow).
