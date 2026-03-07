# Google Ads Kampagnenplan — Zimmerei Kindl (kindlholz.at)

Datum: 2026-03-07
Status: Approved

---

## Kontext

Zimmerei Florian Kindl e.U. in Ladendorf (NÖ) betreibt drei Geschäftsbereiche: Zimmerei, Dachdeckerei und Holzhandel (Shopify-Shop). Aktuell läuft 1 Google Ads Kampagne mit 1 Anzeigengruppe, 42 Broad-Match-Keywords, ~900 €/Monat Budget — ohne Conversion-Tracking. Ziel: 3 getrennte, datengetriebene Kampagnen mit vollständigem Tracking-Setup.

## Ziel

Zwei Deliverables:
1. **Strategie-Dokument** für den Kunden (PDF)
2. **Umsetzungs-Playbook** für die Implementierung (copy-paste-fertig)

---

## Phase 1: Research (DataForSEO)

### 1.1 Keyword-Discovery

**Seed-Keywords Zimmerei/Holzbau:**
zimmerei, zimmerer, holzbau, holzbau firma, zimmermann, holzkonstruktion, dachstuhl, carport holz, terrassenüberdachung holz, pergola holz, holzriegelbau, aufstockung holzbau, vordach holz, balkon holz, gartenhaus holz, holzfassade

**Seed-Keywords Dachdecker:**
dachdecker, dachdeckerei, dach reparieren, dachsanierung, dach decken, dachziegel, flachdach, steildach, dachreparatur, dachrinne, dach undicht, dachdämmung, dachfenster einbau

**Seed-Keywords Holzhandel/Shop:**
konstruktionsholz, bauholz, holz kaufen, bretter, kantholz, lärche, fichte, nut feder bretter, holzbalken, holzbretter kaufen, dhf platte, zellulose einblasdämmung, hochbeet holz, lärchenpfosten

**API-Calls pro Seed:**
- keyword_suggestions — verwandte Suchbegriffe
- keyword_ideas — breitere Ideensammlung
- keyword_overview — SV, CPC, Wettbewerb, Saisonalität

**Geo:** Österreich (AT), Deutsch

### 1.2 Konkurrenz-Analyse

**Domains:** longin.at, mp-holzbau.at, holzbau-k.at, holzbau-noe.at, kindlholz.at

**Pro Domain:**
- ranked_keywords — organische Rankings
- domain_rank_overview — Gesamtstärke
- competitors_domain — organische Wettbewerber

### 1.3 SERP-Analyse

Für Top-20 Keywords: serp_organic_live_advanced — Wer rankt, wer schaltet Ads, Local Pack vorhanden?

### 1.4 Website-Audit

kindlholz.at: Welche Landingpages existieren, Shop-Kategorien, Service-Seiten.

---

## Phase 2: Kampagnenstruktur

### Kampagne 1: Zimmerei, Dachdecker & Holzbau (Dienstleistung)

**Ziel:** Anfragen (Anrufe, Formulare, E-Mails)
**Budget:** 15-20 €/Tag (~450-600 €/Monat)
**Geo:** NÖ + Wien, ~60km Radius um Ladendorf
**Geräte:** Alle, +15% Mobile

| Anzeigengruppe | Match Type | Landingpage |
|---|---|---|
| Zimmerei allgemein | Phrase + Exact | Startseite/Leistungen |
| Carport | Phrase | /pages/carport |
| Dachstuhl | Phrase | /pages/dachstühle |
| Dachdecker | Phrase | /pages/dacharbeiten |
| Terrasse & Pergola | Phrase | /pages/terrassenüberdachung |
| Spezialleistungen | Phrase | Jeweilige Unterseite |

Pro Anzeigengruppe: 5-15 Keywords, 1 RSA (15 Headlines, 4 Descriptions), Sitelinks, Callouts, Structured Snippets, Anruferweiterung.

### Kampagne 2: Holzhandel & Online-Shop

**Ziel:** Shop-Bestellungen (Shopify ↔ Google Ads)
**Budget:** 8-10 €/Tag (~240-300 €/Monat)
**Geo:** Österreichweit

| Anzeigengruppe | Match Type | Landingpage |
|---|---|---|
| Bauholz | Phrase | /collections/bauschnittholz |
| Lärche & Bretter | Phrase | /collections/holz |
| Dämmung | Phrase | /products/isocell-zellulose-daemmung-sack |
| Hochbeet & Garten | Phrase | /products/hochbeet-bausatz |

### Kampagne 3: Marke (Brand Protection)

**Ziel:** Marke absichern
**Budget:** 2-3 €/Tag (~60-90 €/Monat)
**Geo:** Österreichweit
**Keywords:** zimmerei kindl, kindl ladendorf, kindlholz, kindl holz, kindl zimmerei

### Negative Keywords

**Account-Level:** DIY, Jobs, Bildung, Schnäppchenjäger, Irrelevant (brennholz, möbel, etc.)
**Zimmerei-Kampagne:** kaufen, bestellen, online shop, amazon, hornbach, obi, bauhaus
**Holzhandel-Kampagne:** zimmerei, zimmerer, dachdecker, bauen lassen, montage

---

## Phase 3: Gebotsstrategien-Roadmap

| Phase | Zeitraum | Zimmerei/Dachdecker | Holzhandel/Shop | Marke |
|---|---|---|---|---|
| Datensammlung | Woche 1-4 | Manueller CPC | Manueller CPC | Manueller CPC |
| Umstellung | Woche 5-6 | Conversions max. | Conv.-Wert max. | Bleibt manuell |
| Optimierung | Ab Woche 7 | Ziel-CPA (~50€) | Ziel-ROAS | Bleibt manuell |

---

## Phase 4: Budget-Szenarien

| Szenario | Zimmerei/Dachdecker | Holzhandel/Shop | Marke | Gesamt/Monat |
|---|---|---|---|---|
| Konservativ | 450 € | 240 € | 60 € | ~750 € |
| Mittel | 600 € | 300 € | 90 € | ~990 € |
| Aggressiv | 900 € | 450 € | 90 € | ~1.440 € |

Start: Konservativ. Nach 4 Wochen Conversion-Daten auf Mittel skalieren.

---

## Phase 5: Rollout-Timeline (8 Wochen)

**Woche 1:** Tracking-Fundament (GTM, GA4, Cookie-Banner, Conversion-Tags, Shopify-Integration, Search Console, Google Business, Clarity)

**Woche 2:** Kampagnen aufsetzen (alle 3 Kampagnen, Anzeigengruppen, Keywords, Anzeigen, Negative, Extensions). Alte Kampagne pausieren.

**Woche 3-4:** Monitoring & Quick Wins (Suchbegriffe, CPC-Anpassungen, Anzeigen-Optimierung, Clarity-Sessions)

**Woche 5-6:** Gebotsstrategien umstellen, Budget skalieren

**Woche 7-8:** Feinschliff, Ziel-CPA/ROAS testen, Vorher-Nachher-Report, Übergabe

---

## Erwartete Ergebnisse

| Metrik | Jetzt | Nach 8 Wochen |
|---|---|---|
| Kampagnen | 1 | 3 |
| Messbare Conversions | 0 | 15-25/Monat |
| Kosten pro Anfrage (Zimmerei) | Unbekannt | ~35-60 € |
| Kosten pro Bestellung (Shop) | Unbekannt | ~20-50 € |
| Budget-Effizienz | Blindflug | Datengetrieben |

---

## Research-Deliverables

1. **Keyword-Masterliste** (Excel/CSV) — alle Keywords mit SV, CPC, Wettbewerb, Zuordnung
2. **Konkurrenz-Report** — organische Rankings, Traffic, Ads-Aktivität pro Wettbewerber
3. **SERP-Analyse** — Top-20 Keywords, wer rankt, wer schaltet Ads
4. **Strategie-PDF** (für Kunden) — Marktübersicht, Struktur, Budget, Timeline
5. **Umsetzungs-Playbook** (für Implementierung) — copy-paste Keywords, Anzeigentexte, Einstellungen, Checklisten
