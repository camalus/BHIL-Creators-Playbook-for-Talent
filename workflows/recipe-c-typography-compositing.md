# Recipe C — Typography Compositing

The canonical pipeline for typographic deliverables: generate atmospheric texture in Midjourney v7, generate precise typography in Ideogram v3, composite the layers in Figma. The result combines MJ's archival-cinema texture with Ideogram's brand-precise typesetting — neither model alone produces this combination at deliverable quality.

## Why This Recipe Exists

Each model has a strength and a hard limitation:

- **Midjourney v7** produces unmatched archival-cinematic *texture*. It cannot reliably produce precise typography — kerning is off, letterforms are approximate, multi-line hierarchies wander.
- **Ideogram v3** produces *the most accurate typography of any image model*. Its texture is functional but flat — no archival depth, no editorial atmosphere.
- **Figma** is the layer-and-blend orchestration tool. It preserves vector typography, composites raster textures cleanly, and handles brand-locked color management.

Composite of the three: a deliverable with editorial-archival background and precise brand-locked typography. This is the only way to get both at the level a serious deliverable requires.

## When to Use This Recipe

- The deliverable is a whitepaper hero, conference poster, briefing-cover plate, or any typographic-forward asset.
- Both atmospheric texture *and* precise typography are required.
- The brand requires exact typeface, color, and hierarchy reproduction.

## When Not to Use This Recipe

- If vector-native output is required (multi-size deployment) → use [prompt 24 / Recraft V3](../prompts/07-typographic-posters/24-conference-keynote.md) instead.
- If only typography is needed (no texture) → use [prompt 04 / Ideogram alone](../prompts/01-intelligence-report-covers/04-market-intelligence-whitepaper.md).
- If only texture is needed (no typography) → generate in MJ alone.

## The Pipeline

### Step 1 — Define the Hierarchy

Before opening any model, write the typographic hierarchy on paper:

- **Kicker** — the small uppercase mono identifier at the top.
- **Title** — the dominant headline, typically 2-4 stacked lines in heavy serif.
- **Rule** — a thin horizontal line separating sections.
- **Subhead** — italic serif positioning line below the title.
- **Footer block** — client name, issue/date, brand mark.

Decide:
- **Color palette** — typically background + type + single accent. Lock the hex values.
- **Typeface register** — typically heavy geometric serif for display + thin uppercase mono for kickers/footer.
- **Aspect ratio** — 2:3 portrait is the default for whitepapers and posters; 16:9 for briefing-deck banners.

### Step 2 — Generate the Background Texture in Midjourney v7

Texture is *backdrop*, not foreground. The MJ generation must be quiet enough to sit underneath dominant typography without competing.

```text
A textured editorial backdrop suitable for a [DELIVERABLE TYPE] hero:
faint [MOTIF — topographic contours / paper grain / engraved
meridians / drifting atmospheric haze], rendered at very low contrast
and saturation, restrained palette of [BG COLOR 1] and [BG COLOR 2]
only, deeply muted and quiet, designed to sit underneath dominant
typography. Editorial archival aesthetic, not modern digital.
Generous negative space distributed evenly across the frame, no focal
point, no dominant element.

--ar [PROJECT ASPECT] --style raw --s 75 --exp 5
--no text, watermark, logo, focal point, modern
--p [BHIL TEXTURE PROFILE] --sref [BHIL ARCHIVAL SREFS] --sw 100
--v 7
```

Notes on parameters:
- **Low `--exp` (5)** — minimal visual exposure. The texture should be subtle.
- **Low `--s` (75)** — minimal stylization. Keep it close to the prompt.
- **`--no text, watermark, logo, focal point, modern`** — explicitly suppress competing elements.
- **Texture-tuned profile and srefs** — `[BHIL TEXTURE PROFILE]` and `[BHIL ARCHIVAL SREFS]` should be project-specific texture-tuned references, not the hero-portrait references.

Generate 6-8 candidates. Pick the one with the most evenly distributed quietness — no focal point that will fight the typography.

**Deliverable:** A raster texture image at the project aspect ratio.

### Step 3 — Generate the Typography Layer in Ideogram v3

Ideogram v3 is configured for typography-first work. Use **Design style** with **Magic Prompt OFF** for the most predictable rendering.

```text
A [PROJECT ASPECT] [DELIVERABLE TYPE] typography layer, transparent
background.

Upper-third: a small uppercase mono kicker "[KICKER]" in [TYPE COLOR],
letter-spaced 0.4em, left-aligned, indented 80px from the left
margin.

Center, dominant: the title "[TITLE LINE 1]" / "[TITLE LINE 2]" /
"[TITLE LINE 3]" rendered as three stacked lines in a heavy
geometric serif (Canela Deck / GT Sectra Bold style), [TYPE COLOR],
left-aligned to match the kicker indent, occupying the central 50%
of the frame's vertical height.

Below the title, a single thin [ACCENT COLOR] horizontal rule, 280px
wide, left-aligned to match the title.

Beneath the rule: an italic serif subhead "[SUBHEAD]" in [TYPE
COLOR], two lines, left-aligned.

Bottom of frame: a thin horizontal divider in [TYPE COLOR] across
the full frame width. Below the divider: "[CLIENT/BRAND]" in mono
uppercase on the left, "[ISSUE NUMBER · DATE]" in mono on the right.

Generous margins. All text crisply rendered, perfect kerning.
Editorial, restrained, serious. No background texture; the
background is transparent.
```

Notes:
- **Transparent background** — Ideogram occasionally renders a faint background tint. Mask out in Figma if needed.
- **Exact text quoted** — quoted strings get rendered literally; this is the discipline that prevents auto-text generation.
- **Specific layout instructions** — left-margin indent, line counts, rule width — Ideogram respects these.

Generate 4-6 candidates. Pick the one with the cleanest kerning and the best line breaks.

**Deliverable:** A raster image of the typography layer, ideally with transparent or near-transparent background.

### Step 4 — Composite in Figma

Open Figma, create a frame at the deliverable's exact size and aspect.

**Layer 1 — Background fill.** A solid fill of `[BG COLOR 1]` (the project's background hex) covering the full frame.

**Layer 2 — MJ texture.** Place the MJ texture image, scaled to fill the frame. Set blend mode to `Multiply` or `Soft Light` and reduce opacity to **60-80%**. The texture should be felt, not seen.

**Layer 3 — Typography from Ideogram.** Place the Ideogram typography image. If it has a faint background tint, mask it out — either with a vector mask following the typography shape, or by setting blend mode to `Luminosity` to drop the color and keep only the brightness.

**Layer 4 — Color correction.** Add a `Color` adjustment layer at the top. Apply minor corrections to align the layers — slight desaturation of the texture, slight warmth shift to match the type, etc. The goal is to make the layers feel like they were always together.

**Layer 5 — Optional vignette.** A subtle radial gradient at the edges of the frame, 10-15% opacity, can ease the seam between layers and add depth. Use sparingly.

### Step 5 — Verification at Thumbnail

Reduce the Figma frame to **25% of final size** (thumbnail scale). At this scale:
- The title must still be legible.
- The texture must not interfere with the type.
- The hierarchy must read at a glance.

If the typography is fighting the texture at thumbnail, drop the texture opacity further. If the title doesn't read at thumbnail, the type is too small or the texture is too active.

### Step 6 — Brand QA

Final brand check:
- **Color values** are exact hex (use Figma's color picker on the final composite to verify).
- **Typeface** matches brand spec (visual check; if Ideogram drifted, you may need to retype the title in actual brand-licensed type within Figma).
- **Margins** are within brand grid spec.
- **Spelling and dates** are correct.

### Step 7 — Multi-Size Derivatives

If the deliverable will appear at multiple sizes (poster + LinkedIn tile + email banner):
- Keep the Figma source as a multi-frame file with one frame per format.
- Reuse the texture and typography across formats; re-layout the hierarchy for each aspect ratio.
- For drastically different aspects (1:1 social tile vs 21:9 banner), consider regenerating both layers at the new aspect rather than cropping.

### Step 8 — Export and Archive

Export each frame as PNG (raster) and PDF (print-ready). Archive:
- The Figma source file with all layers preserved.
- The MJ texture source file with prompt metadata.
- The Ideogram typography source file with prompt metadata.
- The final composite exports.

Document in the asset metadata that the composite has *no* SynthID/C2PA signature (MJ doesn't sign; Ideogram doesn't sign by default). If disclosure is required, add C2PA metadata to the final composite manually.

## Failure Modes

- **Texture interferes with typography legibility.** Cause: MJ texture is too active. Fix: drop texture opacity to 50% in Figma; or regenerate MJ with even lower `--exp` and `--s`.
- **Typography has a visible background despite request for transparent.** Cause: Ideogram occasionally renders a faint tint. Fix: mask in Figma, or set typography layer blend mode to `Luminosity`.
- **Color mismatch between MJ texture and Ideogram type.** Cause: subtle color casts in MJ clash with brand neutrals. Fix: HSL adjustment on the MJ layer in Figma until the casts align.
- **Composite feels "stitched together".** Cause: layers feel separately produced. Fix: subtle vignette across the composite; or 5% color overlay (e.g., 5% amber) across the whole composite to unify.
- **Ideogram renders the wrong typeface.** Cause: Ideogram's typeface inventory is its own; it may approximate "heavy geometric serif" with a generic. Fix: if brand-licensed type is required, retype the title in Figma using the actual licensed typeface, then place over the MJ texture. Use Ideogram only as a layout reference in this case.
- **The deliverable looks great at full size but fails at thumbnail.** Cause: hierarchy is too subtle, or texture too active. Fix: increase title weight; reduce texture opacity. The thumbnail test is non-negotiable.

## Related

- [`workflows/README.md`](./README.md)
- [`workflows/pipeline-pillars.md`](./pipeline-pillars.md)
- [`prompts/07-typographic-posters/23-whitepaper-hero.md`](../prompts/07-typographic-posters/23-whitepaper-hero.md) — canonical example.
- [`prompts/07-typographic-posters/24-conference-keynote.md`](../prompts/07-typographic-posters/24-conference-keynote.md) — vector alternative.
- [`prompts/01-intelligence-report-covers/04-market-intelligence-whitepaper.md`](../prompts/01-intelligence-report-covers/04-market-intelligence-whitepaper.md) — Ideogram alone.
- [`frameworks/midjourney/parameter-stacks.md`](../frameworks/midjourney/parameter-stacks.md) — texture parameter stacks.
- [`frameworks/ideogram/README.md`](../frameworks/ideogram/README.md) — Ideogram v3 overview.
- [`reference/color-and-film-stock.md`](../reference/color-and-film-stock.md) — palette discipline.
