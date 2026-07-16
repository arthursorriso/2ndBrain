---
description: Quick capture to your second brain (from anywhere)
---

Capture to the second brain (vault at `~/2ndBrain`): "$ARGUMENTS"

1. Create `~/2ndBrain/00-inbox/YYYY-MM-DD-HHMM-<short-slug>.md` (use `date +%F-%H%M`) with the content as given — no processing, no judgment.
2. Minimal frontmatter: `type: inbox`, `created: <date>`.
3. If "$ARGUMENTS" is empty, ask what to capture.
4. Confirm in 1 line. Do NOTHING else — processing happens later, inside the vault, via /process-inbox.
5. Never invent content beyond what was given.
