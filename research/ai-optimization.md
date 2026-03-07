# AI-Optimierung (GEO) — Zimmerei Kindl (kindlholz.at)

**Datum:** 2026-03-07
**Thema:** Generative Engine Optimization (GEO) — Sichtbarkeit in ChatGPT, Perplexity, Google AI Overviews, Gemini, Claude

---

## Warum AI-Optimierung jetzt wichtig ist

| Kennzahl | Wert | Quelle |
|---|---|---|
| AI-Referral-Traffic Wachstum (Jan–Mai 2025) | +527% | Go Fish Digital |
| Anteil AI-gestützter Suchen bis 2026 | 25% aller Suchen | Gartner |
| Google-Queries mit AI Overview | 55%+ der High-Traffic-Queries | Search Engine Land |
| Klick-Verlust durch AI Overviews (DE/AT-Studie) | -17,8% im Schnitt, bis -40% | Wordsmattr |
| Zero-Click-Suchen (Google gesamt) | 58% werden direkt von AI beantwortet | handwerker.ch |
| Google AI Overviews Launch AT | 26. März 2025 | Google |
| Google AI Mode Launch AT | 8. Oktober 2025 | Trending Topics |

**Kernaussage:** Weniger Klicks, aber die verbleibenden Klicks haben höhere Kaufabsicht. Wer von AI zitiert wird, gewinnt — wer nicht vorkommt, verliert.

---

## Ist-Zustand: kindlholz.at in AI-Suchen

### Aktuelle Sichtbarkeit
- **kindlholz.at wird von keinem AI-System zitiert** (manuell getestet + DataForSEO LLM Mentions API)
- Kein FAQ-Schema, kein LocalBusiness-Schema, keine strukturierten Daten
- Kein Bing Places Profil (ChatGPT nutzt Bing als Datenquelle)
- Website-Content ist nicht im Q&A-Format aufgebaut
- Keine Projekt-Fallstudien oder Ratgeber-Inhalte

### Konkurrenz-Check
| Konkurrent | AI-Readiness | Schwächen |
|---|---|---|
| longin.at | Mittel — Presseerwähnungen, gute Markengeschichte | Kein FAQ, kein Schema |
| mp-holzbau.at | Niedrig — Gute regionale Keywords | Generische Seitenstruktur |
| holz-shop.com | Mittel — Top-Position "holz online kaufen" | Kein Ratgeber-Content |
| woodshop.at | Niedrig — Facebook-Präsenz | Kaum Content-Marketing |
| burgerholz.at | Niedrig — Traditionelle Website | Kein AI-optimierter Content |

**Ergebnis: Kein einziger Konkurrent hat eine GEO-Strategie.** Wer jetzt anfängt, hat einen massiven First-Mover-Vorteil.

---

## Was AI-Systeme bevorzugen

### Content-Format
1. **Front-loaded Answers** — Die ersten 200 Wörter müssen die Frage direkt beantworten. Kein Intro-Gelaber.
2. **Q&A-Format** — Listicles und Q&A erhalten 35% mehr AI-Zitierungen als unstrukturierter Content.
3. **Konkrete Fakten** — "Dachstuhl aus Fichtenholz hält 80–100 Jahre" schlägt vage Aussagen.
4. **Eigenständige Absätze** — Jeder Absatz = eine vollständige Idee. Kein "wie oben erwähnt".
5. **Beschreibende Überschriften** — Als Frage formuliert: "Was kostet eine Dachsanierung in NÖ?"

### Strukturierte Daten (Schema Markup)
- Seiten mit Schema werden bis zu **40% häufiger** von LLMs zitiert
- **61% der von ChatGPT zitierten Seiten** nutzen Schema Markup

| Schema-Typ | Zweck | Priorität |
|---|---|---|
| `HomeAndConstructionBusiness` | Firmenidentität, Adresse, Öffnungszeiten, Einzugsgebiet | MUSS |
| `RoofingContractor` | Spezifischer Subtyp für Dachdeckerei | MUSS |
| `Service` | Einzelne Leistungen (Dachstuhl, Carport, Holzriegelbau) | HOCH |
| `FAQPage` | Häufige Fragen — höchste Zitier-Wahrscheinlichkeit | HOCH |
| `HowTo` | Prozessbeschreibungen ("Wie läuft eine Dachsanierung ab?") | MITTEL |
| `AggregateRating` + `Review` | Kundenzufriedenheit als Vertrauenssignal | HOCH |
| `Article` | Blogposts mit Expertenwissen | MITTEL |
| `GeoShape` / `areaServed` | Definition des Einzugsgebiets | MITTEL |

**Format:** JSON-LD im `<head>` (Googles bevorzugte Methode)

### Autoritätssignale
- Brand Mentions wirken wie Backlinks für AI — ChatGPT erwähnt Marken **3,2x häufiger** als es Links zitiert (BrightEdge)
- Top-Quellen die LLMs zitieren: YouTube, Reddit, LinkedIn, lokale Medien
- Meisterbrief, Zertifikate, Auszeichnungen auf der Website zeigen
- Google-Bewertungen sind ein Hauptsignal für AI-Empfehlungen

---

## Maßnahmenplan

### Phase 1: Grundlagen (Woche 1–2)

**1. Google Business Profile komplett optimieren**
- Alle 3 Kategorien: Zimmerei, Dachdeckerei, Holzhandel
- Vollständige Beschreibung mit Keywords
- Alle Leistungen einzeln eintragen
- 20+ Fotos (Projekte, Team, Werkstatt, Produkte)
- Öffnungszeiten, Telefon, Website-Link
- Auf bestehende Bewertungen antworten

**2. Bing Places Profil anlegen**
- business.bing.com → Firmenprofil erstellen
- Identische Daten wie Google Business Profile
- **Warum:** ChatGPT nutzt Bing als primäre Datenquelle für lokale Suchen

**3. NAP-Konsistenz prüfen**
- Name, Adresse, Telefon müssen überall identisch sein:
  - kindlholz.at (Website)
  - Google Business Profile
  - Bing Places
  - Herold.at
  - WKO Firmen A-Z
  - Facebook
  - Trustpilot
  - Firmenabc.at

**4. Schema Markup implementieren**
- `HomeAndConstructionBusiness` + `RoofingContractor` auf jeder Seite
- `Service`-Schema für jede einzelne Leistungsseite
- `AggregateRating` wenn Trustpilot-Daten vorhanden
- JSON-LD im Shopify Theme `<head>` einfügen
- Validieren: Google Rich Results Test + Schema.org Validator

**5. AI-Baseline messen**
- HubSpot AEO Grader laufen lassen (kostenlos): hubspot.com/aeo-grader
- Manuell testen in ChatGPT, Perplexity, Google AI:
  - "Zimmerei in Niederösterreich empfehlen"
  - "Wo kann ich Bauholz online kaufen in Österreich?"
  - "Dachsanierung Weinviertel wer ist gut?"
  - "Lärchenpfosten kaufen Österreich"
- Ergebnisse dokumentieren als Ausgangspunkt

### Phase 2: Content aufbauen (Woche 3–6)

**6. FAQ-Seite erstellen (höchste Priorität)**

Mindestens 15–20 echte Kundenfragen mit präzisen Antworten (2–4 Sätze pro Antwort). FAQPage-Schema implementieren.

Beispiel-FAQs:

*Zimmerei & Holzbau:*
- Was kostet ein neuer Dachstuhl in Niederösterreich?
- Wie lange dauert der Bau eines Carports?
- Welches Holz eignet sich für eine Terrassenüberdachung?
- Brauche ich eine Baugenehmigung für einen Carport in NÖ?
- Was ist ein Holzriegelbau und welche Vorteile hat er?
- Wie läuft eine Dachsanierung Schritt für Schritt ab?

*Dachdeckerei:*
- Woran erkenne ich, dass mein Dach undicht ist?
- Was kostet eine Dachreparatur in Österreich?
- Wie oft sollte man einen Dachcheck machen lassen?
- Welche Dacheindeckungen gibt es und was kosten sie?

*Holzhandel:*
- Welche Holzarten eignen sich für den Außenbereich?
- Was ist der Unterschied zwischen KVH und BSH?
- Kann ich Bauholz online bestellen und liefern lassen?
- Welches Holz eignet sich für ein Hochbeet?
- Was kostet ein Kubikmeter Konstruktionsholz in Österreich?

**7. Service-Seiten überarbeiten**
- Jede Seite beginnt mit einer direkten Antwort auf die Hauptfrage
- Überschriften als Fragen formulieren
- Konkrete Zahlen/Fakten einbauen (Kosten, Dauer, Materialien)
- Service-Schema auf jeder Seite

**8. Standortseiten erstellen**
- Eigene Unterseiten für regionale Keywords:
  - /pages/zimmerei-weinviertel
  - /pages/dachdecker-mistelbach
  - /pages/holzbau-ladendorf
  - /pages/zimmerei-gaenserndorf
- Jede Seite mit lokalem Content, Referenzprojekten aus der Region, Anfahrtsinformationen

**9. Projekt-Fallstudien veröffentlichen**
- 3–5 Referenzprojekte mit:
  - Vorher/Nachher-Fotos
  - Verwendete Materialien + Mengen
  - Projektdauer
  - Standort (Region/Gemeinde)
  - Kundenzitat (wenn möglich)
- Als eigene Unterseiten oder Blog-Beiträge

### Phase 3: Autorität stärken (laufend)

**10. Bewertungsstrategie**
- Nach jedem abgeschlossenen Projekt: Google-Bewertung anfragen
- QR-Code-Karte für Kunden erstellen (direkt zum Google-Review-Link)
- Ziel: 50+ Google-Bewertungen innerhalb von 6 Monaten
- Auf jede Bewertung antworten (positiv und negativ)

**11. YouTube-Kanal aktivieren**
- Projektdokumentationen (Zeitraffer, Vorher/Nachher)
- Erklärvideos: "So erkennen Sie ob Ihr Dach undicht ist"
- Materialvergleiche: "Fichte vs. Lärche — welches Holz wofür?"
- YouTube ist eine der meistzitierten Quellen von LLMs

**12. Lokale Pressearbeit**
- Artikel in regionalen Medien (meinbezirk.at, NÖN)
- WKO-Mitgliedschaft + Eintrag aktiv pflegen
- Herold.at-Profil mit Beschreibung + Fotos aufwerten
- Holzbau-NÖ Verband (holzbau-noe.at) — Mitgliedschaft und Listing

**13. Handwerkerplattformen bespielen**
- daibau.at — Profil erstellen/optimieren
- my-hammer.at — Profil erstellen
- Relevante Fragen auf gutefrage.net / Reddit beantworten (als Experte, nicht als Werbung)

### Phase 4: Monitoring (monatlich)

**14. AI-Sichtbarkeit monatlich testen**
- 5–10 Test-Prompts in ChatGPT, Perplexity, Google AI
- Ergebnisse in einfacher Tabelle tracken
- Vergleich: Werden wir häufiger erwähnt? Werden Konkurrenten erwähnt?

**15. Optional: Monitoring-Tool**
| Tool | Kosten | Empfehlung |
|---|---|---|
| HubSpot AEO Grader | Kostenlos | Sofort starten |
| Otterly.AI | ab $29/Monat | Bestes Preis-Leistung für KMU |
| Peec AI | ab 89 EUR/Monat | Wenn Budget vorhanden |
| Promptmonitor | Variabel | Alternative zu Otterly |

---

## Zusammenfassung: Die 5 wichtigsten Hebel

| # | Maßnahme | Aufwand | Impact |
|---|---|---|---|
| 1 | Bing Places Profil anlegen | 30 Min | ChatGPT-Sichtbarkeit |
| 2 | Schema Markup implementieren | 2–3 Std | +40% AI-Zitierungen |
| 3 | FAQ-Seite mit 15+ Fragen + Schema | 1 Tag | Höchste Zitier-Wahrscheinlichkeit |
| 4 | Google-Bewertungen aktiv sammeln | Laufend | Vertrauenssignal für AI |
| 5 | Standortseiten für Einzugsgebiet | 1–2 Tage | Lokale AI-Suchen |

---

## Quellen

### GEO Grundlagen
- [Search Engine Land: GEO - How to win AI mentions](https://searchengineland.com/what-is-generative-engine-optimization-geo-444418)
- [Go Fish Digital: GEO Strategies for 2026](https://gofishdigital.com/blog/generative-engine-optimization-strategies/)
- [Phoenix Online Media: GEO, AEO & AIO Guide 2026](https://phoenixonlinemedia.com/geo-aeo-aio-guide-ai-search-optimization-2026/)
- [Conductor: 2026 AEO/GEO Benchmarks Report](https://www.conductor.com/academy/aeo-geo-benchmarks-report/)

### Lokale AI-Optimierung
- [Local Falcon: AI Search Optimization Best Practices](https://www.localfalcon.com/blog/needtoknow-best-practices-for-ai-search-optimization-2025/)
- [SerpremeSEO: 6 Ways to Rank Contractor Company in ChatGPT](https://serpremeseo.com/blog/6-ways-to-rank-your-contractor-company-in-chatgpt/)
- [MapRanks: Google Business Profile 2026 & AI](https://www.mapranks.com/2025/06/26/ai-impact-on-google-business-profile-2025/)

### Structured Data
- [SEOptimer: Schema Markup for AI Search](https://www.seoptimer.com/blog/schema-markup-for-ai-search/)
- [Walker Sands: Schema Markup for LLM Visibility](https://www.walkersands.com/about/blog/how-can-schema-markup-support-llm-visibility/)
- [Coalition Technologies: Schema and LLM Rankings](https://coalitiontechnologies.com/blog/schema-markup-and-llm-rankings-why-youre-missing-out-on-chatgpt)

### Content & Autorität
- [SimpleTiger: How to Rank on ChatGPT](https://www.simpletiger.com/blog/how-to-rank-on-chatgpt)
- [DemandSage: How to Rank on ChatGPT 2025](https://www.demandsage.com/how-to-rank-on-chatgpt/)
- [ALM Corp: How to Rank for Mentions in ChatGPT](https://almcorp.com/blog/how-to-rank-for-mentions-in-chatgpt/)

### DACH-spezifisch
- [Armin Fradler: Google AI Overviews Österreich 2025](https://www.arminfradler.at/blog/google-ai-overviews-zero-click-searches-oesterreich-2025)
- [Wordsmattr: 17,8% weniger Klicks durch AI Overviews](https://wordsmattr.io/exklusive-google-ki-studie/)
- [handwerker.ch: Googles KI frisst 58% Klicks](https://handwerker.ch/news/googles-ki-frisst-58-klicks-alarmstufe-rot-fur-handwerker-websites/2158)
- [Handwerk Magazin: SEO für KI](https://www.handwerk-magazin.de/kuenstliche-intelligenz-bei-der-suche-was-chatgpt-perplexity-co-fuer-die-digitale-sichtbarkeit-von-betrieben-bedeuten-337473/)
- [Webu.at: Digitale Sichtbarkeit Handwerker 2025](https://webu.at/digitale-sichtbarkeit-handwerker-2025/)
- [Brengelmann: SGE & Lokale SEO 2026](https://brengelmann.com/ratgeber/google-ai-overviews-lokale-seo-2026/)

### Tools
- [HubSpot AEO Grader](https://www.hubspot.com/aeo-grader) (kostenlos)
- [Otterly.AI](https://otterly.ai/) (ab $29/Monat)
- [BloggerJet: Best GEO Tools 2025](https://bloggerjet.com/best-generative-engine-optimization-tools-2025/)
