---
description: Set, update, or check the week's goals
---

Week goals. Input: "$ARGUMENTS"

The week note is `60-journal/weeks/YYYY-Wnn.md` (current week: `date +%G-W%V`). Goals live in the "Week goals" section, format `- [ ] description — N/M` (N = done, M = target). Goals without a quantity use 0/1.

Pick the mode from "$ARGUMENTS":

**1. Set goals** (input describes new goals, e.g. "open 3 PRs, review the design doc"):
- If the week note doesn't exist, create it from `templates/weekly.md` filling ONLY frontmatter and "Week goals" — retrospective sections stay empty for `/weekly`.
- If it exists, add the new goals without removing existing ones.
- Extract the numeric target from the description ("3 PRs" → 0/3).

**2. Log progress** (input reports progress, e.g. "opened 1 PR"):
- Find the matching goal, increment the counter, mark `[x]` when N == M.
- Reply with what's left: "2 PRs to go. 3 working days left this week."

**3. Check status** ("$ARGUMENTS" empty):
- Show each goal with progress and what's left, how many working days remain, and flag goals still at 0 after Wednesday.
- If no goals are set this week, offer to set them now.

Never remove a goal without confirmation — an abandoned goal becomes `- [ ] ~~description~~ — abandoned: reason`.
