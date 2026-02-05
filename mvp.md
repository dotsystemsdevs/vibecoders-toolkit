# MVP Guide

The complete guide to building and launching your first product.

---

# Part 1: Understanding

*Background and concepts — read this first.*

---

## What is an MVP?

> "The version of a new product which allows a team to collect the maximum amount of validated learning about customers with the least effort." — Eric Ries

**Minimum Viable Product** = The smallest product you can build that someone will pay for.

The key word is **viable**. Until someone gives you money, you haven't proven the product works.

---

## Why does MVP matter?

| Reason | Effect |
|--------|--------|
| Fast validation | Test the idea before building too much |
| Saves time | Don't build features nobody wants |
| Learn from real users | Not guesses |
| Iterate quickly | Improve based on feedback |

**Without MVP:** You spend months building something nobody wants.

**With MVP:** You know within weeks if the idea works.

---

## What's the difference between MVP, prototype, and finished product?

| Type | What it is | Who uses it |
|------|------------|-------------|
| **Prototype** | Visual draft, mockup, clickable demo | Internal team |
| **MVP** | Working product with core features | Real users who pay |
| **Finished product** | Refined, scalable, polished | Mass market |

**Prototype** proves the concept works.
**MVP** proves people will pay.

---

## How do I know if my idea is validated?

Demos and positive feedback feel good. But they don't validate your product.

| What people say | What it means |
|-----------------|---------------|
| "This looks great!" | They like the idea |
| "I would definitely use this" | They might use it |
| "Here's my credit card" | **Validated** |

**The hard truth:** People love to say your product is great. But when you ask for payment, something always comes up. Until money changes hands, you're guessing.

---

## What is MVP NOT?

| MVP is NOT | MVP IS |
|------------|--------|
| Feature-complete | One thing that works |
| Perfect design | Functional design |
| Scalable architecture | Code that runs |
| All edge cases handled | Happy path works |
| Polished animations | Basic feedback (loading, errors) |

---

## Which companies started with an MVP?

| Company | MVP | What they tested |
|---------|-----|------------------|
| **Uber** | SMS service to call a taxi | Would people order rides via phone? |
| **Dropbox** | Explainer video (no working product) | Is there demand for cloud sync? |
| **Amazon** | Online bookstore from a garage | Will people buy books online? |
| **Spotify** | Landing page with streaming test | Can we make playback fast and stable? |

None of them started with the full product. They tested one hypothesis first.

---

# Part 2: Action

*Concrete steps — do this.*

---

## How do I build an MVP? (6 steps)

```
Pain point → Hypothesis → Build minimal → Test → Learn → Iterate
```

### Step 1: Identify the pain point

What problem are you solving? Talk to potential users:

- [ ] What do they do today?
- [ ] What frustrates them?
- [ ] Would they pay to solve it?

### Step 2: Define your hypothesis

Write it like this:

> "If I build [X], then [target audience] will pay [Y] because it solves [Z]."

Be specific. Vague hypotheses lead to vague products.

### Step 3: Build the minimum

Only what's needed to test your hypothesis. Nothing more.

- [ ] One core feature that works end-to-end
- [ ] User can complete the main flow
- [ ] Basic UI (doesn't need to be pretty)

### Step 4: Test with real users

Not friends. Not family. People who have the problem and would pay to solve it.

- [ ] Find 5-10 people in your target audience
- [ ] Let them use the product
- [ ] Observe — don't just ask

### Step 5: Measure what matters

- [ ] Did they use it?
- [ ] Did they pay?
- [ ] Did they come back?
- [ ] What did they complain about?

### Step 6: Iterate or pivot

If it works → add more.
If it doesn't work → change direction.

---

## How do I know when my MVP is done?

Your MVP is done when:

- [ ] **One core feature works end-to-end**
- [ ] **You can demo it in 60 seconds**
- [ ] **A stranger can use it without your help**
- [ ] **You're slightly embarrassed** — if you're not, you waited too long

> "If you're not embarrassed by the first version of your product, you've launched too late." — Reid Hoffman

---

## What time limit should I set?

If you're still "almost done" after 3 weeks, you're overbuilding.

| Week | Goal |
|------|------|
| 1 | Core feature works |
| 2 | Basic UI + internal testing |
| 3 | Ship to real users |

**Set a deadline. Ship ugly. Learn fast.**

---

## What mistakes should I avoid?

| Mistake | Why it fails |
|---------|--------------|
| Adding too many features | Dilutes focus, delays launch |
| Not launching early enough | Waiting for perfect = never launching |
| Ignoring feedback | Building blind |
| Confusing interest with validation | "Looks great" ≠ "I'll pay" |
| Building for wrong users | Early adopters ≠ target market |

---

# Part 3: Vibe Coding

*How to use AI to build fast.*

---

## What is vibe coding?

> "You talk to your code, accept LLM suggestions, copy-paste error messages, and pray it works. And it mostly does." — Andrej Karpathy

**Vibe coding** = AI-assisted development where you describe what you want and AI generates the code.

---

## What is vibe coding NOT?

- ❌ Pasting prompts and hoping for the best
- ❌ Shipping code you don't understand
- ❌ Skipping security or architecture
- ❌ Letting AI make all decisions

**Key rule:** If you can't read the code AI generates, don't ship it.

---

## How does the vibe coding loop work?

```
Describe → Generate → Review → Test → Repeat
```

| Step | What you do |
|------|-------------|
| 1. Describe | Explain what you want to build (be specific) |
| 2. Generate | AI creates the first implementation |
| 3. Review | You review and correct mistakes |
| 4. Test | Test immediately — don't batch |
| 5. Repeat | Commit often, small changes |

---

## When does vibe coding work?

| Use case | Why |
|----------|-----|
| Demos and prototypes | Fast validation, throwaway code OK |
| Landing pages | Simple, low risk |
| Internal tools | Less security pressure |
| Learning/exploring | Rapid iteration |

---

## When does vibe coding NOT work?

| Use case | Why |
|----------|-----|
| Production with real user data | Security vulnerabilities |
| Complex backends | AI creates inconsistent mess as codebase grows |
| Anything with payments | Too risky without expert review |
| Scaling beyond 100 users | Architecture breaks |

---

## Can I vibe code as a non-technical founder?

**Reality check from Reddit:**

> "I haven't seen anybody who vibecoded entire applications without knowing coding. I have seen landing pages that are vibecoded."

| Approach | Works for |
|----------|-----------|
| Vibe code a demo | Getting initial feedback, showing investors |
| Vibe code MVP, hire devs later | Validate idea cheap, then rebuild properly |
| Hire dev from start | Complex products, security-critical, B2B |

**The honest truth:** Vibe coding is great for demos. For real MVPs with paying users, most non-technical founders eventually need dev help — either to review/fix AI code or rebuild from scratch.

---

## What are the pros and cons?

| Pro | Con |
|-----|-----|
| 10x faster to prototype | Security holes you won't catch |
| Lower barrier to start | Technical debt accumulates fast |
| Instant context recovery | AI makes poor decisions as code grows |
| Validates ideas cheap | May need full rewrite later |

---

## What should I do if I vibe code?

- [ ] **Plan first** — Create implementation plan before coding
- [ ] **Be specific** — Vague prompts = bad code
- [ ] **Review everything** — Don't blindly accept
- [ ] **Test constantly** — Don't batch testing
- [ ] **Know when to stop** — Get dev help before users pay

---

# Part 4: Tools

*Which AI models and tools to use.*

---

## Which AI model should I use?

| Model | Best for |
|-------|----------|
| Claude Sonnet 4.5 | Coding, debugging, refactoring |
| Claude Opus 4.5 | Complex architecture, hard problems |
| GPT-5 | Brainstorming, marketing copy, ideas |
| GPT-4o | Quick tasks, good enough for most |
| v0.dev | UI prototypes (React) |
| Midjourney | Icons, graphics |

---

## What vibe coding tools exist?

| Tool | What it does |
|------|--------------|
| **Cursor** | AI-enhanced VS Code fork, best for coding |
| **Windsurf** | Standalone AI editor, good flow |
| **Claude Code** | Terminal-based, powerful for devs |
| **Bolt.new** | Full app generation (hit or miss) |
| **Lovable** | Similar to Bolt, generates full apps |

---

# Part 5: Next Steps

*What to do when MVP is done.*

---

## What do I do after MVP is validated?

1. **Take screenshots** → [Phase 2: Screenshots](README.md#phase-2-screenshots)
2. **Upload to Play Console** → [Closed Testing Guide](closed-testing.md)
3. **Collect feedback** → [Feedback Guide](feedback.md)

---

## Summary

| Question | Answer |
|----------|--------|
| What is MVP? | Smallest product someone will pay for |
| How do I know it's done? | You're slightly embarrassed + a stranger can use it |
| How long does it take? | Max 3 weeks |
| Can I vibe code it? | Demos yes, production with payments needs dev help |
| Which tool should I use? | Claude for code, ChatGPT for ideas |

---

*Ship first. Polish later.*
