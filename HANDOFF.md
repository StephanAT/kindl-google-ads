# Übergabeprotokoll — Zimmerei Kindl Google Ads Projekt

**Datum:** 2026-03-07
**Kunde:** Zimmerei Kindl (kindlholz.at), Ladendorf, Niederösterreich
**Ansprechpartner:** Flo (Geschäftsführer)
**Bearbeitet von:** Stephan Holzbach
**Google Ads Account:** 6465444616

---

## Projektübersicht

Vollständige Analyse und Planung für Google Ads Kampagnen + AI-Optimierung (GEO) für Zimmerei Kindl — ein Betrieb mit drei Geschäftsbereichen: Zimmerei, Dachdeckerei und Holzhandel (Online-Shop auf Shopify).

---

## Was wurde gemacht

### 1. Ist-Analyse des bestehenden Google Ads Accounts

**Befund:** 1 Kampagne ("Search // Allgemein") mit 1 Anzeigengruppe, 42 Keywords (alle Broad Match), keine Conversion-Messung, kein Tracking (kein GTM, kein GA4, kein Cookie-Banner).

**Hauptprobleme:**
- Alle drei Geschäftsbereiche (Zimmerei, Dachdecker, Holzhandel) in einer generischen Anzeige
- Broad Match Keywords ohne Negatives = hohe Streuverluste
- Keine Conversion-Messung = keine Optimierungsmöglichkeit
- Tippfehler in bestehender Anzeige ("Zeil" statt "Ziel")

### 2. Keyword-Research (DataForSEO)

- **Zimmerei & Dachdecker:** 102 Keywords erhoben (3 von 22 API-Calls erfolgreich)
- **Holzhandel & Brand:** 77 Keywords erhoben (3 von 10 API-Calls erfolgreich)
- **Status:** DataForSEO Credits aufgebraucht — fehlende Calls dokumentiert für Nachholen
- **Dateien:** `research/keywords-zimmerei-dachdecker.md`, `research/keywords-holzhandel-brand.md`

### 3. SERP-Analyse

- 14 Keywords analysiert (via Web-Suche, da DataForSEO 402)
- kindlholz.at rankt #1 für "lärchenpfosten kaufen"
- Größte Chancen: "carport bauen lassen", "terrassenüberdachung holz", "konstruktionsholz kaufen"
- Zimmerei/Dachdecker-SERPs dominiert von Verzeichnissen (herold.at, WKO, firmenabc.at)
- **Datei:** `research/serp-analysis.md`

### 4. Konkurrenzanalyse

- Alle DataForSEO-Calls fehlgeschlagen (402)
- Top-Konkurrenten identifiziert via SERP: longin.at, mp-holzbau.at, holz-shop.com, woodshop.at, burgerholz.at
- **Datei:** `research/competitor-analysis.md` (nur Template, Daten fehlen)

### 5. Website-Audit (via Playwright)

- 9 Service-Seiten + 7 Shop-Kategorien kartiert
- Ad Group -> Landing Page Zuordnung erstellt
- Fehlend identifiziert: Dachdecker-Landingpage, Kontaktformulare, Cookie-Banner
- **Datei:** `research/landing-pages.md`

### 6. Kampagnen-Blueprints (Copy-Paste-Ready)

Vollständige Kampagnenstruktur zum direkten Einrichten:

| Kampagne | Anzeigengruppen | Keywords | Budget/Tag |
|---|---|---|---|
| Zimmerei, Dachdecker & Holzbau | 6 (Zimmerei allg., Carport, Dachstuhl, Dachdecker, Terrasse/Pergola, Spezial) | ~45 | 15 EUR |
| Holzhandel & Online-Shop | 4 (Bauholz, Lärche/Bretter, Dämmung, Hochbeet/Garten) | ~25 | 8 EUR |
| Marke | 1 (Brand) | ~10 | 2 EUR |
| **Gesamt** | **11** | **~80** | **25 EUR** |

Enthält: 11 RSAs (je 15 Headlines + 4 Descriptions mit Pin-Anweisungen), Sitelinks, Callout Extensions, Structured Snippets, Account-Level + Kampagnen-Level Negative Keywords.

- **Datei:** `research/campaign-blueprints.md`

### 7. Implementation Playbook (8 Wochen)

Step-by-Step Anleitung für Setup + Betreuung:
- **Woche 1:** Tracking (GTM, GA4, Cookie-Banner, Conversion-Tags, Search Console, Business Profile, Clarity)
- **Woche 2:** Kampagnen aufsetzen (3 Kampagnen, 11 Anzeigengruppen, Negatives, Extensions)
- **Woche 3–4:** Monitoring & Quick Wins (tägliche/wöchentliche Tasks)
- **Woche 5–6:** Gebotsstrategien umstellen (Manual CPC -> Conversions maximieren / Conv.-Wert maximieren)
- **Woche 7–8:** Feinschliff, Reporting, Übergabe
- **Parallel:** AI-Optimierung (GEO) Track

- **Datei:** `research/implementation-playbook.md`

### 8. AI-Optimierung (GEO)

Vollständige Recherche + Maßnahmenplan für Sichtbarkeit in ChatGPT, Perplexity, Google AI Overviews:
- Ist-Zustand: kindlholz.at wird von keinem AI-System zitiert
- Kein Konkurrent hat eine GEO-Strategie (First-Mover-Vorteil)
- 4-Phasen-Plan: Grundlagen -> Content -> Autorität -> Monitoring
- Top-5 Quick Wins: Bing Places, Schema Markup, FAQ-Seite, Google-Bewertungen, Standortseiten
- 20+ Quellen aus DACH + international

- **Datei:** `research/ai-optimization.md`

### 9. Kunden-Deliverables

- **Strategie-PDF:** Visuelles Dokument für Flo mit Ist-Analyse, Problemen, Lösung, Kampagnenstruktur, Zeitplan
- **E-Mail (Word):** Kurze Zusammenfassung + Angebot (Setup + 8 Wochen Betreuung)

- **Dateien:** `deliverables/kindlholz-gameplan.pdf`, `deliverables/kindlholz-gameplan.html`, `deliverables/kindlholz-email-flo.docx`

---

## Dateistruktur

```
kindl-google-ads/
├── HANDOFF.md                          <- Dieses Dokument
├── README.md                           <- Projekt-Übersicht
├── research/
│   ├── keywords-zimmerei-dachdecker.md <- Keyword-Daten Zimmerei/Holzbau
│   ├── keywords-holzhandel-brand.md    <- Keyword-Daten Holzhandel/Brand
│   ├── serp-analysis.md               <- SERP-Analyse 14 Keywords
│   ├── competitor-analysis.md          <- Konkurrenz (noch leer)
│   ├── landing-pages.md               <- Website-Audit + LP-Mapping
│   ├── campaign-blueprints.md         <- Kampagnenstruktur (copy-paste-ready)
│   ├── implementation-playbook.md     <- 8-Wochen Step-by-Step
│   └── ai-optimization.md            <- GEO-Analyse + Maßnahmenplan
├── deliverables/
│   ├── kindlholz-gameplan.pdf         <- Strategie-PDF für Kunden
│   ├── kindlholz-gameplan.html        <- HTML-Quelle des PDFs
│   └── kindlholz-email-flo.docx      <- E-Mail für Kunden
└── plans/
    ├── 2026-03-07-kindl-google-ads-campaigns-design.md  <- Design-Dokument
    └── 2026-03-07-kindl-google-ads-implementation.md    <- Implementierungsplan
```

---

## Offene Punkte

### Sofort nachholen (wenn DataForSEO Credits aufgeladen)

| Was | Calls | Geschätzter Aufwand |
|---|---|---|
| Keyword Discovery (fehlende Seeds) | ~40 API-Calls | 30 Min |
| Konkurrenzanalyse (5 Domains) | 12 API-Calls | 20 Min |
| SERP-Analyse (exakte Positionen) | 14 API-Calls | 15 Min |
| AI-Suchvolumen (LLM Keyword Data) | 1 API-Call (14 Keywords) | 5 Min |
| LLM Mentions (kindlholz.at) | 3 API-Calls | 5 Min |
| Keywords mit * verifizieren | 5-10 API-Calls | 10 Min |

Genaue API-Parameter dokumentiert in: `research/implementation-playbook.md` (Anhang)

### Vor Kampagnen-Start

- [ ] PDF an Flo schicken + Angebot besprechen
- [ ] Zugänge einholen (Google Ads Admin, Shopify Admin, Google Account)
- [ ] Google Ads Account prüfen (aktueller Status der alten Kampagne)
- [ ] DataForSEO aufladen und fehlende Research nachholen
- [ ] Keywords mit `*` im Blueprint durch echte Daten ersetzen

### Während der Umsetzung

- [ ] Dachdecker-Landingpage erstellen lassen (fehlt auf kindlholz.at)
- [ ] Kontaktformular auf Service-Seiten einbauen
- [ ] Kaputte YouTube-Videos auf der Website fixen
- [ ] Cookie-Banner installieren (DSGVO-Pflicht)

---

## Zeitaufwand

| Phase | Dauer |
|---|---|
| Ist-Analyse + Strategie-PDF | ~3 Std |
| Keyword-Research (DataForSEO) | ~1 Std (teilweise, Credits leer) |
| SERP-Analyse + Website-Audit | ~1 Std |
| Kampagnen-Blueprints | ~2 Std |
| Implementation Playbook | ~1 Std |
| AI-Optimierung (GEO) Research + Plan | ~1 Std |
| E-Mail + Dokument-Formatierung | ~1 Std |
| **Gesamt** | **~10 Std** |
