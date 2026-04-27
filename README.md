<div align="center">
  <img src="docs/assets/logo.png" alt="Bamdra Loom" width="128" />
  <h1>Bamdra Loom</h1>
  <p><strong>Desktop AI orchestration workspace — turn intent into shipped code via multi-agent collaboration.</strong></p>
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

Bamdra Loom is a desktop workspace for **multi-agent collaboration on real codebases**. You describe intent; a team of agents handles analysis, design, implementation, review, and wrap-up in a verifiable loop. It does not replace you — it removes the boilerplate so you stay focused on judgment and acceptance.

## Why Loom

Most AI coding tools optimize for one-shot prompt → patch. That breaks down on tasks bigger than a single function:

- One agent both designs and implements, reinforcing its own assumptions
- Long contexts decay; you re-explain the project each session
- Plans, decisions, and progress live in chat history that nobody can audit later

Loom takes a different stance: **persist context to files, split roles across agents, and run a closed loop with explicit acceptance.**

```
intent → plan → tasks → implement → review → wrap up
```

Each step writes to a known file (`solution-plan.md`, `INSTRUCTIONS.md`, `STATUS.md`, `ARCH.md`). Reopen the project tomorrow and any agent can recover full context from those files.

## Who it's for

- Developers who already describe requirements in natural language and let AI implement
- Solo builders juggling product, architecture, implementation, and review on their own
- Teams that want multiple agents collaborating on hard tasks, not just isolated Q&A

## Highlights

- **Multi-agent orchestration** — bind different agents to plan / implement / review roles; they collaborate via files, not chat
- **Persistent project context** — `.vibeflow/` directory captures plan, tasks, status; commit it to share state with your team
- **Native desktop performance** — built on Tauri 2; the binary is small and the UI feels native
- **Auto-update** — signed update channel via GitHub Releases
- **Multi-project tabs** — each project has its own isolated agent session and PTY

## Install

Download the installer for your platform from [Releases](https://github.com/bamdra/Loom/releases/latest):

| Platform | File |
|---|---|
| macOS (Apple Silicon) | `Bamdra Loom_<version>_aarch64.dmg` |
| macOS (Intel) | `Bamdra Loom_<version>_x64.dmg` |
| Linux x64 | `bamdra-loom_<version>_amd64.deb` or `.AppImage` |
| Windows x64 | `Bamdra Loom_<version>_x64-setup.exe` |

Detailed install notes (including macOS quarantine handling) live in [INSTALL.md](INSTALL.md).

## Quickstart

1. Open the app and pick a project directory
2. Start a new session in the agent panel on the right
3. Describe what you want this round in the intent panel
4. Let the agent ask follow-up questions, settle the plan
5. Hit run, review the diff, accept or push back

A `.vibeflow/` directory appears at the project root with the plan and task list. Commit it; next time you reopen the project, work continues from there.

## Updates

The app checks for updates at startup. When one is available, a download button appears in the top bar. The update channel is signed — only releases from this repository can install.

## License

[MIT](LICENSE) © Bamdra

## Links

- Homepage: <https://www.bamdra.com>
- Releases: <https://github.com/bamdra/Loom/releases>
- Issues: <https://github.com/bamdra/Loom/issues>
