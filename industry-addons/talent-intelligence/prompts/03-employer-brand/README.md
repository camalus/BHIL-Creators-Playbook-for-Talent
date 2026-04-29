# Employer Brand — Prompts (Sub-Register C)

Four prompts for employer brand and recruitment marketing deliverables in the recruiting-agency editorial-illustration hybrid register.

This is the **highest-stakes category** for the candidate-imagery problem. Every prompt in this directory enforces the default rule: AI for abstract concept and environmental/background; real photography (with consent and C2PA-tagged provenance) for humans wherever a viewer might mistake the subject for a real employee or candidate.

## Prompts In This Directory

| # | Prompt | Models | Tier | Compliance Stakes |
| :- | :--- | :--- | :-: | :-: |
| 09 | [Career Site Hero](./09-career-site-hero.md) | Recraft V3 (illustrated) / real photo (preferred) | 2 | **Highest** |
| 10 | [LinkedIn Recruiter Tile](./10-linkedin-recruiter-tile.md) | Ideogram v3 (typographic) | 1 | High |
| 11 | [EVP Pillar Treatment](./11-evp-pillar-treatment.md) | Recraft V3 + Ideogram | 2 | Moderate |
| 12 | [Job Posting Environmental](./12-job-posting-environmental.md) | NB Pro / MJ v7 (no faces) | 1 | Moderate |

## Sub-Register C — Brief Recap

The recruiting-agency editorial-illustration hybrid register. Lower-case sentence-case headlines (Randstad, AMS, Adecco). Custom typefaces as luxury cue. Documentary daylight portraiture with copy room around subjects. Illustration libraries function as authenticity hedges and localization tools. Single-color chapter dividers and section breaks.

Anchor brands and their dominant accents:

- **Randstad** — `#0F69AF` blue + sentence-case headlines + touch-illustration accents.
- **Adecco** — `#FF0000` red + desaturated worker cinematography.
- **Robert Half** — coral hero portraits + squircle masks.
- **ManpowerGroup** — blue choropleths + Ceros scrollytelling.
- **AMS** — high-contrast magenta-on-black geometric data art.
- **Cielo** — sky-blue gradients + "Illuminate Talent" torch motif.

See [`../../reference/sub-register-c-agency.md`](../../reference/sub-register-c-agency.md) for the full visual specification.

## Customization Fields Across This Category

These fields recur throughout the prompts in this directory:

| Field | Example | Notes |
| :--- | :--- | :--- |
| `[CLIENT FIRM]` | "Atlassian" or your organization | The employer brand anchor |
| `[BRAND PROFILE]` | Client's brand profile (palette, typography, photography spec) | Replaces parent BHIL profile for this sub-register |
| `[BRAND ACCENT]` | "#0F69AF" / "#FF0000" / "#FF5C39" / etc. | The single-accent color |
| `[EVP PILLAR NAME]` | "Begin / Belong / Become" | EVP framework specific |
| `[EMPLOYEE NAME]` | "Sarah Park" | For tiles featuring real employees only — NEVER for AI-generated faces |
| `[ROLE TITLE]` | "Senior Software Engineer, Platform" | The depicted role |
| `[LOCATION]` | "Sydney, Australia" or "Atlanta, GA" | Geographic context |
| `[QUOTE]` | Real employee quote, attributed | Quote requires consent |
| `[JOB FAMILY]` | "Engineering" / "Sales" / "Operations" | Department or function |

## Compliance Posture Across This Category

Every prompt in this directory is annotated with its compliance posture. The category-wide defaults:

- **No fabricated employees in candidate-facing assets.** AI-generated portraits depicting "employees" are prohibited per [`../../compliance/ai-imagery-policy.md`](../../compliance/ai-imagery-policy.md) Section 4.1. Real photography or illustrated alternatives are the permitted paths.
- **Quote attribution requires consent.** A LinkedIn tile featuring a real employee's quote requires that employee's documented consent.
- **Visible AI disclosure** for any AI-generated imagery in candidate-facing channels per [`../../compliance/disclosure-standards.md`](../../compliance/disclosure-standards.md).
- **Representation testing** for every asset depicting people per [`../../compliance/representation-testing.md`](../../compliance/representation-testing.md).
- **Five-year recordkeeping** of prompts, model versions, reference images, reviewer identity, and consent documentation.

## Workflow Tier Guidance

These prompts cluster in production tiers 1 and 2. See [`../../workflows/three-production-tiers.md`](../../workflows/three-production-tiers.md):

- **Tier 1 (fast iteration)**: LinkedIn recruiter tiles, job posting environmental headers. Hours-to-days.
- **Tier 2 (mid-tier)**: Career site heroes, EVP pillar systems. 4-12 weeks.

## Related

- [Add-on README](../../README.md)
- [Prompts master library](../README.md)
- [Sub-register C specification](../../reference/sub-register-c-agency.md)
- [Candidate imagery decision tree](../../workflows/candidate-imagery-decision-tree.md)
- [Three production tiers](../../workflows/three-production-tiers.md)
