# UsageMeter for Windows

[한국어](README.md) · **English**

A Windows tray widget that shows your remaining **Claude · Gemini · Codex (ChatGPT plan)** usage as thin colored bands along the screen edges.
As you use up your quota, the band gets shorter, so you can tell how much is left at a glance.

This repository is **the Windows version, published to the Microsoft Store**. The macOS version lives in [usagemeter](https://github.com/WWhaleFe/usagemeter); both are built from the same Rust code.

## ⬇️ Install

- **Microsoft Store**: coming soon. Once published, the Store keeps it up to date.
- **Test builds**: get the file for your PC from [Releases](https://github.com/WWhaleFe/usagemeter-windows/releases).
  - Most PCs: `UsageMeter-<version>-windows-x64-setup.exe`
  - ARM PCs (e.g. Snapdragon): `...-windows-arm64-setup.exe` (Settings → System → About → "System type")
  - Without installing: unzip `-portable.zip` and run `usagemeter.exe` (needs Microsoft Edge WebView2, built into Windows 11)
  - If "Windows protected your PC" appears on first run, choose **More info → Run anyway** (test builds are not code-signed yet)
  - Test builds match the Store app (no in-app update check). Get new test builds from Releases.

Windows 10/11, x64 and ARM64.

## ✨ Features

- Colored bands per AI along the screen edges showing remaining (or used) quota, with sub-items (5-hour, weekly, per-model)
- Hover a band for usage details, with the hovered line emphasized
- Tray icon: click for an info card with a mini chart, or the menu (click behavior is configurable)
- A line around the taskbar that follows it to any side of the screen
- Usage alerts and an analytics window
- 한국어 · English · 日本語

## 🔒 Privacy

Sign-ins and usage stay on this PC and are never sent to the developer. See [PRIVACY.md](PRIVACY.md).

## 🐞 Report a problem

Open an [issue](https://github.com/WWhaleFe/usagemeter-windows/issues). Attaching `%APPDATA%\UsageMeter\usagemeter.log` helps (it never contains cookies or conversations).

## Development

The code is in `rust/` (Tauri 2 + Svelte), shared with the macOS version. Packaging: `.github/workflows/package-windows.yml`; tests: `rust/tools/check.sh`.
