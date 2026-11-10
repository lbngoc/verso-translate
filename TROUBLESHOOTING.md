# Troubleshooting Verso

Written for **Verso 0.1.0** (macOS 13 or later; Windows 10 or 11, 64-bit).

## The translation service is busy or refuses requests

Verso uses the public Google Translate and Microsoft Translator endpoints, which have no account and no
API key. Under heavy use they can rate-limit or block a network:

- **"The translation service is busy. Try again shortly or change the engine order."** — a temporary rate
  limit (HTTP 429). Wait a minute, or put the other engine first.
- **"The translation service is refusing requests from your network for now. Use another engine or try
  again later."** — the service blocked the network. The other engine usually still works; a VPN or another
  network can help.

Change the order in **Settings › Engines** (tray menu › Settings…): move the working service to the top, or
turn one off. With both on, Verso falls back automatically and tells you which service answered.

## The shortcut does nothing

- Make sure Verso is running: the two-arrow mark is in the menu bar or the notification area.
- The combination may belong to another app. Change it in **Settings › Shortcuts**; a conflict is reported
  when you save.
- On macOS, translating the selected text needs the **Accessibility** permission: **System Settings ›
  Privacy & Security › Accessibility** must list Verso and have it switched on. After replacing
  `Verso.app` with a new build, macOS may keep the old entry switched on while the new build is not
  trusted: remove the entry with minus, add the new app with plus, and switch it on.
- The quick panel (`Alt+Shift+Cmd+T` on macOS, `Ctrl+Alt+Shift+T` on Windows) works without Accessibility;
  use it to check the engines while the selection path is being fixed.

## Nothing is captured, or the popup says no text was selected

- Some apps (password fields, secure input) never expose their selection. Use the quick panel there.
- Select the text first, then press the shortcut; Verso reads the current selection at that moment.
- If macOS shows the Accessibility entry switched on but Verso still reports it as missing, remove and
  re-add Verso as described above.

## Where the logs are

- macOS: `~/Library/Logs/app.versotranslate/verso.log`
- Windows: `%LOCALAPPDATA%\app.versotranslate\logs\verso.log`

Settings live in `~/Library/Application Support/app.versotranslate/settings.json` (macOS) and
`%APPDATA%\app.versotranslate\settings.json` (Windows). At the default level the logs hold engine ids,
counts and error kinds, not the translated text.

## Reporting a problem

Open an issue on this repository with:

- the Verso version (tray menu › About Verso, or **Settings › About**) and the OS version;
- what you did, what you expected and what happened;
- the last lines of the log around the failure (remove anything personal first).

Security problems go through [SECURITY.md](SECURITY.md), not a public issue.
