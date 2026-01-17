# Complete Guide: Ship Your First App

En praktisk guide för att shippa appar till closed testing och få feedback. Baserad på mina egna erfarenheter som junior utvecklare.

*Uppdateras löpande. Inget påhittat — endast saker jag faktiskt testat.*

---

## Innehåll

1. [Innan du börjar](#1-innan-du-börjar)
2. [Closed testing](#2-closed-testing)
3. [Rekrytera testare](#3-rekrytera-testare)
4. [Samla feedback](#4-samla-feedback)
5. [Patch-cykel](#5-patch-cykel)
6. [Content & marknadsföring](#6-content--marknadsföring)
7. [Produktivitet](#7-produktivitet)
8. [Vanliga misstag](#8-vanliga-misstag)

---

## 1. Innan du börjar

### Mål
- Få appen till closed testing så snabbt som möjligt
- Samla riktig feedback från riktiga användare
- Iterera baserat på feedback, inte gissningar

### Verktyg jag använder
- **Figma** — screenshots och basic branding för Play Store
- **GitHub** — versionskontroll + backlog
- **Play Console** — closed testing

### Checklista innan closed testing
- [ ] Appen fungerar (behöver inte vara perfekt)
- [ ] Play Store-bilder finns (Figma)
- [ ] AAB byggt och uppladdat
- [ ] Closed testing-grupp skapad

---

## 2. Closed testing

### Varför closed testing först?
- Få feedback innan du går live
- Hitta buggar tidigt
- Testa om behovet finns

### Mina mål
- **Medlemmar:** sikta på 30+ för att få tillräckligt med data
- **Tidsram:** ~2 veckor aktiv testning innan nästa stora uppdatering

### Rebranding-exempel
- Lotty: "lotty-tracker" → neutral "win/loss tracker"
- Mulligan: "Lost Ball Counter" → "Mulligan: The Real Scorecard"

*Lärdomen: neutralare namn kan nå bredare målgrupp.*

---

## 3. Rekrytera testare

### Vad som fungerade

| Kanal | Resultat |
|-------|----------|
| r/AndroidClosedTesting | ✅ Bäst resultat |
| Nischforum (t.ex. golfforum) | ✅ Bra feedback + validerar behov |
| Reddit test-for-test | ✅ Fungerar med rätt strategi |

### Vad som INTE fungerade

| Kanal | Resultat |
|-------|----------|
| Discord | ❌ 1 person |
| Telegram | ❌ Inget svar |
| Reddit UX/UI-grupper | ❌ Ban + negativ respons |

### Strategi som fungerade
1. Publicera i r/AndroidClosedTesting
2. Sätt på notiser
3. Svara snabbt på "test for test"-kommentarer
4. Schemalägg tid för Reddit (undvik 24/7)
5. Var aktiv när USA är vakna

### Siffror (Lotty closed testing)

| Dag | Members | Users |
|-----|---------|-------|
| Dag 1 | 25 | 1 |
| Dag 2 | 40 | 24 |
| Dag 3 | 57 | 41 |
| Dag 4 | 73 | 53 |
| Dag 5 | 86 | 70 |
| Dag 6 | 90 | 69 |
| Dag 7 | 96 | 71 |

*Lärdomen: mindre effort efter dag 3-4 gav fortfarande resultat.*

### Risker
- Testare kan bli inaktiva efter 14 dagar
- Test-for-test kräver motprestation (tidskostnad)

---

## 4. Samla feedback

### Process
1. **Screenshotta** all feedback direkt
2. **Spara** i `docs/screenshots/YYYY-MM-DD-area-desc.png`
3. **Logga** i backlog med länk till screenshot
4. **Prioritera** — inte allt behöver fixas nu

### Nischforum = guldgruva
Posta i forum där din målgrupp finns. Exempel: golfforum för Mulligan gav:
- Mycket bra feedback
- Förbättringsförslag
- Bekräftelse att behovet finns

---

## 5. Patch-cykel

### Flöde

```
ship → samla feedback → backlog → prioritera → patch → ship
```

### Regler
1. Ge appen ~1 vecka innan nästa uppdatering (distans → bättre beslut)
2. Välj 3–5 items per patch (inte allt på en gång)
3. Sätt prio: P1 = måste fixas, P2 = bör fixas, P3 = kan vänta

### Filer
- `templates/BACKLOG.md` — alla inkommande items
- `templates/CHANGELOG.md` — endast det som shippat

---

## 6. Content & marknadsföring

### Instagram — vad jag lärt mig
- Låg respons initialt (0 likes)
- GPT-copy känns dålig och tar tid
- **Lösning:** skriv själv först, använd AI endast för översättning

### Strategi nu
- Autentiska uppdateringar om app-resan
- Dokumentera utvecklingen (screenshots under dagen)
- Reels för reach/viralitet (testar)

### Tips
- Ta fler screenshots under dagen för content
- Håll det äkta — folk märker fejk

---

## 7. Produktivitet

### Vad jag lärt mig om mig själv
- Mest effektiv på förmiddagen
- Dip efter träning → flyttade träning till efter plugg
- Svårt att följa schema exakt (många fönster/tabbar)

### UI-perfektionism
- **Problem:** fastnar i detaljer, blir frustrerad
- **Lösning:** sätt tidsgräns, ship "good enough"

### Schemaläggning
- Schemalagd Reddit-tid varje dag (inte 24/7)
- Planera lediga dagar (undvik burnout)

---

## 8. Vanliga misstag

| Misstag | Vad som hände | Lärdom |
|---------|---------------|--------|
| Posta i UX/UI-grupper | Ban + mobbad | Använd rätt forum för rätt syfte |
| Discord/Telegram för rekrytering | Nästan ingen respons | Fokusera på Reddit |
| UI-perfektionism | Fastnade, blev frustrerad | Ship först, polera sen |
| GPT för all copy | Kändes dåligt, tog tid | Skriv själv, AI för polish |
| Reddit 24/7 | Svårt att släppa | Schemalägg specifik tid |
| Uppdatera direkt efter feedback | Impulsiva beslut | Vänta ~1 vecka, nya ögon |

---

## Nästa steg för mig

- [ ] Skriva MVP för nästa app
- [ ] Testa "plan mode" (såg på YouTube)
- [ ] Planera lediga dagar
- [ ] Fortsätta dokumentera

---

*Skapad av en junior dev som lär sig genom att shippa. Uppdateras efter varje vecka.*
