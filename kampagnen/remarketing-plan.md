# Kindlholz — Remarketing-Kampagne Plan

**Stand:** 25.03.2026
**Status:** ENTWURF — noch nicht gebaut

---

## Konzept

Besucher die auf kindlholz.at waren aber nicht konvertiert haben (kein Anruf, kein Formular, keine E-Mail) sollen mit **service-spezifischen Text-Sujets** erneut angesprochen werden.

**Stil-Vorbild:** incaseof.law — simple Text-Ads mit perfektem Content-Match:
- Besucher war auf /pages/carport → sieht "Neues Carport gesucht? Zimmerei Kindl baut's."
- Besucher war auf /pages/dachcheck → sieht "Dach schon gecheckt? Kostenloser Dachcheck."

---

## Kampagnentyp: Demand Gen (nicht GDN)

**Warum Demand Gen statt Display Network:**
- Demand Gen ist Googles Nachfolger für Discovery Campaigns (2024 umgestellt)
- Bessere Platzierungen: YouTube, Gmail, Discover Feed, Google Display
- Bessere AI-Optimierung als klassisches GDN
- Unterstützt Image Ads, Carousel Ads und Video Ads
- Für Remarketing mit kleinem Budget effizienter als GDN

**Naming:** `DG_RT_Dienstleistungen_AT-NÖ` (Demand Gen, Retargeting)

---

## Audiences

### Audience 1: Alle Website-Besucher (30 Tage)
- **Regel:** Besucher von kindlholz.at in den letzten 30 Tagen
- **Ausschluss:** Converter (sobald Conversion Tracking steht)
- **Verwendung:** Basis-Remarketing

### Audience 2: Service-Seiten-Besucher (60 Tage)
- **Regel:** Besucher von /pages/carport, /pages/dachstuhle, /pages/terrassenuberdachung-pergola, /pages/holzriegelbau, /pages/dachcheck, /pages/dachausbau, /pages/zellulosedammung
- **Ausschluss:** Converter
- **Verwendung:** High-Intent Remarketing mit Content-Match

### Audience 3: Homepage-Bouncer (14 Tage)
- **Regel:** Besucher von / die NICHT auf Service-Seiten waren
- **Verwendung:** Allgemeines Branding

**Voraussetzung:** Google Ads Tag oder GA4 Audiences müssen auf der Website aktiv sein → GTM muss installiert werden!

---

## Ad Sets (Text-Sujets mit Content-Match)

### Konzept: Einfache, direkte Ansprache
- Weißer/heller Hintergrund
- Große Headline mit Frage
- Subline mit Lösung + Marke
- Optional: Foto vom jeweiligen Service

### Sujet 1: Carport
```
Headline:  Neues Carport gesucht?
Subline:   Zimmerei Kindl baut deins. Seit 1963.
CTA:       Jetzt anfragen
Bild:      carport_landing_-2 (von Homepage)
LP:        /pages/carport
```

### Sujet 2: Dachstuhl
```
Headline:  Dein Dachstuhl vom Meister.
Subline:   Individuell geplant. Millimetergenau gebaut.
CTA:       Angebot anfordern
Bild:      dachstuhl_400x (von Homepage)
LP:        /pages/dachstuhle
```

### Sujet 3: Terrassenüberdachung
```
Headline:  Grillsaison verlängern?
Subline:   Terrassenüberdachung nach Maß. Zimmerei Kindl.
CTA:       Jetzt planen
Bild:      terrassenueberdachung_landing_desktop (von Homepage)
LP:        /pages/terrassenuberdachung-pergola
```

### Sujet 4: Dachcheck
```
Headline:  Dach schon gecheckt?
Subline:   Kostenloser Dachcheck mit Drohne & Kran.
CTA:       Dachcheck anfragen
Bild:      (Dachcheck-Foto oder Drohnen-Bild)
LP:        /pages/dachcheck
```

### Sujet 5: Holzriegelbau
```
Headline:  Mehr Platz? Bau nach oben.
Subline:   Aufstockung & Holzriegelbau vom Profi.
CTA:       Projekt besprechen
Bild:      holzriegelbau_landing_desktop (von Homepage)
LP:        /pages/holzriegelbau
```

### Sujet 6: Allgemein (für Homepage-Bouncer)
```
Headline:  Holzbau aus dem Weinviertel.
Subline:   Zimmerei Kindl — seit 1963. 4,9★ bei 42 Bewertungen.
CTA:       Leistungen ansehen
Bild:      Hero-Bild von Homepage
LP:        /
```

---

## Bild-Assets

### Verfügbare Bilder von kindlholz.at (Shopify CDN):
| Service | Desktop | Mobile |
|---|---|---|
| Carport | `carport_landing_-1_400x.jpg` | `carport_landing_-2_{width}x.jpg` |
| Dachstuhl | `dachstuhl_400x.jpg` | `dachstuhl_landing_mobile-1_{width}x.jpg` |
| Holzhandel | `holzhandel_landing_desktop-1_{width}x.jpg` | `holzhandel_landing_mobile-1_{width}x.jpg` |
| Holzriegelbau | `holzriegelbau_landing_desktop-1_{width}x.jpg` | `holzriegelbau_landing_mobile-1_{width}x.jpg` |
| Terrasse | `terrassenueberdachung_landing_desktop-1_{width}x.jpg` | `terrassenueberdachung_landing_mobile-1_{width}x.jpg` |

### Benötigte Formate für Demand Gen:
- **Landscape:** 1200x628 (1.91:1)
- **Square:** 1200x1200 (1:1)
- **Portrait:** 960x1200 (4:5) — optional

### Option: fal.ai für Text-Overlay-Sujets
Einfache Composites mit:
- Service-Foto als Hintergrund (leicht abgedunkelt)
- Weiße Headline-Textbox
- Kindlholz Logo
- CTA-Button
→ Kann mit fal.ai Image Editing oder einfachem HTML/CSS + Screenshot erstellt werden

---

## Budget & Settings

| Setting | Wert |
|---|---|
| Kampagnentyp | Demand Gen |
| Budget | €5/Tag (~€150/Monat, ~25% vom Gesamtbudget) |
| Bidding | Maximize Conversions (oder Clicks wenn keine Conversions) |
| Geo | NÖ + Wien |
| Sprache | Deutsch |
| Frequency Capping | 3-5 Impressions/Woche/User (Demand Gen steuert automatisch) |
| Zeitraum | Laufend (sobald GTM installiert + Audience min. 100 User) |

---

## Research-Erkenntnisse (März 2026)

### Demand Gen ist der richtige Kampagnentyp
- Google hat Display Network als Placement IN Demand Gen integriert (2025)
- Demand Gen läuft auf YouTube, Gmail, Discover Feed, Maps UND Display
- Eingeloggte User = besseres Audience-Matching ohne Cookie-Abhängigkeit
- Audience-Minimum auf 100 User gesenkt (vorher 1.000) → auch für lokale Betriebe machbar

### Cookie-Situation 2026
- Google hat Cookie-Deprecation NICHT umgesetzt → Third-Party Cookies existieren noch
- ABER: Consent Mode v2 ist seit März 2024 PFLICHT für AT/DE
- Ohne korrekte Consent-Signale baut Google KEINE Remarketing-Listen auf
- `ad_user_data` + `ad_personalization` müssen "granted" sein

### Entscheidungszyklus Bau/Zimmerei
- Bau-Entscheidungen dauern 60-180 Tage
- Daher: Service-Seiten-Besucher auf 90-180 Tage Fenster setzen (nicht nur 30 Tage)
- Remarketing-Listen SOFORT anlegen, auch wenn Kampagne noch nicht läuft — sammelt ab Tag 1 Daten

### Creative-Tipps
- Responsive Ads sind Pflicht (Google optimiert automatisch)
- Spezifische Headlines performen besser als generische ("Neues Carport?" >> "Zimmerei in der Nähe")
- Creatives alle 60-90 Tage rotieren
- Social Proof hinzufügen: "4,9★ bei 42 Bewertungen"

---

## Voraussetzungen (BLOCKER)

1. **GTM muss auf Shopify installiert sein** → Remarketing-Tag braucht Website-Daten
2. **Consent Mode v2 + CMP** (Cookiebot o.ä.) KORREKT einrichten — ohne das funktioniert kein Remarketing in AT!
3. **Google Ads Remarketing Tag** im GTM anlegen (oder GA4 Audiences nutzen)
4. **Audience muss mindestens 100 aktive User haben** bevor Demand Gen Ads ausgespielt werden
5. **Remarketing-Listen SOFORT anlegen** auch wenn Kampagne noch nicht startet — Daten sammeln ab Tag 1

---

## Umsetzungsplan

### Phase 1: Vorbereitung (wenn GTM bereit)
1. Google Ads Remarketing Tag im GTM anlegen
2. GA4 Audiences erstellen (All Visitors, Service Page Visitors)
3. Audiences in Google Ads importieren
4. Bild-Assets erstellen (6 Sujets × 2 Formate = 12 Bilder)

### Phase 2: Kampagne bauen
1. Demand Gen Kampagne erstellen: `DG_RT_Dienstleistungen_AT-NÖ`
2. Ad Group 1: "Service-Besucher" (Audience 2)
3. Ad Group 2: "Allgemein" (Audience 1 exkl. Audience 2)
4. Ads mit Content-Match-Sujets eintragen
5. Budget €5/Tag, Frequency Cap setzen

### Phase 3: Optimierung (nach 2 Wochen)
1. Performance pro Sujet prüfen
2. Schlecht performende Sujets pausieren
3. Audience-Windows anpassen (30→60 Tage wenn zu wenig Volumen)
4. Budget anpassen basierend auf CTR/CPA

---

## Naming Convention

| Ebene | Name |
|---|---|
| Kampagne | `DG_RT_Dienstleistungen_AT-NÖ` |
| Ad Group 1 | `Service-Besucher_60d` |
| Ad Group 2 | `Alle-Besucher_30d` |
| Ads | `Carport_Landscape`, `Dachstuhl_Square`, etc. |
