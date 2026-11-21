# Lekhok (লেখক) — public builds

Lekhok is a free, on-device **Bengali + English predictive writing tool** for
Windows and Android. It predicts words and phrases, fixes typos and common
grammar slips, and learns your recurring phrasing on your own machine. There is
no account, no telemetry and no advertising. Optional AI actions use your own
endpoint and are off by default.

This repository is the **public download and support surface only**. The source
repository is private. Builds are produced by GitHub Actions and attached to
[Releases](https://github.com/rjruet/compilot-release/releases).

## Download

Open [Releases](https://github.com/rjruet/compilot-release/releases) and choose
the newest build. Preview builds are marked **Pre-release**; only a signed build
that has passed the compatibility gate is stable.

- **Windows 11 x64** — `Lekhok_<version>_x64-setup.exe` (NSIS installer) or
  `Lekhok_<version>_x64-portable.zip`.
- **Android 8+** — `Lekhok_<version>_android.apk`, or
  `Lekhok_<version>_android-debug.apk` for an unsigned preview.

Every release includes `SHA256SUMS.txt`. Verify a download before installing:

```powershell
Get-FileHash .\Lekhok_0.1.0_x64-setup.exe -Algorithm SHA256
```

## Install

### Windows

1. Run the installer.
2. Windows SmartScreen may warn until the installer is signed and has reputation.
3. Open **Lekhok**. Write anywhere is **off by default**; enable it in
   **Settings -> Write anywhere**, then enable only the apps you have checked on
   your PC.

### Android

1. Download the APK and allow installation from your browser or file manager.
2. Open **Lekhok** and follow the setup steps.
3. Enable **Lekhok Keyboard** in system settings and select it as the current
   keyboard.
4. Switch বাংলা/EN from the bottom row.

## Status

This is an early public preview. **No Windows launch workflow is Verified yet.**
Notepad, Gmail in Chrome and Microsoft Word still need the manual compatibility
checks recorded in the source project. Do not assume system-wide support.

Known limitations:

- Direct Bengali input at the caret in other Windows apps is not implemented.
  External apps type Latin first and can replace a finished word with Bengali;
  that is transliteration, not a key-level UniBijoy/Avro keyboard.
- Chrome is app-level only. Gmail site scoping (`mail.google.com` + compose body)
  is not implemented.
- No snippets, clipboard history, styles, insights, profile backup/export, or
  read-aloud yet.
- Android includes no `INTERNET` permission, so updates are manual.

## Privacy

Typing, learning, prediction and Android voice recognition are local. There is no
telemetry, account or ads. The Windows app contacts a model only when you run an
explicit AI action or opt into assist AI. The Android IME cannot make network
calls. Read [PRIVACY.md](PRIVACY.md).

## Support

Use [Issues](https://github.com/rjruet/compilot-release/issues) for installation
questions and bug reports. For security reports, follow [SECURITY.md](SECURITY.md).
Release changes are recorded in [CHANGELOG.md](CHANGELOG.md).

## License

The binaries are free to download and use. The source code is not distributed.
See [LICENSE](LICENSE).
