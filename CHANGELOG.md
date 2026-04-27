# Changelog

All notable changes to Bamdra Loom are documented here.

The format is loosely based on [Keep a Changelog](https://keepachangelog.com/), and this project adheres to semantic versioning where practical.

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
