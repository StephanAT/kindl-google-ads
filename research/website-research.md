# Kindlholz — Website-Research

**Stand:** 18.03.2026
**Website:** https://www.kindlholz.at (Shopify)

---

## 1. Website-Struktur

### Navigation (Hauptmenü)
| Menüpunkt | URL | Typ |
|---|---|---|
| Home | / | Startseite |
| Dachcheck | /pages/dachcheck | Service |
| Online-Shop | /collections | Shop |
| Leistungen | (Dropdown) | Service-Seiten |
| Über uns | /pages/uber-uns | Info |
| Kontakt | /pages/kontakt | Kontakt |

### Service-Seiten (Leistungen)

| Seite | URL | Status | CTA | Formular | Video |
|---|---|---|---|---|---|
| Carport | /pages/carport | OK | "Jetzt Kontakt aufnehmen!" → /pages/kontakt | Nein | Ja (funktioniert) |
| Dachstuhl | /pages/dachstuhle | OK | "Jetzt Angebot anfordern!" → /pages/kontakt | Nein | Ja (funktioniert) |
| Terrassenüberdachung / Pergola | /pages/terrassenuberdachung-pergola | OK | "Jetzt Kontakt aufnehmen!" → /pages/kontakt | Nein | Nein |
| Holzriegelbau | /pages/holzriegelbau | OK | "Jetzt Kontakt aufnehmen!" → /pages/kontakt | Nein | Ja (FEHLER auf Startseite) |
| Reparaturarbeiten | /pages/reparaturarbeiten | OK | "Jetzt Kontakt aufnehmen!" → /pages/kontakt | Nein | Nein |
| Zellulosedämmung | /pages/zellulosedammung | OK | "Jetzt Kontakt aufnehmen!" → /pages/kontakt | Nein | Ja (funktioniert) |
| Dachausbau | /pages/dachausbau | OK | "Jetzt Kontakt aufnehmen!" → /pages/kontakt | Nein | Nein |
| Sonderbauten | /pages/sonderbauten | OK | "Jetzt Kontakt aufnehmen!" → /pages/kontakt | Nein | Nein |
| Dachcheck | /pages/dachcheck | OK | "Jetzt Dachcheck anfragen" | **JA** (Jotform iframe) | Nein |
| **Dacharbeiten** | **/pages/dacharbeiten** | **404!** | — | — | — |

### Info-Seiten (Footer)

| Seite | URL |
|---|---|
| Kontakt & Öffnungszeiten | /pages/kontakt |
| Abholung, Zahlung & Lieferung | /pages/versand-zahlung |
| Datenschutzerklärung | /pages/datenschutzerklarung |
| Widerrufsbelehrung | /pages/widerrufsbelehrung |
| Impressum | /pages/impressum |
| AGB | /pages/agb |
| Sonderbestellung | /pages/sonderbestellung |

### Blog
- /blogs/aktuelles/ (verlinkt von Sonderbauten-Seite, z.B. Gossenüberdachung)

---

## 2. Kontaktdaten

| Kanal | Details |
|---|---|
| Telefon | 0 25 75 / 82 07 (tel:025758207) |
| E-Mail | office@kindlholz.at |
| Adresse | F. Kindl Zimmerei GmbH, Hauptstraße 145, A-2126 Ladendorf |
| Öffnungszeiten | Mo-Do 07:00-16:00 |
| Telefonisch erreichbar | Mo-Fr 08:00-15:00 (jeder 2. Freitag geschlossen, ungerade KW) |
| **Kontaktformular** | **KEINES vorhanden** (nur auf Dachcheck-Seite: Jotform iframe) |
| Google Maps | Eingebettet auf Kontaktseite |
| Trustpilot | Widget im Footer auf jeder Seite |
| Facebook | facebook.com/profile.php?id=61553237262678 |
| Instagram | instagram.com/zimmereikindl/ |
| YouTube | youtube.com/channel/UCSJEJrrvJw_di-m-ZfZIWeQ |

---

## 3. Online-Shop (Shopify)

### Collections (Kategorien)

| Collection | URL | Produkte |
|---|---|---|
| Holz | /collections/holz | 15+ Produkte (Kantholz, Staffel, Pfosten, Bretter, Latten, BSH, Glattkant — jeweils Fichte + Lärche) |
| Montagematerial | /collections/montagematerial | Schrauben, Winkel etc. |
| Holzschutz | /collections/holzschutz | Lasuren, Öle etc. |
| Bausätze | /collections/bausatze | 4x Weinviertler Hochbeet (Fichte/Lärche, sägerau/gehobelt), Noppenbahn, Holzpfahl |
| Dämmung | /collections/dammung | Isocell Zellulose |
| Platten | /collections/platten | OSB, DHF etc. |
| Dachbahnen, Kleber | /collections/dachbahnen-kleber | Dachbahnen, Kleber |

### Hochbeet-Produkte (Bestseller)

| Produkt | URL | Preis |
|---|---|---|
| Weinviertler Hochbeet Fichte sägerau | /products/hochbeet-bausatz-fichte-saegerau | ab €280,64 |
| Weinviertler Hochbeet Fichte gehobelt | /products/hochbeet-bausatz-fichte-gehobelt | ab €345,78 |
| Weinviertler Hochbeet Lärche sägerau | /products/hochbeet-bausatz-laerche-saegerau | ab €360,07 |
| Weinviertler Hochbeet Lärche gehobelt | /products/hochbeet-bausatz-laerche-gehobelt | ab €471,27 |

### Shop-Features
- Click & Collect (Abholung in Ladendorf, auch außerhalb der Öffnungszeiten)
- Preise inkl. MwSt.
- Varianten über Größen/Dimensionen
- Tag-basierte Filterung (z.B. "bauschnittholz", "lärche", "fichte")

---

## 4. URL-Korrekturen für Kampagnen

**KRITISCH — Diese URLs aus dem Gameplan stimmen NICHT:**

| Gameplan-URL | Tatsächliche URL | Problem |
|---|---|---|
| /pages/dacharbeiten | **EXISTIERT NICHT (404)** | Keine Dachdecker-Seite vorhanden! |
| /pages/dachstühle | /pages/dachstuhle | Umlaut-Unterschied |
| /pages/terrassenüberdachung | /pages/terrassenuberdachung-pergola | Anderer Slug + Pergola im Namen |
| /collections/bauschnittholz | /collections/holz (Tag: /collections/holz/bauschnittholz) | Ist ein Tag, keine eigene Collection |
| /products/hochbeet-bausatz | /collections/bausatze | Mehrere Hochbeet-Produkte, kein einzelnes |
| /products/isocell-zellulose-daemmung-sack | /collections/dammung | Muss verifiziert werden |

### Empfohlene Landingpages für Kampagnen

| Anzeigengruppe | Empfohlene Landingpage | Notiz |
|---|---|---|
| Zimmerei allgemein | / (Startseite) | OK |
| Carport | /pages/carport | OK |
| Dachstuhl | /pages/dachstuhle | URL ohne Umlaut! |
| **Dachdecker** | **/pages/dachcheck** oder **/pages/reparaturarbeiten** | /pages/dacharbeiten existiert nicht! |
| Terrasse & Pergola | /pages/terrassenuberdachung-pergola | Korrigierte URL |
| Spezialleistungen | Jeweilige Unterseite | OK |
| Bauholz | /collections/holz | Oder Tag-Filter /collections/holz/bauschnittholz |
| Lärche & Bretter | /collections/holz | Tag-Filter möglich: /collections/holz/larche |
| Dämmung | /collections/dammung | OK |
| Hochbeet & Garten | /collections/bausatze | Mehrere Hochbeet-Produkte |

---

## 5. YouTube-Videos (Startseite)

| Slide | Video | Status |
|---|---|---|
| Carport | "carport" (youtube.com/watch?v=2mOgZL15Q2M) | Funktioniert |
| Dachstuhl | "Vom Plan zum Dachstuhl!" | **FEHLER: Playback Error** |
| Holzriegelbau | (eingebettet) | **FEHLER: Playback Error** |
| Zellulosedämmung | "Isocell Zellulose Dämmung" (youtube.com/watch?v=IcT042QcUnY) | Funktioniert |

**Hinweis:** Dachstuhl-Video funktioniert auf der Unterseite /pages/dachstuhle, nur das Startseiten-Embed ist kaputt.

---

## 6. Cookie-Banner (aktuell)

- Shopify-eigener Cookie-Banner (Storefront Privacy Banner)
- 3 Buttons: "Konfigurationen verwalten", "Ok", "Nein, danke"
- **NICHT DSGVO-konform:** Kein Consent Mode v2, kein granularer Consent (Marketing/Analytics/Funktional)
- **NICHT geeignet** für Google Ads / GA4 Tracking — muss ersetzt werden durch Cookiebot oder CMP

---

## 7. Beobachtungen & Empfehlungen

### Kritisch
1. **Kein Kontaktformular** auf Service-Seiten — nur Telefon + E-Mail. Einziges Formular ist auf der Dachcheck-Seite (Jotform iframe). Conversion-Tracking für Formulare daher aktuell nur auf Dachcheck möglich.
2. **Keine Dachdecker/Dacharbeiten-Seite** — trotz Positionierung als "Zimmerei und Dachdeckerei". /pages/dacharbeiten ist 404. Für Ads muss eine alternative Landingpage gewählt werden.
3. **Cookie-Banner nicht DSGVO-konform** — kein Consent Mode v2, Tags können nicht nach Consent-Typ gesteuert werden.

### Hoch
4. **2 von 4 YouTube-Videos kaputt** auf der Startseite (Dachstuhl + Holzriegelbau Playback Error)
5. **Telefonnummer nicht im Header/Sticky-Bereich** — nur auf Kontaktseite sichtbar
6. **Kein Trust-Element** (Google Bewertungen, 4,9 Sterne) auf Service-Seiten — nur Trustpilot im Footer

### Mittel
7. Service-Seiten haben gleiches Template (6 Schritte) — gut für Konsistenz, aber wenig differenziert
8. Blog existiert (/blogs/aktuelles/) aber scheint wenig gepflegt
9. Sonderbestellung-Seite vorhanden (/pages/sonderbestellung) — nicht im Gameplan erwähnt

---

## 8. Tracking-Status (IST)

| Tool | Status |
|---|---|
| Google Tag Manager | Nicht vorhanden |
| Google Analytics 4 | Nicht vorhanden |
| Google Ads Conversion Tag | Nicht vorhanden |
| Google Search Console | Nicht vorhanden |
| Consent Mode v2 | Nicht vorhanden |
| Microsoft Clarity | Nicht vorhanden |
| Facebook Pixel | Nicht vorhanden |
| Shopify Google Channel | Nicht geprüft |

**Fazit:** Kompletter Blindflug — kein einziges Analytics- oder Tracking-Tool aktiv.
