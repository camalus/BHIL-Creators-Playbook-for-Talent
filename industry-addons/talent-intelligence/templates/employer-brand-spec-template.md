# Employer Brand Project Spec Template

Project-level brief for an employer brand campaign or content production project. Instantiate by copying this template to your project workspace and filling in the bracketed fields.

---

## Project: [PROJECT NAME]

| Field | Value |
| :--- | :--- |
| **Project name** | [e.g., "2026 Career Site Refresh"] |
| **Project type** | [Career Site / EVP Launch / LinkedIn Campaign / Conference / Multi-channel] |
| **Client / organization** | [Organization name] |
| **Project lead** | [Lead name and role] |
| **Production agency / partner** | [Agency name, if applicable] |
| **Production tier** | [1 — Fast iteration / 2 — Mid-tier / 3 — Archival] |
| **Project start** | [YYYY-MM-DD] |
| **Project end target** | [YYYY-MM-DD] |
| **Total asset count target** | [N] |

## Register Declaration

**Sub-register:** [A — Retained-search editorial / B — Talent-intelligence platform dashboard / **C — Recruiting-agency editorial-illustration hybrid**]

For mixed-register projects, declare register per asset in the asset inventory below.

| Element | Value |
| :--- | :--- |
| **Brand primary** | [Hex value] |
| **Brand accent** | [Hex value] |
| **Brand neutral / ground** | [Hex value] |
| **Display typeface** | [Named typeface] |
| **Body typeface** | [Named typeface] |
| **Photography register** | [Documentary daylight / Studio editorial / Architectural / Illustrated alternative] |
| **Headline convention** | [Title Case / Sentence case / lower-case sentence-case (sub-register C)] |
| **Brand profile (BHIL parent)** | [Reference to brand profile file or sref ID set] |

## Channel Matrix

| Channel | Asset Types | Aspect Ratios | Volume |
| :--- | :--- | :--- | :--- |
| Career site (desktop) | Hero, secondary, role pages | 1920×1080, 1600×900 | [N] |
| Career site (mobile) | Hero, secondary | 750×1334 | [N] |
| LinkedIn organic | Recruiter tiles, EVP posts | 1200×1200, 1080×1350 | [N] |
| LinkedIn paid | Sponsored content tiles | 1200×627, 1200×1200 | [N] |
| Job postings (LinkedIn req page) | Header banners | 1600×400 | [N] |
| Job postings (careers site detail) | Detail page hero | 1920×400 | [N] |
| Instagram / Meta | Square, story | 1080×1080, 1080×1920 | [N] |
| TikTok | Vertical motion / static | 1080×1920 | [N] |
| Email recruitment | Header banner | 600×300 | [N] |
| Print collateral | Brochures, EVP toolkit | A4 portrait, A3 landscape | [N] |

## Asset Inventory

| Asset | Prompt Reference | Sub-Register | Source (Real Photo / AI / Mixed) | Notes |
| :--- | :--- | :-: | :-: | :--- |
| Career site hero — Engineering | [`../prompts/03-employer-brand/09-career-site-hero.md`](../prompts/03-employer-brand/09-career-site-hero.md) | C | Real photo | Named consenting employee |
| Career site hero — Design | [`../prompts/03-employer-brand/09-career-site-hero.md`](../prompts/03-employer-brand/09-career-site-hero.md) | C | AI illustrated | Recraft V3 illustrated alternative |
| EVP pillar grid | [`../prompts/03-employer-brand/11-evp-pillar-treatment.md`](../prompts/03-employer-brand/11-evp-pillar-treatment.md) | C | AI mixed | Icon set AI; supporting imagery real |
| LinkedIn recruiter tiles (×12) | [`../prompts/03-employer-brand/10-linkedin-recruiter-tile.md`](../prompts/03-employer-brand/10-linkedin-recruiter-tile.md) | C | Real photo + AI typography | Real employee headshots; layout AI |
| Job posting hero variants (×6) | [`../prompts/03-employer-brand/12-job-posting-environmental.md`](../prompts/03-employer-brand/12-job-posting-environmental.md) | C | AI environmental | No faces, no figures |
| ... | ... | ... | ... | ... |

## Consent Inventory

For each asset depicting a real person:

| Asset | Person Depicted | Role / Title | Consent Status | Consent Scope | Notes |
| :--- | :--- | :--- | :-: | :--- | :--- |
| Career site hero — Engineering | [Employee name] | [Role] | [Documented / Pending / Refused] | [Channels, geographies, period] | Re-confirmation triggered upon role change |
| LinkedIn tile — Quote 1 | [Employee name] | [Role] | [Documented] | LinkedIn organic + paid, US, 12 months | Quote is original employee testimony |
| ... | ... | ... | ... | ... | ... |

## Jurisdiction Footprint

| Jurisdiction | Applicable Obligations | Notes |
| :--- | :--- | :--- |
| United States — Federal | Title VII, ADEA, ADA, GINA, EPA, OFCCP April 2024 guidance | EEOC withdrawn 2025 — statutes still apply |
| US — State (Colorado) | Colorado AI Act SB 24-205, effective June 30, 2026 | "Reasonable care" duty; risk management policy |
| US — State (Illinois) | Illinois HB 3773, effective January 1, 2026 | Candidate notice when AI used |
| US — State (Tennessee) | ELVIS Act | No likeness of real persons without consent |
| EU | EU AI Act Annex III §4 (high-risk recruitment) effective Aug 2, 2026; Article 50 (deepfakes) | Conformity assessment for in-scope systems |
| United Kingdom | UK ICO November 2024 recommendations; UK GDPR | DPIA for candidate imagery |
| Canada — Ontario | Bill 149 (Working for Workers Four), effective January 1, 2026 | AI-use disclosure in job postings (≥25 employees) |
| Canada — Quebec | Law 25 §12.1 | Notice for automated decisions; CAI 60-day biometric notice |

Multi-jurisdiction projects apply the most stringent applicable obligations across all dimensions.

## AI Imagery Compliance

| Question | Decision |
| :--- | :--- |
| **AI imagery permitted in this project?** | YES — for abstract concept, environmental/background, illustrated alternatives, and template/explainer composite persons. Per default rule. |
| **AI imagery for human subjects in candidate-facing assets?** | NO — except illustrated alternatives clearly stylized. |
| **AI imagery for fabricated employees?** | NO. |
| **C2PA Content Credentials applied?** | YES — to all AI-generated assets. |
| **SynthID complementary?** | [Where Google DeepMind tools used: YES] |
| **Visible AI disclosure on candidate-facing assets?** | YES — per [`../compliance/disclosure-standards.md`](../compliance/disclosure-standards.md). |
| **Disclosure language standard** | Per channel matrix in disclosure standards file. |

## Representation Testing Plan

For every asset depicting people:

| Test | Applied? | Reviewer | Threshold |
| :--- | :-: | :--- | :--- |
| Test 1 — Monk Skin Tone Scale audit | YES | [Reviewer name] | 15-percentage-point deviation threshold from comparison populations |
| Test 2 — Intersectional audit | YES | [Reviewer name] | No intersectional band systematically excluded |
| Test 3 — Bias amplification check (AI assets only) | YES — for AI-generated assets | [Reviewer name] | Variations consistent with prompt intent and target population |
| Failure-mode review | YES | [Reviewer name] | All documented failure cases checked |

Comparison populations:
- **Depicted organization workforce demographics:** [Source — HRIS data, dated]
- **Target audience demographics:** [Source — recruiting analytics or market data]
- **Geographic market demographics:** [Source — Census or equivalent]

## Production Workflow

| Stage | Owner | Target Date |
| :--- | :--- | :--- |
| Brief approved | [Lead] | [Date] |
| Brand profile and srefs locked | [Designer] | [Date] |
| Asset list finalized | [PM] | [Date] |
| Real photography scheduled | [PM + photographer] | [Date] |
| Consent process initiated | [HR + employees] | [Date] |
| AI assets generated (first pass) | [Designer] | [Date] |
| Representation testing applied | [Reviewer] | [Date] |
| Compliance review | [Compliance] | [Date] |
| Stakeholder review | [Lead + brand stakeholders] | [Date] |
| Final approval | [Lead] | [Date] |
| Channel deployment | [Marketing ops] | [Date] |

## Recordkeeping

The following are archived for **five years from each asset's last published date**:

- This spec, completed.
- All prompts used (with iteration history).
- Model versions used.
- All reference images and brand profiles.
- All generated and photographed assets (final + variants).
- Reviewer identities and notes.
- Representation test results (per asset).
- Consent documentation (per real person depicted).
- Disclosure language and channel placement.
- Publication / deployment records.
- Withdrawal / retirement records.

Archive location: [project workspace path or DAM identifier].

## Related

- [Templates README](./README.md)
- [Employer brand prompts](../prompts/03-employer-brand/README.md)
- [AI imagery policy](../compliance/ai-imagery-policy.md)
- [Disclosure standards](../compliance/disclosure-standards.md)
- [Representation testing](../compliance/representation-testing.md)
- [Consent and likeness](../compliance/consent-and-likeness.md)
- [Sub-register C specification](../reference/sub-register-c-agency.md)
- [Three production tiers](../workflows/three-production-tiers.md)
