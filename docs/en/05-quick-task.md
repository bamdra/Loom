# ⚡ Quick Task — fire and forget

Quick Task is for things that don't need a full planning cycle. A small fix, a one-off experiment, a quick tweak — type it, send it, done.

## Opening Quick Task

Two ways:
- Click the **Quick Task** button in the ActionBar (left of the Run button)
- Press `⌘⇧E` (macOS) / `Ctrl+Shift+E` (Windows/Linux)

<!-- screenshot: quick-task-dialog -->

## Writing a task

The dialog opens with a text area. Write what you need in plain language:

> "Add a dark border to all buttons on the settings page."

Press `⌘Enter` (macOS) / `Ctrl+Enter` (Windows/Linux) to submit, or click **Save & Execute**.

What happens:
1. Your task is saved to a local file (`.vibebridge/quick-tasks/tasks.jsonl`)
2. It's sent to the running agent via `/bamdra-vibeflow-run`
3. The agent executes it immediately — no planning phase

## Task history

The bottom of the dialog shows your recent tasks (up to 20):

- Each entry shows the task content, time, and whether it was executed
- Filter with "Show unexecuted only" to find pending tasks
- Click any past task to re-execute it

## Batch execution

Need to run several small tasks at once?

1. Check the boxes next to multiple tasks
2. Click **Execute Selected**
3. They're bundled into a single execution file

## When to use Quick Task vs Intent

| Use | Quick Task | Intent (ActionBar) |
|-----|-----------|-------------------|
| Small standalone change | ✅ | Overkill |
| Needs planning + review | ❌ | ✅ |
| One-off experiment | ✅ | Overkill |
| Multi-step feature | ❌ | ✅ |
| Bug fix you can describe in one line | ✅ | Either works |

**Rule of thumb**: if you can describe it in one sentence and it doesn't touch many files, Quick Task. Otherwise, use Intent so the agents can plan first.
