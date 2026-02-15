# What is Vibecode

## Definition

Vibecoding is AI-assisted development where you describe requirements in natural language and AI generates working code. You then review, test, and iterate.

The name comes from the workflow: fast, intuitive, high-energy coding sessions where you "vibe" with the AI rather than manually writing every line.

## How it works

Modern AI models (Claude Sonnet, GPT-4) have been trained on billions of lines of code from GitHub, Stack Overflow, and documentation. They recognize patterns and can translate descriptions into implementations.

**Example:**
- You: "Add email validation to the login form"
- AI: Generates regex pattern, error handling, UI feedback
- You: Review for edge cases, test with invalid emails, commit

## The critical trade-off

**Speed vs. Control**

- You ship 10x faster than traditional coding
- But you must review 3x harder than code you wrote yourself
- AI doesn't understand business logic, edge cases, or security context
- Every generated line is a potential bug or vulnerability

## When to use vibecoding

| Use case | Why it works | Risk level |
|----------|--------------|------------|
| MVPs with no backend | AI knows common UI patterns | Low |
| Landing pages | Static content, well-understood structure | Low |
| Internal tools | Limited users, low security requirements | Low-Medium |
| Prototypes for user testing | Speed matters more than quality | Low |

## When NOT to use vibecoding

| Use case | Why it fails | Risk level |
|----------|--------------|------------|
| Production apps with paying users | AI introduces bugs users encounter | High |
| Payment processing | Security vulnerabilities = liability | Critical |
| Authentication systems | One mistake = data breach | Critical |
| Apps with 100+ active users | Technical debt accumulates fast | High |

## Tools

**Recommended:**
- **Cursor** (AI-enhanced VS Code) — best for daily work
- **Claude Code** (terminal-based) — complex refactoring
- **Claude Sonnet** model — best code quality

**Avoid:**
- **Bolt.new** — generates low-quality code, burns credits
- **GPT-3.5** — outdated, poor code quality

## Real-world benchmark

**Project:** 3 Android apps (todo app, golf tracker, income tracker)

**Timeline:** 1 week each (40 hours per app)

**Stack:** React Native, Expo, local storage only

**Result:** All shipped to Google Play Store, 137 combined users

**What made it work:**
- Zero backend (no auth, no database, no API)
- Well-known patterns (todo lists, form inputs, local storage)
- Immediate testing after each change
- No paying users during development

**Critical lesson:** The moment we considered adding backend or payments, we stopped and planned to hire a developer for security review.

## The workflow

```
1. Write specific requirement
2. AI generates code
3. Review line by line (don't skip)
4. Test immediately
5. Commit if it works
6. Repeat
```

**Time breakdown for a typical feature:**
- Writing requirement: 2 minutes
- AI generation: 30 seconds
- Your review: 5 minutes
- Testing: 3 minutes
- **Total: ~10 minutes per feature**

Compare to traditional coding:
- Understanding requirement: 5 minutes
- Writing code: 20 minutes
- Debugging: 10 minutes
- Testing: 5 minutes
- **Total: ~40 minutes per feature**

**4x speed increase, but only if you review properly.**

## Bottom line

Vibecoding is a tool, not magic. It accelerates MVPs and prototypes. It's dangerous for production systems with security requirements.

Use it to ship fast, test ideas, and validate products. Don't use it to cut corners on security or quality for paying users.
