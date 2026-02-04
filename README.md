# Vibecoders Toolkit

A step-by-step guide to shipping apps — from MVP to closed testing to your first users.

Built from real experience. Nothing made up.

---

## The Journey

```
MVP → Screenshots → Closed Testing → Recruit Testers → Feedback → Marketing
```

---

## Step 1: MVP

Build the app. It doesn't need to be perfect.

- [ ] App works (core features)
- [ ] Build UI one screen at a time
- [ ] Standardize (buttons, cards) last

### UI Workflow

1. Browse Pinterest for UI inspiration — save cards you like as a moodboard
2. Ask AI: describe app + features → how should screens look?
3. Build home screen first → refine until satisfied
4. Continue screen by screen
5. Settings last, then standardize components

**Why standardize last?** Doing it early limits creativity.

### Trap: Perfectionism

Don't get stuck polishing. MVP means minimum viable — ship when it works, polish later. Set a time limit if needed.

> Details: [UI & UX](ui-ux.md)

---

## Step 2: Screenshots

When building in Expo, create Play Store images.

- [ ] Screenshots of all key screens
- [ ] Figma for Play Store graphics
- [ ] Save to `docs/screenshots/`

**Tip:** Do this while building — easier than going back later.

---

## Step 3: Closed Testing

Upload to Play Console.

- [ ] AAB built and uploaded
- [ ] Closed testing group created
- [ ] Play Store images uploaded

| Goal | Target |
|------|--------|
| Members | 30+ for feedback, 100+ for approval |
| Timeline | ~2 weeks |

> Details: [Closed Testing](closed-testing.md)

---

## Step 4: Recruit Testers

Post everywhere. Some groups ban you — keep going until you find ones that work.

### Do This

| Channel | Why |
|---------|-----|
| r/AndroidClosedTesting | Best results — post here first |
| Niche forums (golf, poker, etc.) | Best feedback + validates demand |
| Reddit test-for-test | Works if you reply fast |

### Skip This

| Channel | Why |
|---------|-----|
| Discord / Telegram | Low response |
| Reddit UX/UI groups | High ban risk |

### Strategy

1. Post in r/AndroidClosedTesting
2. Turn on notifications
3. Reply fast to "test for test"
4. Be active when USA is awake
5. ~15 messages per day
6. Pace yourself after day 3-4 — still works with less effort

### Real Numbers

| App | Result |
|-----|--------|
| Lotty | 110 members → approved |
| Mulligan | 130 installs (via golf forums) |

| Day | Members |
|-----|---------|
| 1 | 25 |
| 3 | 57 |
| 7 | 96 |
| 12 | 110 (approved) |

> Details: [Closed Testing](closed-testing.md)

---

## Step 5: Feedback & Patch

Collect feedback and fix in batches — not everything at once.

### Collect Feedback

1. Screenshot all feedback immediately
2. Save to `docs/screenshots/`
3. Log in BACKLOG.md with screenshot link

### Patch Cycle

```
ship → feedback → backlog → prioritize → patch → ship
```

| Rule | Why |
|------|-----|
| Wait ~1 week | Distance = better decisions |
| Pick 3-5 items | Avoid scope creep |
| P1 = must, P2 = should, P3 = later | Focus on impact |

### Trap: Reacting Too Fast

Don't update immediately after feedback. Wait, get distance, then decide with fresh eyes.

> Details: [Feedback](feedback.md)

---

## Step 6: Marketing

*Coming soon.*

---

## Templates

| Template | Use |
|----------|-----|
| [BACKLOG.md](templates/BACKLOG.md) | Bugs, features, feedback |
| [CHANGELOG.md](templates/CHANGELOG.md) | Shipped changes |

---

## Deep Dives

Background and more details:

- [Closed Testing](closed-testing.md) — case studies, day-by-day numbers
- [Feedback](feedback.md) — change management process
- [UI & UX](ui-ux.md) — tools, productivity tips
- [CNN & Backend](cnn.md) — ML, security, AI prompts

---

## Common Traps

| Trap | Solution |
|------|----------|
| Perfectionism | Ship MVP first, polish later |
| Reacting to feedback immediately | Wait ~1 week, fresh eyes |
| Letting AI decide everything | Be specific, steer the plan yourself |
| Using wrong channels | Niche forums > general channels |
| Burning out on recruiting | Pace after day 3-4, still works |

---

## What Worked

| Thing | Why |
|-------|-----|
| Pinterest moodboard | Visual inspiration before building |
| UI one screen at a time | Avoids overwhelm |
| Screenshots while building | Easier than going back |
| Niche forums | Validates demand + quality feedback |
| Test-for-test | Works with fast replies |

---

## What Didn't Work

| Thing | Problem |
|-------|---------|
| bolt.new / rapidexpo | Bad UI output, wastes credits |
| Discord / Telegram | Low response rate |
| Reddit UX/UI groups | High ban risk |
| "Do what you think is best" to AI | Vague = bad results |
| Building all components first | Hard to change, more errors |

---

## Contributing

This is a living document. PRs welcome.

---

*Real experience. Nothing made up.*
