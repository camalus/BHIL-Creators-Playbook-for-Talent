# 02 — Talent Intelligence Platform

Four production-grade prompts for talent intelligence platform marketing and product imagery. Sub-register B throughout. Prompts in this category use a separate `[PLATFORM PROFILE]` and `[PLATFORM SREFS]` set declared per project.

## Prompts

| # | Prompt | Use Case | Recommended Model |
| :- | :--- | :--- | :--- |
| 05 | [Dashboard Hero Plate](./05-dashboard-hero-plate.md) | Hero image on platform marketing site, product page, or sales deck | GPT Image 2 / Flux.2 Pro |
| 06 | [Skills Graph Network](./06-skills-graph-network.md) | Force-directed glowing node graph for skills intelligence | Flux.2 Pro / Recraft V3 |
| 07 | [Talent Flow Sankey](./07-talent-flow-sankey.md) | Width-weighted ribbon visualization of talent migration | GPT Image 2 / Flux.2 Pro |
| 08 | [Vendor Pitch Deck Hero](./08-vendor-pitch-deck-hero.md) | Hero image for HR Tech vendor pitch deck with recognition badges | GPT Image 2 + Ideogram |

## Sub-Register Anchor

All four prompts target sub-register B — talent-intelligence platform dashboard. See [`../../reference/sub-register-b-platform.md`](../../reference/sub-register-b-platform.md) for the full visual specification.

Anchor exemplars:

- Eightfold AI "Infinite Workforce" hero
- Gloat homepage + Loomra Knowledge Graph
- Lightcast 2025 brand 2.0
- Beamery Digital Twin
- Draup AI-Ready Maturity Model
- TalentNeuron Workforce Insights

## Platform Profile Declaration

Sub-register B requires a per-project palette declaration. Each prompt carries placeholders for:

- `[PLATFORM PROFILE]` — text declaration of palette, typography, accent treatment.
- `[PLATFORM SREFS]` — Midjourney sref slots when MJ is used.

A typical declaration:

```text
PLATFORM PROFILE: Eightfold-style — primary deep-purple #2D1B69 to #0A0518 gradient,
accent aqua #00D4FF and orange #FF6B35 light streaks, body type Inter or Eightfold custom,
display type geometric sans bold.
```

Lock the declaration at the project level in [`../../templates/employer-brand-spec-template.md`](../../templates/employer-brand-spec-template.md) (which serves platform marketing as well as employer brand).

## Compliance Posture

This category produces high-volume marketing imagery with these compliance considerations:

- **No photo-realistic AI agent avatars.** AI agent UI elements use stylized geometric, abstract, or illustrated avatars. Photo-realistic AI-generated faces in this slot trigger the candidate-imagery problem.
- **Synthetic data must be obviously sample/illustrative.** Dashboard data is decorative; do not use real candidate or employee data without consent.
- **Recognition badges require licensing.** Fosway 9-Grid, IDC MarketScape, Brandon Hall, etc. require entitlement; using these badges without licensing is a trademark exposure.
- **Source attribution.** When the imagery uses third-party data (LinkedIn Talent Insights, Lightcast, Revelio Labs), attribution per the data provider's licensing terms.
- **C2PA Content Credentials** applied at generation; composite assets carry C2PA from source layers.

## Production Tier

Most deliverables in this category are Tier 2 (mid-tier, 4-12 weeks). Conference keynote backdrops can run shorter when the platform is iterating quickly. See [`../../workflows/three-production-tiers.md`](../../workflows/three-production-tiers.md).

## Related

- [Prompts master library](../README.md)
- [Sub-register B specification](../../reference/sub-register-b-platform.md)
- [Exemplar library](../../reference/exemplar-library.md)
- [Employer brand spec template](../../templates/employer-brand-spec-template.md)
