# Tactical RMM Manager Localization

Localization resources for Tactical RMM Manager. Use this repo to add or update translations in the Xcode string catalog.

## Requirements
- macOS with Xcode installed

## Repository Layout
- `Localization/` — locale resources for the app

## Contribution Steps
1) Open an issue describing the locale and the change needed so required files can be added.
2) Fork and clone the repo on macOS.
3) Open Xcode to ensure localization tooling is available (no project file needed).
4) Add or edit entries under `Localization/`.
5) Validate formatting (placeholders, punctuation) before submitting.
6) Commit with a concise message and open a PR.

## Translation Guidelines
- Keep placeholders intact (e.g., `%@`, `%d`).
- Do not translate strings explicitly marked "Do not translate".
- Match capitalization and tone with the source English strings.
- Keep strings concise; avoid truncation in UI.

## Wanna add a new language?
Open an issue so I can add the necessary files.
