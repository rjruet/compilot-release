# Release policy

## Channels

- **Preview** — a `-preview` tag or a manual `Release` run with channel
  `preview`. It may be unsigned or debug-signed. Compatibility is not guaranteed.
- **Stable** — a plain `vX.Y.Z` tag or a manual run with channel `stable`. It
  requires Windows Authenticode and Android release-keystore secrets, plus the
  three launch-workflow checks recorded by the source project.

A stable release must not be published while the compatibility matrix still says
**Untested** for the named workflows.

## What every release includes

- Windows NSIS installer and portable ZIP.
- Android APK, plus an AAB when the release keystore is configured.
- `SHA256SUMS.txt`.
- `WINDOWS-SIGNING.txt` and `ANDROID-SIGNING.txt` so the signing state is explicit.
- Release notes with known limitations.

## Signing

- Windows: Authenticode through the private build workflow's certificate.
- Android: a release keystore held only in GitHub Actions secrets.
- Tauri updater signatures are not published yet. Android updates are manual
  because the IME has no `INTERNET` permission.

## Reproducibility and support

- Builds come from the private `rjruet/compilot` repository's GitHub Actions.
- The public repository contains binaries and documentation only; it never
  contains source code or signing keys.
- Security reports use GitHub private vulnerability reporting; see
  [SECURITY.md](SECURITY.md).
