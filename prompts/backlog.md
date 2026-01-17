```text
You are my repo maintainer. Create (or refactor) BACKLOG.md for my app.

GOAL
A single markdown backlog that is fast to maintain for 1-day patch cycles.

REQUIREMENTS
1) File name: BACKLOG.md (root).
2) Keep it technical and minimal.
3) Include these sections in this order:
   - Entry template
   - P1 — Next patch
   - P2 — Planned
   - P3 — Later
   - Ready for review
   - Done (keep short)
4) Entry template must be markdown with a table containing:
   - Status (New / In progress / Blocked / Ready for review / Done)
   - Priority (P1 / P2 / P3)
   - Type (Bug / Feature / Task / Feedback)
   - Target version (e.g., 1.1.1 / 1.2.0 / Later)
   - Evidence (path to screenshot) using: `docs/screenshots/YYYY-MM-DD-area-desc.png` or N/A
5) Add a one-line rule for screenshots:
   - All screenshots go in `docs/screenshots/` with filename `YYYY-MM-DD-area-desc.png`
6) Next steps must be a checklist where each item starts with a verb.

OUTPUT
Return the full BACKLOG.md content only (no explanations).
```
