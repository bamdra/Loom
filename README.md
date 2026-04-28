<div align="center">
  <img src="docs/assets/logo.png" alt="Bamdra Loom" width="128" />
  <h1>Bamdra Loom</h1>
  <p><strong>Tell Loom what you want — its AI team builds it. You don't need to write or read any code.</strong></p>
  <p>
    <a href="https://github.com/bamdra/Loom/releases/latest"><img alt="latest release" src="https://img.shields.io/github/v/release/bamdra/Loom?style=flat-square" /></a>
    <a href="LICENSE"><img alt="license" src="https://img.shields.io/badge/license-MIT-blue?style=flat-square" /></a>
    <a href="https://www.bamdra.com"><img alt="homepage" src="https://img.shields.io/badge/homepage-bamdra.com-2b6cb0?style=flat-square" /></a>
  </p>
  <p>
    English · <a href="README.zh-CN.md">简体中文</a>
  </p>
</div>

---

Bamdra Loom isn't a code editor or a chatbot. It's **a small AI team that lives in your computer**: you describe what you want; they argue about how to do it, write the code, review each other's work, and hand you the result. You never need to open code or learn jargon — you only **say what you want** and **say yes or no**.

## What it does for you

### 🔬 Researchers and analysts

A folder full of PDFs, web clippings, raw spreadsheets — turn them into searchable little tools, dashboards, or topic-filtered web pages. Just say what shape you want; the agents wire it up.

### 🚀 People who want to build software but don't write code

That product idea you've been carrying around — a tool, a small game, a personal site, an app for friends — describe it in plain words. The agents ask back, decide on an approach, build it, run it, and hand you something you can open.

### 🛠️ Developers who want to stop hand-holding

Already shipping with AI? Drop the prompt-juggling. Say one sentence; the team runs the full *analyze → plan → implement → review* loop on its own. You only look at the result. Step in whenever you want.

## Built by itself

Loom itself was built this way. The author started from one sentence — *"I want a local desktop client for orchestrating multiple AI agents"* — opened nothing but Loom, never wrote or read a line of generated code, and shipped this very app you're holding.

## Why it works

Most AI coding tools optimize for *one prompt → one patch*. That breaks down on anything bigger than a single function. Loom takes a different stance:

- **Multiple agents, distinct roles** — one drafts, another critiques, another implements. They keep each other honest.
- **Persistent context to files** — plans, task lists, progress all land in `.vibeflow/`. Reopen the project tomorrow; any agent recovers the full picture.
- **A real loop with acceptance** — `intent → plan → tasks → implement → review → wrap up`, with you standing at the start and the end.

## Install

Download the installer for your platform from [Releases](https://github.com/bamdra/Loom/releases/latest):

| Platform | File |
|---|---|
| macOS (Apple Silicon) | `Bamdra Loom_<version>_aarch64.dmg` |
| macOS (Intel) | `Bamdra Loom_<version>_x64.dmg` |
| Linux x64 | `bamdra-loom_<version>_amd64.deb` or `.AppImage` |
| Windows x64 | `Bamdra Loom_<version>_x64-setup.exe` |

Detailed install notes (including macOS quarantine handling) live in [INSTALL.md](INSTALL.md).

## After you install

1. Open the app and pick a project directory (an empty one works fine)
2. Type a sentence in the box at the bottom: *"I want X."*
3. Look at the plan it shows you — accept or push back
4. Watch it work; or come back when it's done
5. Open the result; ask for tweaks if you want

The full walkthrough lives in [docs/en/01-quickstart.md](docs/en/01-quickstart.md).

## Updates

The app checks for updates at startup. When one is available, a download button appears in the top bar. The update channel is signed — only releases from this repository can install. If a download fails, a dialog will offer to retry or open the releases page directly.

## License

[MIT](LICENSE) © Bamdra

## Links

- Homepage: <https://www.bamdra.com>
- Releases: <https://github.com/bamdra/Loom/releases>
- Issues: <https://github.com/bamdra/Loom/issues>
