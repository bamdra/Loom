# ⚙️ 设置与配置

## Agent 配置

每个 agent 定义在项目中的 `.vibebridge/agents.toml`。你可以配置：

- **Provider**：用哪个 AI 服务（`claude`、`codex`、`gemini`）
- **Model**：具体模型（如 `claude --model opus`）
- **System prompt**：塑造 agent 行为的指令
- **Auto-start**：打开项目时是否自动启动

通过界面操作：点击齿轮图标 → **Agents** 标签页。

## 分域 Agent 提示词

每个角色 —— 分析、设计、实现、审核 —— 在 **Product** 模式和 **Dev** 模式有不同的系统提示词，影响 agent 思考方式。

Loom 自带合理的默认值。你可以自定义让 agent 遵循团队规范或聚焦特定事项。

**在哪里找**：设置（齿轮图标）→ **Agents** → 点击角色卡片 → 切换 **Product** / **Dev** 标签。

**重置**：点击重置按钮恢复默认。

**什么时候自定义**：
- 团队有自己的代码风格
- 用特定框架，希望 agent 不越界
- 希望审核 agent 用你自己的评分标准

配置保存在项目的 `.vibeflow/orchestration.yaml` 中，不同项目可以不同。

## 主题

三种主题：**Bamdra**（默认深色）、**Dark**、**Light**。在顶栏或设置中切换。

## 语言

顶栏的语言按钮切换中英文，跨会话记住。

## 布局

三个面板可以拖动边缘调整大小：

- **左侧边栏**（文件树）：140–480px
- **右侧面板**（agent）：180–480px
- **底部面板**（终端）：80–600px

布局偏好保存在 `localStorage`，下次启动恢复。

## 快捷键自定义

所有快捷键可重新映射。编辑 `settings.toml` 的 `[shortcuts]` 段：

```toml
[shortcuts]
open_agent_1 = "Meta+1"
open_quick_task = "Meta+Shift+E"
```

修改后自动重新注册。完整列表见[快捷键指南](06-shortcuts.md)。
