# What is Vibecode

## Background

Traditional coding: learn syntax, frameworks, best practices. Takes years.

Vibecoding: describe what you want, AI generates code. Takes hours.

Modern AI models (Claude, GPT-4) trained on millions of code examples. They know patterns. They translate descriptions into working code.

**The trade-off:** Speed vs. control.

You ship faster. You review harder. AI makes mistakes. AI doesn't understand your full context. AI introduces security holes.

**The workflow:**

```
Describe → AI generates → You review → Test → Repeat
```

Fast iteration. Constant testing. Ship MVPs in days, not months.

## When it makes sense

Vibecoding has a sweet spot. Use it wrong, you waste time or ship vulnerabilities.

---

## Tools you need

| Tool | What | Recommended |
|------|------|-------------|
| Cursor | AI-enhanced VS Code | Best for daily coding |
| Claude Code | Terminal-based AI | Complex tasks |
| Windsurf | Standalone AI editor | Alternative |
| Bolt.new | Full app generation | Skip it (wasted credits) |

---

## Models

| Model | Best for |
|-------|----------|
| Claude Sonnet | Coding, debugging |
| Claude Opus | Architecture decisions |
| GPT-5 | Marketing copy, brainstorming |
| v0.dev | UI prototypes |

---

## When it works

| Works | Doesn't work |
|-------|--------------|
| Demos, MVPs | Production with paying users |
| Landing pages | Complex backends |
| Internal tools | Payment systems |
| Prototypes | Apps with 100+ users |

---

## Why it works (and why it doesn't)

Works when the problem is well-known. Todo app? AI's seen thousands. Login screen? AI knows the pattern.

Breaks when:
- Problem is novel
- Security matters (payments, user data)
- Codebase is large
- Performance is critical

## Evidence

We shipped 3 Android apps in 1 week each. Claude + Cursor. Zero backend. All offline. 40 hours per app, idea to Play Store.

**Sweet spot:** Simple apps. No server. No auth. No payments.

Add backend/auth/payments? Slow down. Get a security audit. Don't ship vulnerabilities to paying users.
