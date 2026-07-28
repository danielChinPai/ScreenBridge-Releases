<p align="center">
  <img
    src="assets/screenbridge-windows.png"
    alt="ScreenBridge"
    width="180">
</p>

<h1 align="center">ScreenBridge Downloads</h1>

<p align="center">
  <strong>Turn an Android device into a Windows external display over USB or local Wi-Fi.</strong>
</p>

ScreenBridge creates independent Windows virtual displays, streams them to
Android over USB or the local network, and returns Android touch input to
Windows.

## Download

Open the [Releases](../../releases) page and download the newest
`ScreenBridge-<version>-win-x64-setup.exe`.

The self-contained installer adds the Windows application, ScreenBridge IddCx
display driver, Android receiver, USB transport tools, uninstaller, Start menu
shortcut, and optional desktop shortcut. It does not require a separately
installed .NET runtime.

## Version 0.5.1

- Adds a local QR download dialog for installing the Android receiver without
  first connecting a USB cable.
- Serves the packaged APK only while the dialog is open through a
  token-protected local-network address.
- Selects the active network automatically and exposes interface selection
  only when more than one usable address is available.
- Ships a release APK signed with the stable ScreenBridge Android signing
  identity for consistent future updates.
- Adds a native local Wi-Fi transport with encrypted TCP control and paced UDP
  H.264 video.
- Uses P-256 ECDH for first pairing, HMAC-authenticated remembered sessions,
  and independent AES-256-GCM keys for control and video.
- Recovers short packet-loss bursts with adaptive Reed-Solomon parity and a
  bounded 2–8 ms reordering window.
- Uses receiver loss, jitter, queue, and frame-assembly feedback to adjust
  packet pacing and recovery overhead.
- Treats USB and Wi-Fi connections for the same physical receiver as one
  device assignment.
- Adds English and Traditional Chinese interface selection plus expanded
  stream status metrics.
- Preserves the independent capture, hardware-encoding, touch, and display
  state of every active virtual display.

The selected FPS is a maximum update rate. A static desktop can report a lower
frame rate because no duplicate frames are generated.

## Requirements

- Windows 11 x64
- Android 11 or later
- A GPU with hardware H.264 encoding support
- A data-capable USB connection with Android USB debugging enabled, or both
  endpoints on the same local IPv4 network
- Administrator access for display driver installation

Local Wi-Fi streaming does not use internet bandwidth. A low-contention
5 GHz or 6 GHz connection is recommended for high-resolution,
high-refresh-rate modes.

The current `0.x` line is an alpha release. The setup executable is not yet
Authenticode-signed, the virtual display driver uses a development test
certificate, and the bundled Android receiver uses the stable ScreenBridge
release signature.

Source code and technical documentation are available in the
[ScreenBridge repository](https://github.com/danielChinPai/ScreenBridge).
