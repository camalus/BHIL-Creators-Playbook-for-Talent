# CHANGELOG — Talent Intelligence Add-On

All notable changes to this add-on are documented here. Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) and adheres to semantic versioning.

This add-on versions independently of the parent BHIL Creators Playbook. Compatibility is documented per release.

## [1.2.0] — 2026-04-29

Layout refinement of the v1.1.0 quick-reference release. Compatible with parent BHIL Creators Playbook v1.0.0.

### Changed

- Tightened the BHIL-branded reference document layout (`BHIL-Talent-Intelligence-Addon-Reference-v1.2.0.docx`) so 3-4 prompt blocks fit per page rather than one-per-page. Document compressed from 35 to 24 pages while preserving full-width code blocks, cobalt number badges, and red-bold `[PLACEHOLDER]` highlighting.
- The underlying source-of-truth file in `quick-reference/20-prompt-library.md` is unchanged from v1.1.0; only the rendered branded-doc representation was tightened.

### Notes

- The tightened layout is the preferred presentation for stakeholder review and designer handoff. The full prompt files in `prompts/` remain the authoritative resource for production work requiring four-variant libraries, parameter tables, and detailed failure-mode documentation.

## [1.1.0] — 2026-04-29

Adds a copy/paste prompt library as a fast-path companion to the full prompt files. Compatible with parent BHIL Creators Playbook v1.0.0.

### Added

**Quick Reference (`quick-reference/`) — new directory**
- `README.md` — orientation for the new directory; explains the relationship between the quick-reference and the full prompt files
- `20-prompt-library.md` — 20 production-ready prompts in a single scannable file. Each prompt: number, title, sub-register, model, aspect ratio, use case, compliance posture, copy/paste code block. The source of truth for Section 11 of the BHIL-branded reference document.

The 20 prompts:

*Sub-Register A — Executive Search & Retained-Search Editorial (5)*
- 01 — Candidate Dossier Cover — Mountain Summit (MJ v7)
- 02 — Candidate Dossier Cover — Architectural Building (MJ v7)
- 03 — Dossier Cover — Typographic Overlay (Ideogram v3)
- 04 — Anonymized Market Map — Bubble Cluster (GPT Image 2 / NB Pro)
- 05 — Board Search Deliverable — Spencer Stuart Register (MJ v7 + Ideogram)

*Sub-Register B — Talent Intelligence Platform Dashboard (4)*
- 06 — Platform Dashboard Hero — Eightfold Register (GPT Image 2 / Flux.2 Pro)
- 07 — Skills Graph Network — Force-Directed Glow (Flux.2 Pro / Recraft V3)
- 08 — Talent Flow Sankey — Width-Weighted Ribbons (GPT Image 2 / Flux.2 Pro)
- 09 — Vendor Pitch Deck Hero — With Recognition Badges (GPT Image 2 + Ideogram)

*Sub-Register C — Employer Brand & Recruitment Marketing (7)*
- 10 — Career Site Hero — Illustrated Alternative (Recraft V3)
- 11 — Career Site Hero — Environmental Workspace (Nano Banana Pro)
- 12 — LinkedIn Recruiter Tile — Typography-Only Quote (Ideogram v3)
- 13 — EVP Pillar Icon Set — Three-Pillar Grid (Recraft V3)
- 14 — EVP Pillar Layout — Three-Column Grid (Ideogram v3)
- 15 — Job Posting Environmental — Engineering Workspace (Nano Banana Pro)
- 16 — Job Posting Environmental — Lab / Scientific Workspace (NB Pro / MJ v7)

*Workforce Reports & Conference Materials (4)*
- 17 — Workforce Trends Cover — Topographic Gradient (MJ v7 + Ideogram)
- 18 — Salary Guide Cover — Brand-Color Wave (MJ v7)
- 19 — DEI Report Cover — Architectural Restraint (MJ v7)
- 20 — Conference Keynote Backdrop — Ultra-Wide LED (MJ v7 + Ideogram)

A customization field reference table covering all `[PLACEHOLDERS]` used across the library is included.

### Branded Reference Document

A companion BHIL-branded `.docx` reference (`BHIL-Talent-Intelligence-Addon-Reference-v1.1.0.docx`) is produced from this release. The branded doc renders the 20-prompt library as Section 11 with a cobalt-badge layout, full-width monospace code blocks, and red-bold `[PLACEHOLDER]` highlighting for fast scanning by stakeholder reviewers and designers.

### Notes

- Default rule applied across all 20 prompts: AI for abstract concept and environmental/background; real photography (with consent and C2PA-tagged provenance) for humans wherever a viewer might mistake the subject for a real employee or candidate.
- No new compliance, prompt, template, or workflow files were added or modified in v1.1.0 — only the new `quick-reference/` directory.

## [1.0.0] — 2026-04-29

Initial release. Compatible with parent BHIL Creators Playbook v1.0.0.

### Added

**Documentation (`docs/`)**
- Introduction and rationale for the add-on
- The three sub-registers framework (retained-search editorial / talent-intelligence platform dashboard / recruiting-agency editorial-illustration hybrid)
- 14 canonical deliverable types mapped to prompts
- The candidate-imagery problem and the default rule
- Industry glossary

**Compliance (`compliance/`)**
- AI imagery policy template
- C2PA Content Credentials disclosure standards
- Jurisdiction matrix covering EU AI Act, Colorado AI Act, Illinois HB 3773 + Illinois AI Video Interview Act, NYC Local Law 144, Maryland HB 1202, Tennessee ELVIS Act, Ontario Bill 149, Quebec Law 25, UK ICO recommendations
- Demographic representation testing protocols (Monk Skin Tone Scale + intersectional audit)
- Consent and likeness rules for people in imagery

**Reference (`reference/`)**
- Sub-register A specification — retained-search editorial
- Sub-register B specification — talent-intelligence platform dashboard
- Sub-register C specification — recruiting-agency editorial-illustration hybrid
- Exemplar library — 15+ curated industry benchmark references

**Prompts (`prompts/`) — 16 production prompts in four categories**

*Executive Search (sub-register A)*
- 01 — Candidate Dossier Cover (MJ v7, architectural metaphor, codename + confidential stamp)
- 02 — Executive Bio Plate (MJ v7, no-real-person guardrail, signature wins layout)
- 03 — Anonymized Market Map (GPT Image 2 / NB Pro, redacted nodes with lock icons)
- 04 — Board Search Deliverable (MJ v7 + Ideogram composite, board-grade restraint)

*Talent Intelligence Platform (sub-register B)*
- 05 — Dashboard Hero Plate (GPT Image 2 / Flux.2 Pro, bento-grid stats + AI agent panel)
- 06 — Skills Graph Network (Flux.2 Pro / Recraft V3, force-directed glow on dark)
- 07 — Talent Flow Sankey (GPT Image 2 / Flux.2 Pro, width-weighted ribbons)
- 08 — Vendor Pitch Deck Hero (GPT Image 2 + Ideogram, recognition badges and dashboard cards)

*Employer Brand (sub-register C)*
- 09 — Career Site Hero (Recraft V3 illustration alternative + concept exploration mode)
- 10 — LinkedIn Recruiter Tile (Ideogram v3, brand-color block + employee pull-quote)
- 11 — EVP Pillar Treatment (Recraft V3 + Ideogram, three-pillar grid)
- 12 — Job Posting Environmental (NB Pro / MJ v7, workplace detail no faces)

*Workforce Reports*
- 13 — Workforce Trends Cover (Ideogram + MJ composite, year as typographic anchor)
- 14 — Salary Guide Cover (Ideogram + MJ composite, market-condition subtitle)
- 15 — DEI Report Cover (MJ v7 + Ideogram, architectural restraint, named-employee alternative)
- 16 — Conference Keynote Backdrop (MJ v7 + Ideogram, ultra-wide LED with particle aurora)

**Templates (`templates/`)**
- Candidate Dossier Spec Template
- Employer Brand Project Spec Template
- AI Disclosure Statement Template (per-asset and per-campaign)

**Workflows (`workflows/`)**
- Three Production Tiers (fast iteration, mid-tier, archival quality)
- Candidate Imagery Decision Tree (the central design constraint)

### Notes

- This release establishes a default rule that all subsequent prompts and templates inherit: **AI for abstract concept and environmental/background; real photography (with consent and C2PA-tagged provenance) for humans wherever a viewer might mistake the subject for a real employee or candidate.**
- All prompts that produce imagery resembling real people require visible AI disclosure per the standards in [`compliance/disclosure-standards.md`](./compliance/disclosure-standards.md).
- All prompts include explicit guardrails against synthetic-diversity failure modes documented in the Levi's × Lalaland (2023), Mango Teen (2024), Coca-Cola (2024-2025), and Google Gemini (2024) reference cases.

## Roadmap

### [1.3.0] — Planned Q3 2026

- Worked case studies in `examples/` — anonymized end-to-end project walkthroughs.
- Expanded compliance section: California regulatory updates (AB 2930, SB 7 reintroductions if passed), additional state laws as enacted.
- Two additional prompts: anonymized longlist treatment, succession plate.
- Translation guide for adapting prompts to non-English markets (initial focus: French, German, Japanese employer-brand registers).
- Expanded quick-reference: a 30-prompt library variant covering more vertical contexts.

### [1.4.0] — Planned Q4 2026

- Sub-register D — boutique/specialist search firms (life sciences executive search, executive coaching firms, niche verticals like climate-tech and AI talent firms) with their distinct visual registers.
- Industry-vertical reference files (financial-services exec search, healthcare exec search, tech exec search) — each carrying distinct typographic and palette conventions.
- AI imagery in candidate experience: assessment center visuals, onboarding hero plates, internal mobility dashboards.

### [2.0.0] — Planned 2027

- Motion deliverables for talent: recruiter video assets, conference stage motion, animated dashboard demos.
- Veo 3.1 / Runway Gen-4 prompt patterns for talent-industry motion.
- Voice / audio considerations for AI-generated recruiting content (Tennessee ELVIS Act compliance, voice-cloning disclosure).
- Live AI-generated content in interviewing contexts — guidelines for what is and is not acceptable in candidate-facing live AI imagery.

## Compatibility

| Add-On Version | Parent BHIL Playbook Version | Notes |
| :--- | :--- | :--- |
| 1.0.0 | 1.0.0 | Initial release (47 files). |
| 1.1.0 | 1.0.0 | Adds `quick-reference/` directory with 20-prompt copy/paste library (49 files total). |
| 1.2.0 | 1.0.0 | Layout refinement of the BHIL-branded reference doc; no source-file content changes from v1.1.0. |

## Related

- [Add-on README](./README.md)
- [Parent repo CHANGELOG](../../CHANGELOG.md)
