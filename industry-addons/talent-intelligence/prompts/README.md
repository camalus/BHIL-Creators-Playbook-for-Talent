# Prompts — Master Library

Sixteen production-grade prompts for talent intelligence and recruiting deliverables, organized by category and sub-register. Each prompt is copy-paste-ready with parameters, customization fields, variants, and failure modes documented.

## Organization

| Category | Sub-Register | Prompts |
| :--- | :-: | :-: |
| [`01-executive-search/`](./01-executive-search/) | A | 4 |
| [`02-talent-intelligence-platform/`](./02-talent-intelligence-platform/) | B | 4 |
| [`03-employer-brand/`](./03-employer-brand/) | C | 4 |
| [`04-workforce-reports/`](./04-workforce-reports/) | mixed | 4 |

## The 16 Prompts

### 01 — Executive Search (Sub-Register A)

| # | Prompt | Recommended Model |
| :- | :--- | :--- |
| 01 | [Candidate Dossier Cover](./01-executive-search/01-candidate-dossier-cover.md) | MJ v7 + Ideogram |
| 02 | [Executive Bio Plate](./01-executive-search/02-executive-bio-plate.md) | MJ v7 (archetypal) |
| 03 | [Anonymized Market Map](./01-executive-search/03-anonymized-market-map.md) | GPT Image 2 / NB Pro |
| 04 | [Board Search Deliverable](./01-executive-search/04-board-search-deliverable.md) | MJ v7 + Ideogram |

### 02 — Talent Intelligence Platform (Sub-Register B)

| # | Prompt | Recommended Model |
| :- | :--- | :--- |
| 05 | [Dashboard Hero Plate](./02-talent-intelligence-platform/05-dashboard-hero-plate.md) | GPT Image 2 / Flux.2 Pro |
| 06 | [Skills Graph Network](./02-talent-intelligence-platform/06-skills-graph-network.md) | Flux.2 Pro / Recraft V3 |
| 07 | [Talent Flow Sankey](./02-talent-intelligence-platform/07-talent-flow-sankey.md) | GPT Image 2 / Flux.2 Pro |
| 08 | [Vendor Pitch Deck Hero](./02-talent-intelligence-platform/08-vendor-pitch-deck-hero.md) | GPT Image 2 + Ideogram |

### 03 — Employer Brand (Sub-Register C)

| # | Prompt | Recommended Model |
| :- | :--- | :--- |
| 09 | [Career Site Hero](./03-employer-brand/09-career-site-hero.md) | Recraft V3 (illustrated) / real photo |
| 10 | [LinkedIn Recruiter Tile](./03-employer-brand/10-linkedin-recruiter-tile.md) | Ideogram v3 |
| 11 | [EVP Pillar Treatment](./03-employer-brand/11-evp-pillar-treatment.md) | Recraft V3 + Ideogram |
| 12 | [Job Posting Environmental](./03-employer-brand/12-job-posting-environmental.md) | NB Pro / MJ v7 |

### 04 — Workforce Reports (Mixed)

| # | Prompt | Recommended Model |
| :- | :--- | :--- |
| 13 | [Workforce Trends Cover](./04-workforce-reports/13-workforce-trends-cover.md) | Ideogram + MJ |
| 14 | [Salary Guide Cover](./04-workforce-reports/14-salary-guide-cover.md) | Ideogram + MJ |
| 15 | [DEI Report Cover](./04-workforce-reports/15-dei-report-cover.md) | MJ v7 + Ideogram |
| 16 | [Conference Keynote Backdrop](./04-workforce-reports/16-conference-keynote-backdrop.md) | MJ v7 + Ideogram |

## Common Conventions Across All Prompts

Every prompt in this add-on follows these conventions:

### Sub-Register Declaration

Every prompt declares its sub-register (A, B, or C) explicitly in its frontmatter. The sub-register determines the palette, typography, photography conventions, and data-viz grammar used in the prompt construction.

### Talent-Specific Placeholders

Beyond the parent BHIL placeholders (`[BHIL profile]`, `[BHIL sref]`), this add-on uses talent-specific placeholders:

- `[CLIENT FIRM]` — the search firm or agency producing the deliverable.
- `[CLIENT CODE NAME]` — anonymized client codename for confidential dossiers.
- `[PROJECT CODENAME]` — the search or campaign codename (e.g., "Project Aurora").
- `[SEARCH SLATE NUMBER]` — slate iteration (e.g., "Slate III").
- `[PRACTICE AREA]` — search practice (e.g., "CEO & Board of Directors").
- `[PLATFORM PROFILE]` — declared per-project for sub-register B (e.g., "Eightfold-style purple gradient").
- `[PLATFORM SREFS]` — Midjourney sref slots for sub-register B platform palettes.
- `[CLIENT BRAND]` — agency-specific brand declaration for sub-register C.
- `[EVP PILLAR NAME]` — for EVP work (e.g., "begin" / "belong" / "become").
- `[JOB FAMILY]` — for job-specific marketing (e.g., "engineering" / "sales" / "operations").

### Compliance Declaration

Every prompt that produces imagery depicting people declares its compliance posture, referencing:

- The default rule from [`../docs/03-candidate-imagery-problem.md`](../docs/03-candidate-imagery-problem.md).
- The decision tree from [`../workflows/candidate-imagery-decision-tree.md`](../workflows/candidate-imagery-decision-tree.md).
- The disclosure standards from [`../compliance/disclosure-standards.md`](../compliance/disclosure-standards.md).
- The representation testing protocols from [`../compliance/representation-testing.md`](../compliance/representation-testing.md).
- The consent and likeness rules from [`../compliance/consent-and-likeness.md`](../compliance/consent-and-likeness.md).

### Variants

Each prompt provides 4 variants (A-D) showing how to adapt the prompt across:

- A: the canonical/default version.
- B: a tonal alternative (e.g., warmer / cooler / more austere / more inviting).
- C: a structural alternative (e.g., portrait / landscape; environmental / portraiture; etc.).
- D: an explicit fallback to a non-AI alternative (real photography brief, illustrated alternative, anonymous-silhouette convention).

### Failure Modes

Each prompt documents 3-5 specific failure modes and how to mitigate them. The most common failure modes across the add-on:

- **Off-register output** — generated imagery that reads in the wrong sub-register.
- **Real-person resemblance** — AI-generated person too closely resembling a real, identifiable individual.
- **Synthetic diversity** — AI-generated demographic variety not matching depicted population.
- **Stock-photo register** — AI output that reads as stock photography.
- **Stylization mismatch** — illustration register that's photo-real enough to confuse viewers.

### Cross-References

Each prompt cross-references:

- The relevant sub-register specification.
- The relevant exemplar(s) from the library.
- The relevant template(s) for project-level briefing.
- The relevant compliance documentation.

## Quick-Use Decision Path

To select the right prompt:

1. **Identify your deliverable type.** ([`../docs/02-deliverable-types.md`](../docs/02-deliverable-types.md))
2. **Confirm your sub-register.** ([`../docs/01-three-sub-registers.md`](../docs/01-three-sub-registers.md))
3. **Read the relevant prompt.** Apply the customization fields. Generate.
4. **Apply compliance:** representation testing, disclosure, consent (where applicable), provenance archive.
5. **Document.** Save the prompt, output, and compliance documentation per [`../compliance/ai-imagery-policy.md`](../compliance/ai-imagery-policy.md) Section 9.

## Related

- [Add-on README](../README.md)
- [Three sub-registers](../docs/01-three-sub-registers.md)
- [Deliverable types](../docs/02-deliverable-types.md)
- [Candidate imagery decision tree](../workflows/candidate-imagery-decision-tree.md)
- [Three production tiers](../workflows/three-production-tiers.md)
- [Reference library](../reference/README.md)
- [Compliance documentation](../compliance/README.md)
- [Templates](../templates/README.md)
- [Parent prompts library](../../../prompts/README.md)
