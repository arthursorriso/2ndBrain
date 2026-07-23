---
description: Process and empty the inbox
---

Process every item in `00-inbox/`.

1. List the inbox files. If empty, say so and stop.
2. Classify each item: idea → `20-ideas/` (template idea.md) · new project/update → `10-projects/` · tutorial (how to do) → `40-tutorials/` · **concept/article/reference (what it is)** → knowledge base: follow the /learn flow (compile into `70-knowledge/`, enriching existing notes instead of creating loose ones) · fact about a person → `50-people/` · task → "Next steps" of the right project or `current-state.md` pending items.
3. Always use the type's template and create wikilinks to what already exists in the vault.
4. When ambiguous, ask before moving.
5. After migrating the content, delete the inbox file.
6. Summarize at the end: what went where.

Critical rule: an item related to a project does NOT go into `10-projects/` — it goes to its TYPE's folder, and the project gets a wikilink in its "Links" section + a log entry. `10-projects/` contains only each project's note.
