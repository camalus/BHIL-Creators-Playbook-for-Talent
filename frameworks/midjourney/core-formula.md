# The Core Midjourney Formula

V7 is **not a keyword engine.** V6 rewarded comma-soup. V7 punishes it.

V7 parses prompts as full natural-language sentences organized into a descriptive hierarchy. Writing for Midjourney now means writing like a cinematographer drafting a shot list, not like an SEO copywriter stacking keywords.

---

## The formula

```text
[SUBJECT] [SUBJECT DETAILS], [CONTEXT], [STYLE/MEDIUM],
[TECHNICAL — camera / lens / lighting / medium]
--parameters
```

---

## The descending-weight hierarchy

| Rank | Element | Function |
| :--- | :--- | :--- |
| 1 | **Subject** | What the image is *of* |
| 2 | **Subject Details** | Age, posture, wardrobe, expression |
| 3 | **Context** | Time of day, environment, scale, occupancy |
| 4 | **Style / Medium** | Photographic register, illustration style, director reference |
| 5 | **Technical** | Camera body, lens, aperture, lighting pattern, color grade |
| 6 | **Parameters** | The flag stack |

**Lead with what you see, not what you want.**

The model parses left-to-right with diminishing attention. The first 30 tokens have the most influence on composition; the next 50 tokens shape style; anything beyond ~150 tokens rarely changes the output meaningfully.

---

## Position effects to know

- **Medium at the start or end of the prompt** carries more weight than medium in the middle. If "editorial photography" or "isometric illustration" is critical, surface it.
- **Adjectives stack heavily.** "Moody, atmospheric, cinematic" registers as three reinforcing pulls in the same direction. Use this deliberately or eliminate redundancy.
- **Camera + lens information** is more effective in the second half of the prompt, after the subject is described.

---

## What to avoid

| Anti-pattern | Why it fails |
| :--- | :--- |
| **Actor names** ("looks like Tom Cruise") | Uncanny valley. The model averages a generic likeness that reads as off. |
| **Quality filler** ("8k, masterpiece, trending on artstation, award-winning") | V6 hangover. V7 ignores it at best, degrades at worst. |
| **Contradictory modifiers** ("photorealistic illustration", "minimalist baroque") | Adds noise without signal. Pick one register. |
| **Negative-prompt language inline** ("not blurry, no people, without text") | See [Rule 2](../../docs/01-foundational-rules.md#rule-2--describe-what-you-want-not-what-you-dont). Use `--no` only for the narrow exceptions. |
| **Ambiguous subject** ("a person", "a building") | The model picks for you; specificity matters most at the subject layer. |

---

## Worked example — the rewrite from v6 style to v7 style

### v6-style (works in v7 but underperforms)

```text
beautiful intelligence analyst, cinematic, moody, dramatic lighting,
8k, masterpiece, trending on artstation, dark background, professional,
high quality, photorealistic, dramatic, atmospheric --v 6 --ar 16:9
```

### v7-style (rewrite)

```text
A composed woman in her late 30s, intelligence analyst, leaning forward
at a workstation reviewing three large translucent map projections on
glass, index finger pointing at a node over the Black Sea. Cool monitor
glow on her face from camera-right, single warm desk lamp behind her
on a brushed-steel arm. Editorial documentary realism, shot on Fujifilm
medium-format with a 50mm lens at f/2.0, shallow depth of field, faint
film grain, muted teal-and-amber color grade.
--ar 16:9 --style raw --s 150 --v 7
```

The v7 rewrite is longer, but every sentence carries a real instruction. None of the v6 prompt's words survive — they were aesthetic pleas, not specifications.

---

## The 30/80/150 token windows

| Token range | What gets shaped |
| :--- | :--- |
| **0–30** | Composition, subject identity, broad framing |
| **30–80** | Lighting, palette, photographic register, technique |
| **80–150** | Fine detail, materiality, secondary elements |
| **150+** | Diminishing returns. Most of what you write here doesn't change the output. |

This is why the descending-weight hierarchy works: it puts the highest-leverage information in the highest-attention window.

---

## Diagnostic — is your prompt v7-ready?

Read it aloud. Could a cinematographer execute the shot from your description alone? If yes, it will work in v7. If you find yourself reading "cinematic, moody, professional" as an instruction, rewrite it.

---

## Where to go next

- The full parameter table: [`parameters.md`](parameters.md)
- The four default parameter stacks: [`parameter-stacks.md`](parameter-stacks.md)
- The cinematographer's vocabulary that fills out the technical layer: [`../../reference/`](../../reference/)
