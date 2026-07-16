---
description: Build the quarter retrospective from weekly notes
---

Build the quarterly retrospective. "$ARGUMENTS" may specify the quarter (e.g. 2026-Q3); if empty, use the current one (Q1 = Jan–Mar, Q2 = Apr–Jun, Q3 = Jul–Sep, Q4 = Oct–Dec).

1. Read every weekly note for the period in `60-journal/weeks/` (fall back to dailies where weeklies are missing).
2. Read project states in `10-projects/` and decisions/learnings in `90-memory/`.
3. Create `60-journal/quarters/YYYY-Qn.md` from `templates/quarter.md`: overview, each project's evolution, wins, what didn't work, defining decisions, learnings, key people, next quarter's objectives.
4. Ask the user for next quarter's objectives before finalizing that section.
5. List the weeklies used, with wikilinks.
