# BHIL Default Parameter Stacks (Midjourney v7)

Four parameter stacks cover roughly 80% of BHIL Midjourney production. They are the defaults; deviate only when you have a specific reason.

Replace bracketed fields with values from the BHIL brand vault before running.

---

## Stack 1 — Report Cover

**Use for:** Intelligence report covers, briefing covers, whitepaper covers — any deliverable where a restrained still-life or documentary-realism register dominates and the cover will be overlaid with typography in post.

```text
--v 7 --style raw --s 75 --ar 2:3
--p [BHIL PROFILE]
--no text, watermark, logo
```

**Rationale:**

- `--style raw` flips MJ from auto-beautification to literal interpretation. Without this, every cover drifts toward glossy.
- `--s 75` keeps stylization low. Documentary realism, not MJ-default editorial.
- `--ar 2:3` matches standard print/digital cover proportion.
- `--p [BHIL PROFILE]` applies the BHIL personalization profile so the cover lives in the brand register.
- `--no` block removes the most common cover-killing artifacts. Negative-prompt exception is justified here per [Rule 2](../../docs/01-foundational-rules.md#rule-2--describe-what-you-want-not-what-you-dont).

**Variants:**

- For 3:4 instead of 2:3 (slightly more square, less elongated): swap `--ar 3:4`.
- For framework-cover variant where one accent color must dominate, add `--sref [BHIL COVER SREFS] --sw 100`.

---

## Stack 2 — Editorial Punch (Executive Brief Hero)

**Use for:** Hero images for executive briefings, LinkedIn thought-leadership tiles, conference deck heroes, annual report opener spreads — any deliverable that needs to be visually striking inside a business context.

```text
--v 7 --s 200 --exp 15 --ar 3:2
--p [BHIL PROFILE]
--sref [BHIL COVER SREFS] --sw 120
```

**Rationale:**

- `--s 200` is editorial-with-style range. More aesthetic opinion than the cover stack.
- `--exp 15` is in the BHIL sweet spot (5–25). Adds editorial punch without overwhelming the personalization or Sref stack.
- `--ar 3:2` is the editorial-photography default ratio.
- `--sref` with the BHIL cover-line codes plus `--sw 120` keeps brand register without locking too tightly.

**Variants:**

- For 16:9 slide hero: swap `--ar 16:9`.
- For 21:9 banner: swap `--ar 21:9`. Recheck the composition; some shots that work in 3:2 collapse at 21:9.
- If output is drifting too dark: drop `--exp` to 10 or lift `--s` to 250.

---

## Stack 3 — Framework Diagram

**Use for:** Framework hero art, taxonomy illustrations, isometric pipeline visuals, schematic-style cover art for new BHIL frameworks (LOCUS, MERIDIAN, SENTINEL, etc.).

```text
--v 7 --s 300 --exp 15 --ar 16:9
--p [BHIL FRAMEWORK PROFILE]
--sref [BHIL FRAMEWORK SREFS] --sw 150
```

**Rationale:**

- `--s 300` enters the illustrative range. Frameworks are not photographs; they want stylization.
- `--exp 15` keeps the illustrative quality from going generic.
- `--ar 16:9` is the standard slide / hero ratio.
- A separate framework profile and Sref family — not the cover-line — keeps frameworks visually distinct from publication covers.
- `--sw 150` is a tighter Sref grip than the cover stack, because framework imagery is more sensitive to drift.

**Variants:**

- For a 1:1 social tile of the same framework: swap `--ar 1:1`. May require recomposing the prompt around a centered subject.
- For an unlabeled hero version (no diagram callouts): drop any text references in the prompt.
- For the labeled diagram version, **don't generate it in MJ** — go to Nano Banana Pro per the prompt library (Prompt 6).

---

## Stack 4 — Portrait

**Use for:** Executive portraits, persona art, recurring character imagery across a deliverable series.

```text
--v 7 --style raw --s 100 --ar 4:5
--p [BHIL PORTRAIT PROFILE]
--oref [EXEC REFERENCE URL] --ow 150
```

**Rationale:**

- `--style raw` for documentary realism. Portrait drift toward "AI portrait" aesthetic is the most common failure mode; `--style raw` is the strongest counter.
- `--s 100` is the balanced range for portraiture.
- `--ar 4:5` is the LinkedIn / dossier portrait standard.
- A separate portrait personalization profile keeps faces from picking up cover-aesthetic artifacts.
- `--oref [EXEC REFERENCE URL] --ow 150` is the V7 Omni-Reference identity lock. `--ow 150` is the practical default; raise if `--s` or `--exp` is fighting the identity.

**Variants:**

- For wardrobe / setting changes with the same face: keep `--oref`, lift `--ow` to 100, change wardrobe and environment in the prompt.
- For 3:2 environmental portraits: swap `--ar 3:2`. The portrait will widen; be specific about the environment in the prompt.
- For persona archetypes that are *not* a real person (no `--oref`): drop the `--oref` and `--ow` lines and use a moodboard `--p [BHIL PERSONA PROFILE]` instead.

---

## Anti-stacks — combinations to avoid

| Bad combination | Why |
| :--- | :--- |
| `--style raw --s 500 --exp 50` | Contradictory. `--style raw` says "literal," high `--s` and `--exp` say "stylize hard." Output is incoherent. |
| `--draft --oref [URL]` | Not compatible. Draft mode does not support Omni-Reference. |
| `--cref [URL] --v 7` | `--cref` is V6.1 only. Use `--oref` in V7. |
| `--sw 0 --p [profile]` | The Sref weight is off but the profile is on; you've nullified the Sref stack but kept the personalization. Probably not what you wanted. |
| Stacking 5+ Sref codes with `--sw 200+` | Smushes the codes into incoherent average; hold to 3–5 codes. |

---

## Where to go next

- The full parameter table: [`parameters.md`](parameters.md)
- Sref curation that produces the brand-vault codes referenced above: [`sref-library.md`](sref-library.md)
- The 24-prompt library, where these stacks are applied to specific deliverables: [`../../prompts/`](../../prompts/)
