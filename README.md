# Flow downloads

# Flow 0.3 alpha — display quality and Windows sender setup

Update **both computers**. Quit the old Flow app from its tray/menu-bar menu before opening this version; closing the window is not enough.

- [Download Windows x64 ZIP](https://github.com/PlatiniumTermite/flow-downloads/releases/download/v0.3.0-alpha.20261012/Flow-Windows-x64.zip)
- [Download Mac Apple-silicon ZIP](https://github.com/PlatiniumTermite/flow-downloads/releases/download/v0.3.0-alpha.20261012/Flow-Mac-arm64.zip) (M-series Macs; not Intel)

Extract the entire Windows ZIP and open `win-unpacked/Flow.exe`. Extract the Mac ZIP and open the new `Flow.app`. These are development builds without distribution signing/notarization.

## Pair the computers

Use the same Wi-Fi. On the Mac, **Connect a device → Copy invitation**. On Windows, **Settings → Join a space**, paste that complete private invitation, and click **Join space**. Do not paste the GitHub download link. Keep invitations private.

## Mac → Windows: create a separate desktop

Select Windows on the Mac, choose **Resolution** and **Priority**, then **Extend Mac desktop**. Accept **Use as display** on Windows. Move windows to the right of the Mac display with the Mac keyboard/pointer. Full screen provides Exit and Stop controls.

New resolutions are **1080p, 1440p and 4K**, each targeting up to 60 fps. Text clarity preserves resolution under load; Smooth motion may downscale. H.264 is preferred with other codecs retained as fallback. Live stats show the codec/encoder, capture FPS, encode/decode time, resource limitations, resolution and received FPS where available.

## Windows → Mac: existing extended monitor required

Windows now offers **Use Windows extended display**. For wireless extension without a spare physical monitor, first install/configure a compatible signed virtual-display driver and choose **Extend these displays** in Windows Display settings. Flow's setup dialog links to the [Virtual Display Driver project](https://github.com/VirtualDrivers/Virtual-Display-Driver). Flow does **not** install or create a Windows virtual monitor automatically.

Choose the separate virtual monitor in Flow's native dialog and accept **Use as display** on the Mac. Use the Windows keyboard/pointer. Primary and overlapping/mirrored layouts are excluded; Flow does not substitute mirroring when extension is unavailable. Stopping Flow leaves the externally configured Windows monitor in place. This new Windows sender path requires physical Windows validation.

## Validation and limits

20 connection unit tests, 11 browser scenarios, native clipboard/helper lifecycle checks, and integrated native 1440p/4K pixel-delivery/full-screen/stop tests passed. The user reported the earlier Windows receiver build works; that is not certification of the new Windows sender.

Short local animated-pattern samples used VideoToolbox H.264. 1440p reached about 60 fps after startup; later 4K samples were 47–50 fps with higher encode time. These are neither sustained Wi-Fi benchmarks nor a guaranteed improvement over a controlled baseline. No 4K60, crash-free, or end-to-end-latency guarantee is made. The Mac virtual display uses experimental private APIs. Flow does not use Apple's Sidecar implementation.

See attached `WINDOWS-START-HERE.txt` and `DISPLAY-SETUP.md`. Checksums are in `SHA256SUMS.txt`.
