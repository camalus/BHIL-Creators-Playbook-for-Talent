# 05 · The Copy-Paste Prompt Library Overview

The prompt library is in [`../prompts/`](../prompts/). It contains **24 production-ready prompts** organized into seven BHIL deliverable categories. Each prompt uses bracketed customization fields for quick adaptation. Parameters are tuned to the recommended model for that use case.

This document is the routing layer. Use it to find the right prompt fast, then jump to the file and adapt the bracketed fields.

---

## The seven categories

| # | Category | Path | Prompts |
| :--- | :--- | :--- | :--- |
| 01 | Intelligence Report Covers | [`../prompts/01-intelligence-report-covers/`](../prompts/01-intelligence-report-covers/) | 4 |
| 02 | Framework / Taxonomy Diagrams and Cover Art | [`../prompts/02-framework-diagrams/`](../prompts/02-framework-diagrams/) | 4 |
| 03 | Executive Briefing Deck Visuals | [`../prompts/03-executive-briefing-deck/`](../prompts/03-executive-briefing-deck/) | 4 |
| 04 | Data-Intelligence Hero Imagery | [`../prompts/04-data-intelligence-hero/`](../prompts/04-data-intelligence-hero/) | 4 |
| 05 | Character / Persona Design for Frameworks | [`../prompts/05-character-personas/`](../prompts/05-character-personas/) | 3 |
| 06 | Architectural / Geospatial / Location-Intelligence Renders | [`../prompts/06-geospatial/`](../prompts/06-geospatial/) | 3 |
| 07 | Typographic Report Cover Posters and Whitepaper Heroes | [`../prompts/07-typographic-posters/`](../prompts/07-typographic-posters/) | 2 |

---

## The 24 prompts at a glance

| # | Prompt | Recommended Model | Aspect |
| :--- | :--- | :--- | :--- |
| 1 | OSINT Quarterly Brief Cover | Midjourney v7 | 2:3 |
| 2 | Geopolitical Threat Digest Cover (4K) | Nano Banana Pro | 4:5 |
| 3 | Due Diligence Briefing Cover | Flux.2 Pro | 2:3 |
| 4 | Market Intelligence Whitepaper Cover | Ideogram v3 | 3:4 |
| 5 | Five-Layer Threat Model Hero | Midjourney v7 | 16:9 |
| 6 | Pipeline Framework Diagram | Nano Banana Pro | 16:9 |
| 7 | Taxonomy Radial Diagram | GPT Image 2 | 1:1 |
| 8 | Framework Cover Art (abstract) | Midjourney v7 | 3:2 |
| 9 | LinkedIn Thought-Leadership Tile | Ideogram v3 | 1:1 |
| 10 | Executive Banner Hero | Midjourney v7 | 21:9 |
| 11 | YouTube-Thumbnail Hero | Nano Banana 2 | 16:9 |
| 12 | Carousel Cover for LinkedIn Explainer | Ideogram v3 | 4:5 |
| 13 | Abstract Signal / Surveillance Motif | Midjourney v7 | 16:9 |
| 14 | Network-Graph Hero | Nano Banana Pro | 16:9 |
| 15 | Tileable Brand Texture | Midjourney v7 | 1:1 |
| 16 | Dashboard / SaaS Hero Mockup | GPT Image 2 | 16:9 |
| 17 | Analyst Archetype "VIGIL" | Flux.2 Pro | 3:2 |
| 18 | Executive Dossier Persona | Midjourney v7 (Omni-Reference) | 4:5 |
| 19 | Field Operator Archetype | Nano Banana Pro | 4:5 |
| 20 | Tilt-Shift Geospatial Render | Nano Banana Pro | 16:9 |
| 21 | Declassified Satellite Aesthetic | Midjourney v7 | 16:9 |
| 22 | Architectural Brief Render — LOCUS Style | Flux.2 Pro | 3:2 |
| 23 | Whitepaper Hero Poster (composite) | Ideogram v3 + Midjourney | 2:3 |
| 24 | Conference / Keynote Poster | Recraft V3 (vector) | 2:3 |

---

## How to read a prompt file

Every prompt file in the library follows the same structure:

```markdown
# NN · Prompt Name

## Use case
What deliverable this is for, and the brand register it serves.

## Recommended model
Specific model and version. Why this model, not another.

## Prompt
The copy-paste prompt with bracketed [CUSTOMIZATION FIELDS].

## Parameters
The full parameter stack (for Midjourney) or API config notes
(for Nano Banana / Flux / GPT / Ideogram).

## Variants
Adaptations for closely related deliverables.

## Failure modes
What to watch for. When this prompt drifts.

## Related
Links to adjacent prompts and the workflows they connect to.
```

---

## Bracketed customization fields — reference

The library uses a consistent set of placeholders. When you fill them in, replace the brackets with the actual values. A prompt with leftover brackets is not production-ready.

| Placeholder | What it represents |
| :--- | :--- |
| `[ACCENT COLOR]` | The single accent color (typically amber, signal red, or cyan) |
| `[BG COLOR]` | The background color (typically obsidian, ivory, or charcoal) |
| `[CLIENT CODE NAME]` | Redacted/synthetic client identifier |
| `[REPORT TITLE]` | The actual title of the deliverable |
| `[SUBTITLE / SERIES NAME]` | The subtitle or series mark |
| `[ISSUE NUMBER · DATE]` | Issue marker, e.g., "Issue 014 · April 2026" |
| `[BHIL PROFILE]` | Personalization profile code from the brand vault |
| `[BHIL COVER SREFS]` | Sref codes from the brand vault, cover-line |
| `[BHIL FRAMEWORK PROFILE]` | Personalization profile for framework diagrams |
| `[BHIL PORTRAIT PROFILE]` | Personalization profile for executive portraits |
| `[EXEC REFERENCE URL]` | Omni-Reference URL for the locked executive |

---

## Prompt selection by deliverable type

### "I need a cover for a quarterly OSINT brief"

→ Prompt 1 (Midjourney v7, restrained editorial still-life)

### "I need a cover with a long, multi-line headline that has to be perfectly legible at print resolution"

→ Prompt 2 (Nano Banana Pro, 4K, typography-first)

### "I need a framework diagram explaining a five-stage pipeline"

→ Prompt 6 (Nano Banana Pro) — text precision matters more than aesthetic flourish.
Or Prompt 5 (Midjourney v7) for the unlabeled hero version that lives next to the diagram.

### "I need an executive portrait, and the same executive needs to appear in three more deliverables"

→ Prompt 18 (Midjourney v7 with `--oref`). Lock the face once; reuse the URL across the series.

### "I need a hero image for a LinkedIn explainer carousel"

→ Prompt 12 (Ideogram v3) for the cover slide; Prompt 9 (Ideogram v3) for individual social tiles.

### "I need a tilt-shift aerial of a port for a maritime security briefing"

→ Prompt 20 (Nano Banana Pro) — the world-knowledge reasoning matters here.

---

## Where to go next

- Full prompt library entry point: [`../prompts/README.md`](../prompts/README.md)
- Prompt templates (for writing new prompts): [`../templates/`](../templates/)
- Deliverable spec sheet (fill out before you start): [`../templates/deliverable-spec-template.md`](../templates/deliverable-spec-template.md)
