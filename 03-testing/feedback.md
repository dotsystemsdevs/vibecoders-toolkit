# Feedback & Patch Cycles

## Background

The temptation is to fix everything immediately. Don't. Wait a week, then decide with fresh eyes.

```
Ship → Collect feedback → Backlog → Prioritize → Patch → Ship
```

---

## Do this

### Collect feedback

| Step | Action |
|------|--------|
| 1 | Screenshot all feedback immediately |
| 2 | Save to `docs/screenshots/YYYY-MM-DD-area-desc.png` |
| 3 | Log in backlog with link to screenshot |
| 4 | Prioritize — not everything needs fixing now |

Every backlog item must have:
- Priority (P1/P2/P3)
- Target version
- Evidence (screenshot link)

No backlog item without evidence. Template: `templates/BACKLOG.md`

### Patch cycle

| Rule | Why |
|------|-----|
| Wait ~1 week before next update | Distance = better decisions |
| Pick 3-5 items per patch | Don't try to fix everything at once |
| P1 = must fix, P2 = should fix, P3 = can wait | Focus on what matters |

### Change management

1. Ship (closed test) — write bullets in CHANGELOG.md under `[Unreleased]`
2. Collect feedback — save screenshots in `docs/screenshots/`
3. Log — create item in BACKLOG.md
4. Triage — pick 3-5 items, set P1/P2 + target version
5. Patch — status: In progress, Ready, Done
6. Ship again — move `[Unreleased]` to new version

---

## Mistakes we made

| Mistake | What happened | What to do instead |
|---------|---------------|-------------------|
| Updated immediately after feedback | Impulsive decisions, regretted changes | Wait ~1 week, fresh eyes |

---

*Follow the loop. Don't skip steps.*
