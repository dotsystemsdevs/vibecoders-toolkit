# What is Vibecode

## Background

Traditional coding requires years of learning syntax, frameworks, and best practices. Vibecoding flips this: you focus on describing what you want to build, and AI generates the code for you.

This approach works because modern AI models (like Claude, GPT-4) have been trained on millions of code examples. They understand patterns, common solutions, and can translate natural language descriptions into working code.

**The trade-off:** Speed vs. control. You build faster, but you need to review carefully. AI makes mistakes. It doesn't understand your full context. It can introduce security vulnerabilities.

**The workflow:**

```
Describe what you want → AI generates code → You review it → Test immediately → Repeat
```

This loop is vibecoding. Fast iteration. Constant testing. Ship MVPs in days instead of months.

## When it makes sense

Vibecoding is not for everything. It has a sweet spot.

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

Vibecoding works when the problem is well-understood and the AI has seen similar solutions. Building a todo app? AI has seen thousands. Building a login screen? AI knows the patterns.

It breaks down when:
- The problem is novel or domain-specific
- Security is critical (payments, user data)
- The codebase is large and complex
- You need optimal performance

## Evidence from real projects

We shipped 3 Android apps in 1 week each using Claude + Cursor. Zero backend, all offline, local storage only. Each app took roughly 40 hours from idea to Google Play Store.

**That's the sweet spot:** simple apps with no server, no authentication, no payments.

The moment you add backend, authentication, or payments — slow down. Review everything. Get an experienced developer to audit the security before shipping.
