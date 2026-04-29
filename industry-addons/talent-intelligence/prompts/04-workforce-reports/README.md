# Workforce Reports — Prompts (Mixed Sub-Registers)

Four prompts for workforce trend reports, salary guides, DEI reports, and conference materials. This category spans sub-registers — the choice between A (retained-search editorial) and C (recruiting-agency editorial-illustration hybrid) depends on audience.

## Prompts In This Directory

| # | Prompt | Default Register | Models | Tier | Compliance Stakes |
| :- | :--- | :-: | :--- | :-: | :-: |
| 13 | [Workforce Trends Cover](./13-workforce-trends-cover.md) | A or C | Ideogram + MJ composite | 3 | Moderate |
| 14 | [Salary Guide Cover](./14-salary-guide-cover.md) | C | Ideogram + MJ composite | 2 | Moderate |
| 15 | [DEI Report Cover](./15-dei-report-cover.md) | A or C | MJ v7 + Ideogram | 3 | **Highest** |
| 16 | [Conference Keynote Backdrop](./16-conference-keynote-backdrop.md) | B | MJ v7 + Ideogram | 2 | Moderate |

## Register Selection For This Category

- **Sub-register A (retained-search editorial)** — when the report's primary audience is board-level, institutional investors, or the executive search context (Korn Ferry *Workforce 2025*, Spencer Stuart leadership research, Heidrick *Route to the Top*, McKinsey/Bain/BCG workforce research aimed at boards).
- **Sub-register C (agency editorial)** — when the report's primary audience is recruiting marketing, candidate-facing, or general-business context (LinkedIn *Global Talent Trends*, Robert Half *Salary Guide*, Mercer *Global Talent Trends*, Deloitte *Global Human Capital Trends* in marketing context).
- **Sub-register B (platform dashboard)** — for conference keynote backdrops in the HR Tech / talent intelligence / vendor-marketing context (UNLEASH, HR Tech Conference, Transform).

## Three Aesthetic Camps Within The Category

Workforce report covers cluster into three aesthetic camps (per the research synthesis in [`../../docs/02-deliverable-types.md`](../../docs/02-deliverable-types.md)):

1. **Photography-led** — McKinsey grayscale-blue-purple-shimmer LUT, Deloitte named-designer credits, Mercer persona cards, Adecco worker cinematography, Korn Ferry editorial portraits, Robert Half squircle masks. Real workers as cover hero.
2. **Illustration-led** — Randstad touch-illustration, LinkedIn flat vector people-and-work scenes, Bain modest editorial illustration. Commissioned art replaces stock photography.
3. **Abstract-data-art-led** — WEF austere Insight Report template, BCG slope-graph rank charts, Lightcast interactive Tableau-public dashboards as the deliverable, PwC fluid orange-burgundy-pink blob covers. The chart itself becomes the cover.

The prompts in this directory primarily target camps 2 and 3 (illustration-led and abstract-data-art-led) because camp 1 (photography-led) requires real photography that AI generation should not substitute for in archival contexts. Where camp-1 register is required, real photography is the production path; AI is used for composite layout work in Ideogram / Photoshop.

## Customization Fields Across This Category

| Field | Example | Notes |
| :--- | :--- | :--- |
| `[REPORT TITLE]` | "Workforce 2026" / "Future of Jobs 2026" | Display title |
| `[REPORT SUBTITLE]` | "The Skills Pivot" / "Beyond the Plateau" | Editorial subtitle |
| `[YEAR]` | "2026" | Year as typographic anchor |
| `[ISSUER]` | "Korn Ferry" / "Lightcast" / "Deloitte" / "Mercer" | Publishing organization |
| `[EDITION]` | "10th Annual" / "Vol. III" | Edition signifier |
| `[BRAND ACCENT]` | Brand single accent color | |
| `[REPORT THEME]` | "skills" / "compensation" / "DEI" / "leadership" | Drives metaphor selection |

## Compliance Posture Across This Category

- **Workforce reports are typically archival publications** with strict provenance and licensing requirements. Tier 3 production posture applies (per [`../../workflows/three-production-tiers.md`](../../workflows/three-production-tiers.md)).
- **Most workforce reports prohibit AI imagery on the cover.** Provenance and licensing certainty trumps AI generation speed. Where AI is used, it is for the abstract / data-art register only, not for human subjects.
- **DEI reports carry the highest stakes.** Synthetic-diversity is the central failure mode. The Levi's × Lalaland (2023), Mango Teen, Coca-Cola, Google Gemini reference cases all sit in this category. Architectural restraint, named-employee storytelling, or data-led abstract are the permitted paths. See [`15-dei-report-cover.md`](./15-dei-report-cover.md).
- **Conference keynote backdrops** carry recognition-badge and IP-licensing obligations.

## Workflow Tier Guidance

| Prompt | Production Tier | Typical Timeline |
| :--- | :-: | :--- |
| 13 — Workforce Trends Cover | 3 | 6-24 weeks |
| 14 — Salary Guide Cover | 2-3 | 4-12 weeks |
| 15 — DEI Report Cover | 3 | 6-24 weeks |
| 16 — Conference Keynote Backdrop | 2 | 4-12 weeks |

## Related

- [Add-on README](../../README.md)
- [Prompts master library](../README.md)
- [Three sub-registers](../../docs/01-three-sub-registers.md)
- [Deliverable types](../../docs/02-deliverable-types.md)
- [Three production tiers](../../workflows/three-production-tiers.md)
