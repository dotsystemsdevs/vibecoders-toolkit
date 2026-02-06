# Vibecode

## Background

AI-assisted development where you describe what you want and AI generates code. Fast for MVPs, dangerous for production.

```
Describe → Generate → Review → Test → Repeat
```

---

## Do this

### The loop

| Step | What |
|------|------|
| Describe | Be specific about what you want |
| Generate | Let AI create the code |
| Review | Don't blindly accept — read it |
| Test | Test immediately, don't batch |
| Repeat | Commit after every working change |

### Tools

| Tool | What | Our take |
|------|------|----------|
| **Cursor** | AI-enhanced VS Code | Best for daily coding |
| **Claude Code** | Terminal-based AI | Powerful for complex tasks |
| **Windsurf** | Standalone AI editor | Good alternative |
| **Bolt.new** | Full app generation | Wasted credits, skip it |

### Models

| Model | Best for |
|-------|----------|
| Claude Sonnet | Coding, debugging |
| Claude Opus | Complex architecture |
| GPT-5 | Brainstorming, marketing copy |
| v0.dev | UI prototypes |

### Rules

- [ ] Plan first — write an implementation plan before coding
- [ ] Be specific — vague prompts = bad code
- [ ] Review everything — don't blindly accept
- [ ] Test constantly — don't batch
- [ ] Know when to stop — get dev help before users pay

---

## When it works vs. when it doesn't

| Works | Doesn't work |
|-------|-------------|
| Demos, prototypes | Production with user data |
| Landing pages | Complex backends |
| Internal tools | Payment systems |
| MVPs | Apps with 100+ users |

---

## Evidence

We built all 3 apps (Slothy, Mulligan, Lotty) using vibecoding with Claude + Cursor. Total time from idea to closed testing: ~1 week per app. Zero backend — all offline, all local storage. That's the sweet spot for vibecoding.

The moment you add a backend, authentication, or payments — slow down and review everything.
