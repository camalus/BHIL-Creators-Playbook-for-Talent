# Contributing to the BHIL Creator's Playbook

This is an internal BHIL reference, not a community-driven open-source project. Contributions are welcome from BHIL team members, contractors, and credentialed collaborators, and they are held to the same standard as the rest of the playbook.

The bar is **production-grade, brand-coherent, reproducible**.

---

## Before you contribute

Read these in order:

1. [`README.md`](README.md) — orientation
2. [`docs/01-foundational-rules.md`](docs/01-foundational-rules.md) — the four universal rules
3. [`workflows/pipeline-pillars.md`](workflows/pipeline-pillars.md) — how the repository fits into BHIL's larger production system
4. The framework folder for the model your contribution targets (e.g. [`frameworks/midjourney/`](frameworks/midjourney/))

If your contribution does not align with the four foundational rules and the relevant framework's prompting register, it will not be merged. This is not a stylistic preference — it is the brand discipline the playbook exists to enforce.

---

## What contributions look like

### 1. New prompts (most common)

If you have shipped a deliverable using a prompt and want to upstream it:

- File it in the correct [`prompts/<category>/`](prompts/) folder using the next sequential number (e.g. `25-something.md` if 24 is the last).
- Follow the prompt template in [`templates/`](templates/) for the model the prompt targets.
- Include all bracketed customization fields (`[ACCENT COLOR]`, `[CLIENT CODE NAME]`, etc.) — never hardcode a specific BHIL deliverable into a copy-paste prompt.
- Document the recommended model, recommended parameters, and at least one rendered example reference (image not required in the repo, but a verified-working seed or note is).
- Add an entry to the relevant category README's index.

### 2. Parameter table updates

If a flagship model's parameter behavior changes (a new `--exp` sweet spot, a new aspect ratio, a parameter deprecation):

- Update the relevant table in [`frameworks/<model>/parameters.md`](frameworks/) (or equivalent).
- Add a CHANGELOG entry under the next minor version.
- Note the discovery date and the source (release notes, official guide, or empirical test with at least 30 renders).

### 3. New workflow recipes

If you've validated a new cross-platform pipeline:

- File it as a new recipe in [`workflows/`](workflows/) using the existing recipe format.
- Document the failure modes you encountered, not just the success path.
- Specify cost characteristics (credits per render, GPU time, wall-clock) where relevant.

### 4. Framework documentation for a new model

If a new flagship hits the BHIL production matrix:

- Create a new folder under [`frameworks/<model-name>/`](frameworks/) following the structure of the existing framework folders.
- Minimum scope: README, parameters or capabilities reference, prompting register notes, and one worked example.
- Add the model to the matrix in [`docs/07-other-models.md`](docs/07-other-models.md).

---

## Review checklist

Every PR is reviewed against this checklist. Don't open a PR until your contribution clears all of these.

### Brand fitness

- [ ] The prompt or framework adheres to the **restrained editorial realism** register (see [`docs/00-introduction.md`](docs/00-introduction.md)).
- [ ] No e-commerce, creator-economy, glossy "make this beautiful" language.
- [ ] No real-world flags, insignia, or identifiable human faces unless explicitly part of an executive portrait workflow with a documented `--oref`.
- [ ] No real client names, projects, or assets — even in examples. Use synthetic or redacted equivalents.

### Prompting discipline

- [ ] Adheres to the four foundational rules (specific, positive framing, cinematographer's vocabulary, in-thread iteration).
- [ ] Bracketed customization fields are present and consistently named.
- [ ] Parameter syntax is correct for the target model and version.
- [ ] No deprecated parameters (e.g. weighted multi-prompt `::` in v7 contexts).
- [ ] No leftover negative-prompt language in models that no longer support it.

### Repository hygiene

- [ ] Files are in the correct folder.
- [ ] Filename matches the convention (`NN-kebab-case-name.md` for prompts).
- [ ] Markdown lints clean (the CI workflow will catch this).
- [ ] All internal links resolve (the link-check workflow will catch this).
- [ ] No images committed unless they're truly load-bearing (this is a text reference; visuals live in the brand vault).

### Reproducibility

- [ ] At least one seed, character ref, or worked example is documented.
- [ ] Recommended model and version are explicit.
- [ ] Cost and time characteristics are noted where they're meaningful.

---

## What we don't merge

- Prompts that work but are off-brand (overly stylized, glossy, kitsch, AI-default-aesthetic).
- "Found a cool sref" PRs without the [Sref curation discipline](frameworks/midjourney/sref-library.md) (stress-test against three unrelated prompt types).
- Workflow recipes built on Sora 2 (deprecated; do not use).
- Anything that hardcodes a real client deliverable into a "reusable" template.
- Changes that contradict the four foundational rules without an extremely well-argued exception note in the PR.

---

## Submission format

```text
type(scope): short summary

Optional longer body explaining the why, not the what.
```

Types: `add`, `update`, `fix`, `docs`, `refactor`, `chore`.
Scopes: `mj`, `nb`, `flux`, `gpt`, `ideogram`, `recraft`, `sd`, `firefly`, `prompts`, `workflows`, `reference`, `templates`, `ci`, `meta`.

Examples:

- `add(prompts): cover prompt for tabletop wargame brief`
- `update(mj): correct --exp sweet spot following v7.1 changes`
- `fix(workflows): remove broken Sora 2 reference`
- `docs(meta): clarify Sref vs moodboard distinction in main README`

---

## Code of conduct

See [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md). Short version: be precise, be honest about failure modes, don't sandbag knowledge, don't perform expertise.

---

## Who reviews

PRs are reviewed by Barry Hurd or a delegated reviewer with merge rights. Expect substantive feedback — this repo is the brand. There is no light-touch review.
