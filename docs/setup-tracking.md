# Kindlholz — Setup & Tracking Dokumentation

**Stand:** 25.03.2026
**Login:** stephan.holzbach@gmail.com

---

## Alle IDs (Schnellreferenz)

| Tool | ID | Status |
|---|---|---|
| GTM Container | **GTM-N5PX9TV2** | Erstellt, Tags konfiguriert, **NICHT auf Shopify installiert** |
| GA4 Measurement ID | **G-68R5XGP2QF** | Erstellt, mit Google Ads verknüpft |
| GA4 Stream ID | 13966091511 | |
| Google Ads Account | **150-077-7686** | 4 Kampagnen, 9 Conversion Actions |
| Search Console | https://www.kindlholz.at/ (URL prefix) | Erstellt, Verifizierung pending |
| Microsoft Clarity | **vxqdjkwepl** | Erstellt, GTM Tag konfiguriert |
| Google Business Profil | Zimmerei Kindl, Ladendorf | Existiert, 4,9★ |
| Telefon | 0 25 75 / 82 07 | Call Extension aktiv |
| Website | https://www.kindlholz.at | Shopify |

---

## Google Ads Kampagnen (Stand 25.03.2026)

| Kampagne | Typ | Budget | AGs | Keywords | Status |
|---|---|---|---|---|---|
| S_NB_Dienstleistungen_AT-NÖ | Search | €20/Tag | 6 | ~52 | Pausiert |
| S_B_Marke_AT-NÖ | Search | €3/Tag | 1 | 3 | Pausiert |
| DG_RT_Dienstleistungen_AT-NÖ | Demand Gen (Remarketing) | €5/Tag | 2 | — | Pausiert |
| Search // Allgemein | Search (bestehend) | €30/Tag | 1 | 42 | Aktiv |

### Naming Convention
```
[Netzwerk]_[Brand/NonBrand]_[Thema]_[Geo]
S = Search, DG = Demand Gen, RT = Retargeting, NB = Non-Brand, B = Brand
```

### Ad Extensions (Account-Level)
- **6 Sitelinks:** Dachstuhl, Carport, Terrassenüberdachung, Kontakt, Dachcheck, Leistungen
- **6 Callouts:** Meisterbetrieb seit 1963, 4,9 Sterne bei 42 Bewertungen, Kostenlose Erstberatung, Computergesteuerter Abbund, Planung & Ausführung, Weinviertel / NÖ
- **1 Structured Snippet:** Dienstleistungen → Dachstuhl, Carport, Terrassenüberdachung, Holzriegelbau, Dachsanierung, Dachcheck
- **1 Call Extension:** +43 2575 8207 (Austria)

### Negativ-Keywords
- **Shared List:** "Kindlholz — Global Negatives" (~80 Keywords)
- Auf beide Kampagnen angewendet
- Kategorien: DIY, Jobs, Bildung, Schnäppchenjäger, irrelevante Produkte, Shop-Keywords

### Conversion Actions (9 Stück)
| Conversion | Quelle | Status |
|---|---|---|
| Lead-Formular – senden | Google hosted | Aktiv |
| Lead-Formular senden | Website | Inaktiv (braucht GTM) |
| Lead-Formular senden (1) | Website | Inaktiv (braucht GTM) |
| Click-to-Call | Google hosted | Aktiv (61 Conv.) |
| Calls from ads | Call from Ads | Aktiv |
| Contact | Website | Inaktiv (braucht GTM) |
| Lokale Aktionen – Wegbeschreibung | Google hosted | Aktiv (31) |
| Lokale Aktionen – andere Interaktionen | Google hosted | Aktiv (59) |
| Lokale Aktionen – Websitebesuche | Google hosted | Aktiv (27) |

### Verknüpfungen
- [x] GA4 ↔ Google Ads (kindlholz.at Property 529037683)
- [x] Search Console ↔ Google Ads
- [ ] Google Business Profil ↔ Google Ads (noch offen)

---

## GTM Container (GTM-N5PX9TV2)

### Tags (konfiguriert, nicht published)
| Tag | Typ | Trigger | Status |
|---|---|---|---|
| GA4 - Google Tag | Google Tag (G-68R5XGP2QF) | Initialization - All Pages | Erstellt |
| Google Ads - Conversion Linker | Conversion Linker | All Pages | Erstellt |
| Microsoft Clarity | Custom HTML (vxqdjkwepl) | All Pages | Erstellt |

### Noch zu konfigurieren im GTM (nach Shopify-Install)
- [ ] Consent Mode v2 (CMP: Cookiebot empfohlen)
- [ ] Google Ads Conversion Tag: phone_click (tel: Link-Klick)
- [ ] Google Ads Conversion Tag: email_click (mailto: Link-Klick)
- [ ] Google Ads Conversion Tag: form_submit (Dachcheck Jotform)
- [ ] GA4 Custom Events: phone_click, email_click als Key Events
- [ ] Remarketing Tag (oder GA4 Audiences nutzen)
- [ ] GTM publishen (erst Preview Mode testen!)

### GTM Snippets für Shopify

**Head-Snippet** (in `<head>` so weit oben wie möglich):
```html
<!-- Google Tag Manager -->
<script>(function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':
new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],
j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';j.async=true;j.src=
'https://www.googletagmanager.com/gtm.js?id='+i+dl;f.parentNode.insertBefore(j,f);
})(window,document,'script','dataLayer','GTM-N5PX9TV2');</script>
<!-- End Google Tag Manager -->
```

**Body-Snippet** (direkt nach öffnendem `<body>`):
```html
<!-- Google Tag Manager (noscript) -->
<noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-N5PX9TV2"
height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript>
<!-- End Google Tag Manager (noscript) -->
```

---

## Remarketing-Assets

22 Creatives in `/remarketing-creatives/png/`:
- **10 Bild-Sujets** (img-1 bis img-5, Landscape + Square) — echte Fotos mit Text-Overlay
- **12 Text-Sujets** (rm-1 bis rm-6, Landscape + Square) — minimalistischer Content-Match-Stil
- **Präsentation:** https://stephanat.github.io/kindl-google-ads/
- **GitHub:** https://github.com/StephanAT/kindl-google-ads

---

## Anleitung für Gerald (Shopify GTM-Installation)

### Was zu tun ist
2 Code-Snippets in Shopify theme.liquid einfügen. Dauert 5 Minuten.

### Schritt-für-Schritt

1. **Shopify Admin öffnen:** kindlholz.myshopify.com/admin
2. **Online Store → Themes → Actions → Edit Code**
3. **theme.liquid öffnen** (unter "Layout")
4. **Head-Snippet einfügen:** Das folgende Snippet direkt nach dem öffnenden `<head>` Tag einfügen (so weit oben wie möglich, VOR anderen Scripts):

```html
<!-- Google Tag Manager -->
<script>(function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':
new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],
j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';j.async=true;j.src=
'https://www.googletagmanager.com/gtm.js?id='+i+dl;f.parentNode.insertBefore(j,f);
})(window,document,'script','dataLayer','GTM-N5PX9TV2');</script>
<!-- End Google Tag Manager -->
```

5. **Body-Snippet einfügen:** Das folgende Snippet direkt nach dem öffnenden `<body>` Tag einfügen:

```html
<!-- Google Tag Manager (noscript) -->
<noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-N5PX9TV2"
height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript>
<!-- End Google Tag Manager (noscript) -->
```

6. **Save** klicken
7. **Fertig!** — Bitte kurz Bescheid geben wenn eingebaut, dann publishe ich den GTM Container.

### Was NICHT angefasst werden muss
- Keine anderen Dateien ändern
- Kein bestehender Code löschen
- Nur diese 2 Snippets an den beschriebenen Stellen einfügen

### Nach der Installation (macht Stephan)
- GTM Container im Preview Mode testen
- GTM publishen
- Search Console verifizieren
- Conversion Tags testen
- Cookie Banner (Consent Mode) einrichten
- Kampagnen aktivieren

---

## Offene TODOs (priorisiert)

### Sofort (braucht Gerald/Shopify-Zugang)
- [ ] GTM Snippet in theme.liquid einbauen (Anleitung oben)

### Nach GTM-Installation (macht Stephan)
- [ ] GTM Preview Mode testen
- [ ] GTM publishen
- [ ] Search Console verifizieren
- [ ] Consent Mode v2 + Cookiebot einrichten
- [ ] Conversion Tags im GTM konfigurieren (tel:, mailto:, form)
- [ ] GA4 Events als Key Events markieren
- [ ] Google Business Profil mit Ads verknüpfen
- [ ] Remarketing Audiences in GA4 anlegen
- [ ] Kampagnen aktivieren (Dienstleistungen → Brand → Remarketing)

### Später
- [ ] Zeitplanung nach 2-4 Wochen Live-Daten
- [ ] Holzhandel/Shop-Kampagne
- [ ] Alte Kampagne "Search // Allgemein" pausieren
