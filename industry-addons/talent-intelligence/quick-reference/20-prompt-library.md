# 20-Prompt Library — Copy/Paste Reference

A scannable copy/paste prompt library covering the most common talent-industry deliverables. Each prompt is numbered, titled, and tagged with its sub-register, recommended model, and aspect ratio. Bracketed `[PLACEHOLDERS]` mark fields you should replace with project-specific values before generating.

This file is the source of truth for Section 11 of the BHIL-branded reference document (`BHIL-Talent-Intelligence-Addon-Reference-v1.x.x.docx`).

---

## Before You Generate

Every prompt below assumes the **default rule** is in force:

> AI for abstract concept and environmental/background. Real photography (with consent and C2PA-tagged provenance) for humans wherever a viewer might mistake the subject for a real employee or candidate. Anonymous-silhouette / illustrated / environmental alternatives are the legitimate exits.

Prompts that produce imagery resembling people are written to produce environmental, illustrated, or clearly archetypal output — never photo-real fabricated employees. If you adapt a prompt and remove the guardrails, you take on the compliance posture of doing so. The add-on's compliance documentation is non-optional for production work — see [`../compliance/`](../compliance/).

---

## Quick Reference

| # | Prompt | Register | Model |
| :-: | :--- | :-: | :--- |
| 01 | Candidate Dossier Cover — Mountain Summit | A | Midjourney v7 |
| 02 | Candidate Dossier Cover — Architectural Building | A | Midjourney v7 |
| 03 | Dossier Cover — Typographic Overlay | A | Ideogram v3 |
| 04 | Anonymized Market Map — Bubble Cluster | A | GPT Image 2 / NB Pro |
| 05 | Board Search Deliverable — Spencer Stuart Register | A | MJ v7 + Ideogram |
| 06 | Platform Dashboard Hero — Eightfold Register | B | GPT Image 2 / Flux.2 Pro |
| 07 | Skills Graph Network — Force-Directed Glow | B | Flux.2 Pro / Recraft V3 |
| 08 | Talent Flow Sankey — Width-Weighted Ribbons | B | GPT Image 2 / Flux.2 Pro |
| 09 | Vendor Pitch Deck Hero — With Recognition Badges | B | GPT Image 2 + Ideogram |
| 10 | Career Site Hero — Illustrated Alternative | C | Recraft V3 |
| 11 | Career Site Hero — Environmental Workspace | C | Nano Banana Pro |
| 12 | LinkedIn Recruiter Tile — Typography-Only Quote | C | Ideogram v3 |
| 13 | EVP Pillar Icon Set — Three-Pillar Grid | C | Recraft V3 |
| 14 | EVP Pillar Layout — Three-Column Grid | C | Ideogram v3 |
| 15 | Job Posting Environmental — Engineering Workspace | C | Nano Banana Pro |
| 16 | Job Posting Environmental — Lab / Scientific Workspace | C | NB Pro / MJ v7 |
| 17 | Workforce Trends Cover — Topographic Gradient | A or C | MJ v7 + Ideogram |
| 18 | Salary Guide Cover — Brand-Color Wave | C | MJ v7 |
| 19 | DEI Report Cover — Architectural Restraint | A | Midjourney v7 |
| 20 | Conference Keynote Backdrop — Ultra-Wide LED | B | MJ v7 + Ideogram |

---

## Sub-Register A — Executive Search & Retained-Search Editorial

### 01 · Candidate Dossier Cover — Mountain Summit

**Register:** Sub-register A · **Model:** Midjourney v7 · **Aspect:** 8.5×11" (`--ar 17:22`)

**Use:** Cover plate for confidential candidate dossier (longlist, slate, final recommendations).
**Compliance:** No real-person likeness. Anonymization conventions enforced. C2PA applied.

```text
Editorial cover photograph for a confidential executive search dossier. A solitary mountain ridge at first light, wreathed in low cloud, the summit lit warm against deep navy sky. Restrained composition, generous negative space in the upper third for typographic overlay. Documentary-photography register, slight grain, slightly desaturated palette, warm cast in highlights, cool cast in shadows. No people, no buildings beyond a distant horizon line. Foreign Affairs editorial photography register. [BHIL profile] --ar 17:22 --style raw --stylize 200 --v 7
```

### 02 · Candidate Dossier Cover — Architectural Building

**Register:** Sub-register A · **Model:** Midjourney v7 · **Aspect:** 8.5×11" (`--ar 17:22`)

**Use:** Alternate cover for corporate-development, financial-services, or institutional searches.
**Compliance:** No real-person likeness. C2PA applied.

```text
A modernist corporate building exterior at dawn, low-angle, the facade lit warm against indigo sky. Restrained, no people in frame, generous negative space above for typographic overlay. Documentary architectural photography register reminiscent of Hedrich Blessing, slight grain, slightly desaturated. [BHIL profile] --ar 17:22 --style raw --stylize 200 --v 7
```

### 03 · Dossier Cover — Typographic Overlay

**Register:** Sub-register A · **Model:** Ideogram v3 · **Aspect:** 8.5×11" portrait

**Use:** Typographic overlay layered onto architectural base from Prompts 01-02.
**Compliance:** Confidentiality stamp non-decorative. Codenames real and project-specific.

```text
Editorial cover layout. Top-left: small-caps tracked label "[PRACTICE AREA] PRACTICE" in warm ivory at 9pt. Center upper-third: editorial display title "[PROJECT CODENAME]" in heavy serif (Canela Deck or GT Sectra Bold register), warm ivory, 72-84pt. Below title: "Slate of Candidates · [SEARCH SLATE NUMBER]" in regular serif italic, warm ivory, 16pt. Lower-right: "[CLIENT FIRM]" wordmark small. Lower-left: diagonal stamp "STRICTLY CONFIDENTIAL" in signal-red, 18pt, rotated -15 degrees, with hairline rule above and below. Footer center: "[YEAR] · [DOSSIER VERSION]" in 9pt regular. Subtle paper-grain texture overlay at 8% opacity.
```

### 04 · Anonymized Market Map — Bubble Cluster

**Register:** Sub-register A · **Model:** GPT Image 2 / NB Pro · **Aspect:** 11×17" tabloid

**Use:** Market mapping visualization for the talent landscape of a search engagement.
**Compliance:** No real-company logo reproduction. No candidate identification.

```text
Editorial bubble-cluster market map for an anonymized executive search talent landscape, 11x17 tabloid landscape. Approximately [N] circular nodes of varying sizes arranged in a constellation, each node sized by candidate-pool count, each colored by industry sector using a restrained 4-color palette (deep navy, warm amber, signal red, neutral gray). Each node labeled with a generic role-and-industry descriptor only ("[ROLE TITLE] - [INDUSTRY ARCHETYPE]") in 10pt humanist sans, warm ivory text. No real company names, no logos, no candidate names. Hatched neutral monogram circles with small lock icons mark confidential nodes. Hairline gray lines suggest relationships. Legend bottom-left explains the anonymization convention. Light cream paper background with subtle grain.
```

### 05 · Board Search Deliverable — Spencer Stuart Register

**Register:** Sub-register A · **Model:** MJ v7 + Ideogram · **Aspect:** A4 portrait

**Use:** Cover for board-search deliverable or board composition study.
**Compliance:** Strictest provenance and licensing. AI imagery requires policy approval per project.

```text
Editorial board-grade publication cover, A4 portrait. Full-bleed warm ivory background with subtle paper-grain texture overlay at 8% opacity. Top-left: small-caps "BOARD OF DIRECTORS PRACTICE" wordmark in 11pt warm navy. Below wordmark: "[EDITION] · [YEAR]" in tracked small caps, 10pt warm navy. Horizontal red bar [#C8102E width 60%] sits below the wordmark zone. Center upper-third: editorial display title "[REPORT TITLE]" in heavy serif (Rotis Serif Regular or Canela Deck register), warm navy, 80-96pt. Below title: subtitle "[REPORT SUBTITLE]" in regular weight serif italic, 24pt warm navy. Lower-third: very large year "[YEAR]" in serif display 144-180pt, warm navy at 25% opacity. Footer: small attribution copy and edition number in 9pt regular.
```

---

## Sub-Register B — Talent Intelligence Platform Dashboard

### 06 · Platform Dashboard Hero — Eightfold Register

**Register:** Sub-register B · **Model:** GPT Image 2 / Flux.2 Pro · **Aspect:** 16:9 landscape

**Use:** Hero plate for platform marketing site, product page, or sales deck.
**Compliance:** AI agent avatars must be clearly stylized. Dashboard data obviously sample.

```text
Talent intelligence platform dashboard hero plate, 16:9 landscape. Dark gradient mesh backdrop transitioning from deep purple [#2D1A4A] in upper-left through deep indigo [#1A1A4A] center to deep navy [#0A0A2E] lower-right. Floating rounded-card UI elements arranged in a bento-grid composition: top-left a choropleth world map quadrant in lavender-coral gradient; top-center a force-directed node graph with 30-40 glowing aqua [#00C4D4] nodes; top-right a giant statistic tile reading "[METRIC] [NUMBER]" with a coral [#FF6B6B] up-delta arrow; mid-left a Sankey-like ribbon flow in coral and aqua; mid-center a stack of skill chips in lime [#B6E55C] and aqua; right-side a docked AI agent chat panel with stylized geometric avatar (no human face). Atmospheric particle effect across the mid-ground. No people, no faces, no figures. Eightfold Infinite Workforce / Gloat Loomra reference.
```

### 07 · Skills Graph Network — Force-Directed Glow

**Register:** Sub-register B · **Model:** Flux.2 Pro / Recraft V3 · **Aspect:** 1:1 square

**Use:** Standalone skills graph visualization for platform marketing or pitch deck.
**Compliance:** Skill names must not surface protected characteristics or disparate-impact patterns.

```text
Force-directed skills network graph rendered on a deep gradient mesh background transitioning from indigo [#1A1A4A] center to near-black at the edges. Approximately 60-80 nodes as glowing dots in a primary platform accent color [#00C4D4 aqua], with selected hub nodes 2-3x larger and labeled with skill names ("[SKILL 1]", "[SKILL 2]", "[SKILL 3]") in 14pt regular humanist sans, warm ivory. Thin glowing lines connect related nodes, line thickness representing relationship strength. A subtle radial light source emanates from the network center. Atmospheric particles drift across the field. No people, no figures, no human shapes. Legend bottom-right with small chip swatches in 10pt regular. Square 1:1 format. Style: Gloat Loomra / Eightfold Capability Dashboard.
```

### 08 · Talent Flow Sankey — Width-Weighted Ribbons

**Register:** Sub-register B · **Model:** GPT Image 2 / Flux.2 Pro · **Aspect:** 16:9 landscape

**Use:** Workforce mobility, migration, or career pathing visualization.
**Compliance:** Source attribution required for third-party data. Privacy considerations for individual data.

```text
Editorial Sankey diagram showing [TALENT FLOW DESCRIPTION] from left to right, 16:9 landscape on a deep navy [#0A0A2E] gradient background. Six source categories on the left labeled "[SOURCE 1]" through "[SOURCE 6]" stack vertically, six destination categories on the right labeled "[DESTINATION 1]" through "[DESTINATION 6]" stack vertically. Width-weighted ribbon flows curve smoothly from source to destination, ribbons rendered with soft glow in graduated colors: aqua [#00C4D4], coral [#FF6B6B], lime [#B6E55C], magenta [#D94BCC]. Major flow junctions marked with small data callouts ("[N]% to [DESTINATION]") in 11pt regular humanist sans, warm ivory. Source attribution caption bottom-center: "Source: [DATA SOURCE], [PERIOD]". No people, no figures.
```

### 09 · Vendor Pitch Deck Hero — With Recognition Badges

**Register:** Sub-register B · **Model:** GPT Image 2 + Ideogram · **Aspect:** 16:9 (1920×1080)

**Use:** Hero slide for HR Tech vendor pitch deck or analyst briefing.
**Compliance:** Recognition badges require licensing. Verify entitlement before deploying.

```text
HR Tech vendor pitch deck hero, 16:9 (1920x1080). Same dashboard hero plate composition as the Eightfold-style hero (deep purple gradient mesh, floating bento-grid UI cards, glowing skills graph, Sankey ribbon, AI agent panel docked right) but with the platform brand mark "[PLATFORM]" prominently placed center-upper, 64pt warm ivory. Below brand mark: tagline "[PLATFORM TAGLINE]" in regular weight italic, 22pt at 70% opacity. Lower-third: a horizontal strip of three recognition badges side-by-side: "[BADGE 1]", "[BADGE 2]", "[BADGE 3]", each rendered as a small rounded plaque in warm ivory on the dark background. Founding-year or scale stat in display type lower-right: "Trusted by [N] enterprises". No people, no faces, no figures.
```

---

## Sub-Register C — Employer Brand & Recruitment Marketing

### 10 · Career Site Hero — Illustrated Alternative

**Register:** Sub-register C · **Model:** Recraft V3 · **Aspect:** 16:9 desktop / 9:16 mobile

**Use:** Career site hero when real photography isn't feasible — illustrated alternative.
**Compliance:** MUST be unmistakably illustrated, not photo-real. Default rule prohibits AI-generated photo-real fabricated employees.

```text
Editorial illustrated workplace scene in flat-vector register reminiscent of GitLab and Notion brand illustration. A team of 3-4 figures collaborating around a laptop in a sunlit modern office, faces stylized and unmistakably illustrated rather than photo-real, gestural rather than detailed, hand-drawn quality. [BRAND ACCENT] as primary fill color with soft cream secondary; deep navy line work. Natural daylight from a window at left, warm cast in highlights. Generous negative space at right for headline overlay. Stylized rather than photographic — this should not read as photography. Style: Recraft V3 illustration register, Mailchimp Collins-influenced outsider art register.
```

### 11 · Career Site Hero — Environmental Workspace

**Register:** Sub-register C · **Model:** Nano Banana Pro · **Aspect:** 1920×1080 desktop

**Use:** Career site hero when no human subject is needed — environmental workplace detail.
**Compliance:** No-people convention sidesteps consent and likeness concerns. Visible AI disclosure required.

```text
Documentary workplace photograph, eye-level perspective, a working desk in a sunlit modern office. Mid-day natural daylight from a window at left, warm cast in highlights, slight desaturation. Visible: an open laptop with a code editor or design tool, a notebook with handwritten notes, a ceramic mug, a small plant. No people in frame, no faces, no figures implied. Slight depth-of-field, focus on the desk surface, background gently blurred. Tailored, lived-in, real — not staged stock photography. [BRAND PROFILE] register applied through subtle ambient color cast. Slight grain, documentary photography register reminiscent of Stripe and Notion careers imagery.
```

### 12 · LinkedIn Recruiter Tile — Typography-Only Quote

**Register:** Sub-register C · **Model:** Ideogram v3 · **Aspect:** 1200×1200 square

**Use:** LinkedIn recruiter campaign tile, InMail attachment, sourcing outreach.
**Compliance:** Quote attribution requires consent. Quote modification requires re-confirmation.

```text
Editorial recruitment social tile, 1200x1200 square. Full-bleed background in [BRAND ACCENT]. Center-left: editorial display pull-quote in serif (Canela Deck or GT Sectra Bold register), warm ivory, weighted at 48-56pt, 5-7 lines. Quote: "[QUOTE]" Below quote, small horizontal hairline rule in warm ivory at 30% opacity. Below rule: attribution in two lines — line one: "[EMPLOYEE NAME]" in regular weight serif italic, 18pt; line two: "[ROLE TITLE] · [LOCATION] · [TENURE]" in 14pt regular sans. Lower-right corner: "[CLIENT FIRM]" wordmark in warm ivory at 16pt. Restrained, lower-case sentence-case quote, generous negative space.
```

### 13 · EVP Pillar Icon Set — Three-Pillar Grid

**Register:** Sub-register C · **Model:** Recraft V3 · **Aspect:** 200×200 per icon

**Use:** Custom icon system for EVP framework (Marriott Be model, CAE Our Promise For All).
**Compliance:** Icon system fully AI-permitted (abstract metaphor). No representation testing required for abstract icons.

```text
A set of three custom icons for an EVP pillar system, in a unified flat-vector illustration register. Each icon is geometric, simple, hand-drawn quality, with consistent line weight (3px) and consistent style across all three. Each icon is rendered in [BRAND ACCENT] line work on a soft cream/ivory ground. Style: flat-vector illustration in the register of GitLab brand iconography or Notion brand iconography. Each icon should fit a 200x200 square with generous padding. Icons are abstract metaphors for: [PILLAR 1], [PILLAR 2], [PILLAR 3]. No text, no labels, no people in the icons.
```

### 14 · EVP Pillar Layout — Three-Column Grid

**Register:** Sub-register C · **Model:** Ideogram v3 · **Aspect:** 16:9 landscape

**Use:** Layout that hosts the EVP pillar icons + headlines + supporting copy.
**Compliance:** Lower-case sentence-case throughout. EVP framework name as IP; trademark search before launch.

```text
EVP pillar layout, three columns side-by-side, full-bleed cream/ivory background. Each column has: small custom icon centered at top (200x200), a short sentence-case word or phrase headline immediately below in serif display 36pt warm navy, 2-3 lines of supporting copy in regular sans 14pt below headline, and a faint horizontal hairline rule at column bottom. Columns separated by generous negative space. Below the three columns: a single banner row with the EVP framework name in serif display 28pt centered. Pillar 1: [PILLAR 1] — "[PILLAR 1 SUPPORTING COPY]". Pillar 2: [PILLAR 2] — "[PILLAR 2 SUPPORTING COPY]". Pillar 3: [PILLAR 3] — "[PILLAR 3 SUPPORTING COPY]". Framework name banner: "[EVP FRAMEWORK NAME]". Lower-right: [CLIENT FIRM] wordmark in 14pt warm navy.
```

### 15 · Job Posting Environmental — Engineering Workspace

**Register:** Sub-register C · **Model:** Nano Banana Pro · **Aspect:** 1600×400 banner

**Use:** Job posting hero, LinkedIn req page, careers-site role detail page.
**Compliance:** No faces, no figures, no implied people. Visible AI disclosure on the page.

```text
Documentary workplace photograph, eye-level, [JOB FAMILY] workspace in a modern office. Mid-day natural daylight from a window at left, warm cast in highlights, slight desaturation. Visible: an open laptop with a code editor, a notebook with handwritten notes, a ceramic mug, headphones, a small plant. No people in frame, no faces, no figures implied, no hands. Slight depth-of-field, focus on the desk surface, background gently blurred showing a sense of an open-office context. Tailored, lived-in, real — not staged stock photography. Documentary photography register reminiscent of Stripe and Notion careers imagery. Subtle [BRAND ACCENT] in the code editor on the laptop screen.
```

### 16 · Job Posting Environmental — Lab / Scientific Workspace

**Register:** Sub-register C · **Model:** Nano Banana Pro / MJ v7 · **Aspect:** 1600×400 banner

**Use:** Job posting hero for research, science, healthcare role contexts.
**Compliance:** No faces, no figures. Documentary register.

```text
Documentary workplace photograph, eye-level, a scientific research workspace in a modern lab. Mid-day natural light from overhead, slight cool cast, slight desaturation. Visible: a microscope on a clean bench, lab notebooks with handwritten notes, sample tubes neatly arranged, a tablet showing data. No people in frame, no faces, no figures, no hands. Slight depth-of-field, focus on the bench surface, lab corridor softly blurred in background. Tailored, lived-in, real — not staged stock photography. Documentary photography register. Subtle [BRAND ACCENT] in a small object on the bench.
```

---

## Workforce Reports & Conference Materials

### 17 · Workforce Trends Cover — Topographic Gradient

**Register:** Mixed (A or C) · **Model:** MJ v7 + Ideogram · **Aspect:** A4 portrait (`--ar 17:22`)

**Use:** Cover of annual or recurring workforce intelligence publication (WEF, Lightcast, Bain register).
**Compliance:** Most archival reports prohibit AI imagery on cover; abstract metaphor only where permitted.

```text
Editorial cover background, abstract metaphor for "[REPORT THEME]". A topographic gradient field reading as a stylized terrain or ocean swell, in restrained palette of [BRAND ACCENT] over deep navy ground, with subtle paper-texture grain. The composition has generous negative space in the upper-third for typographic title overlay and lower-third for subtitle. No people, no figures, no buildings. Restrained, editorial, slightly desaturated, slight grain. Foreign Affairs editorial cover register. [BHIL profile] --ar 17:22 --style raw --stylize 200 --v 7
```

### 18 · Salary Guide Cover — Brand-Color Wave

**Register:** Sub-register C · **Model:** MJ v7 · **Aspect:** A4 portrait (`--ar 17:22`)

**Use:** Annual salary guide / compensation report cover (Robert Half register).
**Compliance:** No human subjects on AI-generated covers. Salary methodology page required separately.

```text
Editorial cover background, abstract wave or undulation motif representing compensation movement and market dynamics. A flowing horizontal banded gradient in [BRAND ACCENT] saturating to deeper [BRAND ACCENT] at the bottom edge, with subtle vertical striations suggesting income bands or cohort divisions. The composition has generous negative space in the upper-third for typographic title overlay. No people, no figures, no buildings. Restrained, editorial, slightly desaturated, slight grain. Sub-register C agency editorial register, Robert Half cover register. [BRAND PROFILE] --ar 17:22 --style raw --stylize 200 --v 7
```

### 19 · DEI Report Cover — Architectural Restraint

**Register:** Sub-register A · **Model:** Midjourney v7 · **Aspect:** A4 portrait (`--ar 17:22`)

**Use:** Annual DEI / belonging / equity report cover (board / institutional audience).
**Compliance:** HIGHEST STAKES IN ADD-ON. Synthetic-diversity prohibited. Architectural restraint sidesteps the problem.

```text
Editorial cover photograph for a DEI report. A modernist corporate building interior, mid-day, generous natural daylight from floor-to-ceiling windows, the architectural structure (columns, exposed beams, an atrium) rendered as the cover subject. No people visible, no figures, no implied human presence. Restrained palette of warm ivory and deep navy with [BRAND ACCENT] subtle accent in a single architectural detail. Slight grain, slightly desaturated, documentary architectural photography register reminiscent of Hedrich Blessing or Iwan Baan. Generous negative space in the upper-third for typographic title overlay. Foreign Affairs editorial cover register. [BHIL profile] --ar 17:22 --style raw --stylize 200 --v 7
```

### 20 · Conference Keynote Backdrop — Ultra-Wide LED

**Register:** Sub-register B · **Model:** MJ v7 + Ideogram · **Aspect:** Ultra-wide 2.5:1 (`--ar 5:2`)

**Use:** LED backdrop behind keynote speaker at HR Tech / talent intelligence conference.
**Compliance:** Recognition badges require licensing. Conference IP licensing for wordmarks. Motion variant requires Veo/Runway provenance.

```text
Conference keynote stage backdrop, ultra-wide 2.5:1 aspect ratio. A dark gradient mesh backdrop transitioning from deep [PLATFORM PRIMARY] in upper-left through deep navy center to deep [PLATFORM SECONDARY] in lower-right. Atmospheric particle effect — small glowing dots and light streaks like an aurora — in [PLATFORM ACCENT] across the mid-ground. Soft volumetric light from upper-left suggesting stage lighting integration. Generous negative space in the center for typographic headline overlay. No people, no figures, no buildings. Atmospheric, theatrical, restrained. Sub-register B platform dashboard register. [PLATFORM PROFILE] [PLATFORM SREFS] --ar 5:2 --style raw --stylize 300 --v 7
```

---

## Customization Field Reference

The placeholders used across this library, with example values:

| Field | Example | Notes |
| :--- | :--- | :--- |
| `[BHIL profile]` | parent BHIL brand profile | Replace with your locked profile / sref ID set |
| `[BRAND PROFILE]` | client brand profile | Sub-register B/C client work |
| `[BRAND ACCENT]` | `#0F69AF` (Randstad) / `#FF0000` (Adecco) / `#0052CC` (Atlassian) | Single-accent color |
| `[CLIENT FIRM]` | "Atlassian" / "Korn Ferry" / your firm | Wordmark / signature |
| `[PROJECT CODENAME]` | "Project Aurora" | Confidential codename |
| `[CLIENT CODE NAME]` | Internal client identifier | Anonymized |
| `[PRACTICE AREA]` | "CEO & BOARD OF DIRECTORS" | Small-caps top label |
| `[SEARCH SLATE NUMBER]` | "Slate III" / "Longlist" / "Final Recommendations" | Slate stage |
| `[REPORT TITLE]` | "Workforce 2026" / "Future of Jobs" | Display title |
| `[REPORT SUBTITLE]` | "The Skills Pivot" | Editorial subtitle |
| `[YEAR]` | "2026" | Publication year |
| `[EDITION]` | "10TH ANNUAL" / "VOL. III" | Small-caps edition signifier |
| `[REPORT THEME]` | "skills migration" / "leadership transitions" | Drives metaphor |
| `[ROLE TITLE]` | "Senior Software Engineer" | Real role |
| `[INDUSTRY ARCHETYPE]` | "Top-5 Global Bank" / "FAANG" | Industry shorthand |
| `[EMPLOYEE NAME]` | "Sarah Park" | Real, named, consented employee only |
| `[QUOTE]` | "I came for the engineering. I stayed for the people." | Real employee quote with consent |
| `[LOCATION]` | "Sydney, Australia" | Real location |
| `[TENURE]` | "5 years at [CLIENT FIRM]" | Optional |
| `[JOB FAMILY]` | "Engineering" / "Design" / "Sales" | Department / function |
| `[PILLAR 1/2/3]` | "begin" / "belong" / "become" (Marriott) | EVP framework pillars |
| `[EVP FRAMEWORK NAME]` | "Be" / "Our Promise. For All." | Trademarked framework name |
| `[PLATFORM]` | "Eightfold" / "Gloat" / "Lightcast" | Platform brand context |
| `[PLATFORM PRIMARY]` | "deep purple #2D1A4A" | Sub-register B gradient primary |
| `[PLATFORM SECONDARY]` | "deep indigo #1A1A4A" | Sub-register B gradient secondary |
| `[PLATFORM ACCENT]` | "aqua #00C4D4" / "coral #FF6B6B" | Sub-register B accent |
| `[PLATFORM SREFS]` | Locked srefs for the platform | Visual consistency |
| `[BADGE 1/2/3]` | "Fosway 9-Grid Strategic Leader" | Recognition badges (require licensing) |
| `[METRIC]` | "Career profiles" / "Skills mapped" | Stat tile metric |
| `[NUMBER]` | "1.6B" / "33,000+" | Stat tile value |
| `[DATA SOURCE]` | "LinkedIn Talent Insights" / "Lightcast" | Source attribution |
| `[PERIOD]` | "2024-2026" | Time range for data |
| `[N]` | numerical value | Approximate counts |

## Related

- [Quick reference README](./README.md)
- [Full prompt library (`../prompts/`)](../prompts/README.md)
- [Three sub-registers reference](../docs/01-three-sub-registers.md)
- [Compliance framework](../compliance/README.md)
- [Candidate imagery decision tree](../workflows/candidate-imagery-decision-tree.md)
