# Shipping Playbook

Min personliga loggbok för app-shipping: erfarenheter, lärdomar och metrics.

---

## Hur du använder detta repo

- **Journal** → Skriv dagbok/veckologg i `journal/` med formatet `YYYY-MM-DD-kort-titel.md`
- **Lärdomar** → Logga i `lessons/` (success-factors, frictions, android-closed-testing, etc.)
- **Mallar** → Backlog- och changelog-mallar finns i `templates/`
- **Metrics** → Uppdatera CSV-filer i `metrics/` (en fil per app)
- **Screenshots** → Spara evidence i `docs/screenshots/` med formatet `YYYY-MM-DD-område-beskrivning.png`
- **Prompts** → Återanvändbara prompts för repo-underhåll i `prompts/`

---

## Namnkonventioner

| Typ | Format | Exempel |
|-----|--------|---------|
| Journal | `YYYY-MM-DD-kort-titel.md` | `2026-01-10-week-01.md` |
| Screenshot | `YYYY-MM-DD-område-beskrivning.png` | `2026-01-17-lotty-feedback-crash.png` |
| Metrics | `closed-testing-{app}.csv` | `closed-testing-lotty.csv` |

---

## Struktur

```
├── journal/           # Löpande loggbok
├── lessons/           # Samlade lärdomar
├── metrics/           # CSV per app
├── templates/         # Mallar för backlog/changelog
├── prompts/           # Återanvändbara prompts
├── docs/screenshots/  # Evidence (länkas i backlog)
└── ROADMAP.md         # Change management-flöde
```

---

*Detta repo uppdateras löpande. Inget påhittat innehåll — endast mina egna erfarenheter.*
