# Backend & Security

AI backend = risky. Review everything.

---

## Plan mode strategy

| Step | Action |
|------|--------|
| 1 | Write high-level plan to production |
| 2 | Ask AI for detailed sub-steps |
| 3 | Give AI one sub-step at a time |
| 4 | Ask what can run parallel |

---

## Security checklist

- [ ] Review all API endpoints for auth
- [ ] Check SQL injection, XSS
- [ ] Environment variables for secrets
- [ ] Test with invalid inputs
- [ ] Security review before shipping

---

## Mistakes

| Mistake | What happened | Do instead |
|---------|---------------|------------|
| "Do what you think" to AI | Bad results | Be specific |
| Skip security review | Shipped vulnerabilities | Always review |
| No version control | Lost work | Branches + commit often |

---

*The more you know, the better you prompt.*
