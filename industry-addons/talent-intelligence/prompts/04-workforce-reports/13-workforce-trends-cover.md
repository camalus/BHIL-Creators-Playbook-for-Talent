# 13 · Workforce Trends Report Cover

The cover of a recurring workforce intelligence publication — Korn Ferry *Workforce 2025*, Mercer *Global Talent Trends*, Lightcast *Fault Lines*, Deloitte *Global Human Capital Trends*, WEF *Future of Jobs*.

| Field | Value |
| :--- | :--- |
| **Use case** | Cover plate for an annual or recurring workforce intelligence publication |
| **Sub-register** | A (board / institutional audience) or C (marketing / candidate-facing audience) |
| **Recommended model** | Ideogram v3 (typographic) + Midjourney v7 (abstract metaphor) composite. Workflow Recipe C. |
| **Aspect ratio** | 8.5×11" portrait (Letter) or A4 portrait |
| **Production tier** | 3 — Archival |
| **Compliance posture** | Most workforce reports prohibit AI imagery on the cover. Where permitted, abstract metaphor and typographic register only — no human subjects. C2PA Content Credentials applied. Visible disclosure on colophon. |

## Format Anatomy

The dominant cover anatomy across leading workforce reports:

- **Issuer wordmark** small, top-left or top-right.
- **Edition signifier** ("10th Annual," "Vol. III," series name) in small caps below the wordmark.
- **Display title** — the report's title, in heavy serif or humanist sans, dominant on the cover.
- **Subtitle** — the year's theme as editorial subtitle in regular weight.
- **Year as typographic anchor** — large, often integrated with the cover composition.
- **Abstract metaphor visual** — gradient field, abstract data art, or austere photographic metaphor (architectural, atmospheric).
- **Footer copy** — small attribution, "in partnership with [N]," edition #, ISBN/ID.

## Prompt — Midjourney v7 (Abstract Metaphor Base)

For the abstract data-art register (WEF, Lightcast, Bain registers):

```text
Editorial cover background, abstract metaphor for "[REPORT THEME]". A topographic gradient
field reading as a stylized terrain or ocean swell, in restrained palette of [BRAND
ACCENT] over deep navy ground, with subtle paper-texture grain. The composition has
generous negative space in the upper-third for typographic title overlay and lower-third
for subtitle. No people, no figures, no buildings. Restrained, editorial, slightly
desaturated, slight grain. Foreign Affairs editorial cover register. [BHIL profile] --ar
17:22 --style raw --stylize 200 --v 7
```

## Prompt — Ideogram v3 (Typographic Composite)

For the typographic overlay layered onto the abstract base:

```text
Editorial workforce report cover layout, 8.5×11" portrait. Top-left small-caps issuer
wordmark "[ISSUER]" in 11pt warm ivory. Below wordmark: edition signifier "[EDITION] ·
[YEAR]" in tracked small caps, 10pt warm ivory. Center upper-third: editorial display
title "[REPORT TITLE]" in heavy serif (Canela Deck or GT Sectra Bold register), warm
ivory, 80-96pt. Immediately below title: subtitle "[REPORT SUBTITLE]" in regular weight
serif italic, 24pt warm ivory. Lower-third: very large year "[YEAR]" rendered as a
typographic anchor in serif display 144-180pt, warm ivory at 30% opacity, integrated
with the composition rather than dominating it. Footer: small attribution copy and ISBN
in 9pt regular. Subtle paper-grain texture overlay at 8% opacity.
```

## Customization Fields

| Field | Example | Notes |
| :--- | :--- | :--- |
| `[REPORT TITLE]` | "Workforce 2026" / "Future of Jobs" / "Fault Lines" | Display title |
| `[REPORT SUBTITLE]` | "The Skills Pivot" / "Beyond the Plateau" | Editorial subtitle |
| `[YEAR]` | "2026" | Year as typographic anchor |
| `[EDITION]` | "10TH ANNUAL" / "VOL. III" / "ANNUAL EDITION" | Small-caps edition signifier |
| `[ISSUER]` | "Korn Ferry" / "Lightcast" / "Deloitte" / "Mercer" / "WEF" | Publishing organization |
| `[BRAND ACCENT]` | Issuer's brand single accent | Drives the abstract metaphor palette |
| `[REPORT THEME]` | "skills migration" / "leadership transitions" / "compensation pressure" | Drives metaphor selection |

## Variants

### Variant A — Topographic gradient (canonical, abstract data-art)

The flagship register. Topographic gradient field reading as terrain, ocean swell, or contour lines. WEF *Future of Jobs* and Lightcast *Fault Lines* register.

### Variant B — Architectural metaphor

For board-grade leadership research (Heidrick *Route to the Top*, Korn Ferry workforce research). A solitary mountain ridge, a building exterior at dawn, or an architectural detail.

### Variant C — Slope-graph chart as cover

For data-led publications where the chart itself is the cover (BCG *Decoding Global Talent*, Lightcast Tableau-public dashboards). The cover reproduces the headline chart at large scale.

### Variant D — Year-as-anchor typographic

For maximally restrained covers where the year dominates as the visual anchor and the rest of the typography clusters around it (Spencer Stuart *2025 US Board Index* register, generalized).

### Variant E — Tension-axis device

The Deloitte 2025 *Turning Tensions Into Triumphs* convention — opposing-arrow sliders between paired concepts as the cover graphic.

## Compliance Notes

1. **Most workforce reports prohibit AI imagery on the cover.** Production posture should default to real photography (where photography is the cover) or commissioned abstract data art (where abstract is the cover). AI generation is acceptable for the abstract-metaphor base if the report's policy permits; document this in the project spec.

2. **Visible AI disclosure** for any AI-generated cover, on the colophon page:

   > *"Cover imagery generated with AI. Charts and data visualizations throughout this report are produced from [DATA SOURCE] data."*

3. **C2PA Content Credentials** applied to the cover asset.

4. **No human subjects on AI-generated covers.** The default rule: AI for abstract metaphor only. Where the cover register requires photography of people, real photography is used.

5. **Source attribution.** Reports built on third-party data (LinkedIn Workforce Reports use Economic Graph data; Lightcast reports use proprietary labor market data) require source attribution per academic / publishing standards. This is independent of AI imagery compliance but lives on the same colophon page.

## Failure Modes

| Failure Mode | What Happens | Mitigation |
| :--- | :--- | :--- |
| **AI imagery in archival report without policy approval** | Asset published without provenance certainty for archival use | Project spec confirms AI permission per report; default to real / commissioned where policy is unclear |
| **Cover too cluttered** | Multiple typographic elements compete; no clear visual hierarchy | Strip to title + subtitle + year + small attribution; avoid pull-quotes or stats on cover |
| **Year as typographic anchor too small** | Cover reads as undated; year is critical to recurring report identity | Year should be visually prominent, often near the title |
| **Stock-photo register on a serious report** | Cover reads as second-tier publication | Match register to publication tier (board-grade vs. marketing) |
| **Source attribution missing** | Data charts without source citation | Source attribution on cover or colophon |

## Related

- [Prompts category README](./README.md)
- [Sub-register A specification](../../reference/sub-register-a-retained-search.md)
- [Sub-register C specification](../../reference/sub-register-c-agency.md)
- [Three production tiers](../../workflows/three-production-tiers.md)
- [Parent: Workflow Recipe C (typography compositing)](../../../../workflows/README.md)
