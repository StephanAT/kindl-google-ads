# Kindlholz — Kampagnen-Review (25.03.2026)

## Status Überblick

| Kampagne | Status | Budget | AGs | KWs | Ads |
|---|---|---|---|---|---|
| Zimmerei & Holzbau - Dienstleistungen | Paused | €20/Tag | 6 | ~52 | 6 RSAs |
| Brand | Paused | €3/Tag | 1 | 3 | 1 RSA |
| Search // Allgemein (alt) | Enabled | €30/Tag | 1 | 42 | 1 RSA |

---

## KRITISCHE ISSUES (müssen gefixt werden)

### 1. Nur 7 Headlines + 2 Descriptions pro RSA (Plan hatte 15 + 4)
**Problem:** Der Wizard hat pro Ad Group nur 7 Headline-Felder und 2 Description-Felder gezeigt. Laut Kampagnenplan sollten es 15 Headlines und 4 Descriptions sein.
**Impact:** Ad Strength bleibt "Poor" statt "Good/Excellent". Google empfiehlt 10-15 Headlines und 4 Descriptions.
**Fix:** In jeder Ad Group die RSAs bearbeiten und die fehlenden Headlines + Descriptions aus `kampagnenplan-dienstleistungen.md` nachtragen:
- Pro AG fehlen ~8 Headlines und ~2 Descriptions
- Besonders wichtig: Keywords in Headlines (Quality Score)
- Pinning von Headline 1 auf Position 1 setzen

### 2. Descriptions mit Telefonnummer — ALLE prüfen
**Problem:** Description 4 im Kampagnenplan enthält überall "Ruf an: 02575/8207" oder "Tel: 02575/8207". Google Ads Policy verbietet Telefonnummern im Ad-Text.
**Impact:** Ads werden abgelehnt.
**Fix:**
- Brand-Kampagne: ✅ Gefixt (Find & Replace)
- Dienstleistungs-Kampagne: Aktuell nur 2 Descriptions pro AG eingetragen, keine hatte Tel-Nummer
- Wenn fehlende Descriptions nachgetragen werden: Description 4 OHNE Telefonnummer formulieren
- Stattdessen **Call Extension** einrichten (02575/8207)

### 3. Keine Negativ-Keywords
**Problem:** Keine Negativ-Keyword-Liste angelegt. Der Kampagnenplan hat eine umfangreiche Liste vorbereitet.
**Impact:** Budget-Verschwendung durch irrelevante Klicks (DIY, Jobs, Billig, etc.)
**Fix:** Shared Negative Keyword List erstellen mit:
- DIY & Selbermachen (selber bauen, anleitung, bauplan, etc.)
- Job & Karriere (job, stelle, gehalt, lehre, etc.)
- Bildung (kurs, schulung, definition, wikipedia, etc.)
- Schnäppchenjäger (kostenlos, billig, gebraucht, etc.)
- Nicht relevant (brennholz, möbel, versicherung, ikea, etc.)
- Kauf-Keywords für Dienstleistungs-Kampagne (kaufen, bestellen, online shop, etc.)

### 4. Keine Sitelinks, Callouts, Call Extension
**Problem:** Keine Ad Extensions angelegt.
**Impact:** Niedrigerer Ad Rank, weniger Anzeigenfläche, niedrigere CTR.
**Fix:**
- **Sitelinks** (6 geplant): Dachstuhl, Carport, Terrassenüberdachung, Kontakt, Dachcheck, Leistungen
- **Callouts** (6 geplant): Meisterbetrieb seit 1963, 4,9★ bei 42 Bewertungen, Kostenlose Erstberatung, etc.
- **Call Extension**: 02575/8207 (Mo-Fr 08:00-15:00)
- **Structured Snippets**: Dienstleistungen → Dachstuhl, Carport, Terrassenüberdachung, etc.

### 5. Bidding-Strategie ist "Maximize Clicks" statt "Manual CPC"
**Problem:** Im Wizard wurde "Clicks" als Focus gewählt + Max CPC Limit gesetzt. Das ergibt "Maximize Clicks with Max CPC" — nicht exakt "Manual CPC" wie im Plan.
**Impact:** Google optimiert automatisch auf Klicks und kann das CPC-Limit voll ausnutzen. Bei Manual CPC hätte man mehr Kontrolle pro Keyword.
**Fix:** Optional — "Maximize Clicks" mit Max CPC ist für den Start akzeptabel und sogar einfacher. Manual CPC kann nachträglich umgestellt werden wenn nötig. **Kein dringender Fix.**

---

## VERBESSERUNGEN (sollten gemacht werden)

### 6. Ad Group "Marke" in Brand-Kampagne umbenennen
**Problem:** Die Ad Group heißt "Ad group 1" statt "Marke".
**Fix:** Umbenennen zu "Marke".

### 7. Display Network abschalten in Brand-Kampagne
**Problem:** Wurde möglicherweise nicht abgewählt im Brand-Wizard (ging alles automatisch durch).
**Fix:** Campaign Settings → Networks → Display Network unchecken.

### 8. Zeitplanung fehlt
**Problem:** Laut Plan: Mo-Fr 06:00-20:00, Sa 08:00-14:00. Aktuell: 24/7.
**Impact:** Klicks außerhalb der Geschäftszeiten bringen weniger Wert (Anrufe gehen ins Leere).
**Fix:** Ad Schedule in Campaign Settings setzen.

### 9. Geo-Targeting verfeinern
**Problem:** Laut Plan: "Radius 60km um Ladendorf". Aktuell: ganz NÖ + Wien.
**Impact:** NÖ + Wien ist OK als Start, aber Teile von NÖ (Waldviertel, Mostviertel) sind weit weg.
**Fix:** Optional für Phase 2 — eventuell Bid Adjustments für Bezirke Mistelbach/Gänserndorf erhöhen.

### 10. Alte Drafts löschen
**Problem:** 2 alte leere Drafts ("Zimmerei & Holzbau — Dienstleistungen") im Account.
**Fix:** Campaigns → Drafts → die 2 ohne Budget löschen.

---

## WAS GUT IST

- **STAG-Struktur**: 6 thematisch getrennte Ad Groups = Best Practice
- **Match Types**: Phrase Match als Standard, Exact Match für Geo-Keywords = korrekt
- **Keywords**: Alle aus dem Research übernommen, richtige Landingpages zugeordnet
- **Budget**: €20/Tag für Dienstleistungen, €3/Tag für Brand = konservativ und richtig für Phase 1
- **Locations**: NÖ + Wien = das Einzugsgebiet
- **Sprache**: Nur Deutsch = korrekt
- **Display Network**: Abgeschaltet in Dienstleistungs-Kampagne = korrekt
- **Kein Wettbewerb**: First-Mover-Vorteil ist riesig — CPCs werden niedrig sein

---

## PRIORITÄTEN FÜR NÄCHSTE SESSION

1. **Headlines + Descriptions vervollständigen** (15 HL + 4 Desc pro AG, Zeichenlimits beachten!)
2. **Negativ-Keywords** als Shared List
3. **Sitelinks + Callouts + Call Extension**
4. **Brand-Kampagne AG umbenennen + Settings prüfen**
5. **Alte Drafts löschen**
6. **Zeitplanung setzen**
7. Shopify GTM-Integration klären (Blocker)
