# Vibecode

AI-generated code. Fast MVPs.

---

## What is vibecode

You describe what you want. AI generates code. You review, test, ship.

```
Describe → Generate → Review → Test → Repeat
```

**Works for:** Demos, MVPs, landing pages, internal tools  
**Doesn't work for:** Production with users, complex backends, payment systems

---

## What you need

### Tools

| Tool | What | Use it? |
|------|------|---------|
| **Cursor** | AI VS Code | ✅ Best for daily coding |
| **Claude Code** | Terminal AI | ✅ Complex tasks |
| **Windsurf** | AI editor | ✅ Alternative |
| **Bolt.new** | Full app gen | ❌ Wasted credits, skip |

### Models

| Model | Best for |
|-------|----------|
| Claude Sonnet | Coding, debugging |
| Claude Opus | Architecture |
| GPT-5 | Marketing copy |
| v0.dev | UI prototypes |

---

## How to do it

### The loop

| Step | Action |
|------|--------|
| 1. Describe | Be specific about what you want |
| 2. Generate | Let AI create the code |
| 3. Review | Read it, don't blindly accept |
| 4. Test | Test immediately, don't batch |
| 5. Repeat | Commit after every working change |

### Rules

- [ ] Plan first — write implementation plan before coding
- [ ] Be specific — vague prompts = bad code
- [ ] Review everything — don't blindly accept
- [ ] Test constantly — don't batch
- [ ] Know when to stop — get dev help before users pay

---

## UI: Build screen by screen

| Step | Action |
|------|--------|
| 1 | Describe app to AI, ask how screens should look |
| 2 | Build home screen first, refine until satisfied |
| 3 | One screen at a time — don't move on until it works |
| 4 | Review all screens, minor tweaks |
| 5 | Settings last, then standardize colors/buttons |

**Why standardize last?** Doing it early kills creativity.

### Content

| Rule | Why |
|------|-----|
| Write copy yourself | GPT copy feels fake |
| AI for translation only | Keeps it authentic |
| Screenshot during the day | Content for Instagram later |

### Productivity

| Observation | What we do |
|-------------|------------|
| Morning = most effective | Hard work before lunch |
| Dip after workout | Workout after work |
| UI perfectionism kills momentum | Time limit, ship "good enough" |
| Reddit addiction | Scheduled time, not 24/7 |
| Burnout risk | Planned rest days |

---

## Backend: Plan mode strategy

| Step | Action |
|------|--------|
| 1 | Write high-level plan to production |
| 2 | Ask AI for detailed sub-steps |
| 3 | Give AI one sub-step at a time |
| 4 | Ask what can run in parallel |

### Security checklist

- [ ] Review all API endpoints for auth
- [ ] Check SQL injection, XSS
- [ ] Environment variables for secrets
- [ ] Test with invalid inputs
- [ ] Security review before shipping

### Mistakes we made

| Mistake | What happened | Do instead |
|---------|---------------|------------|
| "Do what you think" to AI | Bad architecture | Be specific, steer the plan |
| Skip security review | Shipped vulnerabilities | Always review backend |
| No version control discipline | Lost work, messy history | Branches + commit often |

---

## Prompt templates

### Backlog

```
You are my repo maintainer. Create BACKLOG.md.

REQUIREMENTS
1) Sections: Entry template, P1 — Next patch, P2 — Planned, P3 — Later, Ready for review, Done
2) Entry template table: Status, Priority, Type, Target version, Evidence
3) Evidence path: docs/screenshots/YYYY-MM-DD-area-desc.png
4) Next steps = checklist with verbs

OUTPUT: Full BACKLOG.md only.
```

### Changelog

```
You are my repo maintainer. Create CHANGELOG.md following Keep a Changelog + SemVer.

REQUIREMENTS
1) [Unreleased] section with: Added, Changed, Fixed, Known Issues
2) ISO dates: [x.y.z] - YYYY-MM-DD
3) Known Issues: **Issue**: symptom — next action
4) Only shipped changes, no backlog tasks

OUTPUT: Full CHANGELOG.md only.
```

### Rewrite Notes

```
Rewrite messy notes into clean, technical English.

RULES
- Do not invent anything
- Keep meaning, remove fluff
- Every observation must have an action
- If ambiguous, ask first

FORMAT: Tables with Observation | Action
```

---

## Evidence

We shipped 3 Android apps in 1 week each using Claude + Cursor. Zero backend, all offline, local storage. That's the sweet spot.

Add backend/auth/payments → slow down and review everything.

---

*Ship first. Polish later.*
