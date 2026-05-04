# ⌨️ Keyboard shortcuts

Loom is designed for keyboard-first workflows. Once you learn a few shortcuts, your hands never need to leave the keyboard.

## The philosophy: hands never leave the keyboard

Every core action in Loom — switching between agents, opening sessions, launching tasks, closing views, adjusting settings — has a keyboard shortcut. The goal is to let you go from intent to shipped code without reaching for the mouse.

## Quick reference

### Agents & Sessions

| Action | macOS | Windows / Linux |
|--------|-------|----------------|
| Open Agent 1 session | `⌘1` | `Ctrl+1` |
| Open Agent 2 session | `⌘2` | `Ctrl+2` |
| Open Agent 3 session | `⌘3` | `Ctrl+3` |
| Open Agent 4 session | `⌘4` | `Ctrl+4` |

### Tasks & Actions

| Action | macOS | Windows / Linux |
|--------|-------|----------------|
| Open Quick Task | `⌘⇧E` | `Ctrl+Shift+E` |

### Navigation

| Action | macOS | Windows / Linux |
|--------|-------|----------------|
| Close current view | `⌘W` | `Ctrl+W` |
| Settings | `⌘,` | `Ctrl+,` |
| Toggle terminal | `⌘⇧H` | `Ctrl+Shift+H` |
| Toggle agent settings | `⌘⇧D` | `Ctrl+Shift+D` |
| Quit (double-press) | `⌘Q` | `Ctrl+Q` |

## Tips

- **⌘Q is a double-press**: First press shows a confirmation toast. Press again within 2 seconds to actually quit. This prevents accidental exits.
- **Toggle behavior**: ⌘1-4 and similar shortcuts toggle — if the target is already open, pressing again closes it.
- **Customizable**: All shortcuts can be remapped in `settings.toml` under `[shortcuts]`.

## A keyboard-only workflow

Here's what a complete work session looks like without touching the mouse:

```
⌘⇧E    → Open Quick Task, type what you need, ⌘Enter
⌘1      → Check what the Analysis agent found
⌘2      → Read the Design agent's plan
⌘3      → Watch the Implementation agent work
⌘4      → See the Review verdict
⌘W      → Close the current view when done
⌘,      → Tweak a setting if needed
```
