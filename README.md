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
display driver, virtual HID input driver, Android receiver, USB transport
tools, uninstaller, Start menu shortcut, and optional desktop shortcut.

## Version 0.6.0

- Adds a choice between a virtual display and a dedicated Android touchpad
  when creating a ScreenBridge accessory.
- Adds pointer acceleration, tap-to-click, tap-and-drag, auxiliary-finger drag
  extension, two-finger scrolling with inertia, pinch zoom, palm rejection,
  and haptic confirmation.
- Adds direction-latched two-finger browser back and forward navigation,
  three- and four-finger Windows gestures, and optional three-finger drag.
- Routes touchpad pointer movement and buttons through a virtual HID device so
  they remain available on elevated Windows surfaces and secure confirmation
  prompts.
- Carries ordered physical touch contacts over paired USB or encrypted local
  Wi-Fi sessions with exclusive per-device ownership.
- Adds persistent touchpad preferences and clean session release when the
  Android receiver or Windows application closes.
- Updates the Windows interface, settings flow, tray lifecycle, and
  single-instance behavior for display and touchpad sessions.

The selected FPS is a maximum update rate. A static desktop can report a lower
frame rate because no duplicate frames are generated.

## Requirements

- Windows 11 x64
- Android 11 or later
- A GPU with hardware H.264 encoding support; HEVC requires compatible
  hardware on both Windows and Android
- A data-capable USB connection with Android USB debugging enabled, or both
  endpoints on the same local IPv4 network
- Administrator access for driver installation

A low-contention 5 GHz or 6 GHz connection is recommended.

The current `0.x` line is an alpha release. The setup executable is not yet
Authenticode-signed, the virtual display and input drivers use a development
test certificate, and the bundled Android receiver uses the stable
ScreenBridge release signature.

Source code and technical documentation are available in the
[ScreenBridge repository](https://github.com/danielChinPai/ScreenBridge).
