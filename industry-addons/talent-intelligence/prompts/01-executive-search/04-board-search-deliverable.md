# 04 · Board Search Deliverable

A board-grade publication summarizing director searches, board composition trends, or board-search deliverables. Spencer Stuart's annual *US Board Index* is the canonical reference.

| Field | Value |
| :--- | :--- |
| **Use case** | Board-grade annual report, board search deliverable, director-composition study, board-effectiveness publication. |
| **Sub-register** | A — Retained-search editorial (with maximum board-grade restraint) |
| **Recommended model** | Midjourney v7 (abstract data motif base) + Ideogram v3 (typographic). Workflow Recipe C. |
| **Aspect ratio** | 8.5×11" portrait or A4 portrait. |
| **Production tier** | 3 — Archival |
| **Compliance posture** | Highest-stakes archival category. AI imagery on the cover requires explicit firm-policy authorization. Default posture: real photography or abstract/typographic-only. |

## ⚠️ Board-Grade Restraint Notice

Board-grade publications carry the strictest provenance and licensing standards in the industry. **Default posture: avoid AI imagery on the cover unless the firm's policy explicitly permits it.** Real photography of named directors requires individual consent. The prompt below produces an abstract data motif suitable for board-grade contexts where AI generation is permitted; the typographic-only variant (Variant D) is the safest fallback.

## Prompt — Midjourney v7 (abstract data motif)

```text
Editorial cover artwork for a board governance annual report. An abstract topographic
engraving on warm-ivory ground: overlapping contour lines in deep navy ink, each line
representing a percentage value in board composition data, the lines clustering around
key thresholds (30%, 40%, 50%) marked by faint signal-red horizontal rules. The
composition reads as a serious data document, not a decorative pattern. Subtle paper-grain
texture, warm cast in highlights, slightly desaturated. Generous negative space in the
upper third for typographic overlay. Spencer Stuart Board Index editorial register applied
to BHIL parent palette. [BHIL profile] --ar 17:22 --style raw --stylize 150 --v 7
```

### Parameters

| Parameter | Value | Rationale |
| :--- | :--- | :--- |
| `--ar` | 17:22 | US Letter portrait |
| `--style raw` | raw | Editorial restraint |
| `--stylize` | 150 | Lower for documentary register |
| `--v` | 7 | Latest Midjourney |

## Prompt — Ideogram v3 (typographic overlay)

```text
Board-grade editorial cover layout. Top-left: small-caps tracked label "[CLIENT FIRM]"
wordmark in deep navy at 9pt. Top-right: small-caps "[REPORT TITLE]" in deep navy at
9pt. Center upper-third: editorial display title — a year as typographic anchor —
"[YEAR]" in heavy serif (Canela Deck or GT Sectra Bold) at 144pt deep navy. Below year:
report subtitle "[REPORT SUBTITLE]" in regular serif italic, deep navy, 24pt.
Lower-third: a single oversize stat plate — a 200pt+ percentage in signal-red, followed
by 2-3 lines of 16pt interpretive text in deep navy, with a hairline rule above and
below. Footer center: "[REPORT EDITION] · [PUBLICATION DATE]" in 8pt regular. Layout
follows Spencer Stuart US Board Index convention applied to BHIL register.
```

## Customization Fields

| Field | Example | Notes |
| :--- | :--- | :--- |
| `[CLIENT FIRM]` | "Spencer Stuart" or your firm | Top-left wordmark |
| `[REPORT TITLE]` | "US BOARD INDEX" | Tracked small caps top-right |
| `[YEAR]` | "2026" | The typographic anchor of the cover |
| `[REPORT SUBTITLE]` | "The 41st Annual Survey of Director Trends" | Below the year |
| `[REPORT EDITION]` | "41st Edition" | Footer |
| `[PUBLICATION DATE]` | "October 2026" | Footer |
| Stat plate | "47%" + 2-line interpretive text | Lower third anchor |

## Variants

### Variant A — Abstract data motif (canonical)

The default. Topographic-engraving register that reads as a serious data document. Use for board-grade publications where AI generation is permitted.

### Variant B — Architectural restraint

For maximum-restraint contexts, an architectural exterior with no people.

```text
Editorial photograph: a modernist corporate building exterior in early-morning light, low
angle, warm walnut and limestone facade against deep navy sky. No people, generous
negative space in the upper third for typographic overlay. Documentary photography
register, slight grain. [BHIL profile] --ar 17:22 --style raw --stylize 150 --v 7
```

### Variant C — Boardroom interior detail

For board-effectiveness reports where the boardroom itself is metaphorically appropriate.

```text
Editorial photograph: a boardroom detail — empty leather chair at the head of a polished
walnut table, soft natural light from upper-left, no people, restrained composition.
Documentary photography register. [BHIL profile] --ar 17:22 --style raw --stylize 150 --v 7
```

### Variant D — Typographic-only (safest fallback)

For maximum-conservative board-grade contexts where any AI imagery is restricted.

```text
Pure deep-navy ground. No imagery. Cover is typographic only:
- [CLIENT FIRM] wordmark top-left in warm ivory, 9pt small caps.
- [REPORT TITLE] top-right in warm ivory, 9pt small caps.
- [YEAR] center, 144pt heavy serif, warm ivory.
- [REPORT SUBTITLE] below year, 24pt italic serif, warm ivory.
- Stat plate lower-third: percentage in signal-red 200pt, interpretive text in warm
  ivory 16pt, hairline rules above and below.
- Footer center: [REPORT EDITION] · [PUBLICATION DATE] in 8pt regular.
```

## Failure Modes

| Failure | Symptom | Mitigation |
| :--- | :--- | :--- |
| **Decorative-pattern register** | Generated abstract motif looks like a wallpaper pattern, not a data document | Use anchor language "abstract topographic engraving" + "lines representing percentage values" + "the composition reads as a serious data document" |
| **Color over-saturated** | Output reads as marketing collateral | Specify "warm-ivory ground", "deep navy ink", "slightly desaturated" |
| **Stat plate proportions wrong** | Percentage too small relative to interpretive text | Stat numeral must be 200pt+; interpretive text 14-18pt; 10:1 size ratio approximately |
| **Year-anchor competes with stat plate** | Two large numerals on the cover read as confused | Year is the upper anchor (144pt); stat plate is the lower anchor (200pt+); they must be visually separated by 1/3 page minimum |
| **Off-register typography** | Sans-serif display reads as off-register | Use heavy serif (Canela Deck, GT Sectra Bold, or KF Serif equivalent) |

## Compliance Notes

- **Board-grade strictest standards.** Provenance and licensing certainty required. Default posture: real photography (with consent for any depicted directors) or abstract/typographic-only.
- **AI imagery permitted only with firm-policy authorization.** Where the firm's AI imagery policy explicitly permits AI-generated covers (typically for abstract motifs, not portraits), the prompts above apply. Where the firm's policy restricts AI imagery on archival publications, use Variant D (typographic-only).
- **C2PA Content Credentials** applied at generation; composite assets carry C2PA from source layers; final published asset signed at publication.
- **Visible AI disclosure** on the colophon page when AI imagery is used. Disclosure language: *"Cover artwork generated with AI. Director photographs and biographies depict real individuals with their consent."*
- **No real-director likeness in AI generation.** Director photographs are real photography only.
- **Five-year recordkeeping minimum;** longer for board-grade publications per typical OFCCP and similar archival requirements.

## Related

- [01-executive-search README](./README.md)
- [Sub-register A specification](../../reference/sub-register-a-retained-search.md)
- [Spencer Stuart 2025 US Board Index exemplar](../../reference/exemplar-library.md)
- [AI imagery policy](../../compliance/ai-imagery-policy.md)
- [Disclosure standards](../../compliance/disclosure-standards.md)
- [Workflow Recipe C (Parent)](../../../../workflows/recipe-c-text-typography-composite.md)
