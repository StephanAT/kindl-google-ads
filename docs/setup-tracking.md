# Kindlholz — Setup-Dokumentation

**Stand:** 18.03.2026
**Login:** stephan.holzbach@gmail.com

---

## Google Tag Manager (GTM)

| Parameter | Wert |
|---|---|
| Account | Zimmerei Kindl |
| Container | kindlholz.at |
| Container ID | **GTM-N5PX9TV2** |
| Container Typ | Web |
| Status | Erstellt, nicht installiert |

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

## Google Analytics 4 (GA4)

| Parameter | Wert |
|---|---|
| Account | Zimmerei Kindl |
| Property | kindlholz.at |
| Measurement ID | **G-68R5XGP2QF** |
| Stream ID | 13966091511 |
| Stream URL | https://www.kindlholz.at |
| Zeitzone | Austria (GMT+01:00) |
| Währung | Euro (€) |
| Branche | Home & Garden |
| Unternehmensgröße | Small (1-10) |
| Enhanced Measurement | Aktiv |
| Status | Erstellt, wartet auf Daten |

### Enhanced Measurements (aktiv):
- Page views
- Scrolls
- Outbound clicks
- + 4 weitere (Site search, Video engagement, File downloads, Form interactions)

---

## Google Ads

| Parameter | Wert |
|---|---|
| Account | Zimmerei Florian Kindl e.U. |
| Account ID | **150-077-7686** |
| Status | Besteht bereits |

---

## Google Search Console

| Parameter | Wert |
|---|---|
| Property | https://www.kindlholz.at/ (URL prefix) |
| Verifizierung | **AUSSTEHEND** — via GTM nach Shopify-Installation |
| Status | Erstellt, nicht verifiziert |

---

## Microsoft Clarity

| Parameter | Wert |
|---|---|
| Projekt | Kindlholz |
| Projekt-ID | **vxqdjkwepl** |
| URL | www.kindlholz.at |
| Branche | B2C-Dienstleistungen |
| Status | Erstellt, Tracking-Code noch nicht installiert |
| Hinweis | Shopify-Integration direkt verfügbar |

---

## Noch zu erstellen

- [x] Google Search Console → erstellt, Verifizierung pending
- [ ] Google Merchant Center → Manuelles Setup blockiert (redirected zu bestehendem Rendity-Konto). Alternative: Shopify Google Channel App nutzt eigenes MC.
- [x] Microsoft Clarity → Projekt-ID: vxqdjkwepl
- [ ] Cookie-Consent-Banner (Cookiebot oder CMP)

## GTM Tags (konfiguriert)

| Tag | Typ | Trigger | Status |
|---|---|---|---|
| GA4 - Google Tag | Google Tag (G-68R5XGP2QF) | Initialization - All Pages | Erstellt |
| Google Ads - Conversion Linker | Conversion Linker | All Pages | Erstellt |
| Microsoft Clarity | Custom HTML (vxqdjkwepl) | All Pages | Erstellt |

## Noch zu konfigurieren (GTM)

- [x] GA4 Config Tag (G-68R5XGP2QF)
- [ ] Consent Mode v2 → nach hinten geschoben (CMP-Lösung + Konto nötig, Cookiebot Template bereits im GTM importiert)
- [x] Google Ads Conversion Linker
- [ ] Conversion Tags (Anrufe, E-Mail, Formular) → nächste Session
- [x] Microsoft Clarity Tag (vxqdjkwepl)
- [ ] GTM Snippet in Shopify installieren

## Noch zu verknüpfen

- [ ] GA4 ↔ Google Ads
- [ ] GA4 ↔ Search Console
- [ ] GA4 ↔ Merchant Center
