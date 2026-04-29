# Deliverable Spec Template

A project-level brief template. Before writing any prompts, fill this out. It becomes the source of truth that every prompt and every workflow decision in the project references.

For the four pillars this spec supports, see [`workflows/pipeline-pillars.md`](../workflows/pipeline-pillars.md). For the workflow recipes the spec drives, see [`workflows/`](../workflows/).

## The Template

```markdown
# Deliverable Spec — [PROJECT NAME]

## Brief

**Client / Owner:** [Name or internal team]
**Project:** [One-line project name]
**Deliverable:** [What the project will produce — "12-shot
storyboard for Q3 briefing video", "Hero plate + 4 derivative
formats for the LOCUS launch announcement", "Whitepaper hero
composite for the Geopolitical Threat Digest, issue 14"]
**Due:** [Date]
**Format(s):** [PNG / PDF / SVG / MP4 — and at what resolutions/aspects]

## Brand Lock

- **Palette:** [Hex values for primary background, primary type,
  accent, optional signal-red. e.g., `#0F1A2E`, `#F5EFE3`,
  `#C9A24A`, `#A82A2E`]
- **Typography:** [Heavy serif name, mono name, italic serif name,
  any licensed-typeface notes]
- **Aspect ratios:** [Primary, plus all derivative formats]
- **Brand mark:** [Where it appears, at what size, in what color]
- **Disclosure:** [Required AI-disclosure language and placement
  for this deliverable, if any]

## Aesthetic Lock

- **Project register:** [One-sentence description of the visual
  through-line — e.g., "Restrained editorial realism, Foreign
  Affairs × Palantir field brief, archival cinema stock, no
  high-tech-thriller register"]
- **Lighting register:** [From `reference/lighting.md` — e.g.,
  "Mixed practical lighting at 3200K and 4500K"]
- **Camera register:** [From `reference/camera-and-lens.md` — e.g.,
  "Aaton LTR-54, 35mm prime, T1.4 for character work; Hasselblad
  503CW 50mm Distagon for architectural work"]
- **Color/stock register:** [From `reference/color-and-film-stock.md`
  — e.g., "Shot on Kodak Vision3 500T for interior/character;
  Kodak Ektar 100 for exterior/architectural"]
- **Materiality register:** [If relevant; from
  `reference/materiality-and-texture.md`]
- **Locked references:**
  - **Midjourney sref codes:** [list]
  - **Midjourney `--p` profile:** [code]
  - **Midjourney parameter stack:** [`--s X --exp Y --sw Z`]
  - **Nano Banana reference image set:** [URL or asset path]
  - **Flux.2 IP-adapter reference:** [URL or asset path]

## Character Library

For each recurring subject:

- **Character name (internal):** [Stable internal identifier]
- **Archetypal description:** [The descriptive language used in
  prompts — e.g., "a woman in her late 30s with short dark hair,
  neutral expression, dressed in a navy blazer over an ivory shirt"]
- **Reference URLs (front/three-quarter/profile/full-body):**
  - Front: [URL]
  - Three-quarter: [URL]
  - Profile: [URL]
  - Full-body: [URL]
- **Midjourney `--oref` URL:** [stored URL]
- **Midjourney `--ow` value:** [typically 150]
- **Nano Banana grounded reference set:** [asset path]
- **Notes:** [Any specific staging or pose constraints]

## Shot List (For Multi-Frame Projects)

For each shot:

| # | Description | Subject(s) | Setting | Camera | Light | Aspect | Recipe |
| :- | :--- | :--- | :--- | :--- | :--- | :-: | :--- |
| 1 | [Brief description] | [Character A] | [Setting] | [Lens] | [Register] | 3:2 | A / B / C / D |
| 2 | ... | ... | ... | ... | ... | ... | ... |

## Asset Folder Structure

Use the following structure for all project assets:

```text
[project-slug]/
├── 00-spec/
│   └── [project-slug]-deliverable-spec.md  (this document)
├── 01-aesthetic-lock/
│   ├── [project-slug]-aesthetic-ref-[N].png
│   └── [project-slug]-aesthetic-prompt.txt
├── 02-character-library/
│   ├── [character-name]/
│   │   ├── [character-name]-front.png
│   │   ├── [character-name]-tq.png
│   │   ├── [character-name]-profile.png
│   │   └── [character-name]-prompt.txt
├── 03-shots/
│   ├── shot-01/
│   │   ├── shot-01-iteration-01.png
│   │   ├── shot-01-iteration-02.png
│   │   ├── shot-01-final.png
│   │   ├── shot-01-prompt.txt
│   │   └── shot-01-metadata.json
│   ├── shot-02/...
├── 04-composites/
│   └── [project-slug]-final-[N].pdf
└── 05-deliverables/
    └── [project-slug]-delivery-[YYYY-MM-DD].zip
```

## Workflow Recipes

- **Primary pipeline:** [A / B / C / D / NB→Veo loop / single-model]
- **Per-shot iteration:** [If using Recipe B, document the NB2 → MJ
  promotion pattern]
- **Compositing:** [Figma / InDesign / DaVinci]
- **Motion:** [Veo 3.1 / Runway Gen-4 / N/A]

## Provenance & Disclosure

- **SynthID-bearing assets:** [Which assets carry SynthID — typically
  any NB or Veo output]
- **C2PA-signed assets:** [Which assets carry C2PA — typically same]
- **Manually-added disclosure:** [For MJ, Flux.2, Ideogram outputs —
  document the C2PA Content Credentials process used]
- **Client-facing disclosure language:** [Exact text for any required
  AI-generation disclosure]

## Approvals

- **Concept approval:** [Date, approver, notes]
- **Aesthetic-lock approval:** [Date, approver, notes]
- **Character-library approval:** [Date, approver, notes]
- **Hero-still approvals:** [Per shot]
- **Final delivery approval:** [Date, approver, notes]

## Notes / Open Questions

[Anything still unresolved, decisions deferred, follow-up needed]
```

## How to Use This Template

1. **Fill it out before any prompt is written.** The template is the brief; the prompts are the execution.
2. **Update it as the project evolves.** When the aesthetic lock is established (Step 2 in any recipe), capture the sref codes here. When the character library is generated, capture the URLs here. When shots are completed, mark them done in the shot list.
3. **Make it a living document.** Keep it in the project's `00-spec/` folder. Reference it in standups, in client reviews, in handoffs.
4. **At project close, archive it as the canonical record.** Six months later, when a follow-up project is requested, this document tells the next person (or your future self) exactly how the project was built.

## Related

- [`templates/prompt-template-midjourney.md`](./prompt-template-midjourney.md)
- [`templates/prompt-template-nano-banana.md`](./prompt-template-nano-banana.md)
- [`templates/prompt-template-flux.md`](./prompt-template-flux.md)
- [`workflows/pipeline-pillars.md`](../workflows/pipeline-pillars.md) — the four pillars this spec supports.
- [`workflows/recipe-d-long-form-narrative.md`](../workflows/recipe-d-long-form-narrative.md) — multi-frame projects most directly use this spec.
- [`examples/case-studies/`](../examples/case-studies/) — worked examples (placeholder).
