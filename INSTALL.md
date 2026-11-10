# Installing Verso

Written for **Verso 0.1.0** (macOS 13 or later; Windows 10 or 11, 64-bit). The builds in this release are
not code-signed, so both systems ask for one confirmation on the first launch; the steps below cover it.

Take the installer from the [latest release](../../releases/latest) page. The file names carry the version:

| System | File |
|---|---|
| macOS, Apple Silicon (M1 and later) | `Verso_0.1.0_aarch64.dmg` |
| macOS, Intel | `Verso_0.1.0_x64.dmg` |
| Windows, 64-bit | `Verso_0.1.0_x64-setup.exe` |

## Verify the download (recommended)

Each release lists the SHA-256 of every file in `SHA256SUMS.txt`.

macOS:

```sh
shasum -a 256 Verso_0.1.0_aarch64.dmg
```

Windows (PowerShell):

```powershell
Get-FileHash .\Verso_0.1.0_x64-setup.exe -Algorithm SHA256
```

The value must match the line for that file in `SHA256SUMS.txt`. If it does not, download the file again
from the release page.

## macOS

1. Open the `.dmg` and drag **Verso** into `Applications`.
2. The first launch is blocked by Gatekeeper because the build is not notarized. Either right-click (or
   Control-click) `Verso` in `Applications` and choose **Open**, then **Open** again in the dialog, or open
   **System Settings › Privacy & Security**, click **Open Anyway** next to the message about Verso, confirm
   with an administrator's password, then **Open Anyway** again in the confirmation. The alert reads
   "Apple could not verify 'Verso' is free of malware"; this is expected for an unsigned build.
3. Verso asks for the **Accessibility** permission the first time it needs to read a selection. Grant it in
   **System Settings › Privacy & Security › Accessibility** (switch Verso on; the first time, confirm with
   your password). Without it, translating a selection cannot read the text; the quick panel still works.
4. Start Verso. The mark (two arrows) appears in the menu bar. Select some text in another app and press
   `Alt+Shift+T`; the result appears next to the selection. `Alt+Shift+Cmd+T` opens the quick panel.

Verso starts with the system at login only if **Launch at login** is enabled in Settings.

## Windows

1. Run `Verso_0.1.0_x64-setup.exe`.
2. Windows SmartScreen shows "Windows protected your PC" because the build is unsigned. Choose **More
   info**, then **Run anyway**. The installer needs no administrator rights and installs for the current
   user.
3. Start **Verso** from the Start menu. The mark (two arrows) appears in the notification area; if it is
   hidden, open the overflow arrow next to the clock.
4. Select some text in another app and press `Alt+Shift+T`; the result appears next to the selection.
   `Ctrl+Alt+Shift+T` opens the quick panel.

To remove Verso, use **Settings › Apps › Installed apps › Verso › Uninstall** (or `uninstall.exe` in
`%LOCALAPPDATA%\Verso`).

## First use

The first launch shows a two-step introduction: choose which services may receive your text (Google and
Microsoft are both on by default; at least one must stay on), then pick the target language. Both can be
changed later in **Settings** from the tray menu.

Shortcuts can be changed in **Settings › Shortcuts**. On macOS, a global shortcut needs no permission
beyond Accessibility; if another app already owns the combination, Verso says so and asks for another.

## Where your data lives

- macOS settings: `~/Library/Application Support/app.versotranslate/settings.json`; logs:
  `~/Library/Logs/app.versotranslate/verso.log`.
- Windows settings: `%APPDATA%\app.versotranslate\settings.json`; logs:
  `%LOCALAPPDATA%\app.versotranslate\logs\verso.log`.

Nothing is stored off the device. See [PRIVACY.md](PRIVACY.md).
