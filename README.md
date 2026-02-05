# Vibecoders Toolkit

A step-by-step guide to shipping apps — from MVP to closed testing to your first users.

Built from real experience. Nothing made up.

---

# Roadmap

```
MVP → Screenshots → Closed Testing → Feedback → Go Live (ASO) → Marketing
```

Everything below follows this roadmap. Each phase builds on the previous.

---

## Phase 1: MVP

Build the smallest version of your app that delivers value AND gives you feedback.

### Quick Checklist

- [ ] **One core feature works** end-to-end
- [ ] **User can complete the main flow** without errors
- [ ] **You can demo it in 60 seconds**
- [ ] **A stranger can use it** without your help

### Definition of Done

Your MVP is ready when you're slightly embarrassed by it. If you're not, you waited too long.

> "If you're not embarrassed by the first version of your product, you've launched too late." — Reid Hoffman

### AI Stack

| Task | Best Tool |
|------|-----------|
| Coding & debugging | **Anthropic (Claude)** — better reasoning, fewer bugs |
| Brainstorming & copy | **OpenAI (ChatGPT)** — creative, fast ideas |
| UI prototypes | **v0.dev** — React components fast |
| Graphics | **Midjourney** — icons, marketing images |

> **Full guide:** [MVP Guide](mvp.md) — end product definition, AI stack details, workflow

---

## Phase 2: Screenshots

When building in Expo, create Play Store images.

- [ ] Screenshots of all key screens
- [ ] Figma for Play Store graphics
- [ ] Save to `docs/screenshots/`

**Tip:** Do this while building — easier than going back later.

---

## Phase 3: Closed Testing

Upload to Play Console and recruit testers.

### Setup

- [ ] AAB built and uploaded
- [ ] Closed testing group created
- [ ] Play Store images uploaded

| Goal | Target |
|------|--------|
| Members | 30+ for feedback, 100+ for approval |
| Timeline | ~2 weeks |

### Recruit Testers

Post everywhere. Some groups ban you — keep going until you find ones that work.

**Do this:**

| Channel | Why |
|---------|-----|
| r/AndroidClosedTesting | Best results — post here first |
| Niche forums (golf, poker, etc.) | Quality feedback if they engage |
| Reddit test-for-test | Works if you reply fast |

**Skip this:**

| Channel | Why |
|---------|-----|
| Discord / Telegram | Low response |
| Reddit UX/UI groups | High ban risk |

### Reality Check

**Test-for-test users are not your target audience.** They download for reciprocation, not because they need your app. Expect most to leave — that's normal. Don't measure retention on these users.

**Niche forums are hostile to promotion.** People say "stop coming here with your shit app" before even looking. You will get banned. Post anyway — the few who engage give the best feedback.

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

## Phase 4: Feedback & Patch

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

## Phase 5: Go Live (ASO)

Before going public, optimize your Play Store listing.

### When to Go Live

- [ ] Core bugs from testing fixed
- [ ] One final update with everything from testing period
- [ ] You want real user feedback (not just test-for-test)

### ASO Checklist (App Store Optimization)

ASO = making your app findable and attractive in the store.

**Naming:**

| Before | After | Why |
|--------|-------|-----|
| "lotty-tracker" | "Win/Loss Tracker" | Generic = broader reach |
| "Lost Ball Counter" | "Mulligan: Golf Scorecard" | Professional + keywords |

- [ ] Remove niche jargon from app name
- [ ] Include keywords people search for
- [ ] Keep it short and clear

**Listing:**

- [ ] Screenshots show the app in action (not just UI)
- [ ] Description starts with what problem it solves
- [ ] Short description has main keywords

**Reviews:**

- [ ] Ask happy testers to leave a review before going public
- [ ] Respond to all reviews (shows activity)

> ASO is an ongoing process — revisit after seeing search data.

---

## Phase 6: Marketing

Build audience through Instagram. Test what works, then double down.

Key principles:
- Pick one niche per account
- Reels get 10-30x more reach than static posts
- First 3 seconds = hook (pattern interrupt, curiosity, relatable pain)
- Post when your audience is scrolling (evening for US/UK)
- 5-3-1 daily: Like 5, Comment 3, Follow 1

> Details: [Marketing](marketing.md) — Week 1 calendar with all posts

---

# Resources

## Templates

| Template | Use |
|----------|-----|
| [BACKLOG.md](templates/BACKLOG.md) | Bugs, features, feedback |
| [CHANGELOG.md](templates/CHANGELOG.md) | Shipped changes |

## Deep Dives

- [MVP Guide](mvp.md) — end product definition, AI stack, workflow
- [Marketing](marketing.md) — Week 1 calendar with all posts
- [Closed Testing](closed-testing.md) — case studies, day-by-day numbers
- [Feedback](feedback.md) — change management process
- [UI & UX](ui-ux.md) — tools, productivity tips
- [CNN & Backend](cnn.md) — ML, security, AI prompts

---

# Lessons Learned

## Common Traps

| Trap | Solution |
|------|----------|
| Perfectionism | Ship MVP first, polish later |
| Reacting to feedback immediately | Wait ~1 week, fresh eyes |
| Letting AI decide everything | Be specific, steer the plan yourself |
| Using wrong channels | Niche forums > general channels |
| Burning out on recruiting | Pace after day 3-4, still works |

## What Worked

| Thing | Why |
|-------|-----|
| Pinterest moodboard | Visual inspiration before building |
| UI one screen at a time | Avoids overwhelm |
| Screenshots while building | Easier than going back |
| Niche forums | Validates demand + quality feedback |
| Test-for-test | Works with fast replies |

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
