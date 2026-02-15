# Backend

Adding backend, auth, or payments. High risk. Review everything.

---

## Plan mode strategy

| Step | Action |
|------|--------|
| 1 | Write high-level plan to production |
| 2 | Ask AI for detailed sub-steps |
| 3 | Give AI one sub-step at a time |
| 4 | Ask what can run in parallel |

---

## Security checklist

- [ ] Review all API endpoints for auth
- [ ] Check SQL injection, XSS
- [ ] Environment variables for secrets
- [ ] Test with invalid inputs
- [ ] Security review before shipping

---

## Mistakes we made

| Mistake | What happened | Do instead |
|---------|---------------|------------|
| "Do what you think" to AI | Bad architecture | Be specific, steer the plan |
| Skip security review | Shipped vulnerabilities | Always review backend |
| No version control discipline | Lost work, messy history | Branches + commit often |

---

*The more you know, the better you prompt.*
