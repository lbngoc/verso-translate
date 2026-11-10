# Verso Translate

Verso is a small translator that lives in the menu bar (macOS) or the notification area (Windows). Select
text in any app and press `Alt+Shift+T`: Verso translates it and shows the result in a popup that can copy
or speak it. Text you type yourself goes through the quick panel.

- **Engines**: Google Translate and Microsoft Translator (Bing), no account or API key needed, with
  automatic fallback when one fails.
- **Automatic source language**, dozens of target languages, English or Vietnamese interface.
- **Light and dark themes**; the tray mark follows the system.
- **No telemetry** and no account. See [PRIVACY.md](PRIVACY.md).

## Download

The latest installers are on this repository's [Releases](../../releases/latest) page:

| System | File |
|---|---|
| macOS 13 or later, Apple Silicon | `Verso_<version>_aarch64.dmg` |
| macOS 13 or later, Intel | `Verso_<version>_x64.dmg` |
| Windows 10 or 11, 64-bit | `Verso_<version>_x64-setup.exe` |

Every release also publishes `SHA256SUMS.txt` with the SHA-256 of each file. Start with
[INSTALL.md](INSTALL.md), which covers the first-launch warning on unsigned builds.

## Documentation

- [INSTALL.md](INSTALL.md) — install on macOS and Windows, checksums, permissions
- [TROUBLESHOOTING.md](TROUBLESHOOTING.md) — blocked engines, shortcuts, logs
- [PRIVACY.md](PRIVACY.md) — which engine receives your text
- [TERMS.md](TERMS.md) — terms for the binaries
- [CHANGELOG.md](CHANGELOG.md) — what each release contains
- [THIRD_PARTY.md](THIRD_PARTY.md) — third-party notices
- [SECURITY.md](SECURITY.md) — reporting a problem privately

## Screenshots

Screenshots of the popup, the quick panel and the Settings window will be added after the first public
release.

## Project status

This repository holds the published documents and the release downloads. The source code is not open yet,
so pull requests are disabled; issues are enabled for bug reports and questions. The terms that apply to
the binaries are in [TERMS.md](TERMS.md).
