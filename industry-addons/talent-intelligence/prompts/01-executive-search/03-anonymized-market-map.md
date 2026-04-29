# 03 · Anonymized Market Map

A visualization of the talent landscape for a search — competitor companies, role distribution, candidate clusters — with names and identities redacted to maintain confidentiality.

| Field | Value |
| :--- | :--- |
| **Use case** | Market mapping visualization for retained search — talent landscape, competitor org charts, candidate cluster diagrams. |
| **Sub-register** | A — Retained-search editorial (with structured-graphic discipline) |
| **Recommended model** | GPT Image 2 (best for structured graphics with text) or Nano Banana Pro (good for editorial diagrams). |
| **Aspect ratio** | 16:9 slide or 11×17" tabloid landscape. |
| **Production tier** | 2-3 |
| **Compliance posture** | No real-company logo reproduction without permission. No candidate identification. Anonymization conventions enforced. |

## Prompt — GPT Image 2

```text
Anonymized executive search market map. A bubble cluster diagram on warm-ivory ground.
Twelve circular nodes of varying size representing companies — node size proportional to
employee count. Each node is filled with deep navy and contains a small white lock icon
in the center, with a subtle hatched-line monogram circle replacing real logos. Each
node carries a role-and-industry descriptor below it in 9pt small caps deep navy
(e.g., "TOP-5 GLOBAL BANK", "MID-CAP MEDTECH", "BOUTIQUE PE FIRM"). Node clusters are
spatially arranged into three regions corresponding to candidate-pool segments, with
each region softly tinted in a warm gray. Hairline rules in warm gray separate the
regions. Title at top in heavy serif: "[CLIENT CODE NAME] · MARKET MAP". Legend
bottom-left: "● Confidential node · ◐ Active engagement · ○ Under exploration" in 9pt.
Footer center: "[CLIENT FIRM] · [PROJECT CODENAME] · [DATE]" in 8pt regular. No real
company names, no identifying logos, no candidate names. Foreign Affairs editorial
diagram register applied to executive search context.
```

### GPT Image 2 Configuration

| Field | Value |
| :--- | :--- |
| Model | `gpt-image-2` |
| Quality | `high` |
| Size | `1792x1024` (16:9 landscape) |
| Style | `vivid` (off) — use natural for editorial restraint |

## Prompt — Nano Banana Pro Alternative

```text
Editorial executive search market map for confidential client briefing. Bubble cluster
diagram, 12 circular nodes on warm-ivory ground, each node deep navy with a small white
lock icon and a hatched-line monogram circle. Role-and-industry descriptors below each
node in 9pt small caps. Three softly-tinted regions group the nodes by candidate-pool
segment. Hairline gray rules separate regions. Heavy-serif title top: "[CLIENT CODE
NAME] · MARKET MAP". Legend bottom-left in 9pt. No real names, no real logos, no
candidate identification. Documentary editorial register. 16:9 landscape.
```

## Customization Fields

| Field | Example | Notes |
| :--- | :--- | :--- |
| `[CLIENT CODE NAME]` | "Project Aurora" | Codename, not real client name |
| `[CLIENT FIRM]` | Search firm name | Footer |
| `[PROJECT CODENAME]` | "Project Aurora" (often same as Client Code Name) | Footer |
| `[DATE]` | "April 2026" | Footer |
| Number of nodes | 8-20 typical | Specify in prompt |
| Number of regions | 2-4 typical | Specify in prompt |
| Role descriptors | "TOP-5 GLOBAL BANK", "MID-CAP MEDTECH" | Industry + scale only, no real names |

## Variants

### Variant A — Bubble cluster (canonical)

The Revelio Labs convention. Use for talent-pool mapping where companies are the unit of analysis.

### Variant B — Org-tree with redacted nodes

For succession planning or organization-deep-dive contexts.

```text
Org-chart tree on warm-ivory ground. Top: a single node labeled "BOARD" in deep navy.
Connecting lines (hairline gray) descend to a second tier of redacted role boxes — each
box shows role title in 11pt small caps but with name redacted as "███████" and a small
white lock icon. Third tier shows direct reports as smaller redacted boxes. Confidential
nodes carry a closed-padlock icon; open positions carry an open-padlock icon. Editorial
serif typography throughout. Legend bottom-left explains the icon system. No real names,
no real titles beyond role function (CFO, COO, etc.).
```

### Variant C — Geographic talent landscape

For geographic / market-by-market mapping.

```text
A choropleth map of the United States in single-hue gradient (warm-ivory ground, deep
navy gradient on states by candidate-pool density). State labels in small caps. A
sidebar at right shows a ranked list of top 10 metros with candidate counts (anonymized
as "Metro 1", "Metro 2"). Title top: "[CLIENT CODE NAME] · GEOGRAPHIC TALENT MAP".
Editorial register, restrained palette, hairline rules.
```

### Variant D — Skills-density heatmap

For function-by-function or skill-by-skill mapping.

```text
A heatmap matrix on warm-ivory ground. Y-axis: 10 skills/capabilities labeled in 9pt
small caps. X-axis: 8 anonymized companies labeled "Company A" through "Company H".
Cells filled with deep navy varying in opacity by skills density (darker = higher
density). Hairline gray gridlines. Title top: "[CLIENT CODE NAME] · CAPABILITY DENSITY
MAP". Legend lower-right. Editorial register.
```

## Failure Modes

| Failure | Symptom | Mitigation |
| :--- | :--- | :--- |
| **Real company logos appear** | Generated map includes recognizable corporate logos or brand colors | Explicit "no real company names, no identifying logos" instruction + post-generation review |
| **Real candidate names leak** | Sample names from training data appear in node labels | Use hatched-circle replacements; review every text element |
| **Off-register data-viz** | Generated map looks like a marketing infographic, not an executive search deliverable | Use "Foreign Affairs editorial diagram register" anchor; restraint in palette and typography |
| **Lock icons missing** | Confidentiality icons not generated | Specify lock-icon explicitly in prompt; composite if necessary |
| **Region tints conflicting** | Tint colors compete with the navy nodes | Use only warm-gray tints (very light); navy nodes must remain dominant |

## Compliance Notes

- **No real-company logo reproduction** without explicit licensing. The hatched-circle monogram replacement is the convention.
- **No candidate identification** of any kind. Role-and-industry descriptors only.
- **Anonymization legend** explicitly documents the convention used (lock icon = confidential, hatched circle = redacted logo, etc.).
- **C2PA Content Credentials** applied at generation. Composite assets carry C2PA from source layers.
- **Visible AI disclosure** on the dossier's confidentiality notice page (not on the map itself, where it would compete with the legend).
- **Five-year recordkeeping** including the anonymization key (which real companies map to which "Company A" labels) — stored separately from the deliverable in a secure project file.
- **Source attribution** for any underlying data (LinkedIn Talent Insights, Lightcast, Revelio Labs) per the data provider's licensing terms.

## Related

- [01-executive-search README](./README.md)
- [Sub-register A specification](../../reference/sub-register-a-retained-search.md)
- [AI imagery policy](../../compliance/ai-imagery-policy.md)
- [Candidate Dossier Spec Template](../../templates/candidate-dossier-template.md)
- [GPT Image 2 framework (Parent)](../../../../frameworks/gpt-image-2.md)
- [Workflow Recipe C (Parent)](../../../../workflows/recipe-c-text-typography-composite.md)
