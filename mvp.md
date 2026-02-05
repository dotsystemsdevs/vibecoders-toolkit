# MVP Guide

Build the smallest version of your app that delivers value AND gives you feedback.

---

## What is an MVP?

**Minimum Viable Product** = The smallest version that:
- Solves a real problem
- Can be used by real people
- Gives you data to improve

---

## Why MVP Matters

| Reason | Impact |
|--------|--------|
| Fast validation | Test your idea before building too much |
| Save time | Don't build features nobody wants |
| Learn from real users | Not guesses |
| Iterate quickly | Improve based on feedback |

---

## Questions Your MVP Should Answer

| Question | Why It Matters |
|----------|----------------|
| Does this solve a real problem? | Validates the need |
| Do people want to use it? | Confirms interest |
| Do users understand how it works? | Tests UX |
| What's missing most? | Prioritizes next steps |
| Would people pay for this? | Validates business model |

---

## The End Product

Your MVP is done when you can check these boxes:

### Core Requirements

- [ ] **One core feature works** — not five half-working features
- [ ] **User can complete the main flow** — start to finish without errors
- [ ] **App doesn't crash** — stable enough for real testing
- [ ] **Basic UI is usable** — doesn't need to be pretty, needs to be clear

### What MVP is NOT

| MVP is NOT | MVP IS |
|------------|--------|
| Feature-complete | One thing that works |
| Perfect design | Functional design |
| Scalable architecture | Code that runs |
| Edge cases handled | Happy path works |
| Polished animations | Basic feedback (loading, errors) |

### Definition of Done

Your MVP is ready to ship when:

1. **Core feature works end-to-end**
2. **You can demo it in 60 seconds**
3. **A stranger can use it without your help**
4. **You're slightly embarrassed** — if you're not, you waited too long

> "If you're not embarrassed by the first version of your product, you've launched too late." — Reid Hoffman

---

## MVP Checklist

- [ ] App works (core features only)
- [ ] Build UI one screen at a time
- [ ] Standardize (buttons, cards) last

### UI Workflow

1. Browse Pinterest for UI inspiration — save cards you like as a moodboard
2. Ask AI: describe app + features → how should screens look?
3. Build home screen first → refine until satisfied
4. Continue screen by screen
5. Settings last, then standardize components

**Why standardize last?** Doing it early limits creativity.

---

## AI Stack for Vibecoding

Different AI tools are better for different tasks. Here's what works:

### Anthropic (Claude) — Best for Code

| Use Case | Why Anthropic |
|----------|---------------|
| Writing code | Better reasoning, fewer bugs |
| Debugging | Finds root cause, not just symptoms |
| Architecture decisions | Understands tradeoffs |
| Refactoring | Cleaner, more maintainable code |
| Code review | Catches edge cases |

**Best models:**
- **Claude Opus 4.5** — Complex architecture, hard bugs
- **Claude Sonnet 4.5** — Daily coding, fast + smart
- **Claude Code (CLI)** — Terminal-based coding assistant

### OpenAI (ChatGPT) — Best for Content & Ideas

| Use Case | Why OpenAI |
|----------|------------|
| Brainstorming | Creative, lots of ideas fast |
| Marketing copy | Good at persuasive writing |
| User research | Summarizing feedback |
| Documentation | Clear explanations |
| App store descriptions | SEO-friendly text |

**Best models:**
- **GPT-5** — General tasks, creative work
- **GPT-4o** — Fast responses, good enough for most

### Other Tools

| Tool | Best For |
|------|----------|
| **Cursor / Windsurf** | AI-first code editors (uses Claude or GPT) |
| **v0.dev** | Fast UI prototyping with React |
| **Bolt.new / Lovable** | Fullstack app generation (hit or miss) |
| **Midjourney** | App icons, marketing images |
| **DALL-E** | Quick visuals, screenshots mockups |

### The Stack We Use

```
Planning & Ideas     → ChatGPT
Coding & Debugging   → Claude Code / Cursor
UI Prototypes        → v0.dev
Icons & Graphics     → Midjourney
```

### Warning: What Didn't Work

| Tool | Problem |
|------|---------|
| bolt.new | Bad UI output, wastes credits |
| rapidexpo | Unreliable, poor quality |
| "Do what you think is best" | Vague prompts = bad results |

**Key insight:** Be specific with AI. Don't say "make it better" — say exactly what you want changed.

---

## Trap: Perfectionism

Don't get stuck polishing. MVP means minimum viable — ship when it works, polish later.

Set a time limit if needed:
- **Week 1:** Core feature working
- **Week 2:** Basic UI + testing
- **Week 3:** Ship to closed testing

If you're still "almost done" after 3 weeks, you're overbuilding.

---

## Next Steps

Once your MVP is ready:
1. Take screenshots → [Screenshots Guide](README.md#phase-2-screenshots)
2. Upload to Play Console → [Closed Testing](closed-testing.md)
3. Get feedback → [Feedback Guide](feedback.md)

---

*Ship MVP first, polish later.*
