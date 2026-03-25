# Kindlholz — Google Ads Umsetzungsplan

**Kunde:** Zimmerei Florian Kindl e.U.
**Website:** kindlholz.at (Shopify)
**Stand:** 16.03.2026
**Basiert auf:** kindlholz-gameplan.pdf (März 2026)
**Budget Setup + 8 Wochen:** 2.000 €
**Dein Login:** stephan.holzbach@gmail.com

---

## Ausgangslage

| Kennzahl | Aktuell |
|---|---|
| Budget | 903 €/Monat (30 €/Tag) |
| Klicks | 1.869/Monat |
| CTR | 11,7% (überdurchschnittlich) |
| CPC | 0,48 € (günstig) |
| Conversions | **0 gemessen** |
| Tracking | Keines (kein GTM, GA4, Cookie-Banner) |
| Kampagnen | 1 Kampagne, 1 Anzeigengruppe, 42 Keywords Broad Match |
| Gebotsstrategie | Klicks maximieren |

**Kernproblem:** Es wird für Klicks bezahlt, nicht für Ergebnisse. Kein Conversion-Tracking = Blindflug.

---

## Zugänge — Status (16.03.2026)

| Zugang | Status |
|---|---|
| Shopify Admin | ✅ Collaborator-Einladung erhalten |
| Google Ads | ✅ Zugang erhalten |
| Google Analytics (GA4) | 🆕 wird von mir erstellt |
| Google Search Console | 🆕 wird von mir erstellt |
| Google Tag Manager | 🆕 wird von mir erstellt |
| Google Merchant Center | 🆕 wird von mir erstellt |
| Microsoft Clarity | 🆕 wird von mir erstellt |
| Google My Business | ❓ noch klären mit Flo |
| Facebook / Meta | ❓ noch klären mit Flo |
| TikTok | ❌ gestrichen (Strafe) |
| Domain/DNS | ✅ LifeDesign Poysdorf, geklärt |

---

## Schritt 1: Konten erstellen & verbinden

Alle Google-Dienste + Tools anlegen und miteinander verknüpfen.

### 1.1 Google Tag Manager
- [ ] GTM-Konto + Container erstellen (Web, kindlholz.at)
- [ ] Container-ID notieren

### 1.2 Google Analytics 4
- [ ] GA4-Property erstellen
- [ ] Datenstream anlegen (Web, kindlholz.at)
- [ ] Measurement ID notieren
- [ ] Enhanced Measurement aktivieren

### 1.3 Google Search Console
- [ ] Property erstellen (kindlholz.at)
- [ ] Domain-Verifizierung via DNS bei LifeDesign
- [ ] Sitemap einreichen
- [ ] Crawling-Fehler prüfen

### 1.4 Google Merchant Center
- [ ] Konto erstellen
- [ ] Website verifizieren + claimen

### 1.5 Microsoft Clarity
- [ ] Projekt erstellen (kindlholz.at)
- [ ] Tracking-ID notieren

### 1.6 Cookie-Consent-Banner
- [ ] Lösung wählen (Cookiebot oder Consentmanager)
- [ ] Konto erstellen, kindlholz.at konfigurieren

### 1.7 Alles verbinden
- [ ] GA4 ↔ Google Ads verknüpfen
- [ ] GA4 ↔ Search Console verknüpfen
- [ ] GA4 ↔ Merchant Center verknüpfen
- [ ] GTM: GA4-Config-Tag anlegen
- [ ] GTM: Consent Mode v2 konfigurieren
- [ ] GTM: Microsoft Clarity Tag anlegen
- [ ] GTM: Google Ads Conversion Linker Tag anlegen
- [ ] GTM: Google Ads Conversion-Tags anlegen:
  - [ ] Anrufe von Website (Weiterleitungsnummer)
  - [ ] Anrufe aus Anzeige (Anruferweiterung)
  - [ ] E-Mail-Klicks (mailto: Click-Event)
  - [ ] Kontaktformular (Form-Submit-Event)
- [ ] GA4 Audiences anlegen (alle Besucher, Service-Besucher, Shop-Besucher)

### 1.8 Shopify — GTM + Tracking einbinden
- [ ] Shopify-Einladung annehmen
- [ ] GTM Container-Snippet in theme.liquid einbinden (`<head>` + `<body>`)
- [ ] Cookie-Banner installieren (via GTM oder Shopify App)
- [ ] Shopify Google-Channel-App prüfen/aktivieren
- [ ] Purchase-Event als Conversion einrichten (Umsatzwert-Tracking)
- [ ] Alle Tags im GTM Preview Mode testen
- [ ] Test-Bestellung → Conversion verifizieren

### 1.9 Google Business Profile
- [ ] Klären mit Flo: Profil vorhanden?
- [ ] Falls ja: Zugang bekommen. Falls nein: anlegen.
- [ ] Fotos, Leistungen, Öffnungszeiten optimieren
- [ ] Auf Bewertungen antworten (4,9 ★, 42 Rezensionen)

### 1.10 Sofort-Fix
- [ ] Tippfehler Structured Snippets: „Zeil" → „Ziel"

---

## Schritt 2: Website-Research

kindlholz.at komplett durchgehen — Seiten, Inhalte, Produkte.

### 2.1 Website-Struktur & Seiten
- [x] Alle Seiten aufnehmen (Service-Seiten, Landingpages, Kontakt) → siehe website-research.md
- [x] Prüfen: Welche Service-Seiten existieren? → 8 Service-Seiten + Dachcheck, /pages/dacharbeiten = 404!
- [x] Prüfen: Gibt es ein Kontaktformular? → NUR auf Dachcheck-Seite (Jotform iframe), sonst KEINES
- [x] Prüfen: Telefonnummer, E-Mail, CTAs auf jeder Seite → Tel nur auf Kontaktseite, CTA auf allen Service-Seiten
- [x] Prüfen: YouTube-Videos → 2 von 4 kaputt auf Startseite (Dachstuhl + Holzriegelbau), bestätigt
- [ ] Mobile-Ansicht testen
- [ ] Ladezeiten prüfen

### 2.2 Shopify Shop & Produkte
- [x] Alle Produktkategorien/Collections aufnehmen → 7 Collections + Sonderbestellung
- [x] Alle Produkte durchgehen → 15+ Holz-Produkte, 4 Hochbeete, Dämmung, Platten, Montagematerial
- [x] Prüfen: Welche Collections passen als Landingpages für Ads? → /collections/holz, /collections/bausatze, /collections/dammung
- [x] Prüfen: Shop-Navigation und Kaufprozess (UX) → Tag-Filter, Seitenleiste, Click & Collect
- [x] Notieren: Produktkategorien für Anzeigengruppen-Mapping → siehe website-research.md

### 2.3 Ergebnisse dokumentieren
- [x] Website-Struktur-Übersicht erstellen → website-research.md
- [x] Produkt-/Collection-Liste mit URLs → website-research.md
- [x] Landingpage-Empfehlungen pro Anzeigengruppe finalisieren → website-research.md (Abschnitt 4)
- [x] Verbesserungsvorschläge für Website notieren → website-research.md (Abschnitt 7)

### 2.4 KRITISCHE URL-KORREKTUREN (aus Research)
- /pages/dacharbeiten → 404! Dachdecker-Landingpage muss /pages/dachcheck oder /pages/reparaturarbeiten sein
- /pages/dachstühle → korrekter Slug: /pages/dachstuhle (ohne Umlaut)
- /pages/terrassenüberdachung → korrekter Slug: /pages/terrassenuberdachung-pergola
- /collections/bauschnittholz → existiert nicht als Collection, nur als Tag: /collections/holz/bauschnittholz

---

## Schritt 3: Ads-Research

Bestehende Kampagne analysieren + Keyword-Strategie finalisieren.

### 3.1 Bestehende Kampagne analysieren
- [x] Alle 42 Keywords durchgehen → Top 10 analysiert, "konstruktionsholz" = 50% Budget! Alle Broad Match.
- [ ] Search Terms Report prüfen (welche Suchbegriffe lösen Anzeigen aus?) → Zugang OK, muss im Detail geprüft werden
- [x] Aktuelle Anzeigentexte prüfen → 1 RSA, Ad Strength "Poor", gemischte Headlines (Holzhandel+Zimmerei+Terrasse)
- [x] Budget-Verteilung nach Keyword-Typ analysieren → ~71% Holzhandel, ~9% Dachdecker, ~8% Projekte, ~7% Zimmerei
- [x] Top-Performer und Geldverschwender identifizieren → "konstruktionsholz" €463/Monat, "Dachdecker" Low Quality Score

### 3.2 Keyword-Strategie finalisieren
- [ ] Keywords aus Gameplan mit realer Website/Produkt-Struktur abgleichen
- [ ] Keyword-Listen pro Anzeigengruppe finalisieren (basierend auf Website-Research)
- [ ] Negativ-Keyword-Listen erstellen
- [ ] Match Types festlegen (Phrase vs. Exact)
- [ ] Landingpage-Zuordnung finalisieren (basierend auf tatsächlich existierenden Seiten)

### 3.3 Anzeigentexte vorbereiten
- [ ] Headlines + Descriptions je Anzeigengruppe schreiben
- [ ] Sitelinks je Kampagne vorbereiten
- [ ] Callout Extensions vorbereiten
- [ ] Structured Snippets vorbereiten

---

## Schritt 4: Kampagnen aufbauen

### 4.1 Bestehende Kampagne sofort verbessern
- [ ] Negativ-Keywords hinzufügen (DIY, Jobs, Billig, Irrelevant)
- [ ] „Dachdecker"-Keywords in eigene Anzeigengruppe
- [ ] Anruf-Tracking aktivieren
- [ ] Gebotsstrategie auf Manueller CPC umstellen

### 4.2 Kampagne 1: Zimmerei, Dachdecker & Holzbau
**Ziel:** Anfragen | **Budget:** 15–20 €/Tag (~450–600 €/Monat, 60%)

| Anzeigengruppe | Keywords (Phrase Match) | SV | Landingpage |
|---|---|---|---|
| Zimmerei allgemein | zimmerei niederösterreich, zimmerei in meiner nähe, zimmerer in der nähe, holzbau firma, zimmerer weinviertel | ~1.070 | Startseite |
| Carport | carport holz, carport bauen lassen, carport niederösterreich, carport nach maß | ~2.960 | /pages/carport |
| Dachstuhl | dachstuhl bauen, dachstuhl erneuern, dachsanierung, neuer dachstuhl | ~900 | /pages/dachstühle |
| Dachdecker | dachdecker niederösterreich, dachdecker in meiner nähe, dach reparieren, dachdeckerei | ~500 | /pages/dacharbeiten |
| Terrasse & Pergola | terrassenüberdachung holz, pergola holz, pergola bauen lassen, überdachte terrasse, vordach holz | ~3.410 | /pages/terrassenüberdachung |
| Spezialleistungen | holzriegelbau, aufstockung holzbau, dachausbau, zellulosedämmung | ~1.820 | Jeweilige Unterseite |

- [ ] Kampagne anlegen
- [ ] 6 Anzeigengruppen mit Keywords
- [ ] Anzeigentexte einpflegen
- [ ] Final URLs setzen
- [ ] Sitelinks + Extensions einrichten
- [ ] Negativ-Keywords (Kauf-Keywords + allgemeine Liste)

### 4.3 Kampagne 2: Holzhandel & Online-Shop
**Ziel:** Shop-Verkäufe | **Budget:** 8–10 €/Tag (~240–300 €/Monat, 30%)

| Anzeigengruppe | Keywords | SV | Landingpage |
|---|---|---|---|
| Bauholz | konstruktionsholz kaufen, bauholz bestellen, kantholz kaufen, holzbalken kaufen, bauholz preisliste | ~720 | /collections/bauschnittholz |
| Lärche & Bretter | lärchenbretter kaufen, lärchenpfosten, bretter sägerau, nut feder bretter, holzbretter kaufen | ~1.640 | /collections/holz |
| Dämmung | zellulosedämmung kaufen, einblasdämmung, isocell zellulose | ~350 | /products/isocell-zellulose-daemmung-sack |
| Hochbeet & Garten | hochbeet lärchenholz, hochbeet bausatz, gartenhaus nach maß | ~160 | /products/hochbeet-bausatz |

- [ ] Kampagne anlegen
- [ ] 4 Anzeigengruppen mit Keywords
- [ ] Anzeigentexte einpflegen
- [ ] Final URLs auf Shop-Kategorien
- [ ] Sitelinks + Extensions

### 4.4 Kampagne 3: Marke (Brand Protection)
**Ziel:** Marke absichern | **Budget:** 2–3 €/Tag (~60–90 €/Monat, 10%)

- [ ] Kampagne anlegen
- [ ] Keywords: „zimmerei kindl", „kindl ladendorf", „kindlholz" (Exact Match)
- [ ] Anzeige mit Brand-Text + Sitelinks
- [ ] **Alte Kampagne pausieren** (nicht löschen!)

### Budget-Übersicht

| Kampagne | Tagesbudget | Monatsbudget | Anteil |
|---|---|---|---|
| Zimmerei & Holzbau | 15–20 € | 450–600 € | 60% |
| Holzhandel / Shop | 8–10 € | 240–300 € | 30% |
| Marke | 2–3 € | 60–90 € | 10% |
| **Gesamt** | **25–33 €** | **750–990 €** | **100%** |

---

## Schritt 5: Website-Optimierungen

- [ ] Kontaktformular auf allen Service-Seiten (HOCH)
- [ ] Referenz-Fotos & Kundenstimmen — 4,9 ★ prominent (MITTEL)
- [ ] YouTube-Videos reparieren (MITTEL)
- [ ] „Dachcheck" prominenter bewerben (MITTEL)
- [ ] Preisindikationen „ab X €" (NICE-TO-HAVE)

---

## Schritt 6: Laufende Optimierung

- [ ] Search Terms Report wöchentlich prüfen
- [ ] Keywords ohne Conversions pausieren
- [ ] Budget zwischen Kampagnen verschieben nach Performance
- [ ] Nach 15–20+ Conversions: auf **„Conversions maximieren"** umstellen
- [ ] Bei ROI-Nachweis: Budget +20–50%
- [ ] Mittelfristig: Ziel-CPA (z.B. max. 50 €/Anfrage)

---

## Erwartete Ergebnisse

| | Aktuell | Nach Setup | Nach Optimierung |
|---|---|---|---|
| Budget | ~900 € | ~750–900 € | ~900–1.200 € |
| Gebotsstrategie | Klicks max. | Manueller CPC | Conversions max. |
| Zimmerei-Anfragen | 0 | 5–10 | 8–15 |
| Shop-Bestellungen | 0 | 3–6 | 5–12 |
| Kosten/Anfrage | nicht messbar | ~50–80 € | ~35–60 € |

**ROI-Rechnung Zimmerei:**
10 Anfragen × 20% Auftragsquote = 2 Aufträge × 10.000 € = **20.000 € Umsatz** bei ~600 € Kosten = **ROI 30:1**
