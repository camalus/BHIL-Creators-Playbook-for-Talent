# The BHIL Sref Library — Curation Discipline

The Sref library is the **operational spine** of a brand-consistent Midjourney practice. It is a design system, and it must be treated like one — versioned, named, access-controlled, and stewarded.

This document is the curation discipline. The actual codes live in the access-controlled BHIL brand vault, not in this repository.

---

## What `--sref` does

`--sref` is Midjourney's **style** reference. It accepts:

- A URL (any image, including non-MJ-generated)
- A numeric code (Midjourney's internal style-fingerprint format)
- The keyword `random` (style-discovery mode)

It does **not** copy subjects. It copies the aesthetic signature — palette, contrast handling, texture, compositional bias, rendering register.

You can stack multiple codes in one prompt: `--sref 1742826451 689668977 2216056865`. The output is an averaged blend.

---

## The Tatiana Tsiguleva curation workflow

The gold-standard discipline, distilled and adapted for BHIL:

### Step 1 — Harvest

Run `--sref random --r 40` across **multiple prompt archetypes**. The archetypes matter — a code that looks great on one type of subject may collapse on another.

Suggested archetype set for BHIL:

- An OSINT map composition
- A classified-document still life
- An analyst-at-workstation portrait
- A framework / isometric diagram

This produces 30–50 candidates per archetype. Save the codes that hit, alongside the prompt that generated each hit.

### Step 2 — Stress-test

Take each surviving candidate and **re-run it across at least three unrelated prompt types.** Any code that collapses on different subjects is off-brand and gets cut.

The failure mode this catches: a code that produces beautiful editorial covers but turns every portrait into glamour photography. That code is genre-specific, not brand-defining. Reject it.

### Step 3 — Stack as a master brand line

The 3–5 surviving stress-test winners become a **master brand line**:

```text
--sref 1742826451 689668977 2216056865 --sw 150
```

Stacking 3–5 averages out individual eccentricities while preserving the shared register that survived the stress test.

### Step 4 — Document

For each code in the brand vault, record:

| Field | Detail |
| :--- | :--- |
| **Code** | The numeric value |
| **`--sv` version** | What style interpreter the code was authored against (V7 default is `--sv 6`; legacy codes are `--sv 4`) |
| **Two baseline samples** | Reference images from the harvest step |
| **Color palette note** | The dominant palette this code biases toward |
| **Use-case tag** | "Cover line", "Framework", "Portrait", "OSINT motif", etc. |
| **Stress-test result** | Which archetypes the code held register on |
| **Owner** | Who curated it; who can authorize promotion to brand-default |

---

## Brand-vault structure

The library is not a flat list of codes. It is organized by **register**:

| Register | What it serves |
| :--- | :--- |
| **BHIL Cover Line** | Report covers and publication covers |
| **BHIL Framework Line** | Framework diagrams, isometric work, schematic |
| **BHIL Portrait Line** | Executive portraits, persona art |
| **BHIL OSINT Line** | OSINT-aesthetic work, surveillance, archival |
| **BHIL Geospatial Line** | Location-intelligence renders, architectural |

Each register has **one master line of 3–5 codes** as the production default, plus a discovery tier of additional candidates that haven't yet been promoted.

---

## Promotion process

A new Sref code becomes a brand default by passing through these gates:

1. **Stress-test passed** (Step 2 above).
2. **Production trial** — used on at least 3 deliverables across 2 different engagements without a brand-fitness flag.
3. **Reviewed by Barry** — codes are not promoted to the master line by individual contributors.
4. **Documented** with all six brand-vault fields above.
5. **Old line versioned, not replaced** — `BHIL_Cover_Line_v3` does not delete `v2`; existing deliverables remain reproducible.

---

## Stewardship rules

> **Treat Srefs like a design system.**
> Versioned, named, access-controlled. Do not let consultants hoard codes in Slack threads. This library is an asset.

- **No personal hoarding.** A consultant who finds a great code and keeps it in their notes is reducing BHIL's collective practice. Contribute it back.
- **No undocumented promotions.** A code in the master line without the six brand-vault fields is a footgun for the next person.
- **No mid-engagement code changes** unless the existing line is producing brand-fitness failures. Lock the code at engagement kickoff.
- **No mixing registers without intent.** Stacking a Cover Line code with a Framework Line code is sometimes the right move, but it should be a deliberate choice, not an accident.

---

## Discovery rhythm

Run an Sref discovery pass every 4–6 weeks. The MJ ecosystem keeps generating new aesthetic signatures, and a static brand library will drift behind the broader visual standard.

A good cadence:

- **Week 1:** Harvest (Step 1) across all five register archetypes.
- **Week 2:** Stress-test (Step 2) on the 30–50 candidates.
- **Week 3:** Production trial of 1–2 promising candidates inside non-critical deliverables.
- **Week 4:** Review with Barry; promote, retire, or shelve.

---

## `--sv` version handling

V7 supports Sref interpreter versions 1, 2, 3, 4, 6. **V7 defaults to `--sv 6`.**

If a legacy favorite code has stopped behaving the way it used to, it was probably authored against `--sv 4`. Add `--sv 4` to the prompt to restore the original behavior.

When recording a new code in the brand vault, **always note the `--sv` version it was authored against.** This is the field most often forgotten and most painful to recover.

---

## Where to go next

- Moodboards (when persistent house style beats raw Sref stacks): [`moodboards.md`](moodboards.md)
- Personalization profiles that pair with Sref lines: [`personalization.md`](personalization.md)
- The four BHIL parameter stacks that consume Sref codes: [`parameter-stacks.md`](parameter-stacks.md)
