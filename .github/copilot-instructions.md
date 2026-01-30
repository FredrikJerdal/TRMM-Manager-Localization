# Copilot Instructions

## Summary
This repository stores localization resources for Tactical RMM Manager. The primary artifact is a single Xcode string catalog in JSON format.

## High-Level Details
- Project type: Localization-only repo (no app source code).
- Primary language/runtime: JSON string catalog consumed by Xcode.
- Size: Small repo with one main data file and GitHub Actions workflows.
- Target runtime/tooling: Xcode string catalogs (.xcstrings) on macOS.

## Project Layout
- Repo root files:
  - README.md — contributor workflow and translation guidelines.
  - Localization/Localizable.xcstrings — main string catalog.
- GitHub Actions workflows:
  - .github/workflows/validate-xcstrings.yml — Xcode string catalog validation (requires `xcstrings`).
  - .github/workflows/validate-json.yml — JSON syntax validation.
  - .github/workflows/validate-localizations.yml — missing/empty translation and duplicate key checks.

## Build/Validate Instructions
There is no build/test/run step for this repo. Validation is performed via GitHub Actions.

Local validations (macOS):
- JSON syntax check:
  - `python3 -m json.tool "Localization/Localizable.xcstrings" >/dev/null`
- Xcode string catalog validation (requires Xcode with `xcstrings` available):
  - `xcrun xcstrings validate "Localization/Localizable.xcstrings"`

CI validations (GitHub Actions):
- JSON syntax validation: .github/workflows/validate-json.yml
- Missing/empty translations + duplicate key checks: .github/workflows/validate-localizations.yml
- Xcode validation: .github/workflows/validate-xcstrings.yml
  - Note: GitHub-hosted macOS runners currently do not ship `xcstrings`, so this job will fail unless run on a self-hosted macOS runner that includes it.

## Contribution Rules (Non-task-specific)
- Open an issue before contributing so required files can be added.
- Do not translate strings explicitly marked “Do not translate”.
- Preserve placeholders exactly (e.g., `%@`, `%d`, `%lld`).
- Keep capitalization and tone consistent with English.
- Avoid empty translations.
- When making changes, report the number of strings added and which language(s) were added or edited.

## Usage Tips
- Prefer editing only `Localization/Localizable.xcstrings` unless asked otherwise.
- Avoid adding new files unless explicitly required.
- Trust these instructions; only search the repo if information here is missing or incorrect.
