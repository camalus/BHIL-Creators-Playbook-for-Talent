# Personalization (`--p`) — Midjourney v7

Personalization is Midjourney's mechanism for binding *your taste* to your account. It is distinct from moodboards, although both surface as `--p` codes. Where a moodboard captures an explicit reference set, personalization captures the implicit signal of your pairwise image rankings over time.

## How It Works

1. Visit [midjourney.com/rank-v7](https://midjourney.com/rank-v7).
2. Midjourney shows you pairs of images and asks which you prefer.
3. After roughly **40 pairs**, you unlock a basic moodboard-tier profile.
4. After roughly **200 pairs**, you unlock the full personalization profile.
5. Midjourney returns a profile code (e.g., `bhil7`) usable as `--p bhil7`.

The profile updates as you continue rating. New ratings refine the profile; old codes remain valid even after refinement, so once you have shipped a deliverable with a particular `--p` state, that exact code will continue to produce a consistent register.

## Personalization vs Moodboards — The Distinction

| | Personalization Profile | Moodboard |
| :--- | :--- | :--- |
| **Built from** | Pairwise image rankings | Curated upload set |
| **Captures** | Operator's implicit taste | Explicit brand reference |
| **Best for** | Calibrated default register | Specific brand or deliverable type |
| **Stacking** | One profile per render | Multiple moodboards per render |
| **Onboarding** | 40–200 pairs of rating | 20–100 image upload |

Both surface as `--p [code]`. Both can be stacked in the same prompt. Treat personalization as the operator's calibrated taste and moodboards as approved brand references — and stack them together: `--p bhil7 bhil-cover`.

## Per-Version Profiles

Each Midjourney model version maintains its own personalization profile. A v7 `--p` code does not transfer to v6.1, and a v6.1 `--p` code does not work in v7. When v8 stabilizes and BHIL migrates, the personalization profile must be rebuilt against v8.

This is the cost of personalization: it is locally maximized, not portable. The 200 pairs of ranking that built the v7 profile do not carry forward.

## Stacking Profiles and Moodboards

Multiple `--p` codes are valid in a single prompt:

```text
--p bhil7 bhil-cover bhil-portrait
```

Order does not strictly matter, but convention is **operator profile first, then moodboards from most to least specific**. The model averages across all referenced profiles and moodboards; if the registers conflict, the result is muddy. Stack only profiles and moodboards that share an aesthetic register.

## Operational Discipline for BHIL

- **One operator per profile.** Don't share login credentials across team members for personalization. The signal degrades fast when two people with different taste co-rate the same profile.
- **Deliverable type, not personal preference.** When rating, calibrate against BHIL deliverables — would this image work as a report cover? — not against what you personally find pretty. The profile inherits whatever standard you rate against.
- **Re-rate quarterly.** 50 additional pairs every quarter keeps the profile current. Without ongoing ratings, the profile drifts toward whatever Midjourney's default aesthetic is doing.
- **Document the profile code.** When a deliverable ships, retain the `--p` code in the deliverable's metadata file. Reproducing the look six months later requires the exact same code.

## Failure Modes

- **Rating too quickly.** Pairwise rating is a thinking exercise, not a clicking exercise. The 5-second-per-pair operator builds a noisy profile.
- **Rating against personal aesthetics rather than brand needs.** A profile calibrated against personal taste produces aesthetically interesting work that doesn't ship as a BHIL deliverable.
- **Stacking too many moodboards on top of the profile.** `--p bhil7 bhil-cover bhil-framework bhil-portrait` produces an averaged result that serves no purpose well. Pick one moodboard plus the profile.
- **Treating `--p` as a brand lock.** It isn't. The profile is operator taste, not brand register. Brand register lives in moodboards and sref codes; personalization is the calibrated default the operator brings to the work.

## Related

- [Moodboards](./moodboards.md) — the explicit-reference counterpart to personalization.
- [Sref Library](./sref-library.md) — sref codes layer on top of `--p` for specific aesthetic locks.
- [Parameter Stacks](./parameter-stacks.md) — where `--p` appears in the four BHIL default stacks.
