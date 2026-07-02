# WCAG AA QA Checklist — Kent Dynamic Web → WordPress Replatform

Source: https://links.elementthree.com/a/kent-wcag-aa-qa-checklist/
(Link currently redirect-loops when fetched directly — content transcribed below from screenshots; original screenshots kept in `screenshots/` for visual reference.)

**Stats banner:** 2 scopes (E3 design specs and Codal development) · 3 checkpoints (style guide, component build, final QA) · Target conformance level: **WCAG 2.2 AA**

---

## 01 · E3 Design Scope — "What we spec"
Items E3 owns through the style guide, component specs, and functionality documentation. Dev builds to these specs — E3 does not originate the fix.

### Color & Contrast
- **Text-on-background contrast ratios in the palette** — every text/background pairing in the new brand palette spec'd at 4.5:1 for body text, 3:1 for large text (24px+ or 19px bold), before it reaches dev. *(1.4.3 Contrast Minimum)*
- **Non-text contrast for UI components & icons** — button borders, form field outlines, icon glyphs, graphical objects spec'd at 3:1 against adjacent colors. *(1.4.11 Non-text Contrast)*
- **Link styling beyond color alone** — inline links spec'd with underline, weight change, or icon (not color difference alone) against surrounding body text. *(1.4.1 Use of Color)*
- **Status & validation states (color-independent)** — form errors, success states, and badges spec'd with icon or text label alongside color so meaning survives grayscale. *(1.4.1 Use of Color)*

### Typography & Layout
- **Text resize & reflow tolerance** — type scale and grid specs confirmed to hold at 200% zoom and at 320px width without horizontal scroll or clipped content. *(1.4.4 Resize Text · 1.4.10 Reflow)*
- **Line-height, letter-spacing & paragraph spacing overrides** — spec confirms the design tolerates user-applied text-spacing overrides without breaking card or nav layouts. *(1.4.12 Text Spacing)*
- **No brand copy locked into flattened images** — hero statements, callouts, and stat blocks spec'd as live text with brand styling applied via CSS, not baked into a JPEG/PNG handoff. *(1.4.5 Images of Text)*

### Focus & Interaction Specs
- **Visible focus indicator design** — a focus style spec'd for every interactive element, distinct enough at 3:1 contrast against adjacent colors, sized per the 2.2 minimum-area guidance. *(2.4.7 Focus Visible · 2.4.11 Focus Appearance)*
- **Touch target sizing** — buttons, nav items, and tap targets spec'd at a minimum 24×24px hit area (with spacing exceptions documented where the brand requires tighter UI). *(2.5.8 Target Size Minimum)*
- **Motion & animation thresholds** — functionality spec for any auto-playing carousel, parallax, or hover animation includes a pause/stop control and a reduced-motion fallback. *(2.2.2 Pause, Stop, Hide · 2.3.3 Animation from Interactions)*

### Content Structure & Functionality Specs
- **Heading hierarchy per template** — functionality spec defines h1–h6 usage by template (home, listing, detail) so editors don't pick heading levels by visual size in Gutenberg. *(1.3.1 Info and Relationships · 2.4.6 Headings and Labels)*
- **Alt text & decorative-image rules** — content spec distinguishes meaningful imagery (requires descriptive alt) from decorative imagery (alt="") per content type, carried into the CMS field guidance. *(1.1.1 Non-text Content)*
- **Form field labeling & error messaging spec** — functionality spec requires a visible, programmatically associated label on every field, plus specific error copy (not color-only) for validation states. *(3.3.1 Error Identification · 3.3.2 Labels or Instructions)*
- **Component interaction patterns (accordion, tabs, modal, slider)** — functionality spec defines expected keyboard behavior, focus handling, and dismissal pattern for every interactive component before dev estimates the build. *(2.1.1 Keyboard · 2.1.2 No Keyboard Trap)*
- **Skip-link & landmark structure spec** — functionality spec defines the skip-to-content target and the intended landmark regions (header, nav, main, footer) per template. *(2.4.1 Bypass Blocks · 1.3.1 Info and Relationships)*

---

## 02 · Development-Exclusive Scope — "What's build-only"
No design spec produces these on its own — they live in markup, theme code, plugin configuration, and CMS implementation. **Codal owns execution; E3 reviews the output against spec.**

- **Semantic HTML markup implementation** — headings, lists, tables, and landmark elements coded to match the structure spec, not just visually styled divs. *(1.3.1 Info and Relationships)*
- **ARIA roles, states & properties** — correct, non-redundant ARIA on custom Gutenberg blocks and third-party plugin components; accessible name, role, and value exposed for every interactive widget. *(4.1.2 Name, Role, Value)*
- **Keyboard event handling & focus management** — tab order, focus trapping/release in modals, and return-focus behavior coded for every interactive component per the spec'd pattern. *(2.1.1 Keyboard · 2.1.2 No Keyboard Trap · 2.4.3 Focus Order)*
- **Theme & page-builder component overrides** — out-of-box Gutenberg/Elementor/Divi block markup patched where the default output ships broken semantics or missing keyboard support. *(1.3.1 · 2.1.1 · 4.1.2)*
- **Forms plugin selection & configuration** — Gravity Forms / WPForms / CF7 (whichever lands) configured and, where needed, theme-overridden to produce associated labels and accessible error states. *(3.3.1 · 3.3.2 · 1.3.1)*
- **Alt text migration & CMS field population** — alt text mapped and migrated from Dynamic Web into WordPress media fields per the content spec; flagged where it didn't migrate cleanly. *(1.1.1 Non-text Content)*
- **Responsive reflow at 320px** — templates built and tested to avoid two-dimensional scrolling at narrow viewports, per the layout spec. *(1.4.10 Reflow)*
- **ARIA live regions for dynamic content** — AJAX-loaded filters, cart updates, and live search results wired with appropriate aria-live regions so screen readers announce changes. *(4.1.3 Status Messages)*
- **Redirect & URL structure migration QA** — 301 map from Dynamic Web verified against the new WordPress URL structure; no orphaned pages breaking breadcrumb or sitemap navigation paths. *(2.4.5 Multiple Ways)*
- **PDF & downloadable document tagging** — carried-over PDFs and downloadable assets checked for tagged, accessible structure — re-tagged or flagged for replacement where they fail. *(1.1.1 · 1.3.1)*
- **Automated scan + manual screen-reader pass execution** — axe/WAVE/Lighthouse run per template, plus a manual NVDA/VoiceOver pass on at least one full conversion journey, with findings logged and fixed in code. *(Conformance verification — all Level A/AA criteria)*

---

## 03 · Process Recommendations — "Catch it at the checkpoint"
Three points in the build where an a11y pass is cheapest. Fixing a contrast token at the style-guide stage costs minutes; fixing it after launch costs a re-deploy across every template that used it.

**Checkpoint 01 — Style guide review** ("Before a single component is built")
Run every color pairing, type scale step, and focus-state token in the new brand style guide through a contrast checker. Cheapest possible point to fail fast — a swapped hex value here is a five-minute fix, not a re-skin.
- Contrast audit of full palette
- Focus state sign-off
- Type scale resize check

**Checkpoint 02 — Module / component development review** ("As each component ships, not after they're all assembled")
E3 and Codal walk every built component (accordion, form, slider, nav) against its functionality spec with a keyboard-only pass and an axe scan, before it's wired into page templates. Fixing a component once here is cheaper than fixing it on every page it appears on later.
- Keyboard walkthrough per component
- axe scan per component
- ARIA spot-check

**Checkpoint 03 — Final site QA** ("Full-site, pre-launch, no exceptions")
Automated scan across every unique template, a manual screen-reader pass on the primary conversion journey, redirect/URL QA from the Dynamic Web migration, and a check on any carried-over PDFs. Re-test once final brand styling is locked, since contrast issues often get reintroduced late when design tokens get swapped in.
- Template-level automated scan
- Screen reader journey test
- Redirect & PDF audit
- Sign-off document

---

## 04 · Resources & Tools — "What we test with"
Free or near-free, widely used, no procurement required. Design-stage tools first, then dev/QA-stage tools.

**Design stage**
- **WebAIM Contrast Checker** (free) — fastest way to spot-check a text/background pairing against AA before it goes into the style guide.
- **Stark** (freemium · Figma & Adobe XD plugin) — contrast, color blindness simulation, and focus-order checks directly inside the design file.
- **W3C WCAG 2.2 Quick Reference** (free · reference) — filterable, plain-language version of every success criterion; fastest way to confirm a rule citation.

**Dev & QA stage**
- **axe DevTools** (free · browser extension) — the standard automated scanner; runs on Chrome/Firefox; flags real WCAG violations with code-level detail.
- **WAVE** (free · browser extension) — visual overlay of issues directly on the rendered page; good for walking a non-technical stakeholder through findings.
- **Lighthouse** (free · built into Chrome) — built into Chrome DevTools; pairs an accessibility score with performance and SEO in the same audit run.
- **Accessibility Insights for Web** (free · Microsoft) — guided manual-test assistant; walks through keyboard, focus order, and tab-stop checks step by step.
- **NVDA** (free · screen reader, Windows) — the most-used free Windows screen reader; standard for manual screen-reader QA passes.
- **VoiceOver** (free · built into macOS/iOS) — already on every Mac and iPhone; no install needed for a quick manual pass on either platform.
- **WP Accessibility** (free · WordPress plugin) — patches common WordPress theme defaults: skip links, long-link warnings, title-attribute removal — at the platform level.
- **Acrobat Pro Accessibility Checker** (free · PDF tagging check) — confirms tagged structure on any carried-over PDFs from the Dynamic Web migration.
