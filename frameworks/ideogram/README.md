# Ideogram v3

> The 2026 typography specialist. First-choice engine for BHIL report-cover headlines, whitepaper titles, LinkedIn tiles, and any deliverable where the typography itself is the visual.

## When to Choose Ideogram v3

| Use Case | Why Ideogram Wins |
| :--- | :--- |
| Editorial typographic posters | Strongest on-image text rendering at headline scale |
| LinkedIn / social tiles with bold headlines | Crisp legibility at small image sizes |
| Whitepaper covers where the title carries the visual | Typography is the model's first-class output, not a renderable afterthought |
| Quick text-driven brand assets at volume | Faster turnaround than Pro-tier flagships |
| Multi-line headline compositions | Reliable line-break behavior |

## When Not to Use Ideogram

- **Long-form body copy** — Nano Banana Pro is better at 100+ word legible passages.
- **Photographic editorial scenes** — Flux.2 and Midjourney lead.
- **Multi-image reference fusion** — not Ideogram's strength.
- **Complex framework diagrams** — GPT Image 2 plans layout better.
- **Air-gapped deployment** — closed model only.

## Prompting Discipline

The Ideogram v3 pattern in three rules:

### 1. Quote Exact Text Verbatim

The same rule as Nano Banana, more strongly enforced. Wrap exact text in quotation marks; assume anything unquoted will be paraphrased.

```text
Headline: 'GRAY-ZONE SIGNALS'
Subhead: 'A Quarterly OSINT Brief'
Footer: 'BHIL · Issue 014 · April 2026'
```

### 2. Break Long Headlines Into Multiple Short Quoted Blocks

For three-line stacked headlines, write each line as a separate quoted string:

```text
Headline rendered on three lines:
Line 1: 'Undersea Cable'
Line 2: 'Risk —'
Line 3: 'North Atlantic'
```

This produces more reliable line breaks than passing a single long string with `\n` characters or relying on the model's automatic wrapping.

### 3. Dictate Case Explicitly

Don't assume Ideogram will respect the case in your quoted string. Add an explicit instruction:

```text
... rendered in uppercase ...
... rendered in title case (initial capitals on major words) ...
... rendered in mixed case as written ...
```

The third option works only when you've already cased the quoted string yourself.

## Worked Example — Editorial Typographic Poster

```text
Editorial typographic poster, 2:3 portrait.

Top third: small monogram 'BHIL' in uppercase grotesk, letter-spaced
0.3em, in warm ivory.

Center: large headline in bold serif display, stacked on three lines:
Line 1: 'GRAY-ZONE'
Line 2: 'SIGNALS'
Line 3: 'Q2 2026'
Rendered in title case as written, left-aligned, generous tracking.

Below headline: thin divider rule in amber #C9A24A.

Subhead: 'Quarterly OSINT Brief from Barry Hurd Intelligence Lab' in
wide-tracked small caps, single line, centered.

Bottom: small footer text 'bhil.lab' in mono.

Swiss typographic style. Generous whitespace. Deep navy background.
Single amber accent line. Flat — no gradients, no 3D, no drop shadows.
```

This produces a print-ready cover with one render and one edit pass.

## Aspect Ratio Patterns That Work

Ideogram is reliable at:

- **1:1** — LinkedIn tiles, social squares
- **2:3 / 3:4** — magazine and report cover proportions
- **16:9** — slide hero images
- **4:5** — vertical social (Instagram, LinkedIn carousel covers)
- **21:9** — banners (less common; works but verify text legibility at width)

Ratios beyond these often produce typography that scales oddly. Stick to the standards.

## Color and Layout Discipline

Ideogram has a tendency toward saturated, "designed" output unless explicitly constrained. For BHIL register, default constraints to add at the end of every prompt:

```text
... swiss typographic discipline, generous margins, flat — no gradients,
no drop shadows, no 3D effects, no decorative ornaments. Restrained
editorial color palette (one accent maximum).
```

This is verbose but reliably keeps the output in BHIL's editorial register rather than drifting toward a more decorative consumer aesthetic.

## Compositing Workflow — The Ideogram + Midjourney Pattern

For deliverables that need both Midjourney's photographic register and Ideogram's typography (report covers especially), the pattern is:

1. Generate the background scene in Midjourney (with `--no text, watermark, logo` and a moodboard for brand register).
2. Generate the typography layer in Ideogram on a transparent background or matching solid color.
3. Composite in Figma (digital deliverables) or Photoshop (print).
4. Hand-tune kerning if needed; export the final.

This is documented as Recipe C in [`workflows/recipe-c-typography-compositing.md`](../../workflows/recipe-c-typography-compositing.md). Production prompt: [`prompts/07-typographic-posters/23-whitepaper-hero.md`](../../prompts/07-typographic-posters/23-whitepaper-hero.md).

## Failure Modes

- **Long single-line headlines** — break into multiple short quoted blocks.
- **No case dictation** — output may not match the case of your quoted string.
- **Default decorative settings** — every prompt should include the "swiss / restrained / no gradients" constraint block.
- **Trying to do scene + typography in one Ideogram render** — Ideogram's photographic backgrounds are weaker than Midjourney's. Use the compositing workflow instead.
- **Special characters in quoted strings** — em-dashes, en-dashes, and curly quotes sometimes render as straight equivalents. Verify and edit.

## Related

- [`docs/07-other-models.md`](../../docs/07-other-models.md) — chapter context.
- [`prompts/01-intelligence-report-covers/04-market-intelligence-whitepaper.md`](../../prompts/01-intelligence-report-covers/04-market-intelligence-whitepaper.md) — whitepaper cover.
- [`prompts/03-executive-briefing-deck/09-linkedin-tile.md`](../../prompts/03-executive-briefing-deck/09-linkedin-tile.md) — LinkedIn tile.
- [`prompts/03-executive-briefing-deck/12-carousel-cover.md`](../../prompts/03-executive-briefing-deck/12-carousel-cover.md) — carousel cover.
- [`prompts/07-typographic-posters/23-whitepaper-hero.md`](../../prompts/07-typographic-posters/23-whitepaper-hero.md) — typographic poster (composite).
- [`workflows/recipe-c-typography-compositing.md`](../../workflows/recipe-c-typography-compositing.md) — the Ideogram + Midjourney compositing pipeline.
