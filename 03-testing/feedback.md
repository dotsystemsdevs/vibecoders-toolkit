# Feedback

How to collect feedback and run patch cycles.

---

## Collect feedback

### Process

| Step | Action |
|------|--------|
| 1 | Screenshot all feedback immediately |
| 2 | Save to `docs/screenshots/YYYY-MM-DD-area-desc.png` |
| 3 | Log in backlog with link to screenshot |
| 4 | Prioritize — not everything needs fixing now |

### Backlog entry requirements

Every item must have:
- Priority (P1/P2/P3)
- Target version
- Evidence (screenshot link)

**Action:** No backlog item without evidence. Screenshot everything.

Template: `templates/BACKLOG.md`

---

## Patch cycle

### Flow

```
ship → collect feedback → backlog → prioritize → patch → ship
```

### Rules

| Rule | Why |
|------|-----|
| Wait ~1 week before next update | Distance → better decisions |
| Pick 3-5 items per patch | Don't try to fix everything at once |
| Set priority: P1 = must fix, P2 = should fix, P3 = can wait | Focus on what matters |

### Change management

| Step | Action |
|------|--------|
| 1 | Ship (closed test) → write bullets in CHANGELOG.md under `[Unreleased]` |
| 2 | Collect feedback → save screenshots in `docs/screenshots/` |
| 3 | Log → create item in BACKLOG.md |
| 4 | Triage → pick 3-5 items → set P1/P2 + target version |
| 5 | Patch → status: In progress → Ready → Done |
| 6 | Ship again → move `[Unreleased]` to new version |

**Action:** Follow this loop. Don't skip steps.

---

## Common mistakes

| Mistake | What happened | Action |
|---------|---------------|--------|
| Update immediately after feedback | Impulsive decisions | Wait ~1 week, fresh eyes |

---

*Real experiences only. Nothing made up.*
