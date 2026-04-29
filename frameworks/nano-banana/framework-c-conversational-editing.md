# Framework C — Editing (Conversational, Mask-Free)

The Nano Banana editing pattern. No masks, no inpainting brushes, no layer selection. Edits happen in plain language across multi-turn chat.

## The Per-Turn Formula

```text
[Strong verb] + [Target element] + [Change] + ["keep everything else unchanged"]
```

Strong verb: **Edit, Replace, Translate, Restore, Focus on, Remove, Add, Adjust, Convert.**

Target element: the thing being changed, named precisely. Not *"the color"* but *"the halftone map tint"*.

Change: what you want done. Specific values, not vague directions. Not *"make it warmer"* but *"shift to amber #C9A24A."*

Anchor phrase: **"keep everything else unchanged"** or *"do not change anything else."* Not redundant. This is the constraint that prevents the model from drifting on elements you weren't asking it to touch.

## Why Multi-Turn Beats Regeneration

The official Google guidance — and the BHIL playbook position — is that multi-turn editing is preferred over regeneration. Two reasons:

1. **State preservation.** The model carries the `thought_signature` across turns. Regenerating from scratch discards that state and the model has to re-reason about composition, lighting, and layout from zero.
2. **Cost.** Multi-turn editing reuses the in-context image; regeneration is a fresh render. For a 5-edit cycle, multi-turn cuts cost roughly in half.

Translated to operating practice: the 80/20 rule from the foundational rules. **When 80% is right, edit; do not regenerate.**

## Worked Example — 5-Turn Cover Iteration

This is the canonical playbook example. Each turn is a discrete `chat.send_message()` call against the same `chats.create()` session.

```text
T1: Generate a 16:9 report cover: deep navy background, a single
    halftone world map at 15% opacity, centered title block reserved
    as blank negative space.

T2: Keep everything exactly the same. In the center, render the title
    'GRAY-ZONE SIGNALS' in bold uppercase serif (Canela Deck style),
    tracking slightly wide, in warm off-white.

T3: Keep title, layout and colors locked. Add a subtitle below in thin
    sans-serif: 'Quarterly OSINT Brief · Q2 2026'.

T4: Change the halftone map tint from gray to amber #C9A24A. Do not
    change anything else.

T5: Export the same cover in a 9:16 vertical aspect ratio by extending
    the background, keeping all text and the map positioned in the
    upper third.
```

What's happening across these turns:

- T1 is generation, not editing — establishes the base.
- T2 adds typography to a known location.
- T3 layers additional text without disturbing T2.
- T4 changes a single visual property without touching anything else.
- T5 changes aspect ratio while preserving content.

Each turn names exactly one transformation and explicitly anchors what should not change.

## The Verb Set in Practice

| Verb | Use Case | Example |
| :--- | :--- | :--- |
| Edit | General-purpose change | *"Edit the lighting to remove the warm desk lamp; keep cool monitor glow only."* |
| Replace | Swap one element for another | *"Replace the world map with a topographic relief map of the Black Sea region."* |
| Translate | Multilingual text swap | *"Translate all on-image text to Arabic, keep everything else identical."* |
| Restore | Undo previous turn | *"Restore the title color to warm ivory."* |
| Focus on | Crop / re-frame attention | *"Focus on the analyst's hand and the screen she is touching; tighter crop, 1:1."* |
| Remove | Delete an element | *"Remove the second monitor from the right side. Keep the central monitor and lamp."* |
| Add | Introduce a new element | *"Add a single amber accent rule under the title, 240px wide."* |
| Adjust | Numerical value change | *"Adjust the halftone opacity from 15% to 8%."* |
| Convert | Format change | *"Convert this composition into a 9:16 vertical layout."* |

## Anchor Phrases That Pay Off

Beyond *"keep everything else unchanged,"* these closing instructions reliably reduce drift:

- *"Do not change anything else."*
- *"Preserve the previous composition exactly."*
- *"Maintain the same character identity, wardrobe, and lighting."*
- *"Same color grade, same aspect ratio."*
- *"All other elements remain locked from the previous turn."*

For turns that involve typography, add *"all other text remains unchanged."*

## When Multi-Turn Drifts Anyway

Even with discipline, long edit chains eventually drift. Symptoms:

- Subject's face shifts subtly across turns.
- Color grade warmth creeps up.
- Composition drifts toward Gemini's default register.
- Text from earlier turns gets re-rendered slightly differently.

The fix: **start a fresh chat session** with the most recent acceptable image as a Framework B reference. Re-anchor the conversation. Document the anchor image's URL or local path in the deliverable's metadata. Drift is normal; the discipline is recognizing it before it ships.

## Long-Horizon Editing — More Than 8 Turns

Past 8 turns, drift is unavoidable on most edits. Two patterns to manage this:

1. **Branch and merge.** When you have a strong intermediate (turn 4 or 5), save it. Continue the chain, but if drift becomes unacceptable, return to the saved intermediate and branch off in a new direction.
2. **Restart with strong reference.** Open a new chat. Upload the latest acceptable image as a Framework B reference. Re-state the constraints in compressed form. Continue.

## The Mask-Free Nuance

"Mask-free" doesn't mean "imprecise." Naming the target element specifically substitutes for masking. *"The lower-left corner halftone gradient"* is more precise than dragging a mask. The discipline is in the language; the tool just reads it.

If you need pixel-precise control (replace a specific 50-pixel region without any other change), Nano Banana is wrong for the job — go to Photoshop or Flux Kontext, which is the dedicated mask-free editor. Nano Banana is for semantic edits, not surgical ones.

## Failure Modes

- **No anchor phrase** — drift on every turn.
- **Vague target** — *"change the color"* (which color?). Always name the specific element and the specific change.
- **Multiple changes per turn** — *"change the title, swap the map, and add a subtitle."* Three turns, not one.
- **Re-uploading references mid-chain** — destroys context. References go in turn 1; subsequent turns reference them by description ("the subject from the reference").
- **Skipping verb at the start** — *"Maybe a bit more amber?"* The model treats this as a question, not an instruction. Lead with `Adjust`, `Edit`, or `Add`.

## Related

- [`framework-a-text-to-image.md`](./framework-a-text-to-image.md) — generation that precedes editing.
- [`framework-b-multi-image-fusion.md`](./framework-b-multi-image-fusion.md) — multi-reference work as a starting point for the chain.
- [`framework-e-typography.md`](./framework-e-typography.md) — typography-specific editing (text changes, font swaps, multilingual translations).
- [`docs/01-foundational-rules.md`](../../docs/01-foundational-rules.md) — Rule 4 on iteration discipline.
