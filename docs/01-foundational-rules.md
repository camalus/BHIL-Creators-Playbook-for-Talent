# 01 · The Four Universal Rules

These four rules are model-agnostic. They apply equally to Midjourney v7, Nano Banana Pro, Flux.2, GPT Image 2, Ideogram v3, and any 2026 flagship that produces images from text. They are the foundation every prompt, framework, and workflow in this repository inherits from.

If a contribution to this repository violates one of these rules, it does not belong in the repository. Full stop.

---

## Rule 1 — Get specific

Every adjective you leave out, the model chooses for you.

- *"An executive at a desk"* gets you stock.
- *"A composed woman in her late 40s in a charcoal tailored blazer, standing at a glass-walled situation room at dusk, cool monitor glow on her left cheek, single warm practical behind her"* gets you a cover.

**Specificity is leverage.** Underwritten prompts produce average output regardless of which flagship you use.

### What "specific" actually requires

| Element | What you must specify |
| :--- | :--- |
| **Subject** | Age, posture, wardrobe, expression, identifying features |
| **Scene** | Time of day, materials, scale, occupancy, weather/atmosphere |
| **Lighting** | Direction, temperature, quality (soft/hard), key/fill/rim |
| **Camera** | Body, lens, aperture, shot size, height, movement |
| **Color** | Palette, grade, saturation register, dominant accents |
| **Style** | Medium, photographic register, director or photographer reference |

If your prompt is shorter than a shot-list entry from a real film production, it is underwritten. The cinematographer's vocabulary in [`../reference/`](../reference/) is the working dictionary for closing this gap.

### Diagnostic

Read your prompt aloud. Could a competent photographer go execute the shot from your description alone, with no follow-up questions? If not, it's not specific enough.

---

## Rule 2 — Describe what you want, not what you don't

Every 2026 flagship except Stable Diffusion has either weakened or removed support for negative prompts.

| Model | Negative-prompt support in 2026 |
| :--- | :--- |
| **Flux.2** | Dropped entirely |
| **Gemini (Nano Banana Pro / NB2)** | Rejected by the model |
| **Midjourney v7** | `--no` retained but blunt; use sparingly |
| **GPT Image 2** | Not supported in the conventional sense |
| **Stable Diffusion 3.5** | Traditional negative array still supported |

The reason this convergence happened is consistent across architectures: **diffusion and autoregressive systems reason by association.** Naming something — even to exclude it — increases its probability in the latent space. "A boardroom with no people" elevates the concept of *people* in the model's attention, raising the chance you get a partially populated room.

### The rewrite pattern

| Don't write | Write |
| :--- | :--- |
| "A boardroom with no people" | "An empty boardroom at dawn" |
| "Not plastic, not airbrushed" | "Natural skin texture, no retouching" |
| "Without text or watermarks" | (in MJ) `--no text, watermark, logo`<br>(elsewhere) describe the negative space |
| "Nothing in the foreground" | "Clean foreground, deep negative space, low-occupancy frame" |

### Narrow exceptions

- **Midjourney `--no text, watermark, logo`** for cover work — still useful and recommended in the BHIL parameter stacks.
- **SD 3.5 traditional negatives** when the open-weights pipeline calls for them.

Treat positive framing as the default and reach for negatives only for these documented cases.

---

## Rule 3 — Talk like a cinematographer

The vocabulary of professional image-making is what separates an AI result from a professional one.

> "Shot on Hasselblad with 80mm f/1.9, Rembrandt lighting from a tall window, muted editorial color palette, *The Economist* cover photography style."

That sentence works across Midjourney, Flux, Gemini, and GPT Image with almost no rewriting. It is an unambiguous instruction that maps to a real-world technique each model has seen referenced thousands of times in its training data.

> "Beautiful professional photo."

That sentence works nowhere. It is an aesthetic plea, not a specification.

### Why this rule disciplines you

Once you are naming lighting patterns by their textbook names — Rembrandt, chiaroscuro, three-point, golden hour backlight — you stop producing glossy AI-default images. The vocabulary itself prevents the failure mode.

The four reference tables in [`../reference/`](../reference/) are the authoritative working vocabulary. Mix one option from each (lighting × camera × color × materiality) when constructing any prompt. This is the fastest way to produce professional-grade results across every model in this playbook.

### The check

Could a film school student tell you what each technical term in your prompt means? If yes, you've passed the cinematographer test. If you've written "cinematic" or "8k" or "high quality" instead of an actual technique, you haven't.

---

## Rule 4 — Iterate in the same chat / thread

The 2026 generation of models reward conversational continuity.

| Model | Continuity mechanism |
| :--- | :--- |
| **Nano Banana / Pro / NB2** | Multi-turn chat preserves reasoning and visual state across edits |
| **GPT Image 2** | Same — conversational edit pattern is the recommended workflow |
| **Flux Kontext** | Mask-free, in-thread editing |
| **Midjourney v7** | Same prompt + same seed + small modification = continuity. Conversational Mode in Draft handles ideation similarly. |

Regenerating from scratch burns tokens and drifts composition. Editing in-thread preserves what's working and changes only what isn't.

### The 80/20 rule

> **When 80% is right, edit; do not regenerate.**
>
> This alone will cut your render budget by half and your time to final by more.

### The pattern in practice

For Nano Banana / GPT Image 2 / Flux Kontext, the canonical edit prompt is:

```text
Keep everything exactly the same. [SPECIFIC CHANGE]. Do not alter [LIST OF
ELEMENTS TO PRESERVE].
```

The explicit "keep everything else unchanged" is not redundant. It is the anchor that prevents drift across turns.

For Midjourney, the equivalent is:

- Lock the seed (`--seed XXXXXX`) once you have a base composition you like.
- Make small modifications to the prompt one at a time.
- Use Vary (Subtle) or Remix Mode rather than starting fresh.
- Keep the parameter stack stable across iterations — only change one variable at a time.

### Multi-turn cover iteration

The full five-turn cover example lives in [`../frameworks/nano-banana/framework-c-conversational-editing.md`](../frameworks/nano-banana/framework-c-conversational-editing.md) — it is the canonical demonstration of this rule.

---

## How the four rules compose

| Rule | What it adds | Why it matters |
| :--- | :--- | :--- |
| 1. Specificity | Information density | Determines the floor of output quality |
| 2. Positive framing | Latent-space hygiene | Prevents the model from hallucinating the things you asked it to exclude |
| 3. Cinematographer's vocabulary | Technique-mapped terminology | Maps your intent to real-world references the model has seen |
| 4. In-thread iteration | Continuity and efficiency | Preserves wins and contains drift while cutting token cost |

Internalize these. Every prompt in [`../prompts/`](../prompts/) and every workflow in [`../workflows/`](../workflows/) was built on this foundation.

---

## Where to go next

- The full [Midjourney v7 framework](../frameworks/midjourney/README.md)
- The full [Nano Banana / Gemini framework](../frameworks/nano-banana/README.md)
- The [Universal Creative Director Toolkit](../reference/README.md)
