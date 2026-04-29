# 07 · The Other 2026 Flagships at a Glance

Beyond Midjourney and Nano Banana, six flagships round out the BHIL production matrix. Each has a specific BHIL use case and a specific failure mode if used outside it. This document is the routing reference; the per-model deep-dives live in [`../frameworks/`](../frameworks/).

---

## Quick matrix

| Model | Released | Strength | BHIL Use Case |
| :--- | :--- | :--- | :--- |
| **OpenAI GPT Image 2** | April 2026 | Reasoning-integrated; near-perfect text rendering; plans composition before rendering | Framework diagrams and cover art where layout reasoning matters more than aesthetic defaults |
| **Black Forest Labs Flux.2** | November 2025 | 24B Mistral-3 vision-language model + rectified-flow transformer; leading photorealism and prompt adherence | Air-gapped / on-prem when client confidentiality requires it; mask-free editing via Flux.1 Kontext |
| **Ideogram v3** | (current 2026) | Typography specialist | First-choice for headlines, whitepaper titles, LinkedIn tiles |
| **Stable Diffusion 3.5 Large** | (current 2026) | Open-weights flagship with the LoRA / ControlNet ecosystem | When data cannot leave the building, or when training a BHIL brand LoRA on prior deliverables |
| **Recraft V3** | (current 2026) | True scalable vector output — only model that does | BHIL icons, logo variations, framework SVGs, cover templates that will live in Illustrator |
| **Adobe Firefly 4** | (current 2026) | Only "commercially safe" model — licensed/owned/public-domain training data, IP indemnification, C2PA Content Credentials | Regulated-industry BHIL clients (finance, defense, legal) where indemnification is the deciding factor |
| **Leonardo Phoenix / Reve / Krea** | (current 2026) | Credible second-tier options | Krea's real-time multi-model aggregator for rapid ideation; Leonardo when LoRA beats complexity; Reve worth A/B testing against Ideogram |

---

## GPT Image 2 (April 2026)

The reasoning advantage is real. GPT Image 2 plans composition before rendering, which makes it the strongest tool for **complex infographics and dense diagrams** — anything where the layout has to be right at the macro level before you start judging it on aesthetics.

**Prompting register:** long descriptive prose, with the **Change / Preserve / Constraints** pattern for edits.

```text
Change: [the specific edit]
Preserve: [what must remain identical]
Constraints: [what the model must not introduce]
```

Documented in [`../frameworks/gpt-image-2/README.md`](../frameworks/gpt-image-2/README.md).

---

## Flux.2 (November 2025) — and Flux.1 Kontext

Flux.2 is a 24B-parameter vision-language model paired with a rectified-flow transformer. The Flux family leads on **photorealism** and **prompt adherence** — two qualities Midjourney compromises for aesthetic flair.

**The deciding factor for client-confidential work:** Flux is the only flagship-grade option you can run **air-gapped**.

- **Flux.2 [dev]** — open weights
- **Flux.2 [klein]** — Apache 2.0

For mask-free editing of an existing image, **Flux.1 Kontext** is the best engine on the market.

Documented in [`../frameworks/flux/README.md`](../frameworks/flux/README.md).

---

## Ideogram v3

The typography specialist. When the deliverable demands **legible, accurate, typographically disciplined on-image text** — headlines, whitepaper titles, LinkedIn tiles, social carousels — Ideogram beats every other 2026 flagship.

**The rules:**

- Wrap exact text in quotation marks.
- Break long headlines into multiple short quoted blocks.
- Dictate case explicitly ("uppercase," "title case").
- Specify typography descriptively ("bold condensed sans-serif, Helvetica-like").

For composite deliverables (typography + scene), Ideogram pairs with Midjourney via Recipe C in the workflows folder. Documented in [`../frameworks/ideogram/README.md`](../frameworks/ideogram/README.md).

---

## Stable Diffusion 3.5 Large

Not best-in-class output. The reason SD 3.5 stays in the BHIL matrix is the **ecosystem**: LoRA, ControlNet, IP-Adapter, T2I-Adapter, and the broader open-weights tooling that makes deterministic on-prem pipelines possible.

**Use SD 3.5 when:**

- Data cannot leave the building.
- You need a BHIL brand LoRA trained on prior deliverables.
- You need ControlNet for deterministic composition control.

Documented in [`../frameworks/stable-diffusion/README.md`](../frameworks/stable-diffusion/README.md).

---

## Recraft V3

Recraft V3 is the only flagship that produces **true scalable vector output** (real SVG, not raster traced to vector).

**Use Recraft V3 for:**

- BHIL icons and logo variations
- Framework SVGs that need to be edited in Illustrator
- Print-ready conference and keynote posters
- Anything that will live in a deck and need to scale

Documented in [`../frameworks/recraft/README.md`](../frameworks/recraft/README.md).

---

## Adobe Firefly 4

The only **commercially safe** model — trained on licensed / owned / public-domain data, with IP indemnification and C2PA Content Credentials baked in.

**Quality is not best-in-class.** The reason Firefly is in the matrix is **defensibility**.

**Use Firefly when:**

- The client is in finance, defense, legal, or another regulated industry.
- Indemnification is contractually required.
- A C2PA paper trail is part of the deliverable.

Trade aesthetic ceiling for legal defensibility, and document the trade in the methodology note. Documented in [`../frameworks/firefly/README.md`](../frameworks/firefly/README.md).

---

## The second tier — Leonardo, Reve, Krea

Worth knowing about; not BHIL defaults.

- **Krea** — real-time multi-model aggregator. Most useful for **rapid ideation** when you don't yet know which engine you want.
- **Leonardo Phoenix** — consistent-character training. Useful when LoRA beats complexity.
- **Reve** — typographic register. Worth A/B testing against Ideogram for cover work.

None of these have dedicated deep-dive folders; they're documented sufficiently here.

---

## Where to go next

- Per-model deep-dives in [`../frameworks/`](../frameworks/)
- The cross-platform recipes that combine these models: [`../workflows/`](../workflows/)
