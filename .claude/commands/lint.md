---
description: Vault health audit (links, orphans, contradictions)
---

Audit the vault's health, focusing on `70-knowledge/` but covering the whole vault. Optional scope in "$ARGUMENTS".

Check:
1. **Broken links** — `[[wikilinks]]` pointing to notes that don't exist. List by frequency: a much-cited concept without a page is a candidate for a new note.
2. **Orphan notes** — `70-knowledge/` notes no other note links to.
3. **Contradictions** — conflicting claims between knowledge notes (and between knowledge and recorded decisions).
4. **Stale content** — notes whose `updated` is old but that have newer sources in `70-knowledge/raw/` not yet compiled.
5. **Duplicates** — concept notes that are the same thing under different names (propose a merge).
6. **Inconsistent frontmatter** — missing required fields (type, created, sources on knowledge notes).

Rules:
- Safe fixes (obvious link, frontmatter fix): apply directly and report.
- Destructive fixes (merge, delete, rewrite): only with the user's confirmation.
- NEVER touch `30-meetings/raw/` or `70-knowledge/raw/`.

End with a scoreboard: X broken links, Y orphans, Z contradictions — and what was fixed.
