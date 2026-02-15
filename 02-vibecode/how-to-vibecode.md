# How to Vibecode

The complete workflow.

---

## The loop

| Step | Action |
|------|--------|
| 1. Describe | Be specific about what you want |
| 2. Generate | Let AI create the code |
| 3. Review | Read it, don't blindly accept |
| 4. Test | Test immediately, don't batch |
| 5. Repeat | Commit after every working change |

---

## Rules

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

### Content tips

| Rule | Why |
|------|-----|
| Write copy yourself | GPT copy feels fake |
| AI for translation only | Keeps it authentic |
| Screenshot during the day | Content for later |

### Tools that DIDN'T work

| Tool | Problem |
|------|---------|
| bolt.new | Wasted credits, bad UI |
| rapidexpo | Same problem |
| "Build all at once" | Ugly, errors, hard to change |
| UX/UI groups | Got banned |
| Discord recruiting | No response, use Reddit |

---

## Backend: Security first

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
| No version control | Lost work, messy history | Branches + commit often |

---

## Productivity patterns

| Observation | What we do |
|-------------|------------|
| Morning = most effective | Hard work before lunch |
| Dip after workout | Workout after work |
| UI perfectionism kills | Time limit, ship "good enough" |
| Reddit addiction | Scheduled time, not 24/7 |
| Burnout risk | Planned rest days |

---

## Example: Good vs bad prompts

**Bad:** "Make a login screen"

**Good:** "Make a login screen with email + password fields, a 'Login' button, and a 'Forgot password?' link. Use React Native, match the existing blue theme, validate email format before submit."

---

*Be specific. Test immediately. Commit often.*
