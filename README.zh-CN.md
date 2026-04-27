<div align="center">
  <img src="docs/assets/logo.png" alt="Bamdra Loom" width="128" />
  <h1>Bamdra Loom · 织梭</h1>
  <p><strong>桌面端多 agent 协作工作台 —— 把"我想做什么"翻译成可以提交的代码。</strong></p>
  <p>
    <a href="https://github.com/bamdra/Loom/releases/latest"><img alt="latest release" src="https://img.shields.io/github/v/release/bamdra/Loom?style=flat-square" /></a>
    <a href="LICENSE"><img alt="license" src="https://img.shields.io/badge/license-MIT-blue?style=flat-square" /></a>
    <a href="https://www.bamdra.com"><img alt="homepage" src="https://img.shields.io/badge/homepage-bamdra.com-2b6cb0?style=flat-square" /></a>
  </p>
  <p>
    <a href="README.md">English</a> · 简体中文
  </p>
</div>

---

Bamdra Loom 是一个桌面端的多 agent 协作工作台。你描述意图，由若干 agent 协作完成分析、设计、实现、评审、收口的整个闭环。它不替你写代码，而是把你从重复的样板劳作里解放出来，让你专注在判断和验收上。

## 为什么是 Loom

主流的 AI 编码工具大多优化"一句话 → 一段补丁"的链路。任务一旦超出单个函数的规模，这种链路就开始失效：

- 一个 agent 同时设计和实现，会自我强化已有假设
- 长上下文随时间衰减，每个会话都在重新解释项目
- 方案、决策、进度散落在聊天历史里，事后没人能回查

Loom 选择了另一种姿态：**把上下文持久化到文件，把角色拆给不同 agent，跑一个有明确验收的闭环。**

```
意图 → 方案 → 任务 → 实现 → 评审 → 收口
```

每一步都写到固定文件（`solution-plan.md`、`INSTRUCTIONS.md`、`STATUS.md`、`ARCH.md`）。明天重新打开项目，任何一个 agent 都能从这些文件里恢复完整上下文。

## 适合谁

- 习惯用自然语言描述需求、再交给 AI 实现的开发者
- 一个人要兼顾多种角色（产品 / 架构 / 实现 / 评审）的全栈工作者
- 想用多 agent 协作完成复杂任务，而不只是单轮问答的团队

## 亮点

- **多 agent 编排** —— 给方案 / 实现 / 评审角色分别绑定不同 agent，它们通过文件协作，不需要互相对话
- **项目上下文持久化** —— `.vibeflow/` 目录里是方案、任务、状态，提交到 git 即可团队共享
- **原生桌面性能** —— 基于 Tauri 2，体积小、响应快
- **自动更新** —— 通过 GitHub Releases 签名更新通道
- **多项目并行** —— 每个项目有独立的 agent 会话和终端

## 安装

到 [Releases](https://github.com/bamdra/Loom/releases/latest) 下载对应平台的安装包：

| 平台 | 安装包 |
|---|---|
| macOS（Apple Silicon） | `Bamdra Loom_<version>_aarch64.dmg` |
| macOS（Intel） | `Bamdra Loom_<version>_x64.dmg` |
| Linux x64 | `bamdra-loom_<version>_amd64.deb` 或 `.AppImage` |
| Windows x64 | `Bamdra Loom_<version>_x64-setup.exe` |

详细的安装说明（含 macOS quarantine 处理）见 [INSTALL.md](INSTALL.md)。

## 快速上手

1. 打开应用，选择一个项目目录
2. 在右侧 agent 面板新建一个会话
3. 在底部意图面板描述这一轮想做的事
4. 让 agent 反问细节，把方案谈清楚
5. 点执行，看 diff，接受或继续修订

项目根会出现 `.vibeflow/` 目录，里面是方案和任务清单。提交到 git，下次打开项目从那里继续。

## 自动更新

应用启动时会检查更新。新版本可用时，TopBar 上会出现一个下载按钮。更新通道是签名的，只有来自本仓库的 release 才能安装。

## License

[MIT](LICENSE) © Bamdra

## 链接

- 主页：<https://www.bamdra.com>
- 发布：<https://github.com/bamdra/Loom/releases>
- 问题反馈：<https://github.com/bamdra/Loom/issues>
