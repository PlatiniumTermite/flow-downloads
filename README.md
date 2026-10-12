# Flow downloads

# Flow 0.3.1 alpha — easier desktop installation

**Engineering alpha, not production-ready.** Update both computers and quit the old Flow app from its tray/menu-bar menu first.

| Download | Installation |
| --- | --- |
| [Windows x64 installer](https://github.com/PlatiniumTermite/flow-downloads/releases/download/v0.3.1-alpha.1/Flow-0.3.1-alpha.1-Windows-x64-Setup.exe) | Open Setup.exe; installs for your account with Start-menu and desktop shortcuts. |
| [Apple silicon Mac disk image](https://github.com/PlatiniumTermite/flow-downloads/releases/download/v0.3.1-alpha.1/Flow-0.3.1-alpha.1-Mac-arm64.dmg) | Open the DMG, drag Flow to Applications, then launch from Applications. |

No Node.js, terminal commands, or ZIP extraction needed. Intel Mac and Windows ARM-native builds are not included. **Windows signing and Mac Developer ID signing/notarization are pending. OS security may warn or block these builds.** Do not disable security controls. These are testing downloads, not a trusted-publisher production release.

## Pair and use

Use the same trusted Wi-Fi. On the hosting Mac: **Connect a device → Copy invitation**. On Windows: **Settings → Join a space**, paste the complete invitation, then **Join space**. Paste into Flow, not PowerShell. Keep the hosting Mac running. Never share your private invitation publicly.

Select the other device to send a file; accept and save it on the receiver. Text clipboard sync is opt-in in each desktop app's settings.

For Mac extension: select Windows on the Mac, choose resolution and **Extend Mac desktop**; accept **Use as display** on Windows. Use the Mac keyboard/mouse. Windows sending requires an existing extended monitor or a separately configured virtual-display driver; Flow does not create/install that driver automatically. See [Windows extension setup](https://github.com/PlatiniumTermite/flow-downloads/releases/download/v0.3.1-alpha.1/WINDOWS-EXTENSION.md).

[Full installation, update and pairing instructions](https://github.com/PlatiniumTermite/flow-downloads/releases/download/v0.3.1-alpha.1/START-HERE.md). Automatic app updates are not implemented; download the next installer manually and quit Flow before updating. Local app data is retained.

## Changes and verification

- Added Windows per-user NSIS installer and Mac drag-to-Applications disk image.
- Clean staging prevents removed assets being shipped in later packages.
- Windows notification identity now matches the installer; startup failures show an actionable error.
- Added packaged-app test and Mac/Windows packaging CI workflow. Hosted CI has not been run from this local workspace.
- Passed 20 connection tests and 11 browser scenarios, including exact 80 MiB transfer integrity. Workspace typecheck/tests passed.
- Packaged Mac app passed real pairing, text delivery, clipboard and discovery-toggle checks. DMG checksum and bundled app/helper comparison passed.
- Production-dependency audit reported zero known advisories at build time; this is not a security audit of Flow or its runtime.

The Windows installer was cross-built on Mac; fresh Windows install/upgrade/uninstall and the new sender path need physical-PC validation. The earlier Windows receiver was reported working by the user. Mac virtual display uses private APIs. Display choices target up to 60 fps; no universal 4K60, sustained wireless latency, or crash-free guarantee is established. Interrupted-file resume, individual device revocation, automatic Windows monitor management and broad physical-device acceptance remain unfinished.

SHA-256 hashes for installers and guides are in `SHA256SUMS.txt`. Checksums do not replace OS publisher signatures.
