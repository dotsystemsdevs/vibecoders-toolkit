# Prompts

## Rules
- No made-up numbers
- Clean up notes without changing meaning
- Ask if unclear

---

## Backlog Prompt

```
You are my repo maintainer. Create BACKLOG.md.

REQUIREMENTS
1) Sections: Entry template, P1 — Next patch, P2 — Planned, P3 — Later, Ready for review, Done
2) Entry template table: Status, Priority, Type, Target version, Evidence
3) Evidence path: docs/screenshots/YYYY-MM-DD-area-desc.png
4) Next steps = checklist with verbs

OUTPUT: Full BACKLOG.md only.
```

---

## Changelog Prompt

```
You are my repo maintainer. Create CHANGELOG.md following Keep a Changelog + SemVer.

REQUIREMENTS
1) [Unreleased] section with: Added, Changed, Fixed, Known Issues
2) ISO dates: [x.y.z] - YYYY-MM-DD
3) Known Issues: **Issue**: symptom — next action
4) Only shipped changes, no backlog tasks

OUTPUT: Full CHANGELOG.md only.
```

---

## Rewrite Notes Prompt

```
Rewrite messy notes into clean, technical English.

RULES
- Do not invent anything
- Keep meaning, remove fluff
- Every observation must have an action
- If ambiguous, ask first

FORMAT: Tables with Observation | Action
```
