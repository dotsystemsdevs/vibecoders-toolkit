# MVP Guide

---

## What is an MVP?

> "The version of a new product which allows a team to collect the maximum amount of validated learning about customers with the least effort." — Eric Ries

**Minimum Viable Product** = The smallest thing you can build that someone will pay for.

Key word: **viable**. Until someone hands you money, you haven't proven viability.

---

## MVP vs Prototype vs Product

| Type | What it is | Who uses it |
|------|------------|-------------|
| **Prototype** | Visual draft, mockup, clickable demo | Internal team |
| **MVP** | Functional product with core features | Real users who pay |
| **Full Product** | Refined, scalable, polished | Mass market |

A prototype proves the concept works. An MVP proves people will pay.

---

## The Real Test

Demos and positive feedback feel good. But they don't validate your product.

| What people say | What it means |
|-----------------|---------------|
| "This looks great!" | They like the idea |
| "I would totally use this" | They might use it |
| "Here's my credit card" | **Validated** |

**The hard truth:** People love to say your product is great. But when you ask for the sale, something always comes up. Until money changes hands, you're guessing.

---

## What MVP is NOT

| MVP is NOT | MVP IS |
|------------|--------|
| Feature-complete | One thing that works |
| Perfect design | Functional design |
| Scalable architecture | Code that runs |
| All edge cases handled | Happy path works |
| Polished animations | Basic feedback (loading, errors) |

---

## Definition of Done

Your MVP is ready when:

1. **One core feature works end-to-end**
2. **You can demo it in 60 seconds**
3. **A stranger can use it without your help**
4. **You're slightly embarrassed** — if you're not, you waited too long

> "If you're not embarrassed by the first version of your product, you've launched too late." — Reid Hoffman

---

## Real Examples

| Company | MVP | What they tested |
|---------|-----|------------------|
| **Uber** | SMS service to call a cab | Would people order rides via phone? |
| **Dropbox** | Explainer video (no working product) | Is there demand for cloud sync? |
| **Amazon** | Online bookstore from a garage | Will people buy books online? |
| **Spotify** | Landing page with streaming test | Can we make playback fast and stable? |

None of these started with the full product. They tested one hypothesis first.

---

## The Process

```
Pain point → Hypothesis → Build minimal → Test → Learn → Iterate
```

### 1. Identify the pain point

What problem are you solving? Talk to potential users:
- What do they currently do?
- What frustrates them?
- Would they pay to fix it?

### 2. Define your hypothesis

"If I build [X], then [target user] will pay [Y] because it solves [Z]."

Be specific. Vague hypotheses lead to vague products.

### 3. Build the minimum

Only what's needed to test your hypothesis. Nothing more.

### 4. Test with real users

Not friends. Not family. People who have the problem and would pay to solve it.

### 5. Measure what matters

- Did they use it?
- Did they pay?
- Did they come back?
- What did they complain about?

### 6. Iterate or pivot

If it works, add more. If it doesn't, change direction.

---

## Common Mistakes

| Mistake | Why it fails |
|---------|--------------|
| Adding too many features | Dilutes focus, delays launch |
| Not launching early enough | Waiting for perfect = never launching |
| Ignoring feedback | Building blind |
| Confusing interest with validation | "Looks great" ≠ "I'll pay" |
| Building for the wrong users | Early adopters ≠ target market |

---

## Time Limits

If you're still "almost done" after 3 weeks, you're overbuilding.

| Week | Goal |
|------|------|
| 1 | Core feature working |
| 2 | Basic UI + internal testing |
| 3 | Ship to real users |

Set a deadline. Ship ugly. Learn fast.

---

## Vibe Coding

Using AI to build fast. Let AI handle implementation while you focus on what to build.

### What It Is

> "You talk to your code, accept LLM suggestions, copy-paste error messages, and pray it works. And it mostly does." — Andrej Karpathy

**Vibe coding** = AI-assisted development where you describe what you want and AI generates the code.

### What It Is NOT

- Pasting prompts and hoping for the best
- Shipping code you don't understand
- Bypassing security or architecture
- Letting AI make all decisions

**Key rule:** If you can't read the code AI generates, don't ship it.

### The Loop

```
Describe → Generate → Review → Test → Repeat
```

1. **Describe** what you want to build (be specific)
2. **AI generates** initial implementation
3. **You review** and correct mistakes
4. **Test immediately** — don't batch
5. **Commit frequently** — small atomic commits

### When It Works

| Use Case | Why |
|----------|-----|
| Demos and prototypes | Fast validation, throwaway code OK |
| Landing pages | Simple, low risk |
| Internal tools | Less security pressure |
| Learning/exploring | Rapid iteration |

### When It Doesn't

| Use Case | Why |
|----------|-----|
| Production with real user data | Security vulnerabilities |
| Complex backends | AI creates inconsistent mess as codebase grows |
| Anything with payments | Too risky without expert review |
| Scaling beyond 100 users | Architecture breaks |

### Non-Technical Founders

**Reality check from Reddit:**

> "I haven't seen anybody who vibecoded entire applications without knowing coding. I have seen landing pages that are vibecoded."

| Approach | Works For |
|----------|-----------|
| Vibe code a demo | Getting initial feedback, showing investors |
| Vibe code MVP, hire devs later | Validating idea cheap, then rebuilding properly |
| Hire dev from start | Complex products, security-critical, B2B |

**The honest truth:** Vibe coding is great for demos. For real MVPs with paying users, most non-technical founders eventually need dev help — either to review/fix AI code or rebuild from scratch.

### Tradeoffs

| Pro | Con |
|-----|-----|
| 10x faster to prototype | Security holes you won't catch |
| Lower barrier to start | Technical debt accumulates fast |
| Instant context recovery | AI makes poor decisions as code grows |
| Validates ideas cheap | May need full rewrite later |

### If You Vibe Code

1. **Plan first** — Create implementation plan before coding
2. **Be specific** — Vague prompts = bad code
3. **Review everything** — Don't blindly accept
4. **Test constantly** — Don't batch testing
5. **Know when to stop** — Get dev help before users pay

---

## AI Models

| Model | Best For |
|-------|----------|
| Claude Sonnet 4.5 | Coding, debugging, refactoring |
| Claude Opus 4.5 | Complex architecture, hard problems |
| GPT-5 | Brainstorming, marketing copy, ideas |
| GPT-4o | Quick tasks, good enough for most |
| v0.dev | UI prototypes (React) |
| Midjourney | Icons, graphics |

### Vibe Coding Tools

| Tool | What it does |
|------|--------------|
| Cursor | AI-enhanced VS Code fork, best for coding |
| Windsurf | Standalone AI editor, good flow |
| Claude Code | Terminal-based, powerful for devs |
| Bolt.new | Full app generation (hit or miss) |
| Lovable | Similar to Bolt, generates full apps |

---

## Next Steps

Once your MVP is validated:
1. Take screenshots → [Phase 2](README.md#phase-2-screenshots)
2. Upload to Play Console → [Closed Testing](closed-testing.md)
3. Get feedback → [Feedback Guide](feedback.md)

---

*Ship first. Polish later.*
