<p align="center">
  <img src="assets/screenbridge-windows.png"
       alt="ScreenBridge icon"
       width="180">
</p>

<h1 align="center">ScreenBridge</h1>

<p align="center">
  <strong>把 Android 裝置變成 Windows 的有線 USB 外接螢幕。</strong><br>
  Turn an Android device into a wired USB external display for Windows.
</p>

ScreenBridge extends the Windows desktop to an Android device through a direct
USB connection. Each display can keep its own resolution, refresh rate,
position, and device assignment, while the video path remains on USB instead
of the local network.

## Official downloads

This public repository contains official ScreenBridge installer downloads and
release notes only. The application source repository is private and is not
published here.

## Download

Open the [Releases](../../releases) page and download:

- `ScreenBridge-<version>-win-x64-setup.exe`

The installer places ScreenBridge under `C:\Program Files\ScreenBridge`,
creates a Start menu shortcut, and selects the desktop-shortcut option by
default. It includes the Windows application, .NET runtime, Android receiver
APK, ADB runtime, virtual display driver, and uninstaller.

## Alpha requirements

- Windows 11 x64
- An NVIDIA GPU with NVENC support
- An Android 11 or newer device
- USB debugging enabled on the Android device

The current 0.x builds are alpha releases. The setup executable is not yet
Authenticode-signed, the virtual display driver uses a development test
certificate, and the bundled Android APK is debug-signed. Windows SmartScreen
may warn before installation. The installer explains these conditions before
making system changes.

GitHub automatically displays “Source code” archives for every release. In
this downloads-only repository those archives contain only this public release
metadata, not the ScreenBridge application source code.
