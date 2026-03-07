# Implementation Playbook — Zimmerei Kindl Google Ads

> Schritt-für-Schritt Anleitung für Setup + 8 Wochen Betreuung
> Datum: 2026-03-07

---

## Pre-Flight Checklist

### Zugänge benötigt
- [ ] Google Ads Account (6465444616) — Admin-Zugang
- [ ] kindlholz.at Shopify Admin — für GTM-Code + Google Channel App
- [ ] Google Account des Kunden — für GTM, GA4, Search Console, Business Profile
- [ ] Telefonnummer für Anruferweiterung

### Accounts erstellen
- [ ] Google Tag Manager Container (Web)
- [ ] Google Analytics 4 Property
- [ ] Google Search Console Property
- [ ] Microsoft Clarity Projekt

---

## Woche 1: Tracking-Fundament

### Tag 1: Google Tag Manager (GTM)

**Schritt 1:** GTM Account erstellen auf tagmanager.google.com
- Container Name: "kindlholz.at"
- Typ: Web

**Schritt 2:** GTM-Code auf Shopify installieren
- Shopify Admin → Online Store → Themes → Edit Code
- `<head>` Bereich: GTM Head-Snippet einfügen
- Nach `<body>`: GTM Body-Snippet einfügen
- Alternativ: Shopify Custom Pixels (keine Code-Änderung nötig)

**Schritt 3:** Verifizieren
- Seite laden → GTM Debugger → Container feuert

### Tag 1: Google Analytics 4 (GA4)

**Schritt 1:** GA4 Property erstellen auf analytics.google.com
- Property Name: "kindlholz.at"
- Zeitzone: Wien
- Währung: EUR

**Schritt 2:** GA4 via GTM einbinden
- GTM → Tags → Neu → Google Analytics: GA4 Configuration
- Measurement ID eintragen (G-XXXXXXXXXX)
- Trigger: All Pages

**Schritt 3:** Enhanced Measurement aktivieren
- GA4 Admin → Data Streams → Web Stream → Enhanced Measurement ON
- Scrolls, Outbound Clicks, Site Search, File Downloads

### Tag 1: Cookie-Consent-Banner

**Schritt 1:** Cookie-Banner App installieren
- Shopify App Store → z.B. "Pandectes GDPR Compliance" oder "Consentmo"
- Kostenloser Plan reicht für Basis-Consent

**Schritt 2:** Consent Mode in GTM konfigurieren
- GTM → Tags → Consent Overview
- GA4 Tag: Consent Required (analytics_storage)
- Google Ads Tags: Consent Required (ad_storage, ad_user_data, ad_personalization)

**Schritt 3:** Testen
- Seite im Inkognito → Banner erscheint → Akzeptieren → Tags feuern

### Tag 2: Google Ads Conversion-Tracking

**Conversion 1: Anrufe von der Website**
- Google Ads → Conversions → Neue Conversion → Anrufe
- Google-Weiterleitungsnummer einrichten
- GTM Tag: Google Ads Conversion Tracking (Anruf)
- Trigger: Klick auf tel: Links

**Conversion 2: E-Mail-Klicks**
- GTM → Trigger → Click URL contains "mailto:"
- GTM → Tag → Google Ads Conversion (E-Mail-Klick)

**Conversion 3: Kontaktformular**
- Prüfen ob Shopify Kontaktformular vorhanden
- GTM → Trigger → Form Submission auf /pages/kontakt
- GTM → Tag → Google Ads Conversion (Formular)

**Conversion 4: Shopify-Käufe**
- Shopify Admin → Settings → Apps → Google & YouTube Channel
- Google Ads Account verknüpfen
- Conversion-Tracking automatisch aktiviert (Purchase Event)

### Tag 2: Google Search Console

**Schritt 1:** Search Console Property erstellen
- search.google.com/search-console
- Property hinzufügen → URL-Prefix: https://www.kindlholz.at
- Verifizierung via HTML-Tag (in Shopify Theme einfügen) oder DNS

**Schritt 2:** Sitemap einreichen
- https://www.kindlholz.at/sitemap.xml

### Tag 2: Google Business Profile

**Schritt 1:** Profil prüfen/beanspruchen
- business.google.com → "Zimmerei Kindl" suchen
- Profil beanspruchen falls noch nicht geschehen

**Schritt 2:** Optimieren
- Alle 3 Kategorien eintragen: Zimmerei, Dachdeckerei, Holzhandel
- Öffnungszeiten aktualisieren
- Fotos hochladen (Projekte, Team, Werkstatt)
- Beschreibung mit Keywords
- Services/Leistungen eintragen
- Website-Link: https://www.kindlholz.at

### Tag 3: Microsoft Clarity

**Schritt 1:** Clarity Projekt erstellen
- clarity.microsoft.com → Neues Projekt
- Name: "kindlholz.at"

**Schritt 2:** Via GTM einbinden
- GTM → Tag → Custom HTML → Clarity Tracking-Code
- Trigger: All Pages

**Schritt 3:** Verifizieren
- Seite besuchen → Clarity Dashboard → Session erscheint

### Tag 3: Abschluss-Check Woche 1

- [ ] GTM Container feuert auf allen Seiten
- [ ] GA4 empfängt Daten (Echtzeit-Report prüfen)
- [ ] Cookie-Banner erscheint und blockiert Tags bis Consent
- [ ] Google Ads Conversion-Tags feuern (GTM Preview Mode)
- [ ] Shopify ↔ Google Channel verknüpft
- [ ] Search Console verifiziert, Sitemap eingereicht
- [ ] Google Business Profile beansprucht und optimiert
- [ ] Clarity empfängt Sessions
- [ ] Tippfehler "Zeil" → "Ziel" in bestehender Anzeige korrigiert

---

## Woche 2: Kampagnen aufsetzen

### Tag 1: Alte Kampagne pausieren + Neue Struktur

**Schritt 1:** Bestehende Kampagne "Search // Allgemein" pausieren
- Google Ads → Kampagnen → "Search // Allgemein" → Pausieren
- NICHT löschen (historische Daten behalten)

**Schritt 2:** 3 neue Kampagnen anlegen
- Kampagne 1: "Zimmerei & Dachdecker"
- Kampagne 2: "Holzhandel & Shop"
- Kampagne 3: "Marke"
- Einstellungen wie in campaign-blueprints.md

### Tag 1-2: Kampagne 1 aufsetzen

Für jede der 6 Anzeigengruppen (aus campaign-blueprints.md):
1. Anzeigengruppe erstellen
2. Keywords einfügen (mit Match Types)
3. RSA erstellen (Headlines + Descriptions + Pins)
4. Final URL setzen
5. Sitelinks hinzufügen
6. Callout Extensions
7. Structured Snippets
8. Anruferweiterung

### Tag 2: Kampagne 2 aufsetzen

4 Anzeigengruppen wie in Blueprints.

### Tag 2: Kampagne 3 aufsetzen

1 Anzeigengruppe (Brand).

### Tag 3: Negative Keywords

**Account-Level Negatives:**
- Google Ads → Tools → Negative Keyword Lists
- Liste "Account Negatives" erstellen
- Alle Account-Level Keywords aus Blueprints einfügen
- Liste auf alle 3 Kampagnen anwenden

**Kampagnen-Level Negatives:**
- Kampagne 1 → Negative Keywords → Kampagnen-Level Keywords einfügen
- Kampagne 2 → Negative Keywords → Kampagnen-Level Keywords einfügen

### Tag 3: Extensions für alle Kampagnen

- Anruferweiterung (Account-Level)
- Standorterweiterung (Google Business Profile verknüpfen)

### Abschluss-Check Woche 2

- [ ] Alte Kampagne pausiert
- [ ] 3 neue Kampagnen aktiv
- [ ] 11 Anzeigengruppen mit Keywords + Anzeigen
- [ ] Negative Keywords auf Account- und Kampagnen-Level
- [ ] Alle Extensions eingerichtet
- [ ] Budget korrekt: 15€ + 8€ + 2€ = 25€/Tag
- [ ] Gebotsstrategie: Manueller CPC überall

---

## Woche 3-4: Monitoring & Quick Wins

### Tägliche Tasks (5-10 min)

1. **Suchbegriffe prüfen**
   - Google Ads → Keywords → Suchbegriffe
   - Irrelevante Begriffe als Negative hinzufügen
   - Neue relevante Begriffe als Keywords hinzufügen

2. **Performance-Check**
   - Klicks, Impressionen, CTR pro Anzeigengruppe
   - Anomalien identifizieren (plötzlicher CTR-Drop etc.)

### Wöchentliche Tasks (30 min)

1. **CPC-Gebote anpassen**
   - Keywords mit vielen Impressionen aber wenig Klicks: CPC erhöhen
   - Keywords mit hohem CPC und niedrigem CTR: CPC senken oder pausieren

2. **Anzeigen-Performance**
   - RSAs mit "Poor" oder "Average" Stärke überarbeiten
   - Headlines mit niedrigem Impression Share austauschen

3. **Conversion-Daten prüfen**
   - Kommen Anrufe/Anfragen rein?
   - Welche Keywords konvertieren?
   - GA4: Welche Landingpages performen?

4. **Clarity Sessions reviewen**
   - 5-10 Sessions pro Woche anschauen
   - Wo steigen Besucher aus?
   - Funktioniert der CTA?

5. **Quality Score prüfen**
   - Keywords mit QS < 5: Landing Page oder Anzeige verbessern

---

## Woche 5-6: Gebotsstrategien umstellen

### Voraussetzung: Mind. 15-20 Conversions pro Kampagne

**Kampagne 1 (Zimmerei/Dachdecker):**
- Umstellen auf "Conversions maximieren"
- KEIN Ziel-CPA setzen (erst genug Daten sammeln)
- 1 Woche beobachten, dann ggf. Ziel-CPA setzen (~50 €)

**Kampagne 2 (Holzhandel):**
- Umstellen auf "Conversion-Wert maximieren"
- Shopify meldet Bestellwert → Google optimiert auf Revenue
- 1 Woche beobachten, dann ggf. Ziel-ROAS setzen

**Kampagne 3 (Marke):**
- Bleibt auf Manuellem CPC (niedrige CPCs, kein Smart Bidding nötig)

### Budget-Anpassung

Wenn Conversions profitabel:
- Kampagne 1: Budget auf 20 €/Tag erhöhen
- Kampagne 2: Budget auf 10 €/Tag erhöhen
- Gesamt: ~32 €/Tag (~960 €/Monat)

---

## Woche 7-8: Feinschliff & Reporting

### Optimierungen

1. **Ziel-CPA / Ziel-ROAS testen**
   - Kampagne 1: Ziel-CPA ~50 € (1 Anfrage)
   - Kampagne 2: Ziel-ROAS ~500% (5x Return on Ad Spend)

2. **Unterperformende Keywords pausieren**
   - Keywords mit >50 Klicks und 0 Conversions

3. **Top-Performer skalieren**
   - Keywords mit guter Conversion-Rate: Budget freigeben
   - Neue ähnliche Keywords hinzufügen

4. **Negativ-Listen finalisieren**
   - Alle irrelevanten Suchbegriffe aus 8 Wochen

### Vorher-Nachher-Report

| Metrik | Vorher (Feb) | Nachher (Apr) |
|---|---|---|
| Kampagnen | 1 | 3 |
| Anzeigengruppen | 1 | 11 |
| Keywords | 42 (Broad) | ~80 (Phrase/Exact) |
| Budget/Monat | ~900 € | ~750-960 € |
| Conversions | 0 (nicht gemessen) | XX |
| Kosten/Conversion | Unbekannt | XX € |
| Conversion-Rate | 0% | XX% |

### Übergabe-Dokument

- Zusammenfassung der 8 Wochen
- Was wurde eingerichtet (Tracking, Kampagnen)
- Performance-Daten
- Empfehlung: Weiterbetreuung oder Selbstmanagement
- Wenn Selbstmanagement: Checkliste für wöchentliche Tasks

---

## Parallel-Track: AI-Optimierung (GEO)

> Detaillierter Plan in: kindl-research/ai-optimization.md

### Woche 1 (parallel zu Tracking-Setup)

- [ ] Bing Places Profil anlegen (business.bing.com) — ChatGPT nutzt Bing als Datenquelle
- [ ] NAP-Konsistenz prüfen (Name/Adresse/Telefon identisch auf Website, Google, Herold, WKO, Facebook)
- [ ] HubSpot AEO Grader laufen lassen (kostenlos) — hubspot.com/aeo-grader
- [ ] AI-Baseline: 5 Test-Prompts in ChatGPT + Perplexity + Google AI, Ergebnisse dokumentieren

### Woche 2 (parallel zu Kampagnen-Setup)

- [ ] Schema Markup implementieren (JSON-LD im Shopify Theme):
  - `HomeAndConstructionBusiness` + `RoofingContractor` (global)
  - `Service`-Schema auf jeder Leistungsseite
  - `FAQPage`-Schema auf FAQ-Seite
  - `AggregateRating` (Trustpilot-Daten)
- [ ] Validieren: Google Rich Results Test + Schema.org Validator

### Woche 3–4 (parallel zu Monitoring)

- [ ] FAQ-Seite erstellen: 15–20 echte Kundenfragen mit präzisen Antworten
- [ ] Service-Seiten überarbeiten: Front-loaded Answers, Überschriften als Fragen
- [ ] 2–3 Standortseiten erstellen (z.B. /pages/zimmerei-weinviertel, /pages/dachdecker-mistelbach)

### Woche 5–8 (laufend)

- [ ] 3–5 Projekt-Fallstudien veröffentlichen (Vorher/Nachher, Materialien, Dauer)
- [ ] Bewertungsstrategie starten: QR-Code-Karte für Google-Reviews
- [ ] YouTube-Kanal: 1–2 Projektvideos hochladen
- [ ] Monatlicher AI-Sichtbarkeits-Check (ChatGPT/Perplexity/Google AI)

---

## Anhang: DataForSEO Keyword-Daten nachholen

Wenn Credits wieder verfügbar, folgende Calls nachholen:

### Keyword Discovery
- keyword_suggestions für ~20 Seeds (Zimmerei, Dachdecker, Holzhandel)
- keyword_ideas für ~9 Keyword-Gruppen
- related_keywords für ~7 Top-Keywords

### Konkurrenz
- domain_rank_overview für 5 Domains
- ranked_keywords für 5 Domains (je 100)
- competitors_domain für kindlholz.at
- domain_intersection (kindlholz.at vs longin.at, vs mp-holzbau.at)

### SERP
- serp_organic_live_advanced für 14 Keywords
- serp_competitors für 5 Core-Keywords

Alle Calls: location_name="Austria", language_code="de"

Detaillierte Parameter in: docs/plans/2026-03-07-kindl-google-ads-implementation.md
