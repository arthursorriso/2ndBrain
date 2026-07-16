---
description: Create or update today's daily note
---

Create or update today's daily note.

1. Get today's date with `date +%F`.
2. If `60-journal/dailies/<today>.md` doesn't exist, create it from `templates/daily.md`.
3. If the user passed content in "$ARGUMENTS", place it in the right sections (done, meetings, decisions, blockers, tomorrow). If not, ask: "What did you do today?" and fill it in from the answer.
4. Cross-reference the vault: if there are meetings from today in `30-meetings/`, link them in the Meetings section. Link mentioned projects with wikilinks.
5. **Weekly goals:** open `60-journal/weeks/<current week>.md` (`date +%G-W%V`). If today's work advances a goal (format `- [ ] description — N/M`), update the counter and mark `[x]` when complete. Report progress: "PR goal: 2/3".
6. If anything said is a relevant decision or learning, also record it in `90-memory/decisions.md` or `90-memory/learnings.md`.
7. Update `90-memory/current-state.md` if the day changed the state of anything.
8. Show the final daily note.
