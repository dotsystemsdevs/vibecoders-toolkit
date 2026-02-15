# How to Vibecode

Complete workflow from idea to shipped code.

---

## The core loop

| Step | Action |
|------|--------|
| 1. Describe | Be specific about what you want |
| 2. Generate | Let AI create the code |
| 3. Review | Read everything, don't blindly accept |
| 4. Test | Test immediately, don't batch changes |
| 5. Repeat | Commit after every working change |

---

## Rules

1. Plan first — write an implementation plan before any code
2. Be specific — vague prompts produce bad code
3. Review everything — AI makes mistakes
4. Test constantly — don't accumulate untested changes
5. Know when to stop — get developer help before users pay

---

## UI: Build screen by screen

| Step | Action |
|------|--------|
| 1 | Describe your app to AI, ask how screens should be structured |
| 2 | Build home screen first, refine until satisfied |
| 3 | Build one screen at a time — don't move on until it works |
| 4 | Review all screens together, make minor adjustments |
| 5 | Build settings screen last, then standardize colors and buttons |

**Why standardize last?** Standardizing early limits creativity. Get the screens right first, then make them consistent.

---

## Content guidelines

| Rule | Reason |
|------|--------|
| Write copy yourself first | AI-generated copy feels generic |
| Use AI only for translation or polish | Keeps the authentic voice |
| Take screenshots during development | You'll need content later |

---

## Tools that didn't work

| Tool | Problem |
|------|---------|
| bolt.new | Wasted credits, poor UI quality |
| rapidexpo | Same issues as bolt.new |
| "Build all components at once" | Produces ugly code with errors |
| UX/UI communities for feedback | Got banned (wrong audience) |
| Discord/Telegram for recruiting | Almost no responses, use Reddit instead |

---

## Backend: Security first

When adding backend, authentication, or payment processing, the risk increases significantly.

| Step | Action |
|------|--------|
| 1 | Write high-level plan all the way to production |
| 2 | Ask AI to break each step into detailed sub-steps |
| 3 | Feed AI one sub-step at a time |
| 4 | Ask what tasks can be done in parallel |

---

## Security checklist

Before shipping any backend code:

- Review all API endpoints for authentication
- Check for SQL injection vulnerabilities
- Check for XSS vulnerabilities
- Use environment variables for all secrets
- Test with invalid and malicious inputs
- Get a security review from an experienced developer

---

## Common mistakes

| Mistake | What happened | Better approach |
|---------|---------------|-----------------|
| Told AI "do what you think is best" | Bad architecture, poor results | Be specific, steer the plan yourself |
| Skipped security review | Shipped with vulnerabilities | Always review backend security |
| No version control discipline | Lost work, messy commit history | Use feature branches, commit often |

---

## Productivity patterns

Observations from shipping multiple projects:

| Observation | What we do now |
|-------------|----------------|
| Most productive in the morning | Schedule hard work before lunch |
| Energy dip after workout | Exercise after other work is done |
| UI perfectionism kills momentum | Set time limits, ship "good enough" |
| Reddit becomes a distraction | Schedule specific Reddit time |
| Risk of burnout | Plan regular rest days |

---

## Example: Good vs bad prompts

**Bad prompt:**
"Make a login screen"

**Good prompt:**
"Make a login screen with email and password text input fields, a blue 'Login' button below them, and a 'Forgot password?' link at the bottom. Use React Native with TextInput components. Match the existing app's blue color scheme (#2196F3). Add email format validation before allowing submit."

The difference: specificity. Good prompts include exact requirements, technologies, and constraints.

---

Be specific. Test immediately. Commit often.
