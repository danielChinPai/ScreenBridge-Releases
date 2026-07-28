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

## Version 0.5.2

- Reports the installed Android receiver version during local Wi-Fi discovery.
- Marks receivers below the packaged version as requiring an update.
- Transfers the packaged APK directly to an updater-capable paired receiver
  through a freshly authenticated AES-256-GCM Wi-Fi session.
- Validates the package name, version, and stable ScreenBridge signing
  certificate before Android stages the update.
- Retains Android's required device-user installation confirmation.
- Keeps the local QR download path available for installation and for
  receivers that predate network updating.
- Streams through direct USB or authenticated local Wi-Fi transport with
  independent virtual displays, hardware H.264 encoding, touch input, and
  persistent per-display settings.

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
