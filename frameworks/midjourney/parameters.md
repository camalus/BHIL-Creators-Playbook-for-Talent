# Midjourney v7 — Full Parameter Reference

Every v7 parameter, what it controls, and the BHIL practical range. This is a reference document, not a tutorial — read [`core-formula.md`](core-formula.md) first if you're new to Midjourney.

---

## Version, aspect, and base settings

### `--v`

**Function:** Model version.

**BHIL practice:** **Pin `--v 7`** explicitly in shared prompts. Use `--v 6.1` only for legacy `--cref` workflows or older Sref codes authored against the v4 style interpreter (`--sv 4`). Do not use v8 alpha or v8.1 alpha for production.

### `--ar`

**Function:** Aspect ratio. **Changes composition, not just crop.**

**BHIL ratios by deliverable:**

| Ratio | Use |
| :--- | :--- |
| `2:3` or `3:4` | Report covers (vertical) |
| `16:9` | Framework hero, slide visuals |
| `21:9` | Executive banners |
| `4:5` | LinkedIn portraits, carousel covers |
| `1:1` | Social tiles, taxonomy diagrams |

### `--style raw`

**Function:** Disables MJ's auto-beautification.

**BHIL practice:** **Single most important parameter for intelligence imagery.** Flips MJ from "cinematic flair" to "literal interpretation." Pair with low `--s` (50–100) for documentary realism. Without `--style raw`, MJ pulls every prompt toward its house aesthetic; with it, you get what you actually wrote.

---

## Aesthetic strength controls

### `--s` / `--stylize`

**Function:** Strength of MJ's aesthetic opinion (0–1000).

| Range | Register |
| :--- | :--- |
| 0–50 | Literal / product photography |
| 50–150 | Balanced editorial |
| 150–300 | Editorial with style |
| 300–500 | Illustrative / stylized |
| 500+ | Heavily interpretive |

**BHIL defaults:** 50–150 for covers, 200–400 for frameworks, 100 for portraits.

### `--c` / `--chaos`

**Function:** Variety across the four-image grid (0–100).

| Range | Use |
| :--- | :--- |
| 0–25 | Final renders, when prompt adherence matters most |
| 50–75 | Exploration, brainstorming |
| 75+ | Prompt adherence drops sharply; rare for production |

### `--weird` / `--w`

**Function:** Aesthetic unconventionality (0–3000).

**BHIL practice:** 300–800 useful for OSINT "glitchy surveillance" covers. Above 2000 is exploration-only.

### `--exp`

**Function:** V7 experimental aesthetic (0–100). Released April 2025.

**BHIL sweet spot:** 5–25. Above 50, `--exp` overwhelms `--stylize` and `--p`. The house editorial-punch setting is `--exp 10 --s 150`.

---

## Image and reference parameters

### `--iw`

**Function:** Image weight for an attached prompt image (0–2).

| Range | Effect |
| :--- | :--- |
| < 1 | Text wins |
| > 1 | Image wins |
| 0.5–1.0 | Brand reference shapes output, prompt still drives |
| 1.5–2 | Near-variations of the input image |

### `--cref`

**Function:** Character Reference (V6.1).

**Notes:**

- Accepts one or multiple image URLs.
- Works best when the reference is itself MJ-generated.
- Use `--v 6.1` explicitly when invoking.
- **In V7, use `--oref` instead.**

### `--cw`

**Function:** Character Weight (0–100, default 100).

| Setting | Behavior |
| :--- | :--- |
| `--cw 100` | Copies face, hair, AND clothing |
| `--cw 0` | Copies face only — the right setting when you want the same person in new outfits, eras, or settings |

---

## Style and personalization

### `--sref`

**Function:** Style Reference. Accepts a URL, a numeric code, or `random`.

**Notes:**

- Does **not** copy subjects, only the aesthetic signature.
- Stack multiple: `--sref 1742826451 689668977 2216056865`.
- `--sref random --r 10` harvests 10 codes in one shot for discovery.

Full Sref discipline in [`sref-library.md`](sref-library.md).

### `--sw`

**Function:** Style Weight (0–1000, default 100).

**Practical range:** 65–175.

**Discovery protocol:** Test new codes at `--sw 1000 --s 0` first to see the style raw, then drop to 100–300 for production.

### `--sv`

**Function:** Sref interpreter version. V7 supports 1, 2, 3, 4, 6.

**Critical:** V7 defaults to `--sv 6`, but **legacy V6-era codes were authored against `--sv 4`.** If an old favorite stopped working, add `--sv 4`.

### `--p` / `--profile`

**Function:** Personalization (profile or moodboard code).

**Unlock:** Rate ~200 image pairs at `midjourney.com/rank-v7` for the personalization profile (~40 ratings for a basic moodboard).

**Stacking:** Free-form. Stack multiple `--p` codes: `--p bhil7 bhil-cover`.

Full personalization workflow in [`personalization.md`](personalization.md). Moodboard guidance in [`moodboards.md`](moodboards.md).

---

## Omni-Reference (V7-only)

### `--oref`

**Function:** Omni-Reference. Released May 2025. **Replaces `--cref` in V7.**

**Handles:** Characters, objects, garments, vehicles, logos. A single mechanism for locking any visual element.

**Cost:** 2× GPU time per render.

### `--ow`

**Function:** Omni-Weight (1–1000, default 100).

**Practical range:** 50–250.

**Tuning rule:** Higher `--ow` is needed when you also have high `--stylize` or `--exp` — the stylization fights the identity lock, and `--ow` is the counterweight.

| Use case | `--ow` |
| :--- | :--- |
| Photo → illustration translation | 40–100 |
| Strict identity lock across deliverables | 200–400 |

Full Omni-Reference workflow in [`omni-reference.md`](omni-reference.md).

---

## Negative prompts

### `--no`

**Function:** Negative prompt (comma-separated).

**BHIL practice:** Keep short (3–5 items). Stock list for cover work:

```text
--no text, watermark, signature, frame, border, logo
```

This is the narrow exception to [Rule 2](../../docs/01-foundational-rules.md#rule-2--describe-what-you-want-not-what-you-dont). Outside cover work, prefer positive framing.

---

## Quality, repetition, and rendering

### `--q`

**Function:** Quality / render-time budget (0.25–4).

**BHIL practice:** Keep at 1 for production. Use `--q 2` for final hero renders where fine texture matters.

### `--tile`

**Function:** Produces a seamlessly tileable texture.

**Use:** Brand background fills across section headers and tileable poster textures.

### `--repeat` / `--r`

**Function:** Run the same prompt N times.

**Discovery use:** `--sref random --r 10` for bulk Sref code discovery.

### `--seed`

**Function:** Fix the noise field.

**Notes:** ~99% reliable within a session in V7. **Use to hold composition while iterating small prompt changes** — this is the Midjourney equivalent of [Rule 4](../../docs/01-foundational-rules.md#rule-4--iterate-in-the-same-chat--thread).

### `--draft`

**Function:** Draft Mode — 10× faster, 50% GPU cost.

**Notes:**

- V7-exclusive.
- Pairs with Conversational Mode for rapid ideation.
- "Enhance" reruns a draft at full quality.
- **Not compatible with `--oref`.**

---

## Deprecated in v7

### `::` (weighted multi-prompt)

**Function (V6.1 legacy):** Numeric weighting of prompt elements.

**Status in V7:** **Not officially supported. Treat as deprecated.**

**Replacement:** Use natural-language emphasis and reordering instead. The descending-weight hierarchy in [`core-formula.md`](core-formula.md) already does this.

---

## Parameter combination notes

A few combinations matter enough to call out:

- **`--style raw` + low `--s`** = the documentary-realism setting. The BHIL OSINT default.
- **`--exp 10 --s 150`** = the editorial-punch setting. The BHIL hero-image default.
- **`--oref [URL] --ow 150`** with high `--s` or `--exp` = identity preserved through stylization. Raise `--ow` higher if the stylization is winning.
- **`--draft` + Conversational Mode** = the ideation loop. Lock final candidates by re-running at full quality with `--q 1` or `--q 2`.
- **`--sref random --r 10`** = the Sref discovery loop. Run across multiple prompt archetypes per [`sref-library.md`](sref-library.md).

---

## Where to go next

- The four BHIL default parameter stacks: [`parameter-stacks.md`](parameter-stacks.md)
- Sref curation discipline: [`sref-library.md`](sref-library.md)
- Omni-Reference workflow: [`omni-reference.md`](omni-reference.md)
