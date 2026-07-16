---
description: Log the current session to your second brain's daily
---

Log what was done in this session to the second brain's daily (vault at `~/2ndBrain`). Extra context: "$ARGUMENTS"

1. Summarize what happened in this conversation/work session (plus anything in "$ARGUMENTS"). If the session lacks clear context, ask what to log.
2. Today's date: `date +%F`. If `~/2ndBrain/60-journal/dailies/<today>.md` doesn't exist, create it with: frontmatter (`type: daily`, `date`), sections "Done", "Meetings", "Decisions & learnings", "Blockers", "Tomorrow".
3. APPEND to the "Done" section — never overwrite what's there. Wikilink projects you recognize in `~/2ndBrain/10-projects/`.
4. **Goals:** open `~/2ndBrain/60-journal/weeks/<week>.md` (`date +%G-W%V`). If the work advances a goal (`- [ ] description — N/M`), increment the counter and mark `[x]` when complete. Report: "PR goal: 2/3".
5. If a relevant decision or learning emerged, add it to `~/2ndBrain/90-memory/decisions.md` or `learnings.md` (`- YYYY-MM-DD — text — context`), most recent on top.
6. Never invent: log only what happened in the session or was stated.
