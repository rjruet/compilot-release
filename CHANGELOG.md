# Changelog

## 0.1.1 — preview

- Windows TSF Bengali IME: live Avro phonetic and UniBijoy, Backspace
  recomposition, Space/`?`/Enter commitment, Win+Space switching.
- One Rust core for desktop and Android; duplicate Kotlin predictor removed.
- Profile schema v3, atomic writes, crash isolation, 10k CI + 100k nightly
  conformance, and a 23-case Android golden snapshot.
- LID/code-switch scoring, 20 synthetic domain slices, cold-start/memory probe,
  and a dated competitor scorecard.
- Android instrumented tests on API 26/30/34 phone, tablet, and low-RAM.
- Windows unsigned and Android debug-signed; compatibility remains **Untested**
  for Notepad, Gmail in Chrome, and Microsoft Word.

## 0.1.0 — preview

- First public preview builds for Windows and Android.
- On-device English + Bengali prediction, spelling and high-confidence grammar
  suggestions.
- Opt-in Windows Write-anywhere overlay; all apps start off.
- Android IME with English and Bengali layouts and no `INTERNET` permission.
- No account, ads, telemetry or trial.
- Compatibility status remains **Untested** for Notepad, Gmail in Chrome and
  Microsoft Word; see the release notes.
