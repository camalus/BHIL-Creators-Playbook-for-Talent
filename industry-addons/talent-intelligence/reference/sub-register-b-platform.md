# Sub-Register B — Talent-Intelligence Platform Dashboard

Visual specification for the talent-intelligence platform dashboard register. The world of Eightfold, Gloat, Lightcast, Beamery, Draup, and TalentNeuron.

## At a Glance

The agentic-AI dashboard idiom. Dark gradient mesh backdrops, glowing node graphs, choropleth globes, bento-grid stat tiles, AI-agent chat panels docked right. Where retained search uses white space, platform marketing uses dark space. Where retained search uses architectural metaphor, platform marketing uses data-as-art. Where retained search uses serif gravity, platform marketing uses geometric-sans precision.

## Palette System

Dark gradient meshes are the dominant ground. Two-or-three-color accent gradients carry the visual identity.

### Anchor Platform Palettes

| Platform | Ground | Accent Set | Notes |
| :--- | :--- | :--- | :--- |
| **Eightfold AI** | Deep purple → near-black | Aqua + orange light streaks | "Infinite Workforce" hero |
| **Gloat** | White (marketing) → indigo (product) | Indigo + Loomra orbital | White minimalism on marketing, dark UI on product |
| **Lightcast** | Lavender → near-white (2025 brand 2.0) | Lavender + coral | Hero-people in coral against lavender |
| **Beamery** | Navy → near-black | Cyan + coral | Digital Twin product imagery |
| **Draup** | Deep navy with dotted-grid backdrop | Magenta + lime + orange icon tiles | Most playful palette of the set |
| **TalentNeuron** | Deep teal → near-black | Lime + coral | Gartner subsidiary, more corporate |

### Custom Palette Per Project

Unlike sub-register A (where the BHIL parent register works unchanged), sub-register B requires per-project palette declaration. Prompts in this register declare a `[PLATFORM PROFILE]` and `[PLATFORM SREFS]` set that should be locked per-project to the client's platform palette.

A typical declaration:

```text
PLATFORM PROFILE: Eightfold-style — primary deep-purple #2D1B69 to #0A0518 gradient,
accent aqua #00D4FF and orange #FF6B35 light streaks, body type Inter or Eightfold custom,
display type geometric sans bold.
```

### Palette Discipline

- **Ground is dark, but not pure black.** Pure black reads as flat; the register uses gradient meshes for depth (#1A0F2E to #0A0518, not #000000).
- **Accents glow.** The signature is the glow effect — accent colors appear as if light-emitting against the dark ground. Typical implementation: 30-50% opacity gradient bloom around accent elements.
- **Typography color is high-contrast white or near-white.** Not pure white; typically `#F5F5F7` or `#E8E8EC` for less harsh contrast.

## Typography

Geometric sans-serif. Tight tracking. Heavy display weights for stat numerals. Light body weights for supporting text.

### Display

- **Inter, Söhne, GT America, Aeonik, or platform-custom display.** The convention is geometric-sans rather than humanist-sans.
- **Bold or extrabold weights** for stat numerals and headlines. Often used at 80-120pt+ for hero stat tiles.
- **Tight tracking** (-0.5 to -1 unit). Display headlines are dense; not airy.

### Body

- **Inter, Söhne, GT America, Aeonik, or platform-custom sans.**
- **Light or regular weights** for body type.
- **Slight letter-spacing increase** for body type at small sizes.

### UI

- **The same family as body**, used for navigation, labels, and dashboard controls.
- **Sentence case headings** in dashboard contexts (vs. title case in retained search).

## Data Visualization Grammar

The register has standardized around a specific data-viz vocabulary. Prompts should encode these as primitives.

### Force-Directed Skill Graph

The signature visual for "skills intelligence" and ontology.

- **Dark gradient backdrop.** The graph appears to float in dark space.
- **Nodes as glowing dots** in the platform's accent color. 30-50% opacity bloom around each node.
- **Edges as thin glowing lines** connecting nodes. Thinner edges (0.5-1pt) for weak relationships, thicker (2-3pt) for strong.
- **Selected nodes labeled** with skill names in white type. Unselected nodes unlabeled to avoid clutter.
- **Sometimes a focal node** that is brighter and slightly larger, with its connections highlighted in a stronger accent.

References: Gloat *Loomra Knowledge Graph*, Eightfold Capability Dashboard, Beamery Digital Twin, Phenom career architecture trees.

### Choropleth Map

The canonical visual for "global supply/demand" semantic load.

- **Dark backdrop or transparent backdrop.**
- **Country/region polygons** filled with platform accent color, varying lightness/opacity to indicate the data variable.
- **Legend** in small white type, lower-right.
- **Sometimes overlay points** for specific cities or job locations.
- **Sometimes an animated layer** showing hire-rate, talent-flow, or hiring-velocity over time.

References: Lightcast 165-country world map, ManpowerGroup blue gradient employer-shortage maps, LinkedIn metro hiring heatmaps.

### Sankey Diagram

The canonical visual for talent flow / migration.

- **Dark backdrop or transparent backdrop.**
- **Width-weighted ribbons** in platform accent colors. Ribbons have soft edges and slight opacity gradients (lighter at edges, stronger in center).
- **Source labels left, destination labels right.**
- **Data callouts at major flow junctions.**
- **Time-period and source-attribution caption** in small white type.

References: LinkedIn #AmericaAtWork, Lightcast Talent Migration Dashboard, Crunchr internal mobility, BCG/CGD *Global Talent Mobility 2025*.

### Bento-Grid Stat Layout

The dominant 2025-2026 marketing-graphic convention.

- **Modular tiles** in a grid layout (2×3, 3×2, 4×3, etc.).
- **Each tile contains:** a giant numeral (80-120pt+), a delta arrow (↑ ↓), a mini-chart (sparkline, mini-bar, mini-Sankey), or a chip cloud (skill tags, role tags).
- **Tile backgrounds** are slightly lighter than the gradient ground, with hairline borders or slight glow.
- **Tile contents** in platform accent colors against the tile background.

References: Lightcast `data-bento-march-2026.png`, Gloat product pages, Beamery dashboard.

### Treemap and Capability Heatmap

For skills-inventory and capability-distribution semantics.

- **Rectangular tiles sized by data value.**
- **Color-coded by category** (skill cluster, function, level).
- **Labels** in white type for larger tiles; legend for smaller.

### Radial / Sunburst Diagram

For maturity-model and hierarchical-distribution semantics.

- **Concentric rings**, each representing a level or category.
- **Segments within rings** sized by data value.
- **Color-coded** with platform accent palette.

References: Draup AI-Ready Maturity Model (four concentric rings).

## AI-Agent UI Convention

A platform-side signature: an AI-agent chat panel docked on the right side of the dashboard.

- **Panel width:** roughly 25-30% of the dashboard width.
- **Background:** slightly different ground from the main dashboard (often a slightly lighter gradient).
- **Header:** the agent's name and avatar (Olivia, Curie, Winston, AI Interviewer all use this template).
- **Conversation thread:** alternating user and agent messages, typically with the agent's name visible.
- **Input field:** at the bottom, with a "send" button in the platform accent.
- **Optional "thinking" indicator:** animated dots or shimmer when the agent is processing.

The agent's avatar is critical — it must be **clearly stylized** (geometric, abstract, illustrated, or a simple monogram) to avoid looking like a real person. AI-generated photo-realistic avatars in this slot trigger the candidate-imagery problem; they should not be used.

## Recognition-Badge Convention

Recognition badges (Fosway 9-Grid, IDC MarketScape, Brandon Hall, Top HR Products) function as visual currency on platform marketing materials.

- **Badge strip** at the bottom of the dashboard hero or landing-page hero.
- **3-6 badges** typically; more reads as cluttered.
- **Each badge** is a small graphic in the awarding body's brand identity, accompanied by short qualifying text ("Strategic Leader 2025," "Major Player 2025").
- **Strip background** is typically a slightly different ground from the rest of the dashboard.

Recognition badges require licensing — using a Fosway 9-Grid badge without entitlement is a trademark exposure.

## Layout Conventions

### Dashboard Hero Plate

- Rounded-card UI on a gradient mesh backdrop.
- Choropleth or dotted-globe quadrant.
- Force-directed skills graph.
- Sankey or talent-flow ribbon.
- Bento-grid stat tiles.
- AI-agent chat panel docked right.
- Recognition badges in a horizontal strip.

### Conference Keynote Backdrop

- Ultra-wide LED format (typically 16:9 with 2.5:1 ultra-wide variant).
- Dark gradient mesh in the platform's brand palette.
- Single typographic headline.
- Abstract particle or aurora animation in background.
- Sometimes synchronized to speaker pacing.

References: Eightfold *Cultivate*, UNLEASH theatrical magenta-and-cyan, HR Tech Conference corporate blue, SHRM Annual traditional red/blue.

## Anchor Platforms and Exemplars

| Reference | What It Anchors |
| :--- | :--- |
| Eightfold "Infinite Workforce" | Dark purple gradient + aqua/orange light streaks; signature dashboard hero |
| Gloat homepage + Loomra | White marketing minimalism + indigo product UI; orbital animation |
| Lightcast 2025 brand 2.0 | Lavender-glow + coral hero-people; choropleth map |
| Beamery Digital Twin | Navy + cyan + coral; force-directed graph signature |
| Draup AI-Ready Maturity Model | Four concentric rings; magenta/lime/orange icon tiles |
| TalentNeuron Workforce Insights | Deep teal + lime + coral; corporate Gartner register |

See [`exemplar-library.md`](./exemplar-library.md) for full URLs and additional anchors.

## Off-Register Signals

Three signals mark imagery as off-register for sub-register B:

1. **Light-mode marketing on product UI imagery.** Most platform marketing now defaults to dark-mode imagery for the dashboard itself (lightmode for landing-page chrome is fine).
2. **Drop shadows on data-viz elements.** The register uses glow, not shadow. Drop shadows read as 2010s SaaS, not 2026 platform.
3. **Stock-photo "team" imagery.** The dashboard hero plate convention does not include team photography — it features the product UI. Imagery of "happy diverse team using the platform" reads as off-register.

## Production Implications for Prompts

Prompts targeting sub-register B:

- Declare a `[PLATFORM PROFILE]` and `[PLATFORM SREFS]` set per project, locked to the client's platform palette.
- Default to dark gradient mesh ground.
- Default to one of the data-viz primitives (force-directed graph, choropleth, Sankey, bento grid) as the dominant visual element.
- Include the AI-agent chat panel docked right when the deliverable is a dashboard hero or product hero.
- Include recognition badges only when licensed.
- Use geometric-sans typography; avoid serif (which reads as off-register).
- Avoid photo-realistic AI-agent avatars (use stylized geometric or illustrated avatars).

## Related

- [Reference README](./README.md)
- [Three sub-registers overview](../docs/01-three-sub-registers.md)
- [Sub-register A (retained search)](./sub-register-a-retained-search.md)
- [Sub-register C (agency)](./sub-register-c-agency.md)
- [Exemplar library](./exemplar-library.md)
- [Platform prompts](../prompts/02-talent-intelligence-platform/README.md)
