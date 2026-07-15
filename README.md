# kent-website

Working repo for KCO2600 — Kent Worldwide (kentww.com) website refresh ahead of the company's 100-year anniversary (Jan 2027). Element Three (E3) owns design, functional specs, wireframes, content outlines, and copywriting; Codal is Kent's development/build partner executing the WordPress replatform.

This repo holds two kinds of content: `/reference` (source documents used to inform the design/content deliverables — brand book, briefs, transcripts, current-site scrape) and `/deliverables` (working drafts of the actual design/content deliverables — discovery guides, content outlines, style guide, functional specs). Everything in `/deliverables` is a draft in progress until it's been through client review — check the status line at the top of each file.

## `/reference` contents

### `brand/`
- `KENTWW_Brand_Book_2025.pdf` — Kent Worldwide's 2025 brand guidelines (source of truth for colors, typography, logo rules, voice, photography direction). Fonts: **Roboto** (headlines/subheads/callouts), **Roboto Serif** (body), **Meow Script** (accent only, sparing use). Primary colors: Kent Green `#8dc63f`, Kent Young Green `#dae8a2`, Kent Rich Black, Kent White. Secondary colors: Deep Woods, Summer Bloom, Blue Sky, Amber Grain, Rich Soil.

### `briefs-proposals/`
- `KENTWW_Client_Project_Brief_May2026.pdf` — Kent's own project brief. Frames this as a **refresh, not a full redesign/replatform** from E3's design side. Defines success criteria, in/out of scope, 8 wireframes (Who We Are, 100-Year, News, Sustainability, Careers, Solutions/Innovation, Brands + one category page), and governance (Johnnie Arnett as sole final approver, up to 2 revision rounds per deliverable).
- `KENT_Web_2027_Proposal_March2026.pdf` — E3's proposal deck. Contains the critical path, design plan (which components are style-updates vs. net-new vs. redesign vs. multi-option), and the two pricing options (Option 1: $30K design-only / Option 2 recommended: $52K including content outlines, build-out consultation, content loading, and QA support). Also contains open questions later resolved in kickoff calls (nav category count, 100-year page placement, Careers page accessibility fix).
- `KCO2600_SOW_Project_Plan_June2026.pdf` — The executed SOW / detailed project plan. Full team, phase-by-phase task breakdown with hours and dates, budget flighting ($64K total across June–December 2026), and named project risks (content delays, unconsolidated feedback, Codal timeline not finalized, 10-hour build-out consultation cap, technical limitations found in QA). **Also contains the literal AI prompt E3 drafted for generating a first-pass web style guide HTML artifact from the brand book** (see SOW page 11) — useful starting point when building that deliverable.

### `transcripts/`
Chronological call transcripts/summaries, most useful read in order:
1. `2026-02-05_web-discussion-qa.md` — Original discovery/prospecting call. Source of Kent's original wishlist (Mars/Clorox-style homepage, history timeline framed around the 100-year coffee-table book, "Founders Museum" story-tile concept, Dynamic Web vs. WordPress debate, brand dropdown nav concept). **Required pre-reading per both internal kickoffs.**
2. `2026-06-24_internal-kickoff.md` — Internal E3 kickoff. Team roles, phase-by-phase plan walkthrough, Codal background, governance/DACI groundwork, and a list of Fathom action items.
3. `2026-07-01_client-kickoff.md` — Official client kickoff with Johnnie and Leandra. **Contains decisions that override earlier drafts** — page renamed Innovation → **Solutions**, Food & Hydration chosen as the sample wireframe category page, explicit **brand ordering rules** (Kent Nutrition → GPC → Pet Care/Food & Hydration; Squincher/Frosty Boy/Mrs. Wages/Dole order within Food & Hydration; World's Best Cat Litter first within Pet Care), accessibility scope boundary (E3 designs to best practice, Codal owns code-level compliance, no third-party overlay plugins), and page-by-page contributor groups (also captured in the Decision Chart below).

### `accessibility/`
- `wcag-aa-qa-checklist.md` — Full text transcription of Kent's WCAG 2.2 AA QA checklist (target conformance level for this project), split into what E3 specs vs. what's Codal/build-only, plus the three-checkpoint QA process (style guide review → component build review → final site QA) and recommended free tools at each stage.
- `screenshots/` — Original screenshots the checklist was transcribed from (kept for visual/layout reference). Original source link (`links.elementthree.com/a/kent-wcag-aa-qa-checklist/`) redirect-loops when fetched directly — use the transcription or screenshots instead.

### `current-site/`
- Content scrape of the live kentww.com site (2026-07-15) — page-by-page copy from the homepage, Who We Are, Innovation, Sustainability, Brands, News, Careers, Contact, and Supplier Central. Baseline for what content already exists vs. what the content outlines need to add, cut, or rewrite. See `current-site/README.md` for scrape notes and known gaps (e.g. brand order differs from the redesign's planned order, only page 1 of News was captured).

### `project-management/`
- `KCO2600_Decision_Chart_DACI.csv` — Finalized DACI chart (Driver / Approver / Contributor / Informed) by activity and by page/business unit. **Johnnie Arnett is Approver on nearly every line item.** Contributor groups by page:
  - 100-Year Timeline → Rich, Tiffany
  - Brands / Solutions → Full brand cohort
  - Pet Care → Marcello, KB, Charles
  - Food & Hydration → Jane, Adriene, Jeff, KB
  - GPC → Leandra (consulted); Jimmy, Brad (informed only)
  - Kent Nutrition → Charles (consulted); Jimmy (informed only)
  - Who We Are, Sustainability, Careers, News → no named contributors; Johnnie approves, COE informed only.

## Key decisions to keep in sync across deliverables
- Page name: **Solutions** (not "Innovation").
- Sample category wireframe: **Food & Hydration**.
- Brand display order: Kent Nutrition → GPC → (Pet Care / Food & Hydration, unordered relative to each other).
  - Food & Hydration internal order: Squincher, Frosty Boy, Mrs. Wages, Dole, then rest.
  - Pet Care internal order: World's Best Cat Litter first, then rest.
- Accessibility target: **WCAG 2.2 AA**. E3 = design/spec only; Codal = code-level build and remediation.
- No lead-gen functionality on kentww.com.
- 100-year timeline content should start from the ~15 milestones already in the brand book, supplemented by Heritage Works' master chronology if more depth/breadth is needed.
- Photography (new family/GPC shoot, archival Heritage Works pulls) is **out of E3's current scope** unless separately flagged and approved.

## `/deliverables` contents

### `discovery-guides/`
- `brands-and-solutions-discovery-guide.md` — Facilitator's script for the combined Brands + Solutions discovery session (one session covers both pages per the DACI chart). Covers session logistics/contributor list, current-state summary pulled from `reference/current-site/`, decisions already locked in, and open discussion questions per page. **Draft** — not yet reviewed internally or scheduled with the client.
