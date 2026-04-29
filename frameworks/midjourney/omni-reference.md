# Omni-Reference (`--oref`) — Midjourney v7

Released May 2025. Replaces `--cref` for v7 workflows. Handles characters, objects, garments, vehicles, and logos through a single reference parameter.

## What it is

Omni-Reference accepts an image URL and uses it as an identity anchor for whatever appears in the reference: a face, a watch, a portfolio, a vehicle, a brand mark. Unlike `--cref` (which was character-only and limited to v6.1), `--oref` is general-purpose and v7-native.

```text
--oref https://s.mj.run/XXXX --ow 150
```

## Why it is the BHIL default for character work

A single intelligence report often features the same executive in three or four different scenes — boardroom, situation room, field environment, portrait crop for the back cover. Without Omni-Reference, each render starts from scratch and the face drifts. With `--oref`, one hero portrait anchors the entire deliverable. The same parameter also locks the executive's wardrobe, the BHIL-branded dossier she carries, and the specific watch on her wrist — across every shot.

## The core trade-off: 2× GPU per render

`--oref` doubles GPU cost on every render. Budget for it; do not panic about it. The alternative is regenerating a face library from scratch in every prompt and accepting drift. The economics favor Omni-Reference for any deliverable with more than two scenes featuring the same subject.

## Omni-Weight (`--ow`)

Range: 1–1000. Default: 100. Practical operating range: 50–250.

| `--ow` Range | Behavior | When to Use |
| :--- | :--- | :--- |
| 40–100 | Loose identity hold; lets style dominate | Photo → illustration translations, painterly persona art |
| 100–200 | Balanced identity preservation | Default for editorial portraits and recurring scenes |
| 200–400 | Strict identity lock | High-stylize renders where you must preserve the face |
| 400+ | Diminishing returns | Rarely needed; often over-constrains composition |

The interaction with `--stylize` and `--exp` is the part most operators get wrong: as `--s` and `--exp` rise, Omni-Reference's identity hold weakens. To compensate, raise `--ow` proportionally. A `--s 300 --exp 25` editorial render typically needs `--ow 200–250` to hold the same face that `--ow 100` would hold at `--s 100`.

## Workflow — Building a Persona Anchor

1. Generate a single hero portrait of the subject using the BHIL portrait stack: `--style raw --s 100 --ar 4:5 --p [BHIL PORTRAIT PROFILE]`. Iterate until the face is exactly right.
2. Right-click the final image in Midjourney → copy the image URL (the `s.mj.run/...` link).
3. In every subsequent prompt featuring that subject, append `--oref https://s.mj.run/XXXX --ow 150`.
4. Keep the URL in the deliverable's metadata file. Six months later, that link is what lets a different team member reproduce the persona.

## What `--oref` Locks

- **Faces** — primary use case; identity preservation across scenes.
- **Wardrobe** — a charcoal blazer in the reference will reappear unless you explicitly prompt a costume change.
- **Accessories** — watches, glasses, lapel pins, branded badges. Useful for executive consistency; sometimes too sticky when you want a wardrobe variation.
- **Objects** — portfolios, dossier folders, briefcases. The BHIL-branded dossier can be the `--oref` if you want it to appear in every shot.
- **Vehicles** — a specific make/model/color of car held across multiple scenes.
- **Logos** — though for crisp typography use Ideogram or Nano Banana Pro instead.

## Loosening the Hold

If you want the same face in different wardrobe (the v6.1 `--cw 0` workflow), `--oref` doesn't have an exact equivalent. Two practical options:

- Drop `--ow` to 50–80 and prompt the new wardrobe explicitly. Often sufficient.
- Use `--cref [URL] --cw 0 --v 6.1` for the wardrobe-flex version, then return to `--oref` in v7 once you have the new wardrobe locked. This is a deliberate downgrade for one render, not a permanent v6.1 fallback.

## Compatibility Notes

- `--oref` is **not compatible with `--draft`**. Draft Mode is for fast ideation; Omni-Reference is for final-grade identity work. Different jobs, different parameters.
- `--oref` works alongside `--sref`, `--p`, and moodboards. Stack freely. The classic BHIL portrait stack is `--p [BHIL PORTRAIT PROFILE] --oref [URL] --ow 150 --sref [BRAND CODES] --sw 100 --v 7`.
- `--oref` accepts only one URL per prompt. For multi-character scenes, this is the current ceiling of v7 — you may need to composite two single-character renders in post.

## Failure Modes

- **Face drift at high `--s`** — raise `--ow`, or lower `--s` to 100–150.
- **Wardrobe locks too hard** — drop `--ow` to 60–80 and prompt the new wardrobe explicitly.
- **Reference image is itself low-quality** — `--oref` inherits the reference's flaws. Use a clean, well-lit hero portrait as the anchor; never use a screenshot of a screenshot.
- **Reference is a real person photo** — works mechanically but produces uncanny-valley results far more often than an MJ-generated reference does. The convention across this playbook: anchor on MJ-generated portraits, not on real people.

## Related

- [Core Formula](./core-formula.md) — where Omni-Reference fits in the v7 prompt structure.
- [Parameter Stacks](./parameter-stacks.md) — the BHIL Portrait stack uses `--oref` by default.
- [`19-field-operator.md`](../../prompts/05-character-personas/19-field-operator.md) and [`18-executive-dossier.md`](../../prompts/05-character-personas/18-executive-dossier.md) — production prompts using this pattern.
