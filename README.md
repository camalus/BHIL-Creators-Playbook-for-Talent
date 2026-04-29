# BHIL Creator's Playbook · Advanced AI Image Generation

> A 2026 production reference for intelligence-brand visuals.
>
> **Human-Directed. AI-Enabled. Commercially Tested.**

[![Markdown Lint](https://img.shields.io/badge/markdown-lint%20passing-brightgreen)]()
[![Link Check](https://img.shields.io/badge/links-checked-brightgreen)]()
[![Version](https://img.shields.io/badge/version-1.0.0-blue)]()
[![License](https://img.shields.io/badge/license-MIT-lightgrey)]()
[![BHIL Field Playbook](https://img.shields.io/badge/BHIL-Field%20Playbook-1f3a5f)]()

This repository is the operating system for BHIL's visual production practice. It codifies the prompt engineering, model routing, parameter discipline, and pipeline orchestration required to ship intelligence-brand visuals — report covers, framework diagrams, executive briefing imagery, OSINT-aesthetic social tiles, persona art, and geospatial renders — at the speed of analytical thinking.

It is **not** a curated list of "cool prompts." It is a working reference, organized so that any team member, six months from now, can reproduce any deliverable from the archive.

---

## Why this exists

The 2026 inflection point in AI image generation is not quality — every flagship now produces broadcast-grade output. The constraint is **discipline**. The delta between amateur and professional AI work is now almost entirely a prompting delta, layered on top of a model-routing and asset-management discipline.

BHIL's advantage is not picking the right model. It is operating a repeatable pipeline where **Midjourney owns aesthetic, Nano Banana owns iteration and text, Flux owns photorealism and on-prem, Ideogram owns typography, Veo owns motion**, and every asset is brand-locked, versioned, and archived.

This playbook is that operating system.

---

## What's in here

| Section | Path | Contents |
| :--- | :--- | :--- |
| **Foundational rules** | [`docs/01-foundational-rules.md`](docs/01-foundational-rules.md) | The four model-agnostic rules that govern every prompt in this repo |
| **Midjourney v7** | [`frameworks/midjourney/`](frameworks/midjourney/) | Core formula, full parameter deep-dive, Sref library discipline, Omni-Reference, moodboards, and BHIL default parameter stacks |
| **Nano Banana / Gemini** | [`frameworks/nano-banana/`](frameworks/nano-banana/) | Model comparison (NB / Pro / NB2), the five core frameworks (text-to-image, multi-image fusion, conversational editing, grounded prompts, typography), and SynthID + C2PA notes |
| **Other 2026 flagships** | [`frameworks/`](frameworks/) | Flux.2, GPT Image 2, Ideogram v3, Recraft V3, Stable Diffusion 3.5, Adobe Firefly 4 — strengths, BHIL use cases, and prompting register for each |
| **Creative Director Toolkit** | [`reference/`](reference/) | Lighting, camera + lens, color + film stock, materiality + texture — model-agnostic vocabulary tables |
| **Copy-paste prompt library** | [`prompts/`](prompts/) | 24 production-ready prompts across seven BHIL deliverable categories, each with bracketed customization fields |
| **Advanced workflows** | [`workflows/`](workflows/) | The Nano Banana → Veo loop, four cross-platform recipes, and the four pillars of a repeatable BHIL brand-visual pipeline |
| **Templates** | [`templates/`](templates/) | Prompt templates per model and a deliverable spec sheet for new visuals |
| **Examples** | [`examples/`](examples/) | Case studies and end-to-end deliverable walkthroughs |

The full table of contents lives in [`docs/00-introduction.md`](docs/00-introduction.md).

---

## How to use this repo

### If you're new to BHIL visual work

Read in this order:

1. [`docs/00-introduction.md`](docs/00-introduction.md) — what this is and why
2. [`docs/01-foundational-rules.md`](docs/01-foundational-rules.md) — the four universal rules
3. [`frameworks/midjourney/README.md`](frameworks/midjourney/README.md) and [`frameworks/nano-banana/README.md`](frameworks/nano-banana/README.md) — the two engines you'll use 80% of the time
4. [`reference/`](reference/) — the cinematographer's vocabulary
5. [`prompts/`](prompts/) — pick the deliverable category you need and adapt a copy-paste prompt

### If you're producing a deliverable today

1. Open [`templates/deliverable-spec-template.md`](templates/deliverable-spec-template.md) and fill it in. This forces you to commit to subject, lighting, palette, aspect ratio, and brand register **before** you start burning renders.
2. Route the spec to the right model using the matrix in [`docs/03-nano-banana-gemini.md`](docs/03-nano-banana-gemini.md#when-to-choose-nano-banana-vs-midjourney).
3. Find the closest copy-paste prompt in [`prompts/`](prompts/) and adapt the bracketed fields.
4. Iterate **in the same chat or on the same seed** (see [Rule 4](docs/01-foundational-rules.md#rule-4--iterate-in-the-same-chat--thread)).
5. When you're done, archive the deliverable per the metadata convention in [`workflows/pipeline-pillars.md`](workflows/pipeline-pillars.md).

### If you're operationalizing this for a team

Start at [`workflows/pipeline-pillars.md`](workflows/pipeline-pillars.md). The four pillars (Aesthetic Lock, Character Library, Asset Management, Orchestration) are the difference between a consultancy that uses AI and one that has operationalized it.

---

## The four operating principles

These show up everywhere in the repo. Internalize them before anything else.

| # | Principle | Where it lives |
| :--- | :--- | :--- |
| 1 | **Get specific.** Every adjective you leave out, the model chooses for you. | [`docs/01-foundational-rules.md#rule-1`](docs/01-foundational-rules.md#rule-1--get-specific) |
| 2 | **Describe what you want, not what you don't.** Negatives are deprecated or harmful in 2026 flagships. | [`docs/01-foundational-rules.md#rule-2`](docs/01-foundational-rules.md#rule-2--describe-what-you-want-not-what-you-dont) |
| 3 | **Talk like a cinematographer.** Camera body, lens, aperture, lighting pattern, film stock, shot size, director reference. | [`docs/01-foundational-rules.md#rule-3`](docs/01-foundational-rules.md#rule-3--talk-like-a-cinematographer) |
| 4 | **Iterate in the same chat / thread.** When 80% is right, edit. Don't regenerate. | [`docs/01-foundational-rules.md#rule-4`](docs/01-foundational-rules.md#rule-4--iterate-in-the-same-chat--thread) |

---

## What this repo is not

- **Not** a generative-AI ethics primer. SynthID + C2PA disclosure is treated as operational reality (see [`frameworks/nano-banana/synthid-c2pa.md`](frameworks/nano-banana/synthid-c2pa.md)), not a debate.
- **Not** an e-commerce or creator-economy resource. No product photography conventions, no thumbnail-bait advice, no "make this look beautiful" prompting.
- **Not** model-evangelism. Each framework folder includes the failure modes and the cases where another tool wins.
- **Not** an introduction to image generation. We assume you know what an aspect ratio is and that you've used at least one of these tools before.

---

## Versioning and stability

This playbook is versioned against the 2026 model landscape:

- **Midjourney v7** is the baseline; v8 alpha exists but is web-only and not production-stable.
- **Nano Banana 2** (`gemini-3.1-flash-image-preview`, Feb 2026) is the everyday workhorse; **Nano Banana Pro** (`gemini-3-pro-image-preview`) is reserved for final deliverables and 4K text-heavy covers.
- **Veo 3.1** is the motion target; **do not build on Sora 2** — OpenAI announced shutdown March 24, 2026.

When the models change again — and they will, in roughly six months — the discipline does not. Update the parameter tables; the principles in [`docs/01-foundational-rules.md`](docs/01-foundational-rules.md) and [`workflows/pipeline-pillars.md`](workflows/pipeline-pillars.md) hold.

See [`CHANGELOG.md`](CHANGELOG.md) for version history and the planned roadmap.

---

## Repository conventions

- **Prompt files** live in [`prompts/<category>/<NN>-<name>.md`](prompts/) and follow the template in [`templates/prompt-template-midjourney.md`](templates/) (or the appropriate model template).
- **Bracketed fields** like `[ACCENT COLOR]`, `[CLIENT CODE NAME]`, `[BHIL PROFILE]` are customization points. Replace them; never ship a prompt with brackets in it.
- **Sref codes** like `1742826451` in this repo are illustrative placeholders. Real BHIL brand codes live in the access-controlled [Sref library](frameworks/midjourney/sref-library.md) — not in this public reference.
- **No real client deliverables** are committed. Use redacted or synthetic examples in [`examples/`](examples/).

---

## Contributing

This is an internal BHIL reference, but contributions follow the same discipline as the [ADR Blueprint](https://github.com/camalus/BHIL-AI-First-Development-Toolkit). See [`CONTRIBUTING.md`](CONTRIBUTING.md) for prompt submission guidelines, the review checklist, and the brand-fitness criteria new prompts must clear.

---

## License

[MIT](LICENSE). The text of this playbook is freely usable. The Sref codes, moodboard IDs, character refs, and brand assets it references are not — those remain BHIL property and are documented separately in the access-controlled brand vault.

---

## Maintainer

**Barry Hurd** — Barry Hurd Intelligence Lab (BHIL)
Frameworks: MERIDIAN · LOCUS · SENTINEL · VANTAGE · VERDICT · CODEX

> *The models will change again in six months. The discipline will not.*
