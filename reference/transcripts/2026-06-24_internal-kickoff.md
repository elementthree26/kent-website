# KCO2600 — Website Consultation Internal Kickoff — June 24, 2026

**Recording:** 40 mins (Fathom, no highlights)
**Attendees:** Colton Angel, Victoria Shaw, Kayla Searles, John Gough, Brian Cole, Rachel Young (Element Three internal team)

Internal E3 kickoff walking the team through scope, timeline, roles, and process before the July 1 client kickoff.

---

**Context / relationship map (Victoria):** Kent Worldwide is GPC's parent company, owned by the Kent family (Gage Kent at the top). Leandra's boss (Johnnie) is the internal project lead, sitting on Kent's corporate communications / "Central Committee." Kent is approaching its 100th year in 2027. The website needs "a lift" — dated look, accessibility issues, and doesn't reflect the refreshed brand.

**Two major concurrent motions at Kent:**
1. Replatforming from Dynamic Web to WordPress.
2. Design and page additions/updates to the site (independent of platform).

**Timeline:** Project slated to run through early fall, possibly through year-end. Reviews will be the hardest part to manage given how many approvers exist in this family-business environment — brand/client approvers → a committee → ultimately Gage Kent, whose name is "on everything."

**Positioning:** Kent wants an "easy button" — E3 owns front-end vision (design, wireframes, functional specs, content/copy support, QA) and translates it into something Codal (the new dev partner, replacing Lithia) can build against. E3 is not doing the platform migration itself.

**Required pre-work:** Read the client brief; watch the original Feb 5 discovery call (source of the initial module list and client vision).

**Victoria's aside:** No visibility yet into the broader 100-year anniversary programming (book, party, etc.) — worth probing for campaign opportunities. Also flagged: this project is a proof point for a hoped-for future GPC website redesign — needs to demonstrate that a redesign isn't scary or prohibitively expensive.

**Deliverables (high level):** Web style guide, functional specs, wireframes (8 pages), dev handoff documentation, content outlines, copywriting for new pages (100-year page + one page per major Kent business unit).

**Dev partner note:** Lithia is being replaced; the new dev partner is Codal. Rachel is being given a tutorial on the current GPC site / Dynamic Web (since she'll support that account too) partly so she has context if Dynamic Web questions come up on the Kent project, and because she'll likely interact with Codal at some point regardless.

## Timeline / Phase Walkthrough (Colton & Kayla)

- **Pipeline:** Done.
- **Project Kickoff (~12 hrs):** Client kickoff scheduled for the following Wednesday (July 1). Attendees: Colton, Victoria, Kayla, and (added mid-meeting) Rachel.
- **Information Architecture (through mid-July, small % of budget):**
  - Document existing modules/nav structure (partially done via Victoria's slide) — still need to go through backend styling options to translate into what needs to be designed in Figma.
  - E3 does **not** yet have Dynamic Web back-end access for Kent (request in progress — Rachel and Kayla).
  - Leandra separately requested a kickoff (not discovery) meeting with Codal — purpose/attendee list still TBD, likely to align on what's useful for their implementation.
  - Rachel asked to follow the same content-outline/discovery-guide process used on the **Hoekstra** project — Colton/Victoria agreed that format landed well.
  - Content scope for writing: Innovation, Our Brands, Timeline, and four category pages (Pet Care, Food & Hydration, GPC, Nutrition) — ~5–6 pages for content outlines, ~8 for copywriting.
  - Reviewer/approver structure not yet fully defined — Kent is expected to be a "death by committee" client; needs clarity on who is a reviewer vs. input-giver vs. approver before finalizing the discovery session format. Considered doing a "daisy chart" (a lightweight RACI variant) to force a single decision-maker per page/section.
  - **Johnnie is the approver** (with the caveat that Gage Kent could override anything, though more likely Gage just gets shown wireframes/page approvals at a lighter touch).

- **Design (Noah & Rachel):**
  - Kent has an existing brand style guide (the Brand Book) — can help jump-start web style guide creation; Claude/"Cloud Design" suggested as a possible accelerant for color palette and typography automation, but buttons/hover states and full module design still need Figma.
  - Lesson from the Feb 5 discovery call: showing a style guide in isolation doesn't land — pair it with a few applied/restyled modules before presenting.
  - New modules/features (e.g., timeline, homepage carousel, logo carousel) require understanding what content will populate them before design can start — overlaps with content development.
  - Footer: likely just a rebrand of the current (crowded) footer, possibly with light simplification.
  - Main nav: adding a new sub-brand section; Kent's own proposed nav reference isn't scalable if another vertical is added later — E3 to present 1–2 alternative options (Mars-inspired was one reference) alongside a version of Kent's ask.
  - Working style: Noah takes first design pass, others review/collaborate — open to change based on team preference; this is Rachel's first web project at E3.

- **Design Review:** Internal QA pass, then client review, then dev handoff meeting with Codal (design + functional specs).

- **Content Development (heavily Nick):**
  - Writing based on content outlines; internal review; V1 copy loaded into Figma mockups (not maintained live, just to remove the "blank page" problem so stakeholders can visualize copy in context); actual review/commenting happens in Ziflow with threaded comments.
  - Flag: need to clearly communicate to Kent that the Figma mockup is not the final say on wording — avoid confusion between visual layout review and copy review.
  - Client-side, someone (likely Johnnie or Leandra) needs to "police" consolidated feedback so ambiguous or contradictory notes don't burn budget getting clarified — this is an explicit ask given multiple client stakeholders.
  - Johnnie is new to working with E3; expectation-setting on this front needs to happen early.

- **Development Support:** Mostly reactive/on-call hours once Codal starts building — walkthroughs of style guide/module changes/functionality, occasional Q&A, no deep day-to-day involvement. CMS training: Codal walks Rachel + Noah through WordPress basics ahead of content loading. Image resizing budgeted conservatively (4 hrs) since scope is only 8 pages — can offload to Haley if it scales up.

- **Timeline planning tip (Colton):** Get ahead of the 100-year timeline content early — push Kent for actual milestone imagery as soon as possible; risk is Kent wanting a rich visual timeline but having no assets ready two weeks before content loading.

- **Launch:** E3 is behind-the-scenes for the actual go-live (Codal handles it); confirming staging matches production. E3 not touching Tag Manager, GA4, or other integrations — Kent's centralized IT/agency partner ("Brian," a great, helpful guy) handles that.
  - Biggest launch-adjacent risk flagged: the developer handoff moment. High-friction if Codal hasn't seen anything before the full handoff — recommend an early "get buy-in on how we'll deliver" intro meeting with Codal before there's anything concrete to show, plus a walkthrough of what a typical functional spec looks like and whether Figma delivery works for them.
  - Kent has also brought in an internal project manager (via their IT-adjacent team) to help bridge across agencies and Codal on admin/invoicing/communication — will loop in via Leandra.

## Codal Background
- Team has not worked with Codal before; understood to have been referred by one of Kent's brands (possibly World's Best Cat Litter) and has done work for Petco, among others — seems to be a go-to for the pet category.
- Working theory: Codal isn't just being hired to build this one site — likely positioning to be Kent's ongoing dev partner (a "sticky" relationship E3 should be aware of if there's any future website revenue to compete for).

## Committee / Governance Notes
- Discovery sessions likely organized per page/vertical (e.g., Pet Care, Kent Feeds) with 1–2 people each, plus a broader ~7-person "Brand Center of Excellence" committee (brand-adjacent SMEs / internal champions) that inputs on overall Kent brand presentation.
- Aspirational ask: get time with Gage Kent (CEO, final approver in spirit) directly if possible — Johnnie (who handles PR/comms for the family) can elicit his input if a direct session isn't possible. Johnnie is described as the practical tiebreaker/final approver day-to-day.
- Colton to send Victoria a daisy-chart template; Victoria/Colton to draft page-level roles and approvers as a follow-up artifact for the client.

## Miscellaneous
- Dynamic Web / Codal access: Rachel, Kayla, and Victoria to be granted access.
- Context on Kent's current dev spend: a prior agency (possibly the same one that built the current site) quoted ~$55K just to add a page and update a menu, itemized ticket-by-ticket — used as informal context for how expensive/opaque the incumbent setup has been.

**Action items logged in Fathom:**
- Send Dynamic Web tutorial to Rachel; then Rachel draft content outlines (Hoekstra format)
- Add Rachel to client kickoff invite (Jun 24)
- Define purpose and attendees for Codal intro; schedule w/ Leandra
- Draft Kent web style guide in Figma; then restyle modules and present together
- Design 2 scalable main nav options for subbrands; present to client
- Design footer options (rebrand + light simplification); present to client
- Draft copy for 8 pages; then load into Figma and send to Ziflow
- Send daisy chart template to Colton; then Colton draft page-level roles/approvers
- Send kickoff discovery questions to Colton (Jun 22)
- Schedule 15-min kickoff prep check-in w/ Colton
