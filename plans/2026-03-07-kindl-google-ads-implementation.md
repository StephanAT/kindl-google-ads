# Kindl Google Ads — Kampagnenplan Implementation

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Complete research-driven Google Ads campaign plan for Zimmerei Kindl (kindlholz.at) — 3 campaigns (Zimmerei/Dachdecker, Holzhandel/Shop, Marke) with full keyword research, competitor analysis, and ready-to-implement deliverables.

**Architecture:** Phase 1 collects all data via DataForSEO API (keywords, competitors, SERPs). Phase 2 processes and structures the data into campaign blueprints. Phase 3 produces two deliverables: a client-facing strategy PDF and an implementation playbook.

**Tech Stack:** DataForSEO MCP (keyword research, SERP analysis, competitor analysis), Python (data processing), HTML/CSS (PDF generation), Chrome headless (PDF export)

**Important:** If DataForSEO API tokens run out during any task, document what was completed, skip remaining API calls, and continue with available data.

---

## Task 1: Keyword Discovery — Zimmerei & Holzbau

**Goal:** Collect all relevant keywords for the Zimmerei/Holzbau business area in Austria.

**Step 1: Run keyword_suggestions for core Zimmerei seeds**

Run these API calls (all with `location_name: "Austria"`, `language_code: "de"`, `limit: 50`):

```
keyword_suggestions("zimmerei") → 50 suggestions
keyword_suggestions("holzbau") → 50 suggestions
keyword_suggestions("zimmerer in der nähe") → 50 suggestions
keyword_suggestions("carport holz") → 50 suggestions
keyword_suggestions("terrassenüberdachung holz") → 50 suggestions
keyword_suggestions("dachstuhl bauen") → 50 suggestions
keyword_suggestions("pergola holz") → 50 suggestions
keyword_suggestions("holzriegelbau") → 50 suggestions
```

**Step 2: Run keyword_ideas for broader discovery**

```
keyword_ideas(["zimmerei", "holzbau", "zimmerer", "holzkonstruktion"]) → 100 ideas
keyword_ideas(["carport holz", "terrassenüberdachung", "pergola", "vordach holz"]) → 100 ideas
keyword_ideas(["aufstockung holzbau", "holzfassade", "balkon holz", "gartenhaus holz"]) → 100 ideas
```

**Step 3: Run related_keywords for "searches related to" expansion**

```
related_keywords("zimmerei niederösterreich", depth=2) → 30 related
related_keywords("holzbau firma", depth=2) → 30 related
related_keywords("carport bauen lassen", depth=2) → 30 related
```

**Step 4: Save raw results**

Save all results to `/Users/stephanholzbach/kindl-research/keywords-zimmerei-raw.json`

**Expected output:** 300-500 unique keywords with SV, CPC, competition data for the Zimmerei/Holzbau area.

---

## Task 2: Keyword Discovery — Dachdecker

**Goal:** Collect all relevant Dachdecker keywords for Austria.

**Step 1: Run keyword_suggestions for Dachdecker seeds**

All with `location_name: "Austria"`, `language_code: "de"`, `limit: 50`:

```
keyword_suggestions("dachdecker") → 50 suggestions
keyword_suggestions("dachdeckerei") → 50 suggestions
keyword_suggestions("dach reparieren") → 50 suggestions
keyword_suggestions("dachsanierung") → 50 suggestions
keyword_suggestions("dach undicht") → 50 suggestions
keyword_suggestions("dachreparatur") → 50 suggestions
```

**Step 2: Run keyword_ideas for broader discovery**

```
keyword_ideas(["dachdecker", "dachdeckerei", "dach reparieren", "dachsanierung"]) → 100 ideas
keyword_ideas(["dachziegel", "dachrinne", "flachdach", "steildach"]) → 100 ideas
keyword_ideas(["dachdämmung", "dachfenster einbau", "dach decken"]) → 100 ideas
```

**Step 3: Run related_keywords**

```
related_keywords("dachdecker niederösterreich", depth=2) → 30 related
related_keywords("dach reparieren lassen", depth=2) → 30 related
```

**Step 4: Save raw results**

Save to `/Users/stephanholzbach/kindl-research/keywords-dachdecker-raw.json`

**Expected output:** 200-400 unique Dachdecker keywords.

---

## Task 3: Keyword Discovery — Holzhandel/Shop

**Goal:** Collect all relevant Holzhandel/Shop keywords for Austria.

**Step 1: Run keyword_suggestions for Shop seeds**

All with `location_name: "Austria"`, `language_code: "de"`, `limit: 50`:

```
keyword_suggestions("konstruktionsholz kaufen") → 50 suggestions
keyword_suggestions("bauholz kaufen") → 50 suggestions
keyword_suggestions("holz kaufen") → 50 suggestions
keyword_suggestions("lärchenpfosten") → 50 suggestions
keyword_suggestions("holzbretter kaufen") → 50 suggestions
keyword_suggestions("zellulose einblasdämmung") → 50 suggestions
keyword_suggestions("hochbeet holz") → 50 suggestions
```

**Step 2: Run keyword_ideas for broader discovery**

```
keyword_ideas(["konstruktionsholz", "bauholz", "kantholz", "holzbalken"]) → 100 ideas
keyword_ideas(["lärche sägerau", "fichte sägerau", "bretter", "nut feder bretter"]) → 100 ideas
keyword_ideas(["dhf platte", "isocell zellulose", "hochbeet bausatz"]) → 100 ideas
```

**Step 3: Run related_keywords**

```
related_keywords("konstruktionsholz kaufen", depth=2) → 30 related
related_keywords("bauholz online bestellen", depth=2) → 30 related
```

**Step 4: Save raw results**

Save to `/Users/stephanholzbach/kindl-research/keywords-holzhandel-raw.json`

**Expected output:** 200-400 unique Holzhandel keywords.

---

## Task 4: Keyword Discovery — Marke (Brand)

**Goal:** Collect all brand-related search terms.

**Step 1: Run keyword_suggestions for brand seeds**

```
keyword_suggestions("kindl zimmerei") → 30 suggestions
keyword_suggestions("kindlholz") → 30 suggestions
keyword_suggestions("kindl ladendorf") → 30 suggestions
```

**Step 2: Run keyword_overview for known brand terms**

```
keyword_overview(["zimmerei kindl", "kindl ladendorf", "kindlholz", "kindl holz", "zimmerei kindl ladendorf", "kindl zimmerei niederösterreich", "kindl dachdeckerei", "kindl holzhandel"]) → SV + CPC data
```

**Step 3: Save results**

Save to `/Users/stephanholzbach/kindl-research/keywords-brand-raw.json`

---

## Task 5: Competitor Analysis — Domain Rankings

**Goal:** Understand what competitors rank for and how strong they are.

**Step 1: Domain rank overview for all 5 domains**

All with `location_name: "Austria"`, `language_code: "de"`:

```
domain_rank_overview("kindlholz.at")
domain_rank_overview("longin.at")
domain_rank_overview("mp-holzbau.at")
domain_rank_overview("holzbau-k.at")
domain_rank_overview("holzbau-noe.at")
```

**Step 2: Ranked keywords for each competitor (Top 100)**

```
ranked_keywords("longin.at", limit=100, order_by=["keyword_data.keyword_info.search_volume,desc"])
ranked_keywords("mp-holzbau.at", limit=100, order_by=["keyword_data.keyword_info.search_volume,desc"])
ranked_keywords("holzbau-k.at", limit=100, order_by=["keyword_data.keyword_info.search_volume,desc"])
ranked_keywords("holzbau-noe.at", limit=50, order_by=["keyword_data.keyword_info.search_volume,desc"])
ranked_keywords("kindlholz.at", limit=100, order_by=["keyword_data.keyword_info.search_volume,desc"])
```

**Step 3: Competitors for kindlholz.at**

```
competitors_domain("kindlholz.at", limit=20, exclude_top_domains=true)
```

**Step 4: Domain intersection — Kindl vs top competitor**

```
domain_intersection("kindlholz.at", "longin.at", limit=50)
domain_intersection("kindlholz.at", "mp-holzbau.at", limit=50)
```

**Step 5: Save all results**

Save to `/Users/stephanholzbach/kindl-research/competitors-raw.json`

**Expected output:** Complete picture of competitor landscape — who ranks for what, how strong they are, where Kindl overlaps/differs.

---

## Task 6: SERP Analysis — Top Keywords

**Goal:** See who actually ranks (organic + ads) for the most important keywords.

**Step 1: Live SERP for Zimmerei keywords**

All with `location_name: "Austria"`, `language_code: "de"`, `depth: 20`:

```
serp_organic_live_advanced("zimmerei niederösterreich")
serp_organic_live_advanced("zimmerer in der nähe")
serp_organic_live_advanced("holzbau niederösterreich")
serp_organic_live_advanced("carport holz")
serp_organic_live_advanced("carport bauen lassen")
serp_organic_live_advanced("terrassenüberdachung holz")
serp_organic_live_advanced("dachstuhl bauen")
```

**Step 2: Live SERP for Dachdecker keywords**

```
serp_organic_live_advanced("dachdecker niederösterreich")
serp_organic_live_advanced("dach reparieren")
serp_organic_live_advanced("dachsanierung niederösterreich")
```

**Step 3: Live SERP for Holzhandel keywords**

```
serp_organic_live_advanced("konstruktionsholz kaufen")
serp_organic_live_advanced("bauholz kaufen")
serp_organic_live_advanced("lärchenpfosten kaufen")
serp_organic_live_advanced("holz kaufen online")
```

**Step 4: SERP competitors analysis**

```
serp_competitors(["zimmerei niederösterreich", "dachdecker niederösterreich", "holzbau niederösterreich", "carport holz", "konstruktionsholz kaufen"], limit=20)
```

**Step 5: Save all results**

Save to `/Users/stephanholzbach/kindl-research/serps-raw.json`

**Expected output:** Who ranks where, who runs ads, SERP features (Local Pack, etc.) for all key queries.

---

## Task 7: Website Audit — kindlholz.at Landing Pages

**Goal:** Map all existing landing pages on kindlholz.at that can be used for Google Ads.

**Step 1: Crawl kindlholz.at pages**

Use Playwright browser to navigate kindlholz.at and document:
- Homepage
- All /pages/* service pages (Carport, Dachstühle, Terrassenüberdachung, etc.)
- All /collections/* shop category pages
- All /products/* product pages (top ones)
- Contact page
- Any other relevant pages

**Step 2: Document each page**

For each landing page, note:
- URL
- Page title
- H1
- Key content/services mentioned
- Has contact form? Phone number? CTA?
- Mobile-friendly?
- Suitable for which ad group?

**Step 3: Save results**

Save to `/Users/stephanholzbach/kindl-research/landing-pages.md`

**Expected output:** Complete landing page map with ad group assignments.

---

## Task 8: Data Processing — Keyword Master List

**Goal:** Deduplicate, categorize, and score all collected keywords into one master list.

**Step 1: Load all raw keyword files**

Read all JSON files from Tasks 1-4.

**Step 2: Deduplicate keywords**

Merge all keywords, remove duplicates (case-insensitive).

**Step 3: Get bulk keyword overview for all unique keywords**

```
keyword_overview([all unique keywords], location_name="Austria", language_code="de")
```

Split into batches of 700 if needed.

**Step 4: Get bulk keyword difficulty**

```
bulk_keyword_difficulty([top 200 keywords by SV], location_name="Austria", language_code="de")
```

**Step 5: Categorize each keyword**

Assign to:
- Campaign: Zimmerei/Dachdecker, Holzhandel, Marke, or NEGATIVE
- Ad Group: specific group within campaign
- Match Type recommendation: Exact, Phrase, or Broad
- Priority: High, Medium, Low
- Status: Use, Monitor, Negative

**Step 6: Save master list**

Save to `/Users/stephanholzbach/kindl-research/keyword-master-list.csv` with columns:
keyword | search_volume | cpc | competition | difficulty | campaign | ad_group | match_type | priority | status

Also save as formatted markdown to `/Users/stephanholzbach/kindl-research/keyword-master-list.md`

**Expected output:** Single source of truth with 500+ categorized keywords.

---

## Task 9: Data Processing — Competitor Report

**Goal:** Create a structured competitor analysis from raw data.

**Step 1: Load competitor raw data from Task 5**

**Step 2: Build competitor profiles**

For each domain (longin.at, mp-holzbau.at, holzbau-k.at, holzbau-noe.at):
- Total organic keywords
- Estimated organic traffic
- Top 20 keywords by search volume
- Do they run Google Ads? For which keywords?
- Strongest pages/URLs
- Content strategy (blog, service pages, etc.)

**Step 3: Build competitive gaps analysis**

- Keywords competitors rank for that Kindl doesn't
- Keywords Kindl ranks for that competitors don't
- Shared keywords where Kindl ranks lower

**Step 4: Save report**

Save to `/Users/stephanholzbach/kindl-research/competitor-report.md`

---

## Task 10: Build Campaign Blueprints

**Goal:** Create exact, copy-paste-ready campaign configurations.

**Step 1: Kampagne 1 — Zimmerei, Dachdecker & Holzbau**

For each of the 6 ad groups, specify:
- Exact keyword list with match types (from master list)
- Final URL (from landing page audit)
- RSA: 15 headlines + 4 descriptions (with pin instructions)
- Sitelinks (4-6 per ad group)
- Callout extensions
- Structured snippets
- Call extension phone number
- Bid strategy settings
- Geo targeting settings
- Device bid adjustments
- Ad schedule (if applicable)

**Step 2: Kampagne 2 — Holzhandel & Online-Shop**

Same structure for 4 ad groups.

**Step 3: Kampagne 3 — Marke**

Same structure for 1 ad group.

**Step 4: Account-level negative keywords list**

Organized by category (DIY, Jobs, Bildung, etc.)

**Step 5: Campaign-level negative keywords**

Cross-campaign negatives to prevent cannibalization.

**Step 6: Save blueprints**

Save to `/Users/stephanholzbach/kindl-research/campaign-blueprints.md`

---

## Task 11: Build Strategy PDF (for client)

**Goal:** Create a professional PDF document for Flo with market data, strategy, and recommendations.

**Step 1: Build HTML document**

Structure:
1. Cover page (Kindl logo, title, date)
2. Executive Summary (key findings, opportunity)
3. Marktanalyse (keyword volumes, seasonal trends, competition landscape)
4. Ist-Zustand (current campaign audit summary)
5. Strategie (3 campaigns, why, budget)
6. Keyword-Recherche (top keywords per area with real data)
7. Konkurrenz-Analyse (who ranks, who advertises, gaps)
8. Kampagnenstruktur (visual overview, ad groups, landing pages)
9. Budget & Prognose (scenarios, expected conversions, ROI)
10. Tracking-Setup (GTM, GA4, etc.)
11. Umsetzungsplan (8-week timeline)
12. Nächste Schritte

**Step 2: Style with existing CSS**

Use the same design system as kindlholz-gameplan.html (Inter font, green/blue/orange palette).

**Step 3: Generate PDF**

```bash
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless --disable-gpu --no-pdf-header-footer --print-to-pdf="/Users/stephanholzbach/kindl-research/kindl-strategie-2026.pdf" --run-all-compositor-stages-before-draw "/Users/stephanholzbach/kindl-research/kindl-strategie-2026.html"
```

**Expected output:** Professional 20-30 page PDF with real market data.

---

## Task 12: Build Implementation Playbook (for Stephan)

**Goal:** Create a step-by-step implementation guide with copy-paste content.

**Step 1: Write playbook document**

Save to `/Users/stephanholzbach/kindl-research/implementation-playbook.md`

Sections:
1. **Pre-Flight Checklist** — accounts needed, access required
2. **Week 1: Tracking Setup** — exact steps for GTM, GA4, Cookie Banner, Conversion Tags, Search Console, Business Profile, Clarity, Shopify integration
3. **Week 2: Campaign Build** — step-by-step for each campaign/ad group with copy-paste keywords and ad texts from blueprints
4. **Week 3-4: Monitoring Checklist** — daily/weekly tasks, what to look for
5. **Week 5-6: Optimization Playbook** — when to switch bid strategies, how to evaluate
6. **Week 7-8: Reporting & Handoff** — metrics to track, report template

**Expected output:** Complete operational playbook that someone could follow without additional context.

---

## Execution Notes

- Tasks 1-4 (keyword discovery) can run in parallel
- Task 5 (competitors) and Task 6 (SERPs) can run in parallel
- Task 7 (website audit) is independent
- Tasks 8-9 (data processing) depend on Tasks 1-6
- Task 10 (blueprints) depends on Tasks 8-9 and 7
- Tasks 11-12 (deliverables) depend on Task 10

```
Tasks 1-4 (parallel) ──┐
Tasks 5-6 (parallel) ──┤──→ Tasks 8-9 ──→ Task 10 ──→ Tasks 11-12
Task 7 (independent) ──┘
```

If DataForSEO tokens run out: skip remaining API calls, document what's missing, continue building deliverables with available data. Missing data can be backfilled later.
