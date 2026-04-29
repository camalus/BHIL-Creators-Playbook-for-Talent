# Canonical Deliverable Types

Fourteen visual deliverable types are canonical in talent-industry work. Each maps to a prompt in this add-on's [`prompts/`](../prompts/) directory, a default sub-register, and a typical production tier from [`workflows/three-production-tiers.md`](../workflows/three-production-tiers.md).

## The Fourteen Types

| # | Deliverable | Default Register | Prompt | Typical Tier |
| :- | :--- | :-: | :--- | :-: |
| 1 | Candidate dossier cover | A | [01](../prompts/01-executive-search/01-candidate-dossier-cover.md) | 3 — Archival |
| 2 | Executive bio plate / leadership brief | A | [02](../prompts/01-executive-search/02-executive-bio-plate.md) | 3 — Archival |
| 3 | Anonymized market mapping / org chart | A | [03](../prompts/01-executive-search/03-anonymized-market-map.md) | 2-3 |
| 4 | Board search deliverable / board index | A | [04](../prompts/01-executive-search/04-board-search-deliverable.md) | 3 — Archival |
| 5 | Platform dashboard hero plate | B | [05](../prompts/02-talent-intelligence-platform/05-dashboard-hero-plate.md) | 2 |
| 6 | Skills graph / capability network | B | [06](../prompts/02-talent-intelligence-platform/06-skills-graph-network.md) | 2 |
| 7 | Talent flow / migration visualization | B | [07](../prompts/02-talent-intelligence-platform/07-talent-flow-sankey.md) | 2 |
| 8 | HR Tech vendor pitch deck hero | B | [08](../prompts/02-talent-intelligence-platform/08-vendor-pitch-deck-hero.md) | 2 |
| 9 | Career site hero imagery | C | [09](../prompts/03-employer-brand/09-career-site-hero.md) | 2 |
| 10 | LinkedIn recruiter campaign tile | C | [10](../prompts/03-employer-brand/10-linkedin-recruiter-tile.md) | 1 |
| 11 | EVP pillar treatment | C | [11](../prompts/03-employer-brand/11-evp-pillar-treatment.md) | 2 |
| 12 | Job posting / req hero | C | [12](../prompts/03-employer-brand/12-job-posting-environmental.md) | 1 |
| 13 | Workforce trends report cover | A or C | [13](../prompts/04-workforce-reports/13-workforce-trends-cover.md) | 3 |
| 14 | Salary / compensation report cover | C | [14](../prompts/04-workforce-reports/14-salary-guide-cover.md) | 2 |
| (15) | DEI report cover | A or C | [15](../prompts/04-workforce-reports/15-dei-report-cover.md) | 3 |
| (16) | Conference keynote backdrop | B | [16](../prompts/04-workforce-reports/16-conference-keynote-backdrop.md) | 2 |

The canonical list is fourteen; this add-on includes sixteen prompts because two additional formats (DEI reports and conference keynotes) carry enough industry-specific complexity to warrant their own treatment despite being adjacent to the fourteen base types.

## Per-Type Anatomy

### 1. Candidate Dossier Cover

The cover of a long-form candidate dossier prepared by a retained-search firm for a client search committee. Always anonymized for top-of-cover purposes (the candidate's identity is revealed inside, not on the cover).

**Anatomy:** Full-bleed firm-color field or architectural metaphor photograph; small-caps practice/series label top-left ("CEO & BOARD OF DIRECTORS PRACTICE"); editorial display title ("Slate of Candidates" / "Longlist" / "Final Recommendations"); project codename and dossier-version footer; diagonal "STRICTLY CONFIDENTIAL" stamp; subtle paper-texture overlay simulating uncoated stock.

**Anchor reference:** Heidrick & Struggles *Route to the Top 2025*, Spencer Stuart 2025 US Board Index. SignalFire's open recruiting-dossier template (signalfire.com/blog/recruiting-dossier) is the only fully public reference.

**Compliance hot spots:** No real-person likeness. Confidentiality stamps non-decorative; codenames real and project-specific. C2PA Content Credentials applied to the cover even though it carries no people.

### 2. Executive Bio Plate / Leadership Brief

A single-spread profile of a candidate or appointed executive, used in dossiers, board materials, and announcement decks.

**Anatomy:** Top-bleed environmental portrait (real photo with consent for actual candidates; archetypal-only AI-generated for templates and explainers); display serif name; small-caps practice line; three-paragraph bio organized as Career Arc / Signature Wins / Distinctions; signature wins formatted as a discreet sidebar with metric bullets.

**Anchor reference:** Korn Ferry KF Serif portraits, Spencer Stuart editorial leadership profiles.

**Compliance hot spots:** When the plate represents a real person, the photograph must be a licensed photo with documented consent; AI-generated portraits of real people are a Tennessee ELVIS Act + state right-of-publicity exposure. When the plate is a template or example, the prompt must produce a clearly archetypal/composite person with no real-person resemblance, and the asset must carry visible AI disclosure.

### 3. Anonymized Market Mapping / Org Chart

A visualization of the talent landscape for a search — competitor companies, role distribution, candidate clusters — with names and identities redacted to maintain confidentiality.

**Anatomy:** Bubble cluster (Revelio Labs convention) or org-tree with redacted nodes; lock icons on confidential nodes; legend bottom-left; gray silhouette avatars with role-and-industry descriptors only; hatched-circle company logo replacements.

**Anchor reference:** Revelio Labs market maps; Lightcast Talent Migration Dashboard; SignalFire dossier reference.

**Compliance hot spots:** No real-company logo reproduction without permission; no candidate identification; legend disclosure of the anonymization convention.

### 4. Board Search Deliverable / Board Index

A board-grade publication summarizing director searches, board composition trends, or board-search deliverables. Spencer Stuart's annual *US Board Index* is the canonical reference.

**Anatomy:** Year as typographic anchor on cover; restrained single-color masthead bar; serif editorial typography throughout; large data plates with 200pt+ percentages; section dividers as full-bleed firm-color fields with white display numerals.

**Anchor reference:** Spencer Stuart *2025 US Board Index*, 40th edition.

**Compliance hot spots:** Board-grade work has the strictest provenance and licensing standards. Avoid AI imagery on the cover unless the firm's policy explicitly permits it. Real photography of named directors requires individual consent.

### 5. Platform Dashboard Hero Plate

The hero image on a talent-intelligence platform's marketing site, product page, or sales deck — depicting the product UI with stylized data, AI agent panel, and recognition badges.

**Anatomy:** Rounded-card UI on a gradient mesh backdrop; choropleth or dotted-globe quadrant; force-directed skills graph; Sankey or talent-flow ribbon; bento-grid stat tiles ("1.6B career profiles"); AI-agent chat panel docked right; recognition badges (Fosway 9-Grid, IDC MarketScape, Brandon Hall) in a bottom strip.

**Anchor reference:** Eightfold "Infinite Workforce" hero, Gloat homepage, Lightcast 2025 brand 2.0 hero, Beamery Digital Twin hero.

**Compliance hot spots:** Even synthetic-data dashboards must avoid producing real-person likeness in the AI agent avatar; agent avatars should be clearly stylized (geometric, abstract, illustrated). Dashboard data must be obviously sample/illustrative.

### 6. Skills Graph / Capability Network

A glowing force-directed network of dots and lines representing a skills ontology, capability map, or organizational skills inventory. The signature visual for "skills intelligence" platforms.

**Anatomy:** Dark gradient backdrop; nodes as glowing dots in platform brand color; edges as thin glowing lines; selected nodes labeled with skill names; edge thickness representing relationship strength; legend bottom-right.

**Anchor reference:** Gloat *Loomra Knowledge Graph*, Eightfold Capability Dashboard, Beamery Digital Twin, Phenom career architecture trees.

**Compliance hot spots:** Skill names must not unintentionally surface protected characteristics (e.g., showing only specific demographic patterns of skill clusters can produce disparate-impact concerns).

### 7. Talent Flow / Migration Visualization

A Sankey diagram, arc map, or directional ribbon showing talent movement between companies, geographies, or roles. Used in workforce reports, conference keynotes, and platform marketing.

**Anatomy:** Width-weighted ribbons (Sankey) or directional curves (arc map); brand-colored ribbons; source/destination labels; data callouts at major flow junctions; time-period and source-attribution caption.

**Anchor reference:** LinkedIn #AmericaAtWork, Lightcast Talent Migration Dashboard, Crunchr internal mobility, BCG/CGD *Global Talent Mobility 2025*.

**Compliance hot spots:** Source attribution required when using third-party data (LinkedIn, Lightcast, Revelio Labs). Privacy considerations when flow data is aggregated from individual-level employee data.

### 8. HR Tech Vendor Pitch Deck Hero

The hero image of an HR Tech / talent intelligence vendor's pitch deck — designed to communicate platform sophistication, market position, and recognition status in a single 16:9 frame.

**Anatomy:** Dashboard hero plate (see type 5) plus product brand mark prominently placed; recognition badges in a horizontal strip; product tagline overlay; founding-year or scale stat in display type.

**Anchor reference:** Eightfold sales deck heroes, Gloat investor decks, Lightcast 2025 brand-launch deck.

**Compliance hot spots:** Recognition badges require licensing — using a Fosway 9-Grid badge without entitlement is a trademark exposure.

### 9. Career Site Hero Imagery

The dominant hero image on an employer's careers landing page. The single highest-stakes employer-brand asset because it sets candidate expectation for everything downstream.

**Anatomy:** Full-bleed daylight portrait of named employee (preferred — gold standard) OR illustrated alternative (GitLab, GitHub, Notion, Mailchimp register) OR environmental workplace detail with no faces (job-detail / req-page convention).

**Anchor reference:** Atlassian "Team Anywhere" location-stamped portraits, Airbnb "Live & Work Anywhere," GitLab handbook public photo briefs, Spotify #LifeAtSpotify TikTok ecosystem.

**Compliance hot spots:** **THIS IS THE PROBLEM CATEGORY.** Real photography with consent is the gold standard. AI-generated portraits of fabricated employees are the principal failure mode (Levi's × Lalaland, Mango Teen). The default rule applies most strongly here. See [`docs/03-candidate-imagery-problem.md`](./03-candidate-imagery-problem.md) and [`workflows/candidate-imagery-decision-tree.md`](../workflows/candidate-imagery-decision-tree.md).

### 10. LinkedIn Recruiter Campaign Tile

A 1200×1200 (or 1080×1350, or 1200×627) social tile produced for LinkedIn recruiter campaigns, sourcing outreach, or InMail attachment.

**Anatomy:** Brand-color block + employee pull-quote in serif display + small headshot inset (real employee with consent) OR typography-only treatment with employee quote and credential.

**Anchor reference:** Recruitics 2024-2025 LinkedIn campaign portfolio; Symphony Talent campaign work.

**Compliance hot spots:** Quote attribution requires consent for the named employee; quote modification requires re-confirmation; AI-generated photo of the quoted employee is impermissible.

### 11. EVP Pillar Treatment

The visual system for an Employer Value Proposition — typically three to five pillars, each with a custom icon, headline, and supporting visual.

**Anatomy:** 3-5 pillar grid; custom icon set (Recraft V3 or Ideogram for the icon system itself); pillar headline in display type; supporting copy in body type; supporting image (illustrated alternative or photography).

**Anchor reference:** Marriott "Be" framework (begin / belong / become); CAE "Our Promise. For All." (Blu Ivy 2025); Salesforce Trailblazer system.

**Compliance hot spots:** Localization across markets — pillar names and visuals must adapt to legal frameworks of each market.

### 12. Job Posting / Req Hero

The hero image at the top of a job posting (LinkedIn req page, careers-site detail page, or job-board listing).

**Anatomy:** Workplace environmental detail (no faces) — a workspace, a window onto a city, a tooling close-up, a team artifact — OR illustrated alternative; subtle brand color overlay; sometimes accompanied by department/team identifier.

**Anchor reference:** Atlassian job detail pages; Stripe job postings; Notion careers detail.

**Compliance hot spots:** Lower-stakes than career site hero, but still subject to AI disclosure when image is AI-generated.

### 13. Workforce Trends Report Cover

A recurring publication's cover (LinkedIn *Global Talent Trends*, Mercer *Global Talent Trends*, Korn Ferry *Workforce 2025*, Lightcast *Fault Lines*, Deloitte *Global Human Capital Trends*).

**Anatomy:** Three aesthetic camps:
- **Photography-led** (McKinsey grayscale-blue-purple-shimmer, Deloitte named-designer credits, Mercer persona cards, Adecco worker cinematography, Korn Ferry editorial portraits).
- **Illustration-led** (Randstad touch-illustration, LinkedIn flat vector, Bain editorial illustration).
- **Abstract-data-art-led** (WEF Insight Report template, BCG slope graphs, Lightcast Tableau-public dashboards as the deliverable, PwC Tom Roope-era fluid blob covers).

**Anchor reference:** WEF *Future of Jobs 2025*, Mercer *Global Talent Trends 2026*, Lightcast *Fault Lines 2026*, Deloitte *Turning Tensions Into Triumphs 2025*.

**Compliance hot spots:** Most workforce reports prohibit AI imagery on the cover — provenance and licensing certainty required for archival publications.

### 14. Salary / Compensation Report Cover

The annual or periodic cover of a salary guide / compensation report (Robert Half *Salary Guide*, Mercer *Total Remuneration Survey*).

**Anatomy:** Year as typographic anchor; market-condition subtitle; brand-color wave or abstract motif; sometimes accompanied by interactive web format.

**Anchor reference:** Robert Half *2026 Salary Guide*; Mercer Marsh Benefits *Health Trends*.

**Compliance hot spots:** Salary data sourcing and methodology disclosure required (typically a methodology page rather than visual concern, but visual must not misrepresent data scale or scope).

### 15. DEI Report Cover

The annual DEI / belonging / equity report cover for an enterprise or institution. Treated separately because the post-2024 register has shifted decisively away from "diversity grid" imagery.

**Anatomy:** Architectural restraint (SOM 2024 model — abstract corporate-architecture photography with no faces) OR named-employee story (single real employee with full consent and full caption attribution) OR data-led abstract (WEF Insight Report register applied to DEI metrics).

**Anchor reference:** SOM 2024 DEI Report (architectural restraint exemplar); Patagonia Indigenous land-stewards approach; GitLab Handbook public diversity stats.

**Compliance hot spots:** **HIGHEST-STAKES CATEGORY.** Synthetic diversity (AI-generated images of demographically varied employees who don't actually exist) is the central failure mode. EEOC guidance treats imagery as part of recruiting practices; representation testing (Monk Skin Tone Scale + intersectional audit) is non-negotiable. See [`compliance/representation-testing.md`](../compliance/representation-testing.md).

### 16. Conference Keynote Backdrop

The ultra-wide LED backdrop behind a keynote speaker at an HR Tech, talent intelligence, or recruiting conference (UNLEASH, HR Tech Conference, Transform, RecFest, ERE).

**Anatomy:** Ultra-wide LED format (typically 16:9 with 2.5:1 ultra-wide variant), dark gradient mesh in platform's brand palette, single typographic headline, abstract particle or aurora animation in background, sometimes synchronized to speaker pacing.

**Anchor reference:** Eightfold *Cultivate* (Ritz-Carlton Laguna Niguel) warm coastal register; UNLEASH theatrical magenta-and-cyan washes; HR Tech Conference corporate blue with amber spotlights; SHRM Annual traditional red/blue.

**Compliance hot spots:** Backdrop motion clips (if generated) require Veo 3.1 / Runway provenance documentation. Conference IP licensing if recognition badges or logos are used.

## Cross-Reference Matrix

| Deliverable Type | Models Recommended | Workflow Recipe (Parent) | Add-On Workflow Tier |
| :--- | :--- | :--- | :-: |
| 1 — Candidate dossier cover | MJ v7 + Ideogram | Recipe C (typography compositing) | 3 |
| 2 — Executive bio plate | MJ v7 (archetypal) + real photo (named) | Recipe B (NB→MJ) | 3 |
| 3 — Market map | GPT Image 2 / NB Pro | Recipe C | 2-3 |
| 4 — Board search | MJ v7 + Ideogram | Recipe C | 3 |
| 5 — Dashboard hero | GPT Image 2 / Flux.2 Pro | (single-model with composite) | 2 |
| 6 — Skills graph | Flux.2 Pro / Recraft V3 | Recipe C | 2 |
| 7 — Talent flow | GPT Image 2 / Flux.2 Pro | Recipe C | 2 |
| 8 — Vendor pitch hero | GPT Image 2 + Ideogram | Recipe C | 2 |
| 9 — Career site hero | Recraft V3 (illustrated) / real photo (preferred) | (mixed) | 2 |
| 10 — LinkedIn tile | Ideogram v3 | Recipe C | 1 |
| 11 — EVP pillar | Recraft V3 + Ideogram | Recipe C | 2 |
| 12 — Job posting | NB Pro / MJ v7 | Recipe A | 1 |
| 13 — Workforce cover | Ideogram + MJ composite | Recipe C | 3 |
| 14 — Salary guide | Ideogram + MJ composite | Recipe C | 2 |
| 15 — DEI report | MJ v7 + Ideogram | Recipe C | 3 |
| 16 — Conference backdrop | MJ v7 + Ideogram | Recipe C | 2 |

## Related

- [Add-on README](../README.md)
- [Three sub-registers](./01-three-sub-registers.md)
- [Candidate imagery problem](./03-candidate-imagery-problem.md)
- [Three production tiers](../workflows/three-production-tiers.md)
- [Prompts master library](../prompts/README.md)
