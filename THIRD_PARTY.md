# Third-Party Notices

Verso bundles or ports code from the following projects. The licenses below are the ones
declared by each upstream project at the time of porting (2026-11).

## translate-shell (Unlicense)

- Upstream: <https://github.com/soimort/translate-shell>
- Ported logic: `include/Translators/GoogleTranslate.awk` (gtx request shape, response parsing),
  `include/Translators/BingTranslator.awk` (session bootstrap, `ttranslatev3` request),
  `include/LanguageData.awk` (locale table, converted to `src-tauri/resources/languages.json`).
- The ports are Rust re-implementations; no AWK code is executed at runtime.
- License: Unlicense (public domain). <https://unlicense.org/>

## tauri-nspanel

- Upstream: <https://github.com/ahkohd/tauri-nspanel>
- Used (when the pinned build is enabled) to convert the popup and quick windows to
  non-activating `NSPanel`s on macOS.
- License: MIT.

## tauri-plugin-liquid-glass

- Upstream: <https://github.com/cloudflyer-project/tauri-plugin-liquid-glass>
- Evaluated for the macOS 26 Liquid Glass surface. If adopted, the plugin is used as-is.
- License: MIT.

## Fluent UI System Icons

- Upstream: <https://github.com/microsoft/fluentui-system-icons>
- Windows icon set used by the Fluent stylesheet (`src/lib/icons/`).
- License: MIT.

## whatlang

- Upstream: <https://github.com/greyblake/whatlang-rs>
- Local language detection (`whatlang` crate).
- License: MIT.

## tts

- Upstream: <https://github.com/ndarilek/tts-rs>
- Text-to-speech on macOS (AVSpeechSynthesizer) and Windows (WinRT SpeechSynthesizer).
- License: MIT.

## screenTranslate

- Upstream: <https://github.com/nobiyou/screenTranslate>
- Clean-room reference only: the selection-capture (`TextGrabber`) and pasteboard snapshot
  (`PasteboardSnapshot`) behaviour was studied and re-implemented; no code is copied.
