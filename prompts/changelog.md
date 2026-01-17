```text
You are my repo maintainer. Create (or refactor) CHANGELOG.md for my app following Keep a Changelog + Semantic Versioning.

GOAL
Make CHANGELOG.md strict and easy to maintain for frequent releases.

REQUIREMENTS
1) File name: CHANGELOG.md (repo root).
2) Keep the standard Keep a Changelog intro.
3) Ensure an [Unreleased] section exists and ALWAYS contains these headings in this exact order:
   ### Added
   ### Changed
   ### Fixed
   ### Known Issues
4) Release format must be: `## [x.y.z] - YYYY-MM-DD`
5) Known Issues bullets must be short and actionable:
   `**Issue**: symptom — workaround/next action`
6) Keep reference links at the bottom:
   - [unreleased]: compare last tag to HEAD
   - [x.y.z]: compare previous tag to this tag (or release tag link)
7) Do not include backlog-style tasks. Only include shipped changes.

OUTPUT
Return the full CHANGELOG.md content only (no explanations).
```
