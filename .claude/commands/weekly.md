---
description: Close the week — evaluate goals and build the summary from dailies
---

Close the week. "$ARGUMENTS" may specify the week (e.g. 2026-W28); if empty, use the current one (`date +%G-W%V`).

1. Determine the range (Monday–Sunday) and read every daily in `60-journal/dailies/` for the period.
2. Also read the period's meetings in `30-meetings/`.
3. The note `60-journal/weeks/YYYY-Wnn.md` may already exist (created by /goals). If so, PRESERVE the "Week goals" section and fill in the retrospective sections. If not, create it from `templates/weekly.md`.
4. **Goal results:** classify each goal as hit / partial / missed, with the reason when missed (search dailies and blockers).
5. Fill the rest by synthesizing (don't copy): deliveries per project, meetings, decisions, learnings, leftover items, next week's focus.
6. List the dailies used, with wikilinks, at the end.
7. If there are fewer dailies than working days, point out the unrecorded days.
8. Update `90-memory/current-state.md` with next week's focus and ask whether to set next week's goals now (/goals).
