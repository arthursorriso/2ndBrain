# Global commands

These commands work in ANY folder where you run Claude Code (not just the vault).

## Install

```bash
mkdir -p ~/.claude/commands && cp ~/2ndBrain/global-commands/brain-*.md ~/.claude/commands/
```

> If your vault lives somewhere other than `~/2ndBrain`, replace the path inside each `brain-*.md` before copying.

## Commands

| Command | What it does |
|---|---|
| `/brain-inbox <text>` | Quick capture to the brain's inbox |
| `/brain-question <question>` | Query the brain's memory (read-only) |
| `/brain-log` | Log the current session to the daily (and update goals) |
| `/brain-briefing` | Daily briefing: goals, open items, focus |

The originals stay versioned here in `global-commands/`. If you edit anything, run the `cp` again to reinstall.
