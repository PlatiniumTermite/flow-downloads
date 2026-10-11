# Flow downloads

Public downloads and setup instructions for the Flow engineering alpha.

# Flow for Windows — alpha

[**Download Flow for Windows x64 (ZIP, approximately 151 MB)**](https://github.com/PlatiniumTermite/flow-downloads/releases/download/v0.2.0-alpha.20261011/Flow-Windows-x64.zip)

1. Download the ZIP, right-click it and choose **Extract All**.
2. Open the extracted **win-unpacked** folder and double-click **Flow.exe**. Keep all companion files together. No terminal commands or developer tools are needed.
3. Connect Windows and your Mac to the same Wi-Fi. Keep the latest Flow app running on both.
4. **On the Mac:** click **Connect a device → Copy invitation**. Send the copied text privately to the Windows PC.
5. **On Windows:** open Flow → **Settings (gear) → Join a space**. Paste the **entire invitation copied from the Mac** into **Paste a Flow invitation**, then click **Join space**.
6. To extend your Mac desktop, select Windows in Flow on the Mac and click **Extend Mac desktop to [device]**. On Windows, accept **Use as display**, then **Full screen**. Use the Mac keyboard and mouse. Exit with **Exit full screen** or Escape; **Stop sharing** ends extension.

## What exactly goes in the Windows box?

Paste your Mac app's complete **private invitation**. It normally looks like `http://192.168.x.x:PORT/#PRIVATE_KEY`, but your app supplies the actual address, port and key. Keep everything after `#`. Do not type the example or invent a key. A complete `flow://join?...#...` invitation is also accepted.

The public download link above is only for downloading the app. **Do not paste the GitHub download link into Join a space.** Paste the invitation inside Flow, not in PowerShell, Command Prompt or a web browser. Share the invitation privately: anyone who has it can join that space.

For clipboard sharing, enable automatic text clipboard sharing in both desktop apps' settings, using your personal device space. Friend sessions keep automatic clipboard sharing disabled.

## If connection fails

Keep the Mac app hosting the space open. Avoid guest Wi-Fi that isolates devices. If Windows prompts for firewall access, allow Flow on your trusted private network; do not disable the firewall. A `localhost` or `127.0.0.1` invitation cannot reach another computer. If the Mac changes networks, copy its current invitation again.

Mac extension may require normal Screen Recording permission and an app restart. Use a current Mac build that shows the **Extend Mac desktop** button. The public download URL does not make a private Wi-Fi pairing invitation work over the internet.

## Status

This is an **unsigned development alpha**. The Windows x64 package was built successfully but has not yet been executed on a physical Windows PC. Mac native virtual-display capture, local video delivery, full-screen controls and cleanup passed tests. Physical Mac-to-Windows wireless performance and end-to-end latency remain unverified. Up to 60 fps is a target, not a guarantee. The Mac virtual-display helper uses experimental private APIs. Windows keyboard/mouse forwarding is not implemented.

`WINDOWS-START-HERE.txt` is included inside the ZIP and attached separately. `SHA256SUMS.txt` contains the archive checksum.
