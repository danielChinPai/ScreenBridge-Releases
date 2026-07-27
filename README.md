<p align="center">
  <img
    src="assets/screenbridge-windows.png"
    alt="ScreenBridge"
    width="180">
</p>

<h1 align="center">ScreenBridge Downloads</h1>

<p align="center">
  <strong>Turn an Android device into a wired USB external display for Windows.</strong>
</p>

ScreenBridge creates independent Windows virtual displays, streams them to
Android over USB, and returns Android touch input to Windows.

## Download

Open the [Releases](../../releases) page and download the newest
`ScreenBridge-<version>-win-x64-setup.exe`.

The self-contained installer adds the Windows application, ScreenBridge IddCx
display driver, Android receiver, USB transport tools, uninstaller, Start menu
shortcut, and optional desktop shortcut.

## Version 0.4.0

- Separates capture and encoding across independent D3D11 devices and worker
  threads.
- Uses a bounded shared GPU texture pool and always consumes the newest
  completed display update.
- Stops encoding duplicate frames while a desktop is unchanged, reducing GPU
  use beside games and other foreground applications.
- Imports Intel Quick Sync input surfaces directly when supported.
- Wakes Android frame presentation only when decoded output is waiting.
- Keeps Android touch reception asynchronous and leaves physical Windows
  keyboard and mouse input on the native Windows input path.

The selected FPS is a maximum update rate. A static desktop can report a lower
frame rate because no duplicate frames are generated.

## Requirements

- Windows 11 x64
- Android 11 or later
- A GPU with hardware H.264 encoding support
- A data-capable USB connection with Android USB debugging enabled
- Administrator access for display driver installation

The current `0.x` line is an alpha release. The setup executable is not yet
Authenticode-signed, the virtual display driver uses a development test
certificate, and the bundled Android receiver is debug-signed.

Source code and technical documentation are available in the
[ScreenBridge repository](https://github.com/danielChinPai/ScreenBridge).
