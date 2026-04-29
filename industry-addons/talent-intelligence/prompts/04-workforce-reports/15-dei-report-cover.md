# 15 · DEI Report Cover

The annual DEI / belonging / equity report cover for an enterprise or institution. **The highest-compliance-stakes deliverable in this add-on.** The post-2024 register has shifted decisively away from "diversity grid" imagery; this prompt encodes that shift.

| Field | Value |
| :--- | :--- |
| **Use case** | Cover plate for annual DEI / belonging / equity report (board audience or candidate-facing) |
| **Sub-register** | A — Retained-search editorial (board / institutional audience) or C — Agency editorial (candidate-facing) |
| **Recommended model** | Midjourney v7 (architectural restraint) + Ideogram v3 (typographic). Workflow Recipe C. |
| **Aspect ratio** | A4 portrait or 8.5×11" Letter portrait |
| **Production tier** | 3 — Archival |
| **Compliance posture** | **HIGHEST STAKES.** Synthetic-diversity is the central failure mode. Architectural restraint, named-employee storytelling, or data-led abstract are the permitted paths. AI-generated demographically-varied employees are prohibited. C2PA Content Credentials applied. Visible disclosure on cover or colophon. |

## The Three Permitted Paths

This prompt encodes the three paths that have emerged as defensible-by-default for DEI report covers in the post-2024 environment:

### Path 1 — Architectural Restraint (SOM 2024 Model)

Abstract corporate-architecture photography with no faces. The 2024 SOM DEI Report is the cleanest exemplar — a building's interior structure rendered as the cover, with the report's narrative carried through internal spreads rather than relying on the cover to depict diversity. Sidesteps the synthetic-diversity problem by not depicting people on the cover at all.

### Path 2 — Named-Employee Storytelling

A single real, named, consented employee in a real workplace context. Patagonia's Indigenous land-stewards approach (showing real Indigenous employees as land stewards in their actual context, with full caption attribution and career narrative inside) is the template. Authenticity comes from depth — one employee with full story rather than six employees as faces in a grid.

### Path 3 — Data-Led Abstract

The chart or data point becomes the cover. WEF Insight Report register applied to DEI metrics. The cover communicates the report's core finding visually, with the narrative carried through interior spreads. GitLab Handbook public diversity stats register.

## The Prohibited Path — Synthetic Diversity Grid

AI-generated demographically-varied employees who don't actually exist. **The Levi's × Lalaland (2023), Mango Teen (2024), Coca-Cola (2024-2025), and Google Gemini (2024) reference cases all sit here.** This path is prohibited per [`../../compliance/ai-imagery-policy.md`](../../compliance/ai-imagery-policy.md) Section 4.2.

## Prompt — Path 1 — Architectural Restraint (Midjourney v7)

```text
Editorial cover photograph for a DEI report. A modernist corporate building interior,
mid-day, generous natural daylight from floor-to-ceiling windows, the architectural
structure (columns, exposed beams, an atrium) rendered as the cover subject. No people
visible, no figures, no implied human presence. Restrained palette of warm ivory and
deep navy with [BRAND ACCENT] subtle accent in a single architectural detail. Slight
grain, slightly desaturated, documentary architectural photography register reminiscent
of Hedrich Blessing or Iwan Baan. Generous negative space in the upper-third for
typographic title overlay. Foreign Affairs editorial cover register. [BHIL profile]
--ar 17:22 --style raw --stylize 200 --v 7
```

## Prompt — Path 3 — Data-Led Abstract (Ideogram v3)

```text
Editorial DEI report cover, A4 portrait. Full-bleed warm ivory background with subtle
paper-grain texture overlay. Center-upper-third: editorial display title "[REPORT TITLE]"
in heavy serif (Canela Deck register), warm navy, 72-84pt. Below title: subtitle
"[REPORT SUBTITLE]" in regular weight serif italic, 24pt warm navy. Lower-half:
single large data visualization rendered minimally — for example, a slope-graph
showing two metrics over time, with very thin lines, all type label values in 14pt
regular sans, the data point representing the report's headline finding circled
discretely with hairline ring. Year "[YEAR]" in serif display 120pt at lower-right
corner at 30% opacity. Issuer wordmark "[ISSUER]" small at top-left in 11pt warm navy.
WEF Insight Report register applied to DEI data.
```

Path 2 (named-employee storytelling) requires real photography of a named, consented employee, composited via Workflow Recipe C with the typographic overlay generated separately. The Ideogram prompt for Path 2's typographic layer:

```text
Editorial DEI report cover layout, A4 portrait. Full-bleed [the real employee photograph
provides the background]. Top-left: issuer wordmark "[ISSUER]" small in 11pt warm ivory
on the photograph. Lower-third: editorial display title "[REPORT TITLE]" in heavy serif,
warm ivory, 72-84pt over a subtle dark gradient at the bottom for legibility. Below
title: subtitle and year. Below subtitle: a single line attribution: "[EMPLOYEE NAME] ·
[ROLE TITLE] · [LOCATION]" in regular weight italic 14pt warm ivory. Subtle paper-grain
texture overlay at 8% opacity.
```

## Customization Fields

| Field | Example | Notes |
| :--- | :--- | :--- |
| `[REPORT TITLE]` | "Belonging" / "Equity in Practice" / "Our Promise. For All." | Report's title |
| `[REPORT SUBTITLE]` | "[YEAR] Annual Report" or theme subtitle | Editorial subtitle |
| `[YEAR]` | "2026" | Report year |
| `[ISSUER]` | Your organization | Publishing organization |
| `[BRAND ACCENT]` | Issuer's brand single accent | Subtle accent only on Path 1 |
| `[EMPLOYEE NAME]` | "Sarah Park" (Path 2 only) | Real, named, consented employee |
| `[ROLE TITLE]` | Real role | Path 2 only |
| `[LOCATION]` | Real location | Path 2 only |

## Variants

### Variant A — Path 1 architectural (board-grade audience)

The default for board / institutional audiences. Minimum risk; sidesteps synthetic-diversity entirely.

### Variant B — Path 2 named-employee (candidate-facing audience)

For DEI reports primarily reaching candidates. Single named employee, full consent, full caption attribution. The Patagonia / GitLab register.

### Variant C — Path 3 data-led abstract (data-first audience)

For DEI reports where the headline data point is itself the most compelling visual statement (e.g., a milestone metric, a year-over-year shift). WEF / Lightcast register.

### Variant D — Hybrid Path 1 + 3

For maximally restrained covers — architectural background with a single overlaid headline data point. Suitable for institutional investor audiences who want both the "this is serious" register and the "here is the headline finding" data signal.

## Compliance Notes — In Detail

This is the highest-stakes prompt in the add-on. Compliance obligations apply with maximum stringency:

1. **No synthetic diversity.** AI-generated demographically-varied employees who don't actually exist are prohibited per [`../../compliance/ai-imagery-policy.md`](../../compliance/ai-imagery-policy.md) Section 4.2. Levi's × Lalaland, Mango Teen, Coca-Cola, Google Gemini reference cases inform this prohibition.

2. **Representation testing applies even to architectural and data-led covers.** Per [`../../compliance/representation-testing.md`](../../compliance/representation-testing.md), where architectural backgrounds incidentally include people (e.g., a distant figure), full representation testing applies. Path 1 should produce no people in frame.

3. **Path 2 — full consent process.** Named-employee storytelling requires the most stringent consent process per [`../../compliance/consent-and-likeness.md`](../../compliance/consent-and-likeness.md): written model release, defined scope (DEI report use is distinct from career-site use; both may be needed), withdrawal rights, GDPR/CCPA-aligned processing, re-confirmation upon employment status change.

4. **Visible AI disclosure** on the cover itself or on the colophon page:

   > *"Cover imagery generated with AI [Path 1] / Cover features [EMPLOYEE NAME] with their consent [Path 2] / Cover data visualization derived from this report [Path 3]. The named individuals featured throughout this report participate with full consent."*

5. **C2PA Content Credentials** applied to the cover asset.

6. **Anti-discrimination law applies to imagery.** EEOC Compliance Manual Section 15 treats imagery as part of recruiting practices. Disparate-impact analysis applies. Imagery that systematically excludes protected groups can produce liability regardless of intent. *Mobley v. Workday* (N.D. Cal., conditional ADEA certification May 2025) is the active enforcement context.

7. **Five-year recordkeeping** of prompts, model versions, reference images, reviewer identity, representation test results, and consent documentation.

## Failure Modes

| Failure Mode | What Happens | Mitigation |
| :--- | :--- | :--- |
| **Synthetic-diversity grid** | AI-generated demographically-varied employees who don't exist | Path 1, 2, or 3 only — prompts explicitly avoid the synthetic-diversity register |
| **Tokenism in Path 2** | Single employee positioned as the "diversity" representative for the whole organization | Path 2 narrative depth — the report's full content treats the employee as a real person with real story, not as a representational placeholder |
| **Over-correction (Google Gemini failure)** | AI-generated demographically inaccurate composition | Representation testing Test 1 + Test 2; reviewer rejection of any output that doesn't match comparison populations |
| **Disclosure missing or buried** | Asset published without visible AI disclosure | Disclosure on cover or first interior spread; not buried in colophon micro-type |
| **Consent gap on Path 2** | Real employee imagery used without DEI-report-specific consent | DEI report use distinct from career-site use; both consent forms required |
| **Departed employee in Path 2** | Featured employee leaves; report still in market | Re-confirmation triggers; operational removal process |

## Related

- [Prompts category README](./README.md)
- [Workforce trends cover (related register)](./13-workforce-trends-cover.md)
- [Sub-register A specification](../../reference/sub-register-a-retained-search.md)
- [AI imagery policy (Section 4.2)](../../compliance/ai-imagery-policy.md)
- [Representation testing](../../compliance/representation-testing.md)
- [Consent and likeness](../../compliance/consent-and-likeness.md)
- [Disclosure standards](../../compliance/disclosure-standards.md)
- [Candidate imagery problem](../../docs/03-candidate-imagery-problem.md)
