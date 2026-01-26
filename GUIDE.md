# Shipping Playbook

A practical guide to shipping apps to closed testing and getting feedback. Based on real experiences — nothing made up.

---

## Contents

1. [Before closed testing](#1-before-closed-testing)
2. [Closed testing](#2-closed-testing)
3. [Recruit testers](#3-recruit-testers)
4. [Collect feedback](#4-collect-feedback)
5. [Patch cycle](#5-patch-cycle)
6. [AI & tools](#6-ai--tools)
7. [Common mistakes](#7-common-mistakes)
8. [Case study: Lotty](#8-case-study-lotty)

---

## 1. Before closed testing

### Checklist

- [ ] App works (doesn't need to be perfect)
- [ ] Play Store images ready (Figma)
- [ ] AAB built and uploaded
- [ ] Closed testing group created in Play Console

### Tools

| Tool | Use |
|------|-----|
| Figma | Screenshots + basic branding for Play Store |
| GitHub | Version control + backlog + branches + CI/CD |
| Play Console | Closed testing |

**Action:** Don't wait for perfection. Ship when it works.

---

## 2. Closed testing

### Why closed testing first?

| Reason | Action |
|--------|--------|
| Get feedback before going live | Ship to closed test, not production |
| Find bugs early | Let real users break it |
| Validate the need exists | Post in niche forums to confirm demand |

### Targets

| Metric | Target | Why |
|--------|--------|-----|
| Members | 30+ | Enough data for decisions |
| Timeline | ~2 weeks | Before next major update |

### Naming

Neutral names reach broader audiences.

| Before | After | Result |
|--------|-------|--------|
| "lotty-tracker" | "win/loss tracker" | Broader appeal |
| "Lost Ball Counter" | "Mulligan: The Real Scorecard" | More professional |

**Action:** Remove niche jargon from app name. Keep it generic.

---

## 3. Recruit testers

### What worked

| Channel | Result | Action |
|---------|--------|--------|
| r/AndroidClosedTesting | Best results | Post here first |
| Niche forums (e.g. golf forums) | Great feedback + validates need | Post to get quality feedback |
| Reddit test-for-test | Works with right strategy | Reply fast, be active |

### What did NOT work

| Channel | Result | Action |
|---------|--------|--------|
| Discord | 1 person | Skip it |
| Telegram | No response | Skip it |
| Reddit UX/UI groups | Ban + negative response | Never post here for testers |

### Strategy

| Step | Action |
|------|--------|
| 1 | Post in r/AndroidClosedTesting |
| 2 | Turn on notifications |
| 3 | Reply fast to "test for test" comments |
| 4 | Schedule Reddit time (avoid 24/7) |
| 5 | Be active when USA is awake |
| 6 | Send ~15 messages per day |

### Key insights

| Observation | Action |
|-------------|--------|
| Less effort after day 3-4 still gave results | Don't burn out early, pace yourself |
| Testers go inactive after 14 days | Plan for churn, keep recruiting |
| Test-for-test requires reciprocation | Budget time to test others' apps |
| Niche forums = goldmine | Always post in forums where your users are |

---

## 4. Collect feedback

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

## 5. Patch cycle

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

## 6. AI & tools

### Plan mode strategy

| Step | Action |
|------|--------|
| 1 | Write high-level plan with steps all the way to production |
| 2 | When starting a step → ask AI to write detailed sub-steps |
| 3 | Give AI sub-steps one at a time |
| 4 | Ask what you can do in parallel |

| Mistake | Better approach |
|---------|-----------------|
| "Do what you think is best" | Be specific, steer the plan yourself |
| Letting AI decide architecture | The more you know, the better you prompt |

**Action:** Never say "do what you think is best". Always be specific.

### UI building method

| Step | Action |
|------|--------|
| 1 | Tell ChatGPT: app, backend, key features → ask how screens should look (content + copy) |
| 2 | Build home screen → refine until satisfied |
| 3 | Continue screen by screen, don't move on until satisfied |
| 4 | At the end: review all screens, minor improvements |
| 5 | Last = settings, then standardize (cards, buttons etc.) |

**Why standardize last?** Doing it early limits your creativity.

**Action:** Build one screen at a time. Standardize at the end.

### Tools that did NOT work

| Tool | Problem | Action |
|------|---------|--------|
| bolt.new | Not satisfied with UI, wastes credits | Skip it |
| rapidexpo | Same problem | Skip it |
| Plan mode "build all components" | Ugly, hard to change, errors | Build screen by screen instead |

### Content & Instagram

| Observation | Action |
|-------------|--------|
| Low response initially (0 likes) | Don't expect immediate results |
| GPT-copy feels bad | Write yourself first, use AI only for translation |
| Need content | Take more screenshots during the day |
| People notice fake | Keep it authentic |

**Action:** Write copy yourself. Use AI for translation only.

### Backend & security

| Observation | Action |
|-------------|--------|
| "Vibecoding" with backend creates vulnerabilities | Always analyze security when building with backend |
| Need version control discipline | Use GitHub branches + CI/CD |
| Need local testing | Build HTML page for diagnostics |

**Action:** If you have a backend, do a security review before shipping.

---

## 7. Common mistakes

| Mistake | What happened | Action |
|---------|---------------|--------|
| Post in UX/UI groups | Ban + bullied | Use the right forum for the right purpose |
| Discord/Telegram for recruiting | Almost no response | Focus on Reddit |
| UI perfectionism | Got stuck, frustrated | Ship first, polish later |
| GPT for all copy | Felt bad, took time | Write yourself, AI for polish |
| Reddit 24/7 | Hard to stop | Schedule specific time |
| Update immediately after feedback | Impulsive decisions | Wait ~1 week, fresh eyes |
| "Do what you think is best" to AI | Bad results | Be specific, steer the plan yourself |
| bolt.new / rapidexpo | Wasted credits | Build screen by screen in Claude |

### Productivity

| Observation | Action |
|-------------|--------|
| Most effective in the morning | Do hard work in the morning |
| Dip after workout | Move workout to after other work |
| Hard to follow schedule with many tabs | Reduce distractions |
| UI perfectionism | Set time limit, ship "good enough" |
| Reddit addiction | Schedule Reddit time (not 24/7) |
| Risk of burnout | Plan rest days |

**Action:** Know your energy patterns. Schedule around them.

---

## 8. Case study: Lotty

Win/loss tracker app. Closed testing → approved in Play Store.

### Growth (members in Google group)

| Day | Members | Active users |
|-----|---------|--------------|
| 1 | 25 | 1 |
| 2 | 40 | 24 |
| 3 | 57 | 41 |
| 4 | 73 | 53 |
| 5 | 86 | 70 |
| 6 | 90 | 69 |
| 7 | 96 | 71 |
| 12 | 110 | ~12 (some days) |

### Key insights

| Observation | Action |
|-------------|--------|
| Less effort after day 3-4 still gave results | Pace yourself, don't burn out early |
| Approved with 110 members | 100+ members is enough for approval |
| Active testers vary a lot (12-71 per day) | Don't stress about daily numbers |

### Mulligan (comparison)

Golf app. Posted in golf forums → great feedback + improvement suggestions. Need validated.

| Day | Members |
|-----|---------|
| 1 | 28 |
| 2 | 44 |
| 3 | 67 |
| 6 | 100+ |

**Action:** Post in niche forums. They validate demand AND give better feedback.

---

## Templates

- `templates/BACKLOG.md` — backlog template
- `templates/CHANGELOG.md` — changelog template

---

*Real experiences only. Nothing made up.*
