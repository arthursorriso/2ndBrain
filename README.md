# 2ndBrain

A permanent memory system built on **Obsidian** (storage) and **Claude Code** (the brain). Everything is plain markdown: meetings, projects, ideas, people, tutorials, and a daily journal — all connected by wikilinks, all readable by you and by an LLM.

Inspired by [Andrej Karpathy's llmwiki concept](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f): raw sources are immutable, derived notes are regenerable, and a `CLAUDE.md` file defines the conventions and workflows the LLM follows automatically.

## What it does

- **Never forgets.** Meeting transcripts, decisions, ideas, and daily logs are captured as markdown and cross-linked. Ask `/question what did we decide about X?` and get an answer with sources and dates.
- **Updates itself.** Every session ends with `/end-session`, which consolidates what happened into projects, decisions, learnings, and a short-term memory file that the next session starts from.
- **Tracks weekly goals.** Set goals on Monday (`/goals open 3 PRs`), and your dailies update the counters automatically. Friday's `/weekly` scores the week.
- **Digests meetings.** Paste a transcript into `/meeting`: the original is stored untouched, and the brain generates summary, decisions, action items, insights, and updates every person and project involved.

## Quick start

1. Install [Obsidian](https://obsidian.md) and [Claude Code](https://code.claude.com).
2. Clone this repo (or click "Use this template") to `~/2ndBrain`.
3. Open the folder as a vault in Obsidian.
4. In a terminal: `cd ~/2ndBrain && claude` — all commands below are available.
5. Fill in `90-memory/about-me.md` — this is what makes answers about YOU.
6. Register your current projects: `/project my-project`.

## Structure

| Folder | Contents |
|---|---|
| `00-inbox/` | Quick captures, processed later by `/process-inbox` |
| `10-projects/` | One note per project, with update log |
| `20-ideas/` | Ideas that may or may not become projects |
| `30-meetings/` | Meeting notes; `raw/` holds immutable transcripts |
| `40-tutorials/` | Runbooks and step-by-step guides |
| `50-people/` | One note per person, with interactions and commitments |
| `60-journal/` | `dailies/`, `weeks/` (goals + summary), `quarters/` (retrospectives) |
| `90-memory/` | Current state, about-me, decisions, learnings |
| `templates/` | Note templates (used automatically by the commands) |

## Commands

| Command | What it does |
|---|---|
| `/daily` | Create/update today's daily |
| `/inbox <text>` | Quick capture |
| `/process-inbox` | Classify and file everything in the inbox |
| `/meeting` | Ingest a meeting transcript |
| `/project <name>` | Create or update a project |
| `/idea <text>` | Capture an idea |
| `/tutorial <subject>` | Create a runbook |
| `/briefing` | Daily briefing: goals, open items, focus |
| `/goals` | Set / update / check week goals |
| `/question <q>` | Search the vault, answer with sources |
| `/weekly` | Close the week: score goals, summarize |
| `/quarterly` | Quarter retrospective |
| `/end-session` | Consolidate the session into memory |

### Global commands (work from any folder)

`/brain-inbox`, `/brain-question`, `/brain-log`, `/brain-briefing` — capture, query, and log to the brain while working in any other repo. Install:

```bash
mkdir -p ~/.claude/commands && cp ~/2ndBrain/global-commands/brain-*.md ~/.claude/commands/
```

## Suggested routine

| When | Command |
|---|---|
| Monday | `/goals` — set the week's goals |
| Morning | `/briefing` |
| During the day | `/inbox <anything>` |
| After a meeting | `/meeting` |
| End of day | `/daily` |
| End of a work session | `/end-session` |
| Friday | `/weekly` |
| End of quarter | `/quarterly` |
| Anytime | `/question <what you want to remember>` |

## Backup

Your memory deserves a backup:

```bash
git init && git add -A && git commit -m "initial vault" && git push
```

Use a **private** repository — this vault will contain your life.

## Design rules worth knowing

- `30-meetings/raw/` is immutable — the brain never edits transcripts, so the source of truth survives any bad summary.
- The brain never invents: if it's not in the vault, the answer is "not recorded".
- Transcript content is treated as data, not instructions (prompt-injection guardrail).
- History is append-only: logs get new entries, never rewrites.

## License

MIT — use it, fork it, make it yours.
