# Three Production Tiers

Three production tiers govern the speed-quality tradeoff in talent-industry imagery work. Tier selection is the first operational decision in any project; it cascades into tooling, team composition, AI-use policy, and compliance posture.

## Tier 1 — Fast Iteration

**Timeline:** Hours to a few days.
**Default audience:** LinkedIn recruiter posts, job posting headers, internal recruiting comms, social tiles.
**Default register:** C — Recruiting-agency editorial (with sub-register A or B variants per project).

### Team Composition

- In-house design (typically embedded in the talent acquisition or employer brand team).
- Often a single designer using component libraries.
- Occasional agency support for bursts.

### Tooling

- **Canva Enterprise** — explicit market leader for HR / recruiting last-mile production. FedEx case cited 77% reduction in brand-review times. Designed for non-designer recruiters and recruitment marketers.
- **Figma** — fastest-growing for component-driven careers-site mockups and EVP toolkit assembly.
- **Adobe Express / Photoshop** — for higher-quality variants requiring brand-precise treatment.
- **Notion / Coda** — for asset libraries and content tracking.
- **AI image generators** — heavy use; Adobe Firefly preferred for enterprise commercial-safety; Midjourney v7 for concept hero work; Ideogram for typography-heavy work; Recraft V3 for illustration; GPT Image 2 in-app.

### AI-Use Policy

- **Heavy AI use permitted.** Tier 1's speed-to-publish economy makes AI generation natural for environmental, illustrated, and typographic assets.
- **Default rule still applies.** No photo-real fabricated employees in Tier 1 outputs. Illustrated alternatives, environmental details, or real-employee photographs (where consent is on file).
- **Compliance review compressed.** Reviewer applies a streamlined checklist; full representation testing applies but the reviewer can apply the three tests in the same session as approval.
- **C2PA Content Credentials applied automatically** through the production tools.

### Workflow Pattern

```text
Brief (15-30 min) → Generate (30-60 min) → Compliance review (15-30 min) → Publish.
Total: 1-3 hours typical. Same-day publication common.
```

### Failure Modes

- **Stock-photo register leak.** Tier 1's speed economy can drift toward iStock / Getty register if brand profiles aren't enforced.
- **Compliance shortcut.** Speed pressure can lead to skipped representation testing. The streamlined checklist is the mitigation; not skipping the test.
- **Disclosure missing.** Tier 1 outputs deployed quickly without visible AI disclosure. Operational mitigation: disclosure language as part of the production tool default template.

### Tier 1 Examples From This Add-On

- [`../prompts/03-employer-brand/10-linkedin-recruiter-tile.md`](../prompts/03-employer-brand/10-linkedin-recruiter-tile.md)
- [`../prompts/03-employer-brand/12-job-posting-environmental.md`](../prompts/03-employer-brand/12-job-posting-environmental.md)

## Tier 2 — Mid-Tier

**Timeline:** 4-12 weeks.
**Default audience:** Career-site refresh, employer-brand campaigns, conference materials, EVP launch toolkits, vendor pitch decks, salary guides.
**Default register:** All three sub-registers represented; project declares per project.

### Team Composition

- Agency-led (employer-brand specialists like Symphony Talent, Radancy, exaqueo, Blu Ivy, Universum, Recruitics, Bayard).
- In-house brand stewardship maintains consistency.
- Real photography typically commissioned for hero assets.

### Tooling

- **Adobe Creative Cloud** retains the high-end production standard. Photoshop, Illustrator, InDesign, Premiere.
- **Figma** for component systems, design system maintenance, prototype review.
- **Sketch / Affinity** for variant production.
- **Real photography** commissioned (typically 2-4 weeks lead time).
- **AI image generators** — moderate use for variant generation, ideation, and abstract / environmental components. Real photography retained for hero human subjects.
- **Midjourney v7, Nano Banana Pro, Flux.2 Pro, Ideogram v3, Recraft V3, GPT Image 2** all in active use.
- **DAM (digital asset management)** — Brandfolder, Bynder, Frontify common.

### AI-Use Policy

- **Moderate AI use.** AI generates abstract / environmental / illustrated components and supports ideation and variant generation. Real photography is retained for hero humans.
- **Full default rule application.** No photo-real fabricated employees.
- **Full compliance review.** Representation testing per [`../compliance/representation-testing.md`](../compliance/representation-testing.md). Disclosure per channel matrix in [`../compliance/disclosure-standards.md`](../compliance/disclosure-standards.md). Consent process per [`../compliance/consent-and-likeness.md`](../compliance/consent-and-likeness.md).
- **C2PA Content Credentials applied** with composite-source preservation.

### Workflow Pattern

```text
Brief (1-2 weeks) →
Brand profile and srefs locked (1 week) →
Real photography commissioned and shot (2-4 weeks) →
AI components generated (1-2 weeks parallel) →
Compositing (1-2 weeks) →
Compliance review (1 week) →
Stakeholder review (1-2 weeks) →
Final approval and deployment (1 week).
Total: 8-16 weeks typical, 4-12 weeks for compressed projects.
```

### Failure Modes

- **AI components don't match real photography register.** Mitigation: lock brand profile and srefs early; review AI / real photo composites for register coherence.
- **Consent gaps in real photography.** Real-photo subjects with incomplete consent for the campaign's full scope. Mitigation: consent process initiated at brief stage, before photography.
- **Stakeholder review extends timeline.** Multiple review rounds extend the campaign. Mitigation: stakeholder map at brief stage; review cadence defined.

### Tier 2 Examples From This Add-On

- [`../prompts/02-talent-intelligence-platform/05-dashboard-hero-plate.md`](../prompts/02-talent-intelligence-platform/05-dashboard-hero-plate.md)
- [`../prompts/02-talent-intelligence-platform/08-vendor-pitch-deck-hero.md`](../prompts/02-talent-intelligence-platform/08-vendor-pitch-deck-hero.md)
- [`../prompts/03-employer-brand/09-career-site-hero.md`](../prompts/03-employer-brand/09-career-site-hero.md)
- [`../prompts/03-employer-brand/11-evp-pillar-treatment.md`](../prompts/03-employer-brand/11-evp-pillar-treatment.md)
- [`../prompts/04-workforce-reports/14-salary-guide-cover.md`](../prompts/04-workforce-reports/14-salary-guide-cover.md)
- [`../prompts/04-workforce-reports/16-conference-keynote-backdrop.md`](../prompts/04-workforce-reports/16-conference-keynote-backdrop.md)

## Tier 3 — Archival Quality

**Timeline:** 6-24 weeks.
**Default audience:** Executive search dossiers, board search deliverables, annual workforce reports (Korn Ferry, Mercer, Deloitte tier), annual DEI reports, premium leadership research.
**Default register:** A (retained-search editorial) primarily; some C variants.

### Team Composition

- Specialist agencies (Wolff Olins, Moving Brands, Pentagram, etc., for top-tier projects).
- Senior in-house design (creative director or design lead level).
- Editorial / writing partners (for report content).
- Photographers commissioned at tier-1-photographer level.
- Compliance / legal review at full project scope.

### Tooling

- **Adobe Creative Cloud** at full breadth. InDesign for long-form layout. Photoshop for retouching and compositing.
- **High-quality print production** for printed deliverables (board indexes, annual reports).
- **Real photography** commissioned at high standard (4-12 weeks lead time, including pre-production, shoot, post).
- **AI image generators** — **low or forbidden use** for hero imagery. Provenance and licensing certainty trumps AI generation speed for archival publications.
- **Manuscript / typography systems** — custom typeface licensing, archival paper stocks for printed deliverables.

### AI-Use Policy

- **Low or forbidden AI use.** Most Tier 3 deliverables prohibit AI imagery on the cover and in hero contexts.
- **Where AI is used:** abstract metaphor only (no human subjects), illustrative diagrams and supporting graphics, typographic composite work.
- **AI-generated section dividers and abstract backgrounds** sometimes permitted with policy approval; document in project spec.
- **Full compliance review.** Maximum stringency on representation testing, disclosure, and consent. Five-year recordkeeping minimum (often longer for archival publications).
- **C2PA Content Credentials applied** to every AI-generated component, with compositing-source preservation.

### Workflow Pattern

```text
Discovery and brief (2-4 weeks) →
Editorial direction and sign-off (1-2 weeks) →
Brand profile, typography, and visual system established (2-4 weeks) →
Real photography commissioned and shot (4-12 weeks) →
Long-form layout (4-8 weeks) →
Editorial review and revision rounds (2-4 weeks) →
Compliance review (1-2 weeks) →
Final stakeholder review (2-4 weeks) →
Print production / digital production (2-4 weeks) →
Distribution.
Total: 16-50 weeks typical for major annual publications; 6-24 weeks for compressed projects.
```

### Failure Modes

- **AI imagery published without policy approval.** Tier 3 publications carry archival expectations; AI imagery without explicit approval can damage publication reputation. Mitigation: project spec confirms AI permission per publication.
- **Typography drift.** Long-form layouts span hundreds of pages; typography drift compromises reader confidence. Mitigation: typography system locked early; reviewers check for drift.
- **Compliance documentation gaps.** Tier 3 publications are reviewed multiple years after publication; recordkeeping gaps create future exposure. Mitigation: archive checklist applied at publication.
- **Stakeholder timeline elasticity.** Tier 3 stakeholders include executives and legal; review timelines can extend significantly. Mitigation: timeline buffers in project plan.

### Tier 3 Examples From This Add-On

- [`../prompts/01-executive-search/01-candidate-dossier-cover.md`](../prompts/01-executive-search/01-candidate-dossier-cover.md)
- [`../prompts/01-executive-search/02-executive-bio-plate.md`](../prompts/01-executive-search/02-executive-bio-plate.md)
- [`../prompts/01-executive-search/04-board-search-deliverable.md`](../prompts/01-executive-search/04-board-search-deliverable.md)
- [`../prompts/04-workforce-reports/13-workforce-trends-cover.md`](../prompts/04-workforce-reports/13-workforce-trends-cover.md)
- [`../prompts/04-workforce-reports/15-dei-report-cover.md`](../prompts/04-workforce-reports/15-dei-report-cover.md)

## Cross-Tier Patterns

### Tooling Stack Continuity

Production teams maintain a unified tool stack across tiers, with tier-specific configuration:

- **Adobe Creative Cloud** — used across all three tiers; complexity scales with tier.
- **Figma** — used across Tiers 1 and 2; less common in Tier 3 archival print.
- **Canva Enterprise** — Tier 1 dominant; some Tier 2 use for component libraries.
- **AI generators** — used across all three tiers; intensity scales inversely with tier (heavy in Tier 1, low in Tier 3).
- **DAM** — used across all three tiers; criticality scales with tier (Tier 3 archival depends on it).

### Compliance Continuity

Every tier applies:

- The default rule from [`../docs/03-candidate-imagery-problem.md`](../docs/03-candidate-imagery-problem.md).
- The applicable jurisdictional obligations from [`../compliance/jurisdiction-matrix.md`](../compliance/jurisdiction-matrix.md).
- C2PA Content Credentials per [`../compliance/disclosure-standards.md`](../compliance/disclosure-standards.md).
- Representation testing per [`../compliance/representation-testing.md`](../compliance/representation-testing.md).
- Consent process per [`../compliance/consent-and-likeness.md`](../compliance/consent-and-likeness.md).
- Five-year recordkeeping minimum per [`../compliance/ai-imagery-policy.md`](../compliance/ai-imagery-policy.md) Section 9.

The intensity and depth of each scales with tier; the floor is consistent.

### Tier Migration

Projects sometimes migrate tiers mid-flight:

- **Tier 1 → Tier 2.** A LinkedIn recruiter campaign that gains executive sponsorship and expands to multi-channel typically migrates to Tier 2. Documentation: re-spec the project.
- **Tier 2 → Tier 3.** A career-site refresh that expands to include a flagship annual report typically requires Tier 3 treatment for the report component.
- **Tier 3 → Tier 2.** Less common; usually compressed timelines requiring Tier 2 economics with Tier 3 expectations create quality risk.

## Related

- [Workflows README](./README.md)
- [Candidate imagery decision tree](./candidate-imagery-decision-tree.md)
- [Compliance README](../compliance/README.md)
- [Templates](../templates/README.md)
- [Parent: Workflow Recipes](../../../workflows/README.md)
