# Moodboards — Midjourney v7

Moodboards are Midjourney's mechanism for binding a persistent house aesthetic to your account. They sit alongside `--sref` codes and personalization profiles but solve a different problem: where `--sref` is a one-off vibe and `--p` is your individual ranked taste, a moodboard is a curated brand reference set that anyone working under your account can invoke.

## What a Moodboard Is

A moodboard is a curated set of 20–100+ reference images uploaded to your Midjourney account. Midjourney analyzes the visual signature across the full set — palette, composition habits, materials, lighting register — and returns a moodboard ID that surfaces as `--p <moodboard-id>` in any prompt.

Unlike a single sref code (which captures one image's signature), a moodboard captures a **distribution** — the central tendency of your reference set. This is what makes it suitable for brand work: the model is averaging across many reference images, so any individual reference's quirks get smoothed out.

## Why Moodboards Beat Raw `--sref` for BHIL Work

`--sref` is right for: discovery, one-off mood matching, mixing multiple aesthetic directions in a single prompt.

Moodboards are right for: persistent brand register, multi-deliverable consistency, onboarding new operators who shouldn't have to memorize seven sref codes to render a BHIL cover.

In a production environment, the moodboard is closer to a design system token — it represents an approved visual register, not a creative experiment.

## Building a BHIL Moodboard

Navigate to [midjourney.com](https://midjourney.com) → Personalize → Create Moodboard.

1. Upload 20–100+ images that represent the target aesthetic. The richer the set, the more stable the moodboard. Below 20 images, results are erratic.
2. Mix sources: prior MJ outputs you've shipped, photographic references from editorial publications (*Foreign Affairs*, *The Economist*, *MIT Technology Review*, *Bloomberg Businessweek*), film stills, fine-art photography. Avoid mixing aesthetic registers — a moodboard with both *Foreign Affairs* covers and *Vogue* editorials will produce a confused average.
3. Save and name. Midjourney returns a moodboard ID resembling `bhil-cover` or a generated string. Document the ID, the image set, and the intended use case.
4. Test against three prompt types: a portrait, a still-life, an environmental shot. If the moodboard collapses on any of them, refine the reference set.

## The Three BHIL Moodboards (Recommended Minimum)

| Moodboard | Purpose | Reference Sources |
| :--- | :--- | :--- |
| `BHIL-Cover` | Report covers, whitepaper hero images, OSINT publication aesthetics | *Foreign Affairs* covers, archival document photography, restrained editorial still-life |
| `BHIL-Framework` | Diagrams, isometric renders, technical illustration | Bauhaus infographic, Otl Aicher pictogram systems, Pentagram editorial diagrams, Nicholas Felton information design |
| `BHIL-Portrait` | Executive portraiture, persona art | *The Economist* portrait covers, Annie Leibovitz editorial work, Platon's political portraits, restrained Hasselblad/medium-format register |

Some practices add a fourth — `BHIL-Geospatial` for satellite, tilt-shift, and architectural location renders. Build it once you've shipped enough geospatial deliverables to have a coherent reference set.

## Stacking Moodboards with Sref Codes

Moodboards and sref codes coexist. The full stack pattern:

```text
--p bhil7 bhil-cover --sref 1742826451 --sw 120 --s 200 --exp 15 --ar 3:2 --v 7
```

Reading right-to-left: this is a v7 render in 3:2 (editorial punch ratio), at moderate stylize and exp, locked to brand sref code 1742826451 at standard sref weight 120, drawing on both the operator's personal `bhil7` profile and the `bhil-cover` moodboard. The moodboard provides the brand register; the sref provides the aesthetic detail; the personalization provides the operator's calibrated taste.

## Moodboards Are Versioned Per Model

A v7 moodboard does not transfer to v6.1 or v8 alpha. Each Midjourney version interprets reference images through its own style interpreter. If Midjourney releases v8 stable in the second half of 2026, the BHIL moodboards will need to be re-built from the same reference sets — fast work, but plan for it.

## Maintenance Discipline

- **Quarterly review.** Add new shipped deliverables to the brand moodboards; remove any references that no longer represent the current direction.
- **Access control.** Moodboards live on the Midjourney account that owns them. Use a single shared BHIL Midjourney workspace, not personal accounts. This is the same governance principle as a design system in Figma.
- **Documentation.** For each moodboard, maintain a one-page note: ID, intended use, reference sources, last updated, sample renders at three prompt types.
- **Pair with sref codes, not in place of them.** Moodboards set the register; sref codes lock the specific signature. Both are needed for production work.

## Failure Modes

- **Too few references** (<20) — moodboard is unstable across prompt types.
- **Mixed registers** — combining editorial and consumer-marketing imagery produces an average that satisfies neither.
- **Stale references** — a moodboard built on 2023 imagery will feel dated by late 2026. Treat moodboards as living artifacts.
- **Over-stacking** — `--p bhil7 bhil-cover bhil-framework bhil-portrait` muddles the signal. Pick one moodboard per deliverable type.

## Related

- [Sref Library](./sref-library.md) — the curation discipline for sref codes that complement moodboards.
- [Personalization](./personalization.md) — `--p` as a profile vs `--p` as a moodboard ID.
- [Parameter Stacks](./parameter-stacks.md) — where moodboards appear in the four BHIL default stacks.
