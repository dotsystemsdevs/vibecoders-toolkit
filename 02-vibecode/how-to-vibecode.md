# How to Vibecode

Practical workflow from idea to shipped code.

---

## The 5-step loop

Every feature follows the same pattern:

**1. Describe (2 minutes)**

Write exactly what you want. Include:
- What it should do
- What technology to use
- What it should look like
- Edge cases to handle

**2. Generate (30 seconds)**

Let AI create the code. Don't interrupt. Let it finish.

**3. Review (5 minutes)**

Read every line. Ask yourself:
- Does this make sense?
- Are there edge cases missing?
- Could this break something?
- Is there a security issue?

**4. Test (3 minutes)**

Run the code. Test:
- Happy path (normal usage)
- Edge cases (empty inputs, wrong format)
- Breaking scenarios (network offline, large data)

**5. Commit (30 seconds)**

If it works, commit. If not, iterate from step 1.

**Total: ~10 minutes per feature**

---

## Rules that matter

### Rule 1: Be specific

**Bad:** "Add validation to the form"

**Good:** "Add email validation to the login form. Check format with regex. Show red error text below input if invalid. Prevent submit button until email is valid. Use email-validator library."

**Why it matters:** Vague prompts = AI guesses. Guesses = bugs.

### Rule 2: Review everything

AI will confidently generate broken code. It doesn't know your business logic. It doesn't test edge cases.

**Real example from our projects:**

AI generated password validation that accepted empty strings. We caught it in review. If we hadn't, users could create accounts with no password.

**Time saved by AI:** 15 minutes  
**Time lost if we shipped the bug:** 2 hours debugging + user complaints

### Rule 3: Test immediately

Don't batch changes. Test after every generation.

**Why:** If you generate 5 features and then test, you won't know which one broke things.

### Rule 4: Commit often

Every working feature = one commit.

**Why:** Easy rollback when something breaks. Clear history of what changed.

### Rule 5: Know when to stop

If you're adding backend, auth, or payments — stop. Get a security review from an experienced developer.

**Real cost of shipping vulnerabilities:**
- SQL injection = entire database leaked
- XSS attack = user sessions stolen
- Missing auth = unauthorized access to paid features

---

## UI workflow: Build screen by screen

**Wrong approach:** "Build the entire app"  
**Result:** Messy code, inconsistent design, hard to fix

**Right approach:** One screen at a time

### Step-by-step

**Day 1: Home screen**
1. Describe to AI how the home screen should look
2. Generate and review
3. Refine until it looks right
4. Commit

**Day 2: Feature screen**
1. Build the next screen
2. Test navigation between screens
3. Commit

**Day 3-N: Repeat**

One screen per day. By the end of the week, you have a working app.

**Day N+1: Settings screen**

Always build settings last. It's the least important screen.

**Day N+2: Standardization**

Now go back and make colors/buttons consistent across all screens.

**Why standardize last?**

If you set strict design rules on day 1, you'll fight against them while building. Get the features right first, then make them pretty.

---

## Backend workflow: Plan before you code

Backend = high risk. One mistake = data breach.

### Pre-coding checklist

Before generating any backend code:

1. **Write the full plan on paper**
   - What endpoints do you need?
   - What does each endpoint do?
   - Who can access each endpoint?
   - What data does each endpoint return?

2. **Break plan into sub-steps**
   - Ask AI: "Break this plan into detailed sub-steps"
   - Review the sub-steps
   - Fix anything that seems wrong

3. **Feed AI one sub-step at a time**
   - Don't give AI the full plan
   - One sub-step = one generation
   - Review and test before moving to next step

### Security review checklist

Before shipping ANY backend code:

- [ ] Every endpoint checks authentication
- [ ] SQL queries use parameterized statements (no string concatenation)
- [ ] User inputs are validated and sanitized
- [ ] Secrets are in environment variables (not hardcoded)
- [ ] Error messages don't leak sensitive info
- [ ] Rate limiting is implemented
- [ ] HTTPS is enforced
- [ ] An experienced developer reviewed the code

**If you skip the security review, don't ship to real users.**

---

## Common mistakes (and how to avoid them)

### Mistake 1: "Do what you think is best"

**What happened:** AI generated complex architecture we didn't need. Took 2 days to untangle.

**Better approach:** Always be specific. "Use local storage, no database" is better than "handle data storage".

### Mistake 2: Skipping commit messages

**What happened:** Broke something, couldn't remember which commit was working. Had to rewrite from scratch.

**Better approach:** Every commit gets a clear message: "Add email validation to login form".

### Mistake 3: Building everything at once

**What happened:** Generated 10 components. 3 had bugs. Spent 4 hours finding which ones.

**Better approach:** Generate one thing, test it, commit it. Repeat.

### Mistake 4: Trusting AI with security

**What happened:** Almost shipped an app with no authentication on the API. Anyone could read all user data.

**Better approach:** Assume AI gets security wrong. Always review. Always test.

---

## Productivity patterns from real projects

### Morning coding

**Observation:** Most productive 9am-12pm.

**What we do:** Schedule vibecoding sessions in the morning. Afternoons for meetings/planning.

### Time limits for perfectionism

**Observation:** Spent 3 hours tweaking button colors.

**What we do:** Set 30-minute timer. When it beeps, ship what you have.

### Regular breaks

**Observation:** After 2 hours of continuous coding, quality drops.

**What we do:** 50 minutes work, 10 minutes break. Every 2 hours, 30-minute break.

---

## Real examples: Good vs bad prompts

### Example 1: Login screen

**Bad (vague):**
"Make a login screen"

**Good (specific):**
"Create a login screen for a React Native app. Two TextInput fields: email (keyboard type: email-address) and password (secureTextEntry: true). Blue button labeled 'Login' below inputs. If email format is invalid, show red text 'Invalid email' below email field. Button disabled until both fields are filled. Use existing theme colors: primary blue #2196F3, error red #f44336."

**Result:** AI generated exactly what we needed. Zero revisions.

### Example 2: Data storage

**Bad (ambiguous):**
"Save the user's data"

**Good (specific):**
"Save user's todo items to AsyncStorage in React Native. Key format: 'todos_${userId}'. Value: JSON array of objects with id (string), text (string), completed (boolean), createdAt (ISO date string). Load on app start. Update after every add/delete/toggle. Handle AsyncStorage errors with try/catch, show alert if save fails."

**Result:** AI generated complete storage logic with error handling. Worked first try.

### Example 3: API call

**Bad (dangerous):**
"Fetch data from the API"

**Good (safe):**
"Fetch user profile from GET /api/user/{id}. Include Authorization header with token from AsyncStorage. Handle 3 cases: success (200) - show data, unauthorized (401) - clear token and redirect to login, error (500) - show 'Server error, try again' message. Set 10-second timeout. Show loading spinner while fetching."

**Result:** AI generated proper error handling and authentication.

---

## Time benchmarks from real projects

**Project 1: Todo app**
- Total time: 38 hours
- Features: Add/edit/delete todos, local storage, notifications
- AI-generated lines: ~2,000
- Lines we rewrote: ~300 (15%)
- Critical bugs caught in review: 8
- Bugs shipped to users: 0

**Project 2: Golf ball tracker**
- Total time: 42 hours
- Features: Track balls, rounds, stats, charts
- AI-generated lines: ~2,500
- Lines we rewrote: ~400 (16%)
- Critical bugs caught in review: 11
- Bugs shipped to users: 2 (minor UI glitches)

**Project 3: Income tracker**
- Total time: 36 hours
- Features: Log income/expenses, export to xlsx
- AI-generated lines: ~1,800
- Lines we rewrote: ~250 (14%)
- Critical bugs caught in review: 6
- Bugs shipped to users: 1 (export formatting)

**Pattern:** ~15% of AI code needs rewriting. Thorough review catches critical bugs before users see them.

---

## Bottom line

Vibecoding is fast, but not magic.

**What makes it work:**
- Specific prompts
- Thorough review
- Immediate testing
- Frequent commits
- Knowing when to stop

**What breaks it:**
- Vague prompts
- Blindly accepting AI code
- Batching changes
- Skipping security review

Use it to ship MVPs fast. Don't use it to skip proper development for production apps with paying users.
