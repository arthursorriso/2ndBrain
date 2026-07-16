---
description: Quick capture to the inbox (zero friction)
---

Quickly capture to the inbox: "$ARGUMENTS"

1. Create `00-inbox/YYYY-MM-DD-HHMM-<short-slug>.md` (use `date +%F-%H%M`) with the content as given — no processing, no judgment.
2. Minimal frontmatter: `type: inbox`, `created: <date>`.
3. If "$ARGUMENTS" is empty, ask what to capture.
4. Confirm in 1 line. Do NOTHING else — processing happens later via /process-inbox.
