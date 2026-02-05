# MVP Guide

Den kompletta guiden för att bygga och lansera din första produkt.

---

# Del 1: Förståelse

*Bakgrund och koncept — läs detta först.*

---

## Vad är ett MVP?

> "The version of a new product which allows a team to collect the maximum amount of validated learning about customers with the least effort." — Eric Ries

**Minimum Viable Product** = Den minsta produkten du kan bygga som någon betalar för.

Nyckelordet är **viable** (livskraftig). Tills någon ger dig pengar har du inte bevisat att produkten fungerar.

---

## Varför spelar MVP roll?

| Anledning | Effekt |
|-----------|--------|
| Snabb validering | Testa idén innan du bygger för mycket |
| Sparar tid | Bygg inte features ingen vill ha |
| Lär av riktiga användare | Inte gissningar |
| Iterera snabbt | Förbättra baserat på feedback |

**Utan MVP:** Du spenderar månader på att bygga något ingen vill ha.

**Med MVP:** Du vet inom veckor om idén fungerar.

---

## Vad är skillnaden mellan MVP, prototyp och färdig produkt?

| Typ | Vad det är | Vem använder det |
|-----|------------|------------------|
| **Prototyp** | Visuellt utkast, mockup, klickbar demo | Internt team |
| **MVP** | Fungerande produkt med kärnfunktioner | Riktiga användare som betalar |
| **Färdig produkt** | Raffinerad, skalbar, polerad | Massmarknad |

**Prototyp** bevisar att konceptet fungerar.
**MVP** bevisar att folk betalar.

---

## Hur vet jag om min idé är validerad?

Demos och positiv feedback känns bra. Men de validerar inte din produkt.

| Vad folk säger | Vad det betyder |
|----------------|-----------------|
| "Det här ser bra ut!" | De gillar idén |
| "Jag skulle definitivt använda detta" | De kanske använder det |
| "Här är mitt kreditkort" | **Validerat** |

**Den hårda sanningen:** Folk älskar att säga att din produkt är bra. Men när du ber om betalning dyker alltid något upp. Tills pengar byter händer gissar du.

---

## Vad är MVP INTE?

| MVP är INTE | MVP ÄR |
|-------------|--------|
| Feature-komplett | En sak som fungerar |
| Perfekt design | Funktionell design |
| Skalbar arkitektur | Kod som kör |
| Alla edge cases hanterade | Happy path fungerar |
| Polerade animationer | Basic feedback (loading, errors) |

---

## Vilka företag började med MVP?

| Företag | MVP | Vad de testade |
|---------|-----|----------------|
| **Uber** | SMS-tjänst för att ringa taxi | Skulle folk beställa resor via telefon? |
| **Dropbox** | Förklaringsvideo (ingen fungerande produkt) | Finns det efterfrågan på molnsynk? |
| **Amazon** | Online bokhandel från ett garage | Kommer folk köpa böcker online? |
| **Spotify** | Landing page med streamingtest | Kan vi göra uppspelning snabb och stabil? |

Ingen av dessa började med hela produkten. De testade en hypotes först.

---

# Del 2: Action

*Konkreta steg — gör detta.*

---

## Hur bygger jag ett MVP? (6 steg)

```
Smärtpunkt → Hypotes → Bygg minimalt → Testa → Lär → Iterera
```

### Steg 1: Identifiera smärtpunkten

Vilket problem löser du? Prata med potentiella användare:

- [ ] Vad gör de idag?
- [ ] Vad frustrerar dem?
- [ ] Skulle de betala för att lösa det?

### Steg 2: Definiera din hypotes

Skriv den så här:

> "Om jag bygger [X], då kommer [målgrupp] betala [Y] eftersom det löser [Z]."

Var specifik. Vaga hypoteser leder till vaga produkter.

### Steg 3: Bygg det minimala

Bara det som behövs för att testa din hypotes. Inget mer.

- [ ] En kärnfunktion som fungerar end-to-end
- [ ] Användaren kan slutföra huvudflödet
- [ ] Basic UI (behöver inte vara snyggt)

### Steg 4: Testa med riktiga användare

Inte vänner. Inte familj. Människor som har problemet och skulle betala för att lösa det.

- [ ] Hitta 5-10 personer i din målgrupp
- [ ] Låt dem använda produkten
- [ ] Observera — fråga inte bara

### Steg 5: Mät det som spelar roll

- [ ] Använde de det?
- [ ] Betalade de?
- [ ] Kom de tillbaka?
- [ ] Vad klagade de på?

### Steg 6: Iterera eller pivotera

Om det fungerar → lägg till mer.
Om det inte fungerar → ändra riktning.

---

## Hur vet jag när mitt MVP är klart?

Din MVP är klar när:

- [ ] **En kärnfunktion fungerar end-to-end**
- [ ] **Du kan demo:a det på 60 sekunder**
- [ ] **En främling kan använda det utan din hjälp**
- [ ] **Du är lite generad** — om du inte är det väntade du för länge

> "If you're not embarrassed by the first version of your product, you've launched too late." — Reid Hoffman

---

## Vilken tidsgräns ska jag sätta?

Om du fortfarande är "nästan klar" efter 3 veckor överbygger du.

| Vecka | Mål |
|-------|-----|
| 1 | Kärnfunktion fungerar |
| 2 | Basic UI + intern testning |
| 3 | Skeppa till riktiga användare |

**Sätt en deadline. Skeppa fult. Lär snabbt.**

---

## Vilka misstag ska jag undvika?

| Misstag | Varför det misslyckas |
|---------|----------------------|
| Lägger till för många features | Späder ut fokus, försenar lansering |
| Lanserar inte tidigt nog | Väntar på perfekt = lanserar aldrig |
| Ignorerar feedback | Bygger blint |
| Förväxlar intresse med validering | "Ser bra ut" ≠ "Jag betalar" |
| Bygger för fel användare | Early adopters ≠ målmarknad |

---

# Del 3: Vibe Coding

*Hur du använder AI för att bygga snabbt.*

---

## Vad är vibe coding?

> "You talk to your code, accept LLM suggestions, copy-paste error messages, and pray it works. And it mostly does." — Andrej Karpathy

**Vibe coding** = AI-assisterad utveckling där du beskriver vad du vill ha och AI genererar koden.

---

## Vad är vibe coding INTE?

- ❌ Klistra in prompts och hoppas på det bästa
- ❌ Skeppa kod du inte förstår
- ❌ Hoppa över säkerhet eller arkitektur
- ❌ Låta AI ta alla beslut

**Nyckelregel:** Om du inte kan läsa koden AI genererar, skeppa den inte.

---

## Hur fungerar vibe coding-loopen?

```
Beskriv → Generera → Granska → Testa → Upprepa
```

| Steg | Vad du gör |
|------|------------|
| 1. Beskriv | Förklara vad du vill bygga (var specifik) |
| 2. Generera | AI skapar första implementationen |
| 3. Granska | Du granskar och korrigerar misstag |
| 4. Testa | Testa direkt — batcha inte |
| 5. Upprepa | Committa ofta, små ändringar |

---

## När fungerar vibe coding?

| Användningsfall | Varför |
|-----------------|--------|
| Demos och prototyper | Snabb validering, throwaway-kod OK |
| Landing pages | Enkelt, låg risk |
| Interna verktyg | Mindre säkerhetstryck |
| Lärande/utforskande | Snabb iteration |

---

## När fungerar vibe coding INTE?

| Användningsfall | Varför |
|-----------------|--------|
| Produktion med riktig användardata | Säkerhetshål |
| Komplexa backends | AI skapar inkonsekvent röra när kodbasen växer |
| Allt med betalningar | För riskabelt utan expertgranskning |
| Skalning över 100 användare | Arkitekturen går sönder |

---

## Kan jag som icke-teknisk grundare vibe-coda?

**Verklighetscheck från Reddit:**

> "I haven't seen anybody who vibecoded entire applications without knowing coding. I have seen landing pages that are vibecoded."

| Approach | Fungerar för |
|----------|--------------|
| Vibe-coda en demo | Få initial feedback, visa investerare |
| Vibe-coda MVP, anställ devs senare | Validera idé billigt, bygg om sen |
| Anställ dev från start | Komplexa produkter, säkerhetskritiskt, B2B |

**Den ärliga sanningen:** Vibe coding är bra för demos. För riktiga MVPs med betalande användare behöver de flesta icke-tekniska grundare till slut dev-hjälp — antingen för att granska/fixa AI-kod eller bygga om från scratch.

---

## Vilka är fördelarna och nackdelarna?

| Fördel | Nackdel |
|--------|---------|
| 10x snabbare att prototypa | Säkerhetshål du inte upptäcker |
| Lägre tröskel att börja | Teknisk skuld ackumuleras snabbt |
| Instant context recovery | AI tar dåliga beslut när koden växer |
| Validerar idéer billigt | Kan behöva full omskrivning senare |

---

## Vad ska jag göra om jag vibe-codar?

- [ ] **Planera först** — Skapa implementationsplan innan kodning
- [ ] **Var specifik** — Vaga prompts = dålig kod
- [ ] **Granska allt** — Acceptera inte blint
- [ ] **Testa konstant** — Batcha inte testning
- [ ] **Vet när du ska sluta** — Skaffa dev-hjälp innan användare betalar

---

# Del 4: Verktyg

*Vilka AI-modeller och verktyg du ska använda.*

---

## Vilken AI-modell ska jag använda?

| Modell | Bäst för |
|--------|----------|
| Claude Sonnet 4.5 | Kodning, debugging, refaktorering |
| Claude Opus 4.5 | Komplex arkitektur, svåra problem |
| GPT-5 | Brainstorming, marketing copy, idéer |
| GPT-4o | Snabba uppgifter, bra nog för det mesta |
| v0.dev | UI-prototyper (React) |
| Midjourney | Ikoner, grafik |

---

## Vilka vibe coding-verktyg finns?

| Verktyg | Vad det gör |
|---------|-------------|
| **Cursor** | AI-förbättrad VS Code-fork, bäst för kodning |
| **Windsurf** | Fristående AI-editor, bra flow |
| **Claude Code** | Terminalbaserad, kraftfull för devs |
| **Bolt.new** | Full app-generering (träff eller miss) |
| **Lovable** | Liknande Bolt, genererar hela appar |

---

# Del 5: Nästa steg

*Vad du gör när MVP är klart.*

---

## Vad gör jag efter MVP är validerat?

1. **Ta screenshots** → [Fas 2: Screenshots](README.md#phase-2-screenshots)
2. **Ladda upp till Play Console** → [Closed Testing Guide](closed-testing.md)
3. **Samla feedback** → [Feedback Guide](feedback.md)

---

## Sammanfattning

| Fråga | Svar |
|-------|------|
| Vad är MVP? | Minsta produkten någon betalar för |
| Hur vet jag att den är klar? | Du är lite generad + en främling kan använda den |
| Hur lång tid tar det? | Max 3 veckor |
| Kan jag vibe-coda den? | Demos ja, produktion med betalningar behöver dev-hjälp |
| Vilket verktyg ska jag använda? | Claude för kod, ChatGPT för idéer |

---

*Skeppa först. Polera senare.*
