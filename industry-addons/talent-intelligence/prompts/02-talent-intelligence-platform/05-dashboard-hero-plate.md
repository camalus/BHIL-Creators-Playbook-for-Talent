# 05 · Dashboard Hero Plate

The hero image on a talent-intelligence platform's marketing site, product page, or sales deck — depicting the product UI with stylized data, AI agent panel, and recognition badges.

| Field | Value |
| :--- | :--- |
| **Use case** | Marketing-site hero, product-page hero, sales-deck hero for a talent intelligence platform. |
| **Sub-register** | B — Talent-intelligence platform dashboard |
| **Recommended model** | GPT Image 2 (best for structured UI compositions) or Flux.2 Pro (best for dark-gradient hero plates with glow). |
| **Aspect ratio** | 16:9 (1920×1080) for hero, 21:9 (2560×1080) for ultra-wide. |
| **Production tier** | 2 — Mid-tier |
| **Compliance posture** | Stylized AI agent avatar (not photo-realistic). Synthetic data must be obviously sample. Recognition badges require licensing. C2PA applied. |

## Prompt — GPT Image 2

```text
A talent intelligence platform dashboard hero image. Dark gradient mesh backdrop:
[PLATFORM PROFILE — e.g., deep purple #2D1B69 to near-black #0A0518]. Center-left of
frame: a rounded-card UI showing a force-directed skills graph — glowing nodes in
[PLATFORM ACCENT 1 — e.g., aqua #00D4FF] connected by thin glowing edges, with a focal
node brighter and slightly larger, its connections highlighted in [PLATFORM ACCENT 2 —
e.g., orange #FF6B35]. Center-right: a bento-grid of three stat tiles — first tile shows
a giant numeral "1.6B" with caption "career profiles" and a small upward delta arrow;
second tile shows a sparkline mini-chart in accent color; third tile shows a chip cloud
of skill tags. Far-right: an AI agent chat panel docked vertically — header with stylized
geometric avatar (a hexagonal monogram icon, NOT a photo-realistic face), agent name,
conversation thread of two short message exchanges, input field with send button at
bottom. Bottom strip: four recognition badge graphics in a horizontal row — small
graphics with awarding-body styling and short qualifying text underneath. Typography
throughout: tight tracked geometric sans-serif (Inter or similar), white #F5F5F7 body
type, accent color for stat numerals. The composition has depth: the cards float in the
gradient mesh with soft glow auras, and the AI agent panel has a subtle parallax offset
from the main dashboard. Eightfold "Infinite Workforce" register applied to [PLATFORM
NAME].
```

### GPT Image 2 Configuration

| Field | Value |
| :--- | :--- |
| Model | `gpt-image-2` |
| Quality | `high` |
| Size | `1792x1024` (16:9 landscape) |
| Style | `vivid` |

## Prompt — Flux.2 Pro Alternative

```text
talent intelligence platform dashboard hero. dark gradient mesh ground: [PLATFORM
PROFILE]. center-left rounded-card UI with force-directed skills graph - glowing nodes
in [PLATFORM ACCENT 1], thin glowing edges, focal node highlighted in [PLATFORM ACCENT
2]. center-right bento-grid with three stat tiles: giant numeral "1.6B" + delta arrow;
sparkline mini-chart; chip cloud of skill tags. far-right AI agent panel with stylized
hexagonal monogram avatar (geometric, not photo-realistic), agent name, two-message
conversation, input field. bottom strip with four recognition badge graphics. tight
geometric sans typography (Inter), white #F5F5F7. cards float in gradient mesh with soft
glow auras. eightfold infinite workforce register. cinematic depth, subtle parallax,
production-grade UI design, 1920x1080.
```

### Flux.2 Pro Configuration

| Field | Value |
| :--- | :--- |
| Model | `flux-2-pro` |
| Width × Height | `1920 × 1080` |
| Steps | 50 |
| Guidance | 4.0 |
| Output format | PNG with alpha (for compositing) |

## Customization Fields

| Field | Example | Notes |
| :--- | :--- | :--- |
| `[PLATFORM PROFILE]` | "Eightfold-style — primary deep-purple #2D1B69 to #0A0518 gradient" | Locked at project level |
| `[PLATFORM ACCENT 1]` | "aqua #00D4FF" | Primary accent |
| `[PLATFORM ACCENT 2]` | "orange #FF6B35" | Secondary accent |
| `[PLATFORM NAME]` | "[Vendor Name]" | Used in register anchor |
| Stat numeral | "1.6B" or relevant scale | Specify per project |
| Stat caption | "career profiles" | Specify per project |
| Recognition badges | 3-6 typical | Specify per project; ensure licensing |
| Agent name | "Olivia" or "Curie" or platform-specific | Stylized only |

## Variants

### Variant A — Skills graph dominant (canonical)

The default — the skills graph is the dominant visual, with bento-grid stats and AI agent as supporting elements.

### Variant B — Choropleth dominant

For platforms emphasizing geographic talent intelligence.

```text
A talent intelligence platform dashboard hero. Dark gradient mesh backdrop. Center: a
rounded-card UI showing a choropleth map of the world in [PLATFORM ACCENT 1] gradient
(country polygons varying in opacity by data variable), with overlay points in [PLATFORM
ACCENT 2] for specific cities. Sidebar to the right: a vertical stat strip with three
stacked tiles. Far-right: AI agent panel docked. Bottom strip: recognition badges.
Typography: tight geometric sans, white. Lightcast Fault Lines register applied.
```

### Variant C — Bento-grid dominant

For platforms emphasizing data abundance and stat-led storytelling.

```text
A talent intelligence platform dashboard hero. Dark gradient mesh backdrop. Center:
a 4×3 bento grid of twelve stat tiles, each tile containing a giant numeral with caption,
delta arrow, and either a mini-chart, a chip cloud, or a small choropleth detail. Tiles
in alternating heavier and lighter weight create rhythm. Far-right: AI agent panel
docked vertically. Bottom strip: recognition badges. Eightfold cultivate register
applied.
```

### Variant D — Marketing minimalism (Gloat register)

For platforms targeting Gloat-style white-marketing aesthetic.

```text
A talent intelligence platform marketing hero in white minimalism register. Pure white
ground (#FFFFFF). Center: a single rounded-card UI showing the product, with subtle
shadow at 5% opacity. The product UI itself is dark — within the card, the platform's
dark gradient mesh and accent palette appear as if "looking through a window" to the
dark product. Around the card: generous white space. Below: a single typographic
headline in tight geometric sans, dark navy or near-black, sentence case. Logo small
upper-left. Recognition badges in a horizontal row at the very bottom. Gloat homepage
register.
```

## Failure Modes

| Failure | Symptom | Mitigation |
| :--- | :--- | :--- |
| **Photo-realistic AI agent avatar** | Generated AI agent panel includes a face that resembles a real person | Explicit "stylized hexagonal monogram avatar, NOT a photo-realistic face" instruction; review every output |
| **Real candidate data leak** | Generated dashboard contains plausible-looking but real-sounding candidate names | Specify "synthetic sample data only" and review every text element |
| **Off-register palette** | Output uses generic SaaS purple/blue not matching the platform brand | Lock `[PLATFORM PROFILE]` at project level with specific hex codes |
| **Drop shadows instead of glow** | Cards have hard drop shadows rather than soft glow | Specify "soft glow auras" not "drop shadows"; the register is glow-driven |
| **AI agent panel competes with main dashboard** | Agent panel too prominent, fighting for attention with the main visual | Specify panel as 25-30% of frame width; subtle parallax offset |
| **Recognition badges overcluttered** | Too many badges, reading as cluttered | Limit to 3-6 badges; ensure each has licensing |

## Compliance Notes

- **Stylized AI agent avatar required.** Photo-realistic AI-generated faces in this slot are prohibited. Use geometric, abstract, or illustrated avatars only.
- **Synthetic data must be obviously sample.** No real candidate or employee data without explicit consent and per-individual review.
- **Recognition badges licensed.** Verify entitlement for every badge before publication. Using a Fosway 9-Grid badge without entitlement is a trademark exposure.
- **C2PA Content Credentials** applied at generation; composite assets carry C2PA from source layers.
- **Visible AI disclosure** in marketing collateral is industry-standard but channel-dependent. The dashboard hero plate is generally understood to be a marketing graphic, but disclosure language *"Dashboard image is illustrative; product UI varies."* is best practice.
- **Source attribution** for any underlying data per data provider's licensing terms.

## Related

- [02-talent-intelligence-platform README](./README.md)
- [Sub-register B specification](../../reference/sub-register-b-platform.md)
- [Eightfold Infinite Workforce exemplar](../../reference/exemplar-library.md)
- [GPT Image 2 framework (Parent)](../../../../frameworks/gpt-image-2.md)
- [Flux.2 framework (Parent)](../../../../frameworks/flux-2.md)
- [AI imagery policy](../../compliance/ai-imagery-policy.md)
