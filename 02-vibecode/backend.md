# Backend & Security

## Background

Vibecoding works great for frontends and MVPs. But the moment you add a backend, the risk goes up. AI-generated backend code often has security vulnerabilities.

---

## Do this

### Plan mode strategy

| Step | Action |
|------|--------|
| 1 | Write high-level plan with steps all the way to production |
| 2 | When starting a step, ask AI to write detailed sub-steps |
| 3 | Give AI sub-steps one at a time |
| 4 | Ask what you can do in parallel |

### Security checklist

- [ ] Review all API endpoints for auth
- [ ] Check for SQL injection, XSS
- [ ] Use environment variables for secrets
- [ ] Test with invalid inputs
- [ ] Do a security review before shipping

---

## Mistakes we made

| Mistake | What happened | What to do instead |
|---------|---------------|-------------------|
| "Do what you think is best" to AI | Bad architecture, bad results | Be specific, steer the plan yourself |
| Skipping security review | Shipped with vulnerabilities | Always review backend security |
| No version control discipline | Lost work, messy history | Use branches + commit often |

---

*The more you know, the better you prompt.*
