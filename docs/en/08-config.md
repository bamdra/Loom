# ⚙️ Settings and configuration

## Agent configuration

Each agent is defined in `.vibebridge/agents.toml` in your project. You can configure:

- **Provider**: which AI service to use (`claude`, `codex`, `gemini`)
- **Model**: specific model variant (e.g., `claude --model opus`)
- **System prompt**: instructions that shape the agent's behavior
- **Auto-start**: whether the agent starts when you open the project

You can edit agent settings through the UI: click the gear icon → **Agents** tab.

## Agent prompts per domain

Each agent role — Analysis, Design, Implement, Review — has a separate system prompt for **Product** mode and **Dev** mode. These prompts shape how each agent thinks about its job.

Loom ships with defaults that work well out of the box. You can customize them if you want agents to follow your team's conventions or focus on specific things.

**Where to find them:** Settings (gear icon) → **Agents** tab → click any role card → switch between **Product** and **Dev** tabs inside the card.

**Reset:** Hit the reset button on any role to restore the built-in default for that domain.

**When to customize:**
- Your team has a house style you want agents to follow
- You're using a specific framework and want agents to stay within it
- You want the Review agent to apply your own rubric

Changes are saved per-project in `.vibeflow/orchestration.yaml`.

## Themes

Loom supports three themes: **Bamdra** (default dark), **Dark**, and **Light**. Switch in the top bar or Settings.

## Language

Toggle between English and Chinese (简体中文) with the language button in the top bar. The setting is remembered across sessions.

## Layout

Three panels can be resized by dragging their edges:

- **Left sidebar** (file tree): 140–480px
- **Right panel** (agents): 180–480px
- **Bottom panel** (terminal): 80–600px

Your layout preferences are saved in `localStorage` and restored on next launch.

## Keyboard shortcut customization

All keyboard shortcuts can be remapped. Edit `settings.toml` under the `[shortcuts]` section:

```toml
[shortcuts]
open_agent_1 = "Meta+1"
open_quick_task = "Meta+Shift+E"
```

After changing, the shortcuts are re-registered automatically. See the [Shortcuts guide](06-shortcuts.md) for the full list of available actions.
