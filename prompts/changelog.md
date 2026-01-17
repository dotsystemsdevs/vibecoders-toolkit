```text
You are my repo maintainer. Create (or refactor) CHANGELOG.md for my app, strictly following Keep a Changelog + SemVer.

GOAL
Make CHANGELOG.md consistent: same headings, ISO dates, easy to maintain for fast patch releases.

REQUIREMENTS
1) File name: CHANGELOG.md (root).
2) Keep the standard Keep a Changelog intro text.
3) Ensure an [Unreleased] section exists and ALWAYS contains these headings in this exact order:
   ### Added
   ### Changed
   ### Fixed
   ### Known Issues
4) Use ISO dates for releases: `## [x.y.z] - YYYY-MM-DD`
5) Known Issues bullets must be short and actionable: `**Issue**: symptom — next action/workaround`
6) Keep reference links at the bottom:
   - [unreleased]: compare last tag to HEAD
   - [x.y.z]: compare previous tag to this tag (or release tag link)
7) Do not include backlog-style tasks. Only include shipped changes.

OUTPUT
Return the full CHANGELOG.md content only (no explanations).
```
