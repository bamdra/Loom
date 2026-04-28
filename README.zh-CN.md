<div align="center">
  <img src="docs/assets/logo.png" alt="Bamdra Loom" width="128" />
  <h1>Bamdra Loom · 织梭</h1>
  <p><strong>你说想做什么，它带着 AI 团队把它做出来 —— 你不需要会写代码、也不需要看代码。</strong></p>
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

Bamdra Loom 不是代码编辑器，也不是问答助手。它更像**你雇了一个小型 AI 团队，住在你电脑里**：你描述想做什么，他们之间分工讨论方案、写代码、互相评审、最后把成果跑给你看。整个过程你不用打开任何代码、不用懂任何技术名词——只做两件事：**说你想要什么** 和 **拍板要不要**。

## 它能帮谁做什么

### 🔬 做研究的人

一堆 PDF、网页剪藏、调研笔记、原始 Excel——把它们做成一个能搜索、能交叉引用的小工具，或一个按主题筛选的图表网页。你只描述想要的样子，agent 把它做出来。

### 🚀 不会写代码、想做软件的人

你脑子里那个产品——一个工具、一个小游戏、一个个人网站、一个能给朋友用的小应用——用大白话描述出来。agent 反问细节、自己拆解、自己实现、自己跑通，最后给你一个能在浏览器或本地打开的产物。

### 🛠️ 会写代码但想提效的开发者

已经在用 AI 写代码？把那些喂提示词、切换上下文、手工 review 的繁活交出去。你说一句意图，agent 团队内部跑"分析 → 方案 → 实现 → 评审"的闭环，你只看成果，需要介入时随时介入。

## Loom 自己就是这么诞生的

作者从一句"我想做一个本地多 agent 桌面客户端"开始，全程没有打开过编辑器、没有看过一行生成的代码，一个版本一个版本迭代到了你现在用的这个 Loom。

## 为什么这样行

主流的 AI 编码工具大多优化"一句话 → 一段补丁"的链路。任务一旦超出单个函数的规模，这种链路就开始失效。Loom 选择了另一种姿态：

- **多个 agent，不同角色** —— 一个出方案、一个挑刺、一个实现，互相牵制
- **上下文持久化到文件** —— 方案、任务、进度都落在 `.vibeflow/` 里，明天重新打开项目，任何 agent 都能从这些文件恢复完整上下文
- **真正的闭环** —— `意图 → 方案 → 任务 → 实现 → 评审 → 收口`，你只在起点和终点出现

## 安装

到 [Releases](https://github.com/bamdra/Loom/releases/latest) 下载对应平台的安装包：

| 平台 | 安装包 |
|---|---|
| macOS（Apple Silicon） | `Bamdra Loom_<version>_aarch64.dmg` |
| macOS（Intel） | `Bamdra Loom_<version>_x64.dmg` |
| Linux x64 | `bamdra-loom_<version>_amd64.deb` 或 `.AppImage` |
| Windows x64 | `Bamdra Loom_<version>_x64-setup.exe` |

详细的安装说明（含 macOS quarantine 处理）见 [INSTALL.md](INSTALL.md)。

## 装好之后

1. 打开应用，选择一个目录（空目录也可以）
2. 在底部输入框写一句话："我想做 xxx"
3. 看屏幕上出现的方案，是想要的就同意，不是就告诉它偏哪边
4. 看它自己干，或者去倒杯咖啡
5. 看成果，要改就告诉它改哪里

完整的上手剧情在 [docs/zh/01-quickstart.md](docs/zh/01-quickstart.md)。

## 自动更新

应用启动时会检查更新。新版本可用时，TopBar 上会出现一个下载按钮。更新通道是签名的，只有来自本仓库的 release 才能安装。如果自动下载失败，会弹窗提示你——可以重试，也可以直接到 releases 页手动下载。

## 发布通道

两档通道，通过 tag 形态区分：

| 通道 | tag 形态 | 自动更新 |
|---|---|---|
| **Stable** | `vX.Y.Z` | ✅ 推送给所有用户 |
| **Beta** | `vX.Y.Z-beta.N` | ❌ 仅手动下载 |

Stable 用户不会收到 beta 推送 —— GitHub 的 "latest" 自动忽略 prerelease，而 beta 构建也不会上传 updater manifest。想试 beta 直接到 [releases 页](https://github.com/bamdra/Loom/releases) 手动下载安装包。

完整规范见 [RELEASE.md](RELEASE.md)。

## License

[MIT](LICENSE) © Bamdra

## 链接

- 主页：<https://www.bamdra.com>
- Releases：<https://github.com/bamdra/Loom/releases>
- Issues：<https://github.com/bamdra/Loom/issues>
