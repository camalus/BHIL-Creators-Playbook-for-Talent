# 10 · LinkedIn Recruiter Tile

A social tile for LinkedIn recruiter campaigns, sourcing outreach, or InMail attachment.

| Field | Value |
| :--- | :--- |
| **Use case** | LinkedIn recruiter campaign tile, InMail visual attachment, or sourcing outreach social asset |
| **Sub-register** | C — Recruiting-agency editorial-illustration hybrid |
| **Recommended model** | Ideogram v3 (typography-led; the dominant register for this format) |
| **Aspect ratio** | 1200×1200 (square), 1080×1350 (4:5 portrait), or 1200×627 (1.91:1 landscape) |
| **Production tier** | 1 — Fast iteration |
| **Compliance posture** | If a real employee quote is used, that employee's documented consent is required. AI-generated photos of the quoted employee are prohibited. Visible AI disclosure on any AI-generated tile. |

## Format Anatomy

The dominant convention for high-performing LinkedIn recruiter tiles in 2025-2026:

- **Brand-color block** (full-bleed background in the brand single accent).
- **Employee pull-quote** in serif display, prominently centered or left-aligned.
- **Attribution** in regular type: name, role, location, tenure.
- **Small headshot inset** (real employee, with consent) in lower-right corner OR no headshot (typography-only).
- **Brand wordmark** in lower-right or upper-left.

Variants exist for typography-only (no headshot) and headshot-led, but the *quote* is the consistent organizing element.

## Prompt — Ideogram v3 (Typography-Led, No Headshot)

The cleanest variant — typography-only, brand-color block, real employee quote attributed:

```text
Editorial recruitment social tile, 1200×1200 square. Full-bleed background in [BRAND
ACCENT]. Center-left: editorial display pull-quote in serif (Canela Deck or GT Sectra
Bold register), warm ivory, weighted at 48-56pt, 5-7 lines.

Quote: "[QUOTE]"

Below quote, small horizontal hairline rule in warm ivory at 30% opacity. Below rule:
attribution in two lines — line one: name in regular weight serif italic, 18pt; line
two: role and location in 14pt regular sans, "[ROLE TITLE] · [LOCATION] · [TENURE]"
format. Lower-right corner: [CLIENT FIRM] wordmark in warm ivory at 16pt. No other
elements. Restrained, sub-register C agency editorial register, lower-case sentence-case
quote, generous negative space.
```

## Prompt — Ideogram v3 (With Headshot Inset)

When a real-employee headshot is available with consent:

```text
Editorial recruitment social tile, 1200×1200. Full-bleed background in [BRAND ACCENT].
Left two-thirds: editorial display pull-quote in serif, warm ivory, 44-52pt, 5-7 lines.
Right one-third: small circular masked headshot of the quoted employee, 280px diameter,
centered vertically, soft fade-into-background ring at 12% opacity. Below quote: hairline
rule, attribution in two lines as in typography-only variant. Lower-right: [CLIENT FIRM]
wordmark.
```

The headshot is a **separate real photograph** of the quoted employee, with documented consent. It is NOT generated. The Ideogram render produces the tile *layout*; the actual headshot is composited in via a design tool.

## Customization Fields

| Field | Example | Notes |
| :--- | :--- | :--- |
| `[CLIENT FIRM]` | "Atlassian" | Wordmark bottom-right |
| `[BRAND ACCENT]` | "#0052CC" or `#0F69AF` (Randstad blue) | Full-bleed background color |
| `[QUOTE]` | "I came for the engineering. I stayed for the people." | **Real employee quote with consent.** Quote modification requires re-confirmation. |
| `[EMPLOYEE NAME]` | "Sarah Park" | **Real name, with consent.** |
| `[ROLE TITLE]` | "Senior Software Engineer, Platform" | Real title |
| `[LOCATION]` | "Sydney, Australia" | Real location |
| `[TENURE]` | "5 years at [CLIENT FIRM]" | Optional |

## Variants

### Variant A — Typography-only square (1200×1200)

The cleanest format. Use when no headshot is available or when the visual register requires typographic restraint.

### Variant B — With headshot inset (1200×1200)

Variant A plus circular headshot inset. Real employee, real photograph, documented consent.

### Variant C — Portrait (1080×1350)

The 4:5 portrait format dominant on LinkedIn mobile. Same anatomy, vertical layout.

### Variant D — Landscape (1200×627)

The link-preview format. Quote tightened to 3-4 lines, attribution single-line.

## Compliance Notes

1. **Quote attribution requires consent.** A LinkedIn tile featuring a real employee's quote requires that employee's documented consent for use of the quote and (if included) the headshot. The release is per [`../../compliance/consent-and-likeness.md`](../../compliance/consent-and-likeness.md).

2. **Quote modification requires re-confirmation.** If the quote is edited from the original employee testimony, re-confirmation is required.

3. **AI-generated photos of the quoted employee are impermissible.** The headshot in Variant B is a real photograph; AI generation of the quoted employee's likeness is a Tennessee ELVIS Act and right-of-publicity exposure.

4. **AI disclosure** for the layout itself (where Ideogram generates the tile composition):

   > *"Tile design generated with AI. Quote and headshot from named employee with consent."*

   Placement: post copy first line on LinkedIn.

5. **Departed employees.** When a quoted employee leaves the organization, the tile is retired or re-confirmed per [`../../compliance/consent-and-likeness.md`](../../compliance/consent-and-likeness.md) re-confirmation triggers.

## Failure Modes

| Failure Mode | What Happens | Mitigation |
| :--- | :--- | :--- |
| **Quote without consent** | Real-employee quote used without documented release | Confirm consent before any tile production |
| **AI-generated employee quote** | Fabricated quote attributed to real employee | Quote sourcing must trace to real employee testimony |
| **AI-generated headshot of real employee** | Tennessee ELVIS, right of publicity exposure | Real photograph only |
| **Departed employee tile in market** | Tile still running after employee departure | Operational retirement workflow tied to HRIS |
| **Quote modification beyond minor edit** | Quote no longer reflects employee testimony | Re-confirmation triggered for any material edit |

## Related

- [Prompts category README](./README.md)
- [Sub-register C specification](../../reference/sub-register-c-agency.md)
- [Consent and likeness](../../compliance/consent-and-likeness.md)
- [Disclosure standards](../../compliance/disclosure-standards.md)
- [Three production tiers](../../workflows/three-production-tiers.md)
- [Parent: Ideogram prompt patterns](../../../../prompts/README.md)
