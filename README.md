# ScreenBridge Releases

This public repository contains official ScreenBridge installer downloads and
release notes only. The application source repository is private and is not
published here.

## Download

Open the [Releases](../../releases) page and download both:

- `ScreenBridge-<version>-win-x64-setup.exe`
- `ScreenBridge-<version>-win-x64-setup.exe.sha256`

The installer places ScreenBridge under `C:\Program Files\ScreenBridge`,
creates a Start menu shortcut, and selects the desktop-shortcut option by
default. It includes the Windows application, .NET runtime, Android receiver
APK, ADB runtime, virtual display driver, and uninstaller.

## Alpha requirements

- Windows 11 x64
- An NVIDIA GPU with NVENC support
- An Android 11 or newer phone or tablet
- USB debugging enabled on the Android device

The current 0.x builds are alpha releases. The setup executable is not yet
Authenticode-signed, the virtual display driver uses a development test
certificate, and the bundled Android APK is debug-signed. Windows SmartScreen
may warn before installation. The installer explains these conditions before
making system changes.

## Verify the download

In PowerShell:

```powershell
Get-FileHash .\ScreenBridge-0.1.0-win-x64-setup.exe -Algorithm SHA256
Get-Content .\ScreenBridge-0.1.0-win-x64-setup.exe.sha256
```

The two SHA-256 values must match.

GitHub automatically displays “Source code” archives for every release. In
this downloads-only repository those archives contain only this public release
metadata, not the ScreenBridge application source code.
