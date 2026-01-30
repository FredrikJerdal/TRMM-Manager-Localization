# Tactical RMM Manager Localization

Localization resources for Tactical RMM Manager. Use this repo to add or update translations.

## Requirements
- macOS with Xcode installed

## Repository Layout
- `Localization/` — locale files for the app

## Workflow
1) Before contributing, open an issue describing the locale and change so necessary files can be added.
2) Fork and clone the repo on macOS.
3) Open Xcode to ensure the localization tooling is available (no project file needed here).
4) Add or edit locale entries under `Localization/`.
5) Validate formatting (e.g., balanced placeholders, punctuation) before submitting.
6) Commit with a concise message and open a PR.

## Translation Guidelines
- Keep placeholders intact (e.g., `%@`, `%d`).
- Do not translate strings explicitly marked "Do not translate".
- Match capitalization and tone with the source English strings.
- Keep strings concise; avoid truncation in UI.
- For new locales, mirror the existing folder structure inside `Localization/`.

## Support
Open an issue with the locale name and a short description of the change needed.