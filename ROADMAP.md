# Change Management (Backlog & Changelog)

## Regler
- **Screenshots:** `docs/screenshots/YYYY-MM-DD-area-desc.png`
- **Backlog-item kräver:** Priority + Target version + Evidence
- **Changelog:** uppdateras bara när något shippar

## Flöde

```
ship → feedback → backlog → triage → patch → ship
```

1. **Ship** (closed test) → skriv under `CHANGELOG.md` → `[Unreleased]`
2. **Samla feedback** → spara i `docs/screenshots/`
3. **Logga** → `BACKLOG.md`
4. **Triage** → välj 3–5 items → sätt P1/P2 + Target version
5. **1-dag patch** → status: In progress → Ready for review → Done
6. **Ship igen** → flytta `[Unreleased]` till ny version, töm `[Unreleased]`

## Filer

| Fil | Syfte |
|-----|-------|
| `BACKLOG.md` | Allt inkommande |
| `CHANGELOG.md` | Ship-history |
| `docs/screenshots/` | Evidence (länkas i backlog) |
