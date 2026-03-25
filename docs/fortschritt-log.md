# Kindlholz — Fortschritt-Log

## Stand: 25.03.2026

---

## NÄCHSTE SESSION: So weitermachen

### Ansatz: Playwright MCP für Google Ads
- **Playwright MCP funktioniert** für Google Ads Kampagnen-Erstellung (Ad Groups, Keywords, Ads)
- **Einschränkung:** "Confirm it's you" Dialog blockiert Publish — User muss Draft im normalen Chrome publishen
- **Ad-Blocker-Warnung:** ist ein False Positive, blockiert NICHT die Funktionalität (Ad-Scripts laden normal)
- **Wahrer Grund für Publish-Fehler in letzter Session:** Description mit 91/90 Zeichen, KEIN Ad-Blocker-Problem

### Was noch zu tun ist:
1. Brand-Kampagne erstellen (3 KW, €3/Tag)
2. Negativ-Keywords als Shared List anlegen
3. Sitelinks + Callouts + Call Extension hinzufügen
4. Kampagnen-Review: Headlines optimieren, Descriptions auf 90 Zeichen prüfen
5. Shopify GTM-Integration (aktuell blockiert — Probleme bei Anbindung)

---

## Was komplett fertig ist

### Naming Convention (professionell)
```
[Netzwerk]_[Brand/NonBrand]_[Thema]_[Geo]
```
Beispiel: `S_NB_Dienstleistungen_AT-NÖ`

### Kampagne 1: `S_NB_Dienstleistungen_AT-NÖ` — ERSTELLT & PAUSIERT
**Campaign ID:** 23694425245 | **Status:** Paused | **Budget:** €20/Tag | **Bidding:** Maximize Clicks (Max CPC €2.50)
**Locations:** Lower Austria + Vienna | **Language:** German | **Networks:** Search + Search Partners

| Anzeigengruppe | Keywords | Match Type | Landingpage | RSA |
|---|---|---|---|---|
| Zimmerei allgemein | 9 KW | Phrase + Exact | / | 7 Headlines, 2 Desc |
| Carport | 8 KW | Phrase | /pages/carport | 7 Headlines, 2 Desc |
| Dachstuhl & Dachsanierung | 8 KW | Phrase | /pages/dachstuhle | 7 Headlines, 2 Desc |
| Dachdecker & Dachreparatur | 8 KW | Phrase + Exact | /pages/dachcheck | 7 Headlines, 2 Desc |
| Terrassenüberdachung & Pergola | 11 KW | Phrase + Exact | /pages/terrassenuberdachung-pergola | 7 Headlines, 2 Desc |
| Spezialleistungen | 8 KW | Phrase | /pages/holzriegelbau | 7 Headlines, 2 Desc |

**Gesamt:** 6 Anzeigengruppen, ~52 Keywords, 6 RSAs

### Research & Planung
| Dokument | Inhalt | Status |
|---|---|---|
| `kampagnenplan-dienstleistungen.md` | **HAUPTDOKUMENT** — alle Keywords, Headlines, Descriptions, Negativ-KW, Budget, Gebotsstrategie | FERTIG |
| `google-ads-best-practices-2026.md` | STAG-Struktur, Match Types, Bidding-Roadmap, QS-Tipps, RSA Best Practices | FERTIG |
| `wettbewerb-google-ads-analyse.md` | Konkurrenten (keiner schaltet Ads!), USPs, Differenzierung | FERTIG |
| `website-research.md` | Alle Seiten, URLs, Landingpages, URL-Korrekturen | FERTIG |
| `ads-research.md` | Bestehende Kampagne analysiert, Keyword-Performance | FERTIG |

### Tools & Tracking (erstellt am 18.03.)
| Tool | ID | Status |
|---|---|---|
| GTM Container | **GTM-N5PX9TV2** | Erstellt, 3 Tags, NICHT published |
| GA4 Property | **G-68R5XGP2QF** | Erstellt, wartet auf Daten |
| Google Ads Account | **150-077-7686** | Kampagnen erstellt |
| Search Console | https://www.kindlholz.at/ (URL prefix) | Verifizierung pending |
| Microsoft Clarity | **vxqdjkwepl** | Erstellt |

---

## Was NICHT funktioniert hat (Lessons Learned)

### AppleScript + Chrome + Google Ads = geht nicht zuverlässig
- AppleScript kann Chrome steuern und JS ausführen
- ABER: Google Ads Angular Material Buttons reagieren nicht auf simulierte Events (isTrusted=false)
- System Events Keystrokes kommen an (isTrusted=true), aber Angular-State bleibt nicht synchron
- Ad-Blocker-Overlay (z-index 100000) ist nur visuell — Funktionalität nicht beeinträchtigt
- **Fazit:** AppleScript für Google Ads = unzuverlässig. Playwright MCP ist der bessere Weg.

### Playwright MCP = funktioniert, aber mit Einschränkungen
- Kampagnen-Erstellung: funktioniert perfekt (Wizard, Ad Groups, Keywords, Ads)
- "Confirm it's you" Dialog: blockiert Publish-Schritt (Cross-Origin-Opener-Policy)
- **Workaround:** Draft im Playwright erstellen → User published im normalen Chrome
- **Lesson:** Description-Zeichenlimit (90) genau prüfen — 91 Zeichen = Publish-Fehler, KEIN Auth-Problem

### CSV-Import in Google Ads Editor = unzuverlässig
- Format extrem empfindlich, mehrere Versuche gescheitert

---

## Offene TODOs (priorisiert)

### Prio 1: Kampagnen finalisieren
- [x] Kampagne 1 `S_NB_Dienstleistungen_AT-NÖ` erstellen (6 AG, ~52 KW, 6 RSAs) — PAUSIERT
- [x] Kampagne 2 `S_B_Marke_AT-NÖ` erstellen (1 AG, 3 KW, 1 RSA) — PAUSIERT
- [x] Alle Kampagnen professionell umbenannt (Naming Convention)
- [x] Brand Ad Group umbenannt zu "Marke"
- [x] Telefonnummer aus Brand-Description gefixt
- [x] Kampagnen-Review erstellt → `kampagnen-review.md`
- [x] Remarketing-Plan erstellt → `remarketing-plan.md`
- [x] Headlines vervollständigt (15/15 pro AG)
- [x] Descriptions vervollständigt (4/4 pro AG)
- [x] Negativ-Keywords als Shared List (~80 KW, auf beide Kampagnen angewendet)
- [x] 6 Sitelinks erstellt (Dachstuhl, Carport, Terrasse, Kontakt, Dachcheck, Leistungen)
- [x] 6 Callouts erstellt (Meisterbetrieb, 4.9 Sterne, Erstberatung, etc.)
- [x] 1 Structured Snippet (Dienstleistungen: 6 Werte)
- [x] 1 Call Extension (+43 2575 8207, Austria)
- [x] 22 Remarketing-Creatives erstellt (12 Text + 10 Bild, Landscape+Square)
- [x] Remarketing-Plan erstellt (`remarketing-plan.md`)
- [x] Alte Kampagne "Search // Allgemein" zurückbenannt (nicht unsere)
- [ ] Zeitplanung setzen (Mo-Fr 06:00-20:00, Sa 08:00-14:00)
- [ ] Alte Drafts (2 Stück) manuell löschen

### Prio 2: Verknüpfungen
- [ ] GA4 ↔ Google Ads verknüpfen
- [ ] GA4 ↔ Search Console verknüpfen
- [ ] Google Ads Conversion Actions anlegen

### Prio 3: Shopify + GTM (BLOCKIERT — Shopify-Anbindung hat Probleme)
- [ ] GTM Snippet in Shopify theme.liquid einbauen
- [ ] GTM publishen (Preview Mode testen)
- [ ] Search Console verifizieren (nach GTM-Install)

### Prio 4: Conversion Tags
- [ ] Trigger: tel: Link-Klick
- [ ] Trigger: mailto: Link-Klick
- [ ] GA4 Events: phone_click, email_click als Key Events
- [ ] Google Ads Conversion Tags

### Prio 5: Später
- [ ] Cookie-Banner / Consent Mode v2
- [ ] Holzhandel/Shop-Kampagne
- [ ] Alte Kampagne pausieren (erst wenn neue Kampagne aktiv + Tracking steht)

---

## Wichtige IDs (Schnellreferenz)

| Tool | ID |
|---|---|
| GTM Container | GTM-N5PX9TV2 |
| GA4 Measurement ID | G-68R5XGP2QF |
| GA4 Stream ID | 13966091511 |
| Google Ads Account | 150-077-7686 |
| Neue Kampagne | Zimmerei & Holzbau - Dienstleistungen (23694425245) |
| Alte Kampagne | Search // Allgemein (21041998947) |
| Clarity Projekt | vxqdjkwepl |
| Search Console | https://www.kindlholz.at/ (URL prefix) |
| Login | stephan.holzbach@gmail.com |
| Telefon Kindlholz | 0 25 75 / 82 07 |
| Website | https://www.kindlholz.at |

---

## Hinweise für nächste Session

1. **Lies `fortschritt-log.md`** — da steht alles
2. **Playwright MCP nutzen** für Google Ads Interaktion (nicht AppleScript)
3. **Descriptions auf max 90 Zeichen prüfen** — war der Grund für Publish-Fehler
4. **Bestehende Kampagne "Search // Allgemein" läuft weiter** — NICHT anfassen
5. **Alles PAUSIERT erstellen** — nichts live schalten bis Tracking steht
6. **Shopify-Anbindung blockiert** — GTM kann noch nicht installiert werden
