# 01 · Candidate Dossier Cover

The cover plate for a long-form candidate dossier prepared by a retained-search firm for a client search committee. Always anonymized at the cover; the candidate's identity is revealed inside, not on the cover.

| Field | Value |
| :--- | :--- |
| **Use case** | Cover of a confidential candidate dossier (longlist, slate, or final recommendations) for a client search committee. |
| **Sub-register** | A — Retained-search editorial |
| **Recommended model** | Midjourney v7 (architectural metaphor base) + Ideogram v3 (typographic overlay). Workflow Recipe C. |
| **Aspect ratio** | 8.5×11" portrait (US Letter) or A4 portrait. `--ar 17:22` for Midjourney US Letter equivalent. |
| **Production tier** | 3 — Archival |
| **Compliance posture** | No real-person likeness on cover. Anonymization conventions enforced. C2PA Content Credentials applied. Visible disclosure on colophon. |

## Prompt — Midjourney v7 (architectural metaphor base)

```text
Editorial cover photograph for a confidential executive search dossier. A solitary mountain
ridge at first light, wreathed in low cloud, the summit lit warm against deep navy sky.
Restrained composition, generous negative space in the upper third for typographic overlay.
Documentary-photography register, slight grain, slightly desaturated palette, warm cast in
highlights, cool cast in shadows. No people, no buildings beyond a distant horizon line.
Foreign Affairs editorial photography register. [BHIL profile] --ar 17:22 --style raw
--stylize 200 --v 7
```

### Parameters

| Parameter | Value | Rationale |
| :--- | :--- | :--- |
| `--ar` | 17:22 | Approximates 8.5×11" US Letter portrait |
| `--style raw` | raw | Reduces Midjourney's default illustrative tendency; produces documentary register |
| `--stylize` | 200 | Mid-low; preserves the editorial restraint |
| `--v` | 7 | Latest Midjourney model with strongest documentary register |

## Prompt — Ideogram v3 (typographic overlay)

After generating the architectural base in Midjourney, composite the typographic overlay in Ideogram or a design tool:

```text
Editorial cover layout. Top-left: small-caps tracked label "[PRACTICE AREA] PRACTICE" in
warm ivory at 9pt. Center upper-third: editorial display title "[PROJECT CODENAME]" in
heavy serif (Canela Deck or GT Sectra Bold register), warm ivory, 72-84pt. Below title:
"Slate of Candidates · [SEARCH SLATE NUMBER]" in regular serif italic, warm ivory, 16pt.
Lower-right: "[CLIENT FIRM]" wordmark small. Lower-left: diagonal stamp "STRICTLY
CONFIDENTIAL" in signal-red, 18pt, rotated -15°, with hairline rule above and below.
Footer center: "[YEAR] · [DOSSIER VERSION]" in 9pt regular. Subtle paper-grain texture
overlay at 8% opacity simulating uncoated archival stock. Layout follows Foreign Affairs
× Palantir field brief register.
```

## Customization Fields

| Field | Example | Notes |
| :--- | :--- | :--- |
| `[CLIENT FIRM]` | "Spencer Stuart" or your firm name | Lower-right wordmark only |
| `[CLIENT CODE NAME]` | Not on cover (revealed inside) | Cover anonymizes the client |
| `[PROJECT CODENAME]` | "Project Aurora" | Display title; project-specific |
| `[SEARCH SLATE NUMBER]` | "Slate III" or "Longlist" or "Final Recommendations" | Slate stage |
| `[PRACTICE AREA]` | "CEO & BOARD OF DIRECTORS" | Small-caps top-left label |
| `[YEAR]` | "2026" | Publication year |
| `[DOSSIER VERSION]` | "v3.0" | Internal version tracking |

## Variants

### Variant A — Mountain summit (canonical)

The canonical Heidrick *Route to the Top* metaphor. Use for CEO and board-level searches.

```text
A solitary mountain ridge at first light, wreathed in low cloud, the summit lit warm against
deep navy sky.
```

### Variant B — Architectural building

For corporate-development, financial-services, or institutional searches.

```text
A modernist corporate building exterior at dawn, low-angle, the facade lit warm against
indigo sky. Restrained, no people in frame, generous negative space above for typographic
overlay.
```

### Variant C — Abstract data motif

For workforce-research-led dossiers or industry-mapping covers.

```text
A minimal abstract motif: a topographic engraving of overlapping contour lines in warm
ivory on deep navy ground, intersected by a single signal-red horizontal rule. Editorial,
restrained, generous negative space for typographic overlay.
```

### Variant D — No-image typographic-only fallback

For maximum-confidentiality contexts where any imagery might leak project context.

```text
Pure deep-navy ground. No imagery. Cover is typographic only with the title, slate
identifier, confidential stamp, and footer.
```

## Failure Modes

| Failure | Symptom | Mitigation |
| :--- | :--- | :--- |
| **Stock-photo register** | Generated imagery looks like generic Getty/iStock landscape | Use `--style raw` and "Foreign Affairs editorial photography register" anchor language |
| **Over-illustrated** | Output looks painted or illustrated | Lower `--stylize` (try 100-150); add "documentary photography" anchor |
| **People in frame** | Distant figures appear despite no-people instruction | Add explicit "no human figures, no silhouettes, no people" negative prompts |
| **Color over-saturated** | Output looks like a stock travel photo | Add "slightly desaturated palette" and "warm cast in highlights, cool cast in shadows" |
| **Confidentiality stamp wrong** | Stamp reads as decorative element | Stamp must be diagonal at -15°, in signal-red, with hairline rules above and below; this is non-decorative |

## Compliance Notes

- **No real-person likeness.** Cover does not depict any person, real or fabricated. Compliance with [`../../compliance/consent-and-likeness.md`](../../compliance/consent-and-likeness.md) automatic.
- **C2PA Content Credentials.** Applied to the AI-generated base layer at generation time. Composite asset carries C2PA from the base layer through compositing.
- **Visible disclosure.** Even though the cover carries no people, the disclosure language *"Cover imagery is illustrative and AI-generated. Candidate biographies and photographs depict real individuals with their consent."* is applied on the dossier's confidentiality notice page.
- **Confidentiality conventions.** "STRICTLY CONFIDENTIAL" stamp is real, not decorative. Project codename is real and project-specific. Client identification is reserved for the dossier interior.
- **Five-year recordkeeping.** Prompt, model version, generation date, reviewer identity, and representation test results archived per [`../../compliance/ai-imagery-policy.md`](../../compliance/ai-imagery-policy.md) Section 9.

## Related

- [01-executive-search README](./README.md)
- [Sub-register A specification](../../reference/sub-register-a-retained-search.md)
- [Heidrick *Route to the Top 2025* exemplar](../../reference/exemplar-library.md)
- [Candidate Dossier Spec Template](../../templates/candidate-dossier-template.md)
- [AI Disclosure Statement Template](../../templates/ai-disclosure-statement-template.md)
- [Workflow Recipe C (Parent)](../../../../workflows/recipe-c-text-typography-composite.md)
- [Three Production Tiers](../../workflows/three-production-tiers.md)
