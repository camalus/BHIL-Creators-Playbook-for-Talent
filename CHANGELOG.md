# Changelog

All notable changes to the BHIL Creator's Playbook for Advanced AI Image Generation will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [1.0.0] — 2026-04-27

Initial release. Codifies the BHIL April 2026 Field Playbook into a reproducible repository structure.

### Added

- **Foundational rules layer** — the four model-agnostic principles (specificity, positive framing, cinematographer's vocabulary, in-thread iteration) at `docs/01-foundational-rules.md`.
- **Midjourney v7 framework** — full parameter deep-dive (28 parameters), Sref library curation discipline, Omni-Reference (`--oref`) workflow, moodboard system, personalization (`--p`), and four BHIL default parameter stacks at `frameworks/midjourney/`.
- **Nano Banana / Gemini framework** — three-model comparison (NB, Pro, NB2), the five core frameworks (text-to-image, multi-image fusion, conversational editing, grounded prompts, typography), SynthID + C2PA disclosure protocol at `frameworks/nano-banana/`.
- **Other 2026 flagships** — capability briefs and BHIL use cases for Flux.2 Pro, GPT Image 2, Ideogram v3, Recraft V3, Stable Diffusion 3.5, and Adobe Firefly 4.
- **Universal Creative Director Toolkit** — model-agnostic vocabulary tables for lighting (8 options), camera + lens (10 options), color + film stock (8 options), and materiality + texture (9 options) at `reference/`.
- **Copy-paste prompt library** — 24 production-ready prompts across seven BHIL deliverable categories: intelligence report covers (4), framework diagrams (4), executive briefing deck visuals (4), data-intelligence hero imagery (4), character/persona design (3), geospatial/architectural renders (3), typographic posters (2).
- **Advanced workflows layer** — the Nano Banana → Veo 3.1 loop (7 steps), four cross-platform recipes (MJ→Runway, NB→MJ, Ideogram+MJ compositing, Kling+Veo long-form), and the four-pillar pipeline architecture at `workflows/`.
- **Templates** — per-model prompt scaffolds and a deliverable spec sheet at `templates/`.
- **CI/CD** — markdown lint, link check, and release packaging workflows at `.github/workflows/`.
- **Issue + PR templates** — prompt-improvement, new-prompt-request, and workflow-issue templates.
- **Governance** — README, CONTRIBUTING, CODE_OF_CONDUCT, SECURITY, and MIT LICENSE.

### Operating decisions

- **Pinned to Midjourney v7** as the production baseline; v8 alpha exists but is web-only and not production-stable.
- **NB2 as workhorse, Pro for final** — based on the cost/quality split documented in `frameworks/nano-banana/model-comparison.md`.
- **Sora 2 explicitly out of scope.** OpenAI announced shutdown on 2026-03-24; app closes 2026-04-26, API closes 2026-09-24.
- **Negative prompts deprecated by default.** Documented per-model exceptions in `docs/01-foundational-rules.md`.

---

## [Unreleased] — Roadmap

Planned for future versions. Items below are tracked but not committed.

### v1.1.0 — Sref Library Live Index (Q3 2026, target)

- Versioned, named Sref code registry with sample images and use-case tags.
- Moodboard governance — per-engagement moodboard naming, retention, and access control.
- Brand-fitness scoring rubric (0–10 across coherence, restraint, typographic discipline, palette adherence, photographic register).

### v1.2.0 — Veo 3.1 Motion Library (Q4 2026, target)

- 12–18 reusable motion prompts, mapped to the existing 24 still-image prompts.
- Audio directive cookbook (`SFX:`, `Ambient noise:`, dialogue conventions).
- Aleph color-match recipes for Kling/Veo continuity.

### v1.3.0 — On-Prem Pipeline (Flux.2 + SD 3.5) (Q1 2027, target)

- Air-gapped deployment guide for client-confidential work.
- BHIL brand LoRA training corpus and scripts.
- ControlNet preset library for deterministic composition.

### v2.0.0 — Re-baselined for the next model generation (when needed)

Triggered when one of the following happens:

- A new flagship displaces Midjourney v7 / NB2 as default workhorse.
- Veo 3.1 is replaced or significantly superseded.
- Negative-prompt support returns at scale (unlikely).
- C2PA enforcement becomes a regulatory requirement in BHIL's main jurisdictions.

---

## Version policy

- **Major (X.0.0)** — model lineup change that invalidates parameter tables, or pipeline architecture change that invalidates the four pillars.
- **Minor (1.X.0)** — new framework, new prompt category, new workflow recipe, or new model added to the matrix.
- **Patch (1.0.X)** — copy edits, link fixes, parameter value tuning within the existing model lineup, prompt refinements that don't change category structure.

[1.0.0]: https://github.com/camalus/BHIL-Creators-Playbook-Image-Generation/releases/tag/v1.0.0
