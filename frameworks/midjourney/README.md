# Midjourney v7 — BHIL Production Framework

Midjourney v7 is the BHIL **aesthetic** engine. It owns mood discovery, cinematic register, and the persistent style system (Sref + moodboard + `--p`) that defines BHIL's visual brand.

This folder contains the full Midjourney production reference. The high-level orientation is in [`../../docs/02-midjourney.md`](../../docs/02-midjourney.md).

---

## Table of contents

| File | Covers |
| :--- | :--- |
| [`core-formula.md`](core-formula.md) | The descending-weight prompt hierarchy and the v6→v7 rewrite pattern |
| [`parameters.md`](parameters.md) | Every v7 parameter, what it does, and the BHIL practical range |
| [`parameter-stacks.md`](parameter-stacks.md) | The four BHIL default parameter stacks (cover, editorial, framework, portrait) |
| [`sref-library.md`](sref-library.md) | The Tatiana Tsiguleva curation discipline; how BHIL builds and stewards a brand Sref library |
| [`omni-reference.md`](omni-reference.md) | `--oref` for V7 character / object / garment lock; V6.1 `--cref` fallback |
| [`moodboards.md`](moodboards.md) | Persistent house style; when moodboards beat raw Sref stacks |
| [`personalization.md`](personalization.md) | The `--p` profile system and how to operate it for a team |

---

## When to reach for Midjourney

| You want | Use Midjourney |
| :--- | :--- |
| Default beauty, cinematic look | ✓ |
| Mood discovery, exploring a register | ✓ |
| Persistent brand aesthetic across deliverables | ✓ (Sref + moodboard) |
| A character that recurs across deliverables | ✓ (`--oref` in V7) |
| Editorial illustration, painterly realism | ✓ |
| Documentary / OSINT register | ✓ (`--style raw` + low `--s`) |
| Legible in-image typography | ✗ — go to Ideogram or Nano Banana Pro |
| Multi-image fusion with role assignment | ✗ — go to Nano Banana |
| Real-world facts / search grounding | ✗ — go to Nano Banana 2 |
| Air-gapped / on-prem | ✗ — go to Flux.2 [dev] |
| Strict edit fidelity, mask-free | ✗ — go to Flux.1 Kontext or Nano Banana |

---

## Production baseline (April 2026)

- **Pin `--v 7`** explicitly in every shared prompt. Never rely on "current default."
- **V8 alpha / V8.1 alpha** are web-only and not production-stable. Do not use for client work.
- **V6.1** is legacy. Use only when a workflow specifically requires `--cref` or older Sref codes authored against `--sv 4`.

---

## The fastest path to production-ready output

1. Read [`core-formula.md`](core-formula.md). Internalize the descending-weight hierarchy.
2. Read [`parameter-stacks.md`](parameter-stacks.md). Pick the stack matching your deliverable.
3. Find the closest copy-paste prompt in [`../../prompts/`](../../prompts/).
4. Replace bracketed fields. Run.
5. When 80% is right, **edit, don't regenerate** ([Rule 4](../../docs/01-foundational-rules.md#rule-4--iterate-in-the-same-chat--thread)).

---

## Where to go next

- Compare to Nano Banana: [`../nano-banana/README.md`](../nano-banana/README.md)
- The cross-platform recipes that combine MJ with other engines: [`../../workflows/`](../../workflows/)
