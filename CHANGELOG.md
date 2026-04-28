# Changelog

All notable changes to Bamdra Loom are documented here.

The format is loosely based on [Keep a Changelog](https://keepachangelog.com/), and this project adheres to semantic versioning where practical.

## v0.41.1 — 2026-04-28

### Changed

- In-app help docs (8 files, zh + en) rewritten end-to-end around the real product positioning: "tell Loom what you want — its AI team builds it; you don't write or read code." Removes prior framing that excluded zero-code users.
- Public README (English + 简体中文) and INSTALL guide rewritten with the same framing; audience defaults to anyone, not just developers.
- Help docs in `docs/zh/` and `docs/en/` are now mirrored from the in-app help by CI on each release (single source of truth).

### Added

- Auto-update failure dialog: if a download fails, the app now pops a clear dialog with retry, open-releases-page, and dismiss actions, plus a collapsible error detail.

## v0.40.0 — 2026-04-28

### Added

- Mermaid diagram support inside the in-app help viewer
- Bilingual (English / 简体中文) public README and INSTALL guide
- Update button promoted to the top bar, sitting to the left of the sync button

### Changed

- Help docs rewritten end-to-end: removed decorative styling, switched workflow descriptions to mermaid, restructured the "writing intent" section as scenario comparisons rather than judgment
- Help viewer styling restyled to a plain prose layout (max 70ch)

### Fixed

- macOS: app no longer reported as "damaged" on first launch (now ad-hoc signed in the bundle stage)

## v0.39.0 — 2026-04-27

Initial public release of the auto-update channel.

### Added

- Auto-update via signed GitHub Releases manifest (`latest.json`)
- Multi-platform CI release pipeline (macOS arm64 / x64, Linux x64, Windows x64)
- Cross-repo publish from internal build repo to this public release repo
