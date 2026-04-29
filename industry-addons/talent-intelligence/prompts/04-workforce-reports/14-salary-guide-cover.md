# 14 · Salary Guide Cover

The annual or periodic cover of a salary guide / compensation report. Robert Half *Salary Guide* is the canonical commercial reference; Mercer *Total Remuneration Survey* is the institutional reference.

| Field | Value |
| :--- | :--- |
| **Use case** | Cover plate for annual salary guide, compensation report, or periodic salary update |
| **Sub-register** | C — Recruiting-agency editorial-illustration hybrid (default) |
| **Recommended model** | Ideogram v3 (typographic) + Midjourney v7 (abstract motif) composite. Workflow Recipe C. |
| **Aspect ratio** | A4 portrait (print) and 1920×1080 landscape (interactive web variant) |
| **Production tier** | 2 — Mid-tier (3 — Archival for institutional reports) |
| **Compliance posture** | Salary guides are typically marketing rather than archival — moderate compliance posture. Abstract motif acceptable; no human subjects on cover. C2PA Content Credentials applied. |

## Format Anatomy

The Robert Half *2026 Salary Guide* and similar compensation reports follow a tight pattern:

- **Year as typographic anchor** — large, often integrated with the cover composition.
- **Display title** — "Salary Guide" or "[YEAR] Salary Guide" in heavy display type.
- **Market-condition subtitle** — a tagline describing the year's compensation environment ("Beyond the Plateau," "The Tightening Market," "Compensation Recalibrated").
- **Brand-color wave or abstract motif** — sub-register C agency editorial register; brand single accent dominant.
- **Issuer wordmark** small.
- **Reach / scope tagline** — "United States · Canada" or "Global" or industry-specific reach.

## Prompt — Midjourney v7 (Abstract Wave / Motif)

For the brand-color wave or abstract motif background:

```text
Editorial cover background, abstract wave or undulation motif representing compensation
movement and market dynamics. A flowing horizontal banded gradient in [BRAND ACCENT]
saturating to deeper [BRAND ACCENT] at the bottom edge, with subtle vertical striations
suggesting income bands or cohort divisions. The composition has generous negative space
in the upper-third for typographic title overlay. No people, no figures, no buildings.
Restrained, editorial, slightly desaturated, slight grain. Sub-register C agency
editorial register, Robert Half cover register. [BHIL profile or BRAND PROFILE] --ar
17:22 --style raw --stylize 200 --v 7
```

## Prompt — Ideogram v3 (Typographic Composite)

For the typographic overlay layered onto the abstract base:

```text
Editorial salary guide cover layout, A4 portrait. Top-left: small-caps issuer wordmark
"[ISSUER]" in 11pt warm ivory. Below wordmark: "[REACH SCOPE]" in tracked small caps,
9pt warm ivory. Center upper-third: editorial display title "Salary Guide" in heavy
serif or humanist sans display, 80-96pt warm ivory. Above title or as a separate row:
the year "[YEAR]" in serif display 144pt warm ivory at 60% opacity, integrated as
typographic anchor. Below title: market-condition subtitle "[REPORT SUBTITLE]" in
regular weight italic, 22pt warm ivory. Footer: edition signifier and ISBN in 9pt
regular. Subtle paper-grain texture overlay at 8% opacity.
```

## Customization Fields

| Field | Example | Notes |
| :--- | :--- | :--- |
| `[YEAR]` | "2026" | Year as typographic anchor |
| `[ISSUER]` | "Robert Half" / "Mercer" / "Adecco" / your firm | Publishing organization |
| `[REACH SCOPE]` | "UNITED STATES · CANADA" / "GLOBAL" / "TECHNOLOGY SECTOR" | Geographic or industry scope |
| `[REPORT SUBTITLE]` | "Beyond the Plateau" / "The Tightening Market" | Market-condition tagline |
| `[BRAND ACCENT]` | Issuer's brand single accent | Drives the wave motif palette |
| `[BRAND PROFILE]` | Issuer's brand profile (palette, typography) | Replaces parent BHIL profile when on client work |

## Variants

### Variant A — Brand-color wave (Robert Half register, canonical)

A flowing horizontal banded gradient in brand color. Robert Half coral / blue is the canonical reference.

### Variant B — Architectural metaphor

For institutional / Mercer-tier compensation reports. Substitute architectural metaphor (a building exterior, a structure detail) for the brand-color wave.

### Variant C — Year-as-anchor typographic only

For maximally restrained covers — typography only, no abstract motif background, the year as the dominant visual element. Spencer Stuart *2025 US Board Index* generalized.

### Variant D — Interactive web variant

Same anatomy resized to 1920×1080 landscape for the interactive web salary guide format. Year and title may shift to upper-left third with negative space allowing for a "search by role" or "filter by market" UI element on the right two-thirds.

## Compliance Notes

1. **No human subjects on AI-generated covers.** The default rule applied — abstract motif only. Where the cover register requires photography of people (the Robert Half career-moment register variant), real photography with consent is used.

2. **Salary data sourcing and methodology** required on a methodology page (typically inside the report, not on the cover). This is independent of AI imagery compliance but is a baseline trust signal for compensation reports.

3. **Visible AI disclosure** on the colophon:

   > *"Cover design generated with AI. Salary data sourced from [METHODOLOGY], collected [PERIOD], [SAMPLE SIZE] respondents."*

4. **C2PA Content Credentials** applied to the cover asset.

5. **Localization.** Salary guides typically have geographic / market variants (US, Canada, UK, Australia, sector-specific). Each variant requires its own localized cover with consistent design system but localized title, subtitle, and reach scope.

## Failure Modes

| Failure Mode | What Happens | Mitigation |
| :--- | :--- | :--- |
| **Year subordinated to title** | Cover reads as undated | Year as typographic anchor, prominent |
| **Brand wave too literal** | Wave reads as decorative wallpaper rather than brand motif | Subtle banding, restrained palette |
| **Subtitle too long** | Layout breaks; reads as descriptive paragraph | Subtitle 3-6 words maximum |
| **Sample size or methodology missing** | Cover signals depth but methodology is buried | Methodology page early in report; cover-relevant scope on cover |
| **Stock-photo human imagery in marketing variant** | Cover signals iStock register | If photography is required, real photography with consent |

## Related

- [Prompts category README](./README.md)
- [Sub-register C specification](../../reference/sub-register-c-agency.md)
- [Workforce trends cover (related register)](./13-workforce-trends-cover.md)
- [Three production tiers](../../workflows/three-production-tiers.md)
- [Parent: Workflow Recipe C](../../../../workflows/README.md)
