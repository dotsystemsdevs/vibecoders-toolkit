# Roadmap

Min samlade erfarenhet från app-shipping. Uppdateras löpande.

---

## Android Closed Testing

### Framgångsfaktorer
- Publicera på r/AndroidClosedTesting
- Sätt på notiser, svara snabbt på "test for test"
- Schemalägg tid för att vara aktiv när USA är vakna
- Posta i forum i appens nisch för att få tidig feedback från målgruppen
- Mindre effort på Reddit kan fortfarande ge resultat (effektivitet > volym)
- Ge appen ~1 vecka innan nästa uppdatering (distans → bättre beslut)
- Screenshotta all feedback direkt och spara som evidence

### Friktioner
- Test-for-test kräver motprestation (tidskostnad)
- Risk för inaktiva testare efter 14 dagar
- Discord gav 1 person
- Telegram gav inget
- Reddit UX/UI-grupper: negativ friktion (ban/mobbad)
- Svårt att släppa Reddit pga press att testet ska lyckas

### Uppföljning — Lotty

| Dag | Members | Users |
|-----|---------|-------|
| Jan 9 | 25 | 1 |
| Jan 10 | 40 | 24 |
| Jan 11 | 57 | 41 |
| Jan 12 | 73 | 53 |
| Jan 13 | 86 | 70 |
| Jan 14 | 90 | 69 |
| Jan 15 | 96 | 71 |

### Uppföljning — Mulligan

| Dag | Members | Users |
|-----|---------|-------|
| Jan 15 | 28 | 1 |
| Jan 16 | 44 | — |
| Jan 17 | 67 | — |

---

## Change Management

Enkel loop: **ship → samla → logga → patcha → ship**

### Regler
- Screenshots: `docs/screenshots/YYYY-MM-DD-area-desc.png`
- Backlog entry måste ha: prio + target version + evidence
- Changelog uppdateras bara när något shippar

### Flöde
1. **Ship** (closed test) → skriv bullets i CHANGELOG.md under `[Unreleased]`
2. **Samla feedback** → spara screenshots i `docs/screenshots/`
3. **Logga** → skapa item i BACKLOG.md
4. **Triage** → välj 3–5 items → sätt P1/P2 + target version
5. **1-dag patch** → status: In progress → Ready → Done
6. **Ship igen** → flytta `[Unreleased]` till ny version

### Filer
- `templates/BACKLOG.md` — mall för backlog
- `templates/CHANGELOG.md` — mall för changelog
- `docs/screenshots/` — evidence (länkas i backlog)

---

## Övrigt

### Produktivitet
- Mest effektiv på förmiddagen, dip efter träning
- Flyttade träning till efter plugg
- Svårt att följa schema exakt (många fönster/tabbar)
- UI-perfektionism → fastnar, blir frustrerad

### Content & Instagram
- Instagram: låg respons initialt
- GPT-copy känns dålig → skriv själv först, be om översättning
- Ta fler screenshots under dagen för content

### Verktyg
- Figma: screenshots + basic branding för store/social

---

## Åtgärder

- [ ] Skriva MVP för nästa app
- [ ] Strukturera upp erfarenhetshantering
- [ ] Planera "lediga dagar"
