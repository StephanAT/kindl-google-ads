# Kindlholz — Ads-Research

**Stand:** 18.03.2026
**Account:** Zimmerei Florian Kindl e.U. (150-077-7686)
**Zeitraum:** 16.02.2026 – 17.03.2026

---

## 1. Kampagnen-Überblick

| Parameter | Wert |
|---|---|
| Kampagnen | 1 ("Search // Allgemein") |
| Anzeigengruppen | 1 ("Anzeigengruppe 1") |
| Status | Enabled |
| Budget | €30/Tag |
| Gebotsstrategie | Maximise clicks |
| Kampagnentyp | Search |
| Optimierungsscore | 71,4% |

### Performance (30 Tage)

| Metrik | Wert |
|---|---|
| Impressionen | 17.509 |
| Klicks | 1.637 |
| CTR | 9,35% |
| Kosten | €923,71 |
| Avg. CPC | €0,56 |
| Conversions | **0** |
| Conv. Rate | 0,00% |

---

## 2. Keywords (Top 10 nach Kosten)

Alle Keywords: **Broad Match**, alle in **einer** Anzeigengruppe, **keine** Negativ-Keywords.

| # | Keyword | Impr. | CTR | Kosten | Klicks | CPC | Status |
|---|---|---|---|---|---|---|---|
| 1 | konstruktionsholz | 8.473 | 9,82% | **€463,40** | 832 | €0,56 | Eligible |
| 2 | holzhandel | 1.931 | 8,34% | €95,66 | 161 | €0,59 | Eligible |
| 3 | Dachdecker | 1.812 | 7,51% | €79,87 | 136 | €0,59 | **Low Quality Score** |
| 4 | holz kaufen | 915 | 8,96% | €52,53 | 82 | €0,64 | Eligible |
| 5 | Carport | 687 | 12,37% | €53,00 | 85 | €0,62 | Eligible |
| 6 | holzhandel NÖ | 920 | 10,22% | €44,24 | 94 | €0,47 | Eligible |
| 7 | Holzbau | 787 | 10,80% | €43,27 | 85 | €0,51 | Eligible |
| 8 | Terrassenüberdachung | 488 | 7,17% | €21,61 | 35 | €0,62 | Eligible |
| 9 | zimmerei | 283 | 7,07% | €12,25 | 20 | €0,61 | Eligible |
| 10 | holzbau in der nähe | 164 | 13,41% | €11,06 | 22 | €0,50 | Eligible |

**Weitere Keywords im Account** (es gibt "many" laut Google, 42 laut Gameplan — restliche nicht in Top-10).

### Keyword-Analyse

**Budget-Verteilung (geschätzt):**
- Holzhandel-Keywords (konstruktionsholz, holzhandel, holz kaufen, holzhandel NÖ): ~€655 = **~71% des Budgets**
- Zimmerei-Keywords (Holzbau, zimmerei, holzbau in der nähe): ~€66 = ~7%
- Dachdecker: €80 = ~9%
- Projekt-Keywords (Carport, Terrassenüberdachung): ~€75 = ~8%

**Problem:** Das Holzhandel-Keyword "konstruktionsholz" allein frisst **50% des Gesamtbudgets**. Zimmerei-Dienstleistungen (die wertvoller sind: Aufträge à €5.000-50.000) bekommen nur ~7%.

**Dachdecker hat Low Quality Score** — die Anzeige passt nicht zum Suchbegriff, es gibt keine Dachdecker-Landingpage.

---

## 3. Anzeige

**1 Responsive Search Ad** — Ad Strength: **Poor**

### Sichtbare Headlines (Beispiel):
- "Bauholz bestellen-Holzhandlung"
- "Zimmerei - Holzbau in der Nähe"
- "überdachte Terrasse"
- +12 weitere Headlines

### Sichtbare Descriptions:
- "Dein Experte im Holzbau - dein verlässlicher Partner für Dachstühle und Überdachungen."
- "Wir unterstützen dich mit unserem Expertenwissen bei der Planung und Ausführung."
- +2 weitere

### Final URL
- **Alles auf die Startseite** (www.kindlholz.at) — keine landingpage-spezifischen URLs

### Probleme:
1. **Gemischte Signale:** Bauholz-Headlines + Zimmerei-Headlines + Terrassen-Headlines in einer Anzeige. Jemand der "Zimmerei" sucht, sieht möglicherweise "Bauholz bestellen"
2. **Ad Strength: Poor** — Google bewertet die Anzeige als schlecht
3. **Nur eine Anzeige** für alle ~42 Keywords
4. **Keine Keyword-spezifischen Landingpages** — alles auf Startseite

---

## 4. Structured Snippets

Laut Gameplan: Tippfehler "Zeil" statt "Ziel" in Structured Snippets. → Muss bei Kampagnen-Aufbau korrigiert werden.

---

## 5. Zusammenfassung der Probleme

| Problem | Impact | Priorität |
|---|---|---|
| Kein Conversion-Tracking | Blindflug, Google kann nicht optimieren | KRITISCH |
| 1 Anzeige für alles | Relevanz-Verlust, schlechter Quality Score | KRITISCH |
| "konstruktionsholz" frisst 50% Budget | Zimmerei-Anfragen werden verdrängt | HOCH |
| Alle Broad Match, keine Negativ-Keywords | Streuverluste durch irrelevante Suchen | HOCH |
| Alles auf Startseite | Keine landingpage-spezifischen Erlebnisse | HOCH |
| Dachdecker Low Quality Score | Geld wird verschwendet | MITTEL |
| Ad Strength: Poor | Google zeigt Anzeige seltener | MITTEL |
| Maximise clicks Strategie | Optimiert auf billige Klicks, nicht auf Ergebnisse | MITTEL |

---

## 6. Nächste Schritte (gemäß Umsetzungsplan)

1. **Tracking-Setup** (Schritt 1): GTM, GA4, Consent, Conversion-Tags
2. **Sofort-Fixes** an bestehender Kampagne (Schritt 4.1):
   - Negativ-Keywords hinzufügen
   - Dachdecker in eigene Anzeigengruppe
   - Manueller CPC als Übergang
3. **Neue Kampagnen** aufbauen (Schritt 4.2-4.4):
   - Kampagne 1: Zimmerei & Holzbau (60% Budget)
   - Kampagne 2: Holzhandel/Shop (30% Budget)
   - Kampagne 3: Brand (10% Budget)
4. **Alte Kampagne pausieren** (nicht löschen!)
