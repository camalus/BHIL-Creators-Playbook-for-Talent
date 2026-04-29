# 08 · Vendor Pitch Deck Hero

The hero image of an HR Tech / talent intelligence vendor's pitch deck — designed to communicate platform sophistication, market position, and recognition status in a single 16:9 frame.

| Field | Value |
| :--- | :--- |
| **Use case** | Hero slide of an HR Tech / talent intelligence vendor pitch deck. Used in sales presentations, investor decks, partnership pitches. |
| **Sub-register** | B — Talent-intelligence platform dashboard |
| **Recommended model** | GPT Image 2 (best for structured composition with text and badges) + Ideogram v3 (for crisp typography overlay). Workflow Recipe C. |
| **Aspect ratio** | 16:9 (1920×1080). |
| **Production tier** | 2 — Mid-tier |
| **Compliance posture** | Recognition badges require licensing. Brand mark and tagline must be approved. Synthetic dashboard data must be obviously sample. |

## Prompt — GPT Image 2 (composition base)

```text
HR Tech vendor pitch deck hero slide. 16:9 frame. Dark gradient mesh ground: [PLATFORM
PROFILE — e.g., deep purple to near-black]. Left half of frame: a dashboard composition
showing [PLATFORM NAME]'s product UI - rounded cards floating in the gradient mesh, with
a force-directed skills graph (nodes in [PLATFORM ACCENT 1]) as the dominant card,
supported by a bento-grid stat tile showing a giant "1.6B" numeral and caption "career
profiles inferred". Right half of frame: clean negative space for typographic overlay
in the gradient mesh, with subtle [PLATFORM ACCENT 2] glow at upper-right. Bottom strip
across full width: four recognition badge graphics in a horizontal row - each badge
includes the awarding-body's styling and short qualifying text in white sans-serif 9pt
(synthetic-style placeholder badges only - real badges require licensing). The top-right
corner reserved for the platform brand mark. Eightfold cultivate keynote register
applied. Cinematic depth, soft glow auras on cards.
```

### GPT Image 2 Configuration

| Field | Value |
| :--- | :--- |
| Model | `gpt-image-2` |
| Quality | `high` |
| Size | `1792x1024` |

## Prompt — Ideogram v3 (typographic overlay)

```text
Vendor pitch deck hero typographic overlay for 16:9 slide. Right half of frame:
- Top: platform brand mark and wordmark, [PLATFORM PROFILE accent color], small.
- Center: tagline in heavy display sans 60pt, sentence case, white #F5F5F7. Example:
  "the agentic talent intelligence platform."
- Below tagline: subtagline in regular display sans 24pt, sentence case, [PLATFORM
  ACCENT 1]. Example: "trusted by 600+ enterprises."
- Optional: a small pull-stat - "Founded [YEAR] · [SCALE METRIC]" in 14pt regular
  italic, white at 60% opacity.
Bottom strip: licensed recognition badges from awarding bodies, replacing placeholder
badges from base layer. Maximum 4-6 badges horizontally. Each badge with awarding-body
graphic and qualifier text "[QUALIFIER 2025]" in 9pt sans, white.
```

## Customization Fields

| Field | Example | Notes |
| :--- | :--- | :--- |
| `[PLATFORM PROFILE]` | "Eightfold-style — primary deep-purple #2D1B69 to #0A0518 gradient" | Locked at project level |
| `[PLATFORM NAME]` | "Eightfold AI" or "Gloat" or "Lightcast" | Used in register anchor |
| `[PLATFORM ACCENT 1]` | "aqua #00D4FF" | Primary accent |
| `[PLATFORM ACCENT 2]` | "orange #FF6B35" | Secondary glow |
| Tagline | "the agentic talent intelligence platform." | Sentence case, ends with period |
| Subtagline | "trusted by 600+ enterprises." | Optional credibility line |
| `[YEAR]` | "2018" or platform's founding year | Optional pull-stat |
| `[SCALE METRIC]` | "Series E · $1.4B raised" | Optional pull-stat |
| Recognition badges | 4-6 badges with licensing verified | Replace placeholders in compositing |
| `[QUALIFIER]` | "Strategic Leader," "Major Player," "Top HR Product" | Per-badge qualifier |

## Variants

### Variant A — Skills graph hero (canonical)

The default. Force-directed skills graph as dominant visual element on the left half.

### Variant B — Choropleth hero (geographic emphasis)

For platforms emphasizing global talent intelligence.

```text
HR Tech vendor pitch deck hero. 16:9 frame. Dark gradient mesh ground. Left half:
choropleth map of the world in [PLATFORM ACCENT 1] gradient as the dominant visual,
with overlay points in [PLATFORM ACCENT 2] for specific markets. Right half: clean
negative space for typographic overlay. Bottom strip: recognition badges. Lightcast
Fault Lines register applied.
```

### Variant C — Bento-grid hero (data abundance emphasis)

For platforms emphasizing breadth and depth of data.

```text
HR Tech vendor pitch deck hero. 16:9 frame. Dark gradient mesh ground. Center: a 4×3
bento grid of twelve stat tiles, each tile with a giant numeral and caption, varying in
weight to create rhythm. Left and right margins for typographic overlay. Bottom strip:
recognition badges. Eightfold "Infinite Workforce" register applied.
```

### Variant D — Marketing minimalism (Gloat register)

For platforms targeting a more restrained, premium feel.

```text
HR Tech vendor pitch deck hero. 16:9 frame. Pure white ground (#FFFFFF). Left half:
single rounded-card UI showing the product, with subtle 5% drop shadow, dark product UI
visible "through the window" of the card. Right half: tagline in dark navy 60pt
sentence case, subtagline in [PLATFORM ACCENT 1] 24pt. Bottom strip: recognition
badges. Gloat homepage register applied.
```

## Failure Modes

| Failure | Symptom | Mitigation |
| :--- | :--- | :--- |
| **Recognition badges unlicensed** | Real badge graphics used without entitlement | Verify licensing before use; replace with platform's approved badge collection or remove |
| **Tagline in title case or all caps** | Tagline reads as marketing-corporate, not sub-register B | Sentence case is the convention; ends with period |
| **Brand mark too large** | Platform brand mark dominates the frame | Brand mark small upper-right; tagline carries the visual weight |
| **Real candidate data leak** | Bento-grid stat tiles include real-sounding candidate counts that imply real data | Specify "synthetic sample data only"; review every text element |
| **Photo-realistic AI agent face** | If AI agent panel included, agent avatar is photo-realistic | Use stylized geometric monogram avatar only |

## Compliance Notes

- **Recognition badges licensed.** Verify entitlement for every badge before publication. Using a Fosway 9-Grid badge without entitlement is a trademark exposure. Brandon Hall, IDC MarketScape, and Top HR Products similarly require entitlement.
- **Brand mark and tagline approved** at the brand-governance level before use.
- **Synthetic dashboard data must be obviously sample.** No real candidate or employee data.
- **C2PA Content Credentials** applied at generation; composite assets carry C2PA from source layers.
- **Stylized AI agent avatar** if AI agent panel included; photo-realistic faces prohibited.

## Related

- [02-talent-intelligence-platform README](./README.md)
- [Sub-register B specification](../../reference/sub-register-b-platform.md)
- [Eightfold + Gloat exemplars](../../reference/exemplar-library.md)
- [GPT Image 2 framework (Parent)](../../../../frameworks/gpt-image-2.md)
- [Ideogram v3 framework (Parent)](../../../../frameworks/ideogram-v3.md)
- [Workflow Recipe C (Parent)](../../../../workflows/recipe-c-text-typography-composite.md)
