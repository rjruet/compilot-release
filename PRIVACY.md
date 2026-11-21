# Lekhok privacy statement

Lekhok is designed to keep your writing on your own device.

## What stays local

- Keystrokes, predictions, spelling corrections, grammar corrections and the
  learned profile.
- Android voice recognition, if a future build adds it; the current Android IME
  has no voice feature and no `INTERNET` permission.
- The Android keyboard cannot make network calls. It does not declare the
  `INTERNET` permission.

## What can leave the device

Only when you explicitly use an optional AI feature:

- The selected text, or the focused line plus read-only nearby context, is sent
  to the endpoint **you** configure.
- A local Ollama/LM Studio endpoint keeps the request on your computer.
- A cloud endpoint receives the text under that provider's terms.

The Windows app does not contact a model for ordinary typing. Assist AI is a
separate switch and is off by default. The API key is stored in Windows
Credential Manager and is never written to the profile or a URL.

## What we do not collect

- No analytics, telemetry, advertising identifiers or crash uploads.
- No account, licence key, subscription or trial.
- No sale or sharing of typing data.

## Learning data

The desktop profile is a local JSON file under the app's data directory. The
Android profile is local `SharedPreferences` data. A future release may add
encrypted export; until then, no profile is uploaded automatically.

## Updates

- Windows builds may check for updates only if the updater is enabled and
  disclosed in the release notes. An update check sends no typing data.
- Android updates are manual from the public release page.

## Contact

For a privacy question, open an issue in this repository. Do not include
passwords, API keys, private documents or other secrets in a public issue.
