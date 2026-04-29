# 07 · Talent Flow Sankey

A Sankey diagram, arc map, or directional ribbon showing talent movement between companies, geographies, or roles. Used in workforce reports, conference keynotes, and platform marketing.

| Field | Value |
| :--- | :--- |
| **Use case** | Talent flow / migration visualization for workforce reports, conference keynotes, platform marketing, vendor decks. |
| **Sub-register** | B — Talent-intelligence platform dashboard |
| **Recommended model** | GPT Image 2 (best for structured chart with text) or Flux.2 Pro (best for ribbon glow on dark ground). |
| **Aspect ratio** | 16:9 landscape (1920×1080) for slides; double-truck 2:1 for editorial spread. |
| **Production tier** | 2 — Mid-tier |
| **Compliance posture** | Source attribution required for third-party data. Privacy considerations when flow data is aggregated from individual-level employee data. |

## Prompt — GPT Image 2

```text
A talent flow Sankey diagram. Dark gradient mesh background: deep navy #0A0F1E to
near-black #050810. Six source labels stacked on the left side in white sans-serif type
at 11pt, sentence case: "Banking · Big Tech · Consulting · Healthcare · Energy ·
Education". Six destination labels stacked on the right side in white sans-serif type at
11pt: "AI / ML · Climate Tech · Cybersecurity · Healthcare Tech · Fintech · Public
Sector". Width-weighted ribbons flow from left to right between source and destination
combinations. Ribbons in [PLATFORM ACCENT 1, ACCENT 2, ACCENT 3] varying by destination
- soft edges, slight opacity gradient (lighter at edges, stronger center). Major flow
ribbons (>10% of total flow) carry a small data callout at the midpoint with the
percentage in white 9pt. Title top-left in display sans: "Where talent is moving" in
sentence case at 24pt. Subtitle below in 12pt italic: "[YEAR] · 12-month migration
data · n=[COHORT SIZE]". Footer bottom-right: "Source: [DATA SOURCE]" in 8pt regular.
LinkedIn #AmericaAtWork register applied to [PLATFORM NAME]. Cinematic depth, soft glow
on ribbons, generous negative space.
```

### GPT Image 2 Configuration

| Field | Value |
| :--- | :--- |
| Model | `gpt-image-2` |
| Quality | `high` |
| Size | `1792x1024` |

## Prompt — Flux.2 Pro Alternative

```text
talent flow sankey diagram. dark gradient mesh ground deep navy to near-black. six
source labels stacked left, six destination labels stacked right, both in white sans
11pt sentence case. width-weighted ribbons flow left to right - ribbons in [PLATFORM
ACCENT 1, 2, 3] varying by destination, soft edges, opacity gradient lighter at edges
stronger center. major flows carry midpoint data callout in white 9pt. title top-left
"Where talent is moving" in 24pt display sans. subtitle in 12pt italic. footer source
attribution. linkedin #americaatwork register. cinematic depth, soft glow, 1920x1080.
```

## Customization Fields

| Field | Example | Notes |
| :--- | :--- | :--- |
| Source categories | "Banking · Big Tech · Consulting · Healthcare · Energy · Education" | 4-8 sources |
| Destination categories | "AI / ML · Climate Tech · Cybersecurity · Healthcare Tech · Fintech · Public Sector" | 4-8 destinations |
| `[PLATFORM ACCENT 1, 2, 3]` | "aqua #00D4FF, orange #FF6B35, lime #00FF85" | 3-6 ribbon colors |
| `[YEAR]` | "2026" | Time period |
| `[COHORT SIZE]` | "n=2.4M" | Sample size for credibility |
| `[DATA SOURCE]` | "LinkedIn Talent Insights" or "Lightcast" or "Revelio Labs" | Source attribution |
| Title | "Where talent is moving" | Sentence case in this register |

## Variants

### Variant A — Industry-to-industry Sankey (canonical)

The default. Six industries on the left flowing to six on the right.

### Variant B — Geographic arc map

For geographic migration visualization where Sankey would be misleading.

```text
A geographic arc map showing talent migration. Dark gradient ground with a faint
choropleth of the world (countries in low-opacity navy). Glowing arc curves connect
origin metros to destination metros - arcs in [PLATFORM ACCENT 1, 2, 3] varying by flow
type, height of arc proportional to distance, thickness proportional to volume. Origin
metros marked with small bright dots in [PLATFORM ACCENT 1]; destination metros marked
with larger dots in [PLATFORM ACCENT 2]. Top 5 corridors labeled with origin →
destination text and volume callout. Title top-left "Top global talent corridors" in
24pt display sans. Footer source attribution. Lightcast Talent Migration Dashboard
register.
```

### Variant C — Internal mobility Sankey (intra-company)

For workforce planning context where the Sankey shows movement within a single organization.

```text
An internal mobility Sankey diagram. Dark gradient ground. Left side: six source
function/role groupings within one organization. Right side: six destination function/role
groupings - same six, showing internal mobility. Ribbons flow between source and
destination, with self-flow ribbons (same function to same function) as horizontal
loops on the same row. Promotions tagged with upward arrows; lateral moves with
horizontal arrows; downgrades (rare) with downward arrows. Crunchr internal mobility
register.
```

### Variant D — Time-series flow

For showing change over time rather than between categories.

```text
A time-series talent flow chart. Dark gradient ground. X-axis shows months (Jan through
Dec) along the bottom. Y-axis shows the cohort split between [Source] and [Destination]
categories. Stacked-area chart with width-weighted shading in [PLATFORM ACCENT 1] for
source and [PLATFORM ACCENT 2] for destination. Smooth transitions between months.
Title top-left "Migration through [YEAR]" in 24pt display sans. Major inflection points
labeled with annotation callouts.
```

## Failure Modes

| Failure | Symptom | Mitigation |
| :--- | :--- | :--- |
| **Ribbon overlap unreadable** | Too many ribbons crossing each other; the chart reads as visual noise | Limit to 6×6 or 8×8 source/destination; if more needed, use a different chart type |
| **Source attribution missing** | No data source visible | Footer attribution required; data source per data provider's licensing |
| **Off-register palette** | Ribbons in generic chart-tool colors | Lock [PLATFORM ACCENT 1, 2, 3] with specific hex codes from the platform's palette |
| **Title in wrong register** | Title in title case or all caps | Sentence case is the Sankey/data-viz register convention |
| **Real-name leak** | Source or destination labels include real company names that imply specific employee movements | Use industry/sector categories, not specific company names |

## Compliance Notes

- **Source attribution** required when using third-party data (LinkedIn, Lightcast, Revelio Labs, etc.). Per data provider's licensing terms.
- **Privacy considerations** when flow data is aggregated from individual-level employee data. The aggregated chart must not allow re-identification of individuals.
- **Synthetic or properly licensed data** only. No use of scraped or unlicensed third-party data.
- **C2PA Content Credentials** applied at generation.
- **Visible AI disclosure** in marketing collateral best practice.
- **Source citation** in academic/research-grade reports required to a higher standard than marketing collateral.

## Related

- [02-talent-intelligence-platform README](./README.md)
- [Sub-register B specification](../../reference/sub-register-b-platform.md)
- [Lightcast Talent Migration Dashboard exemplar](../../reference/exemplar-library.md)
- [GPT Image 2 framework (Parent)](../../../../frameworks/gpt-image-2.md)
- [Flux.2 framework (Parent)](../../../../frameworks/flux-2.md)
