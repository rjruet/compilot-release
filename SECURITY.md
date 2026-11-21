# Security policy

## Reporting a vulnerability

Please do **not** open a public issue for a security problem. Use GitHub's
private vulnerability reporting for this repository:

1. Open the repository's **Security** tab.
2. Choose **Report a vulnerability**.
3. Include the affected version, Windows/Android version, reproduction steps and
   the impact.

If private reporting is unavailable, open a minimal public issue asking for a
private channel; do not include exploit details or personal data.

## Supported versions

Only the newest published release is supported while the project is in preview.
Older preview builds may be removed or superseded.

## Scope

In scope:

- The Windows desktop app and installer.
- The Android IME and APK.
- Release assets and the build/release workflow.

Out of scope:

- Third-party AI endpoints you configure.
- Issues that require a rooted or modified device without a reproducible
  vulnerability in Lekhok.
- Social engineering or physical access.

## Release integrity

Every release includes `SHA256SUMS.txt`. Check it before installing. The release
notes state whether the Windows and Android builds are signed; an unsigned or
debug-signed build is a preview. Do not treat an unsigned build as a stable
release.
