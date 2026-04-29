# Examples

This directory holds worked case studies — full project walkthroughs that demonstrate the playbook end-to-end. Each case study takes a single deliverable from brief → aesthetic lock → character library → per-shot generation → composite → archive, with all prompts, references, and metadata documented.

## Status

The examples directory is intentionally a *placeholder* in this v1.0.0 release. Worked case studies will be added in subsequent releases as projects clear NDA review and can be documented openly. Each case study will live in [`./case-studies/`](./case-studies/) as its own subdirectory with the structure described below.

The placeholder is here for two reasons:

1. **It establishes the convention.** When the first case study lands, the pattern is already documented.
2. **It signals the gap.** This is the part of the playbook that grows over time, project by project.

## Case Study Structure

Each case study in [`./case-studies/`](./case-studies/) will follow this structure:

```text
case-studies/
└── [case-study-slug]/
    ├── README.md                      # Project narrative
    ├── 00-spec/
    │   └── deliverable-spec.md        # Filled-in spec from templates/
    ├── 01-aesthetic-lock/
    │   ├── reference-01.png
    │   ├── reference-02.png
    │   └── lock-prompt.txt
    ├── 02-character-library/          # If applicable
    │   └── [characters]/
    ├── 03-shots/
    │   ├── shot-01/
    │   │   ├── prompt.txt
    │   │   ├── parameters.json
    │   │   ├── iterations/
    │   │   └── final.png
    │   └── shot-NN/
    ├── 04-composites/
    │   └── final-deliverable.pdf
    ├── 05-retrospective.md             # What worked, what didn't
    └── 06-prompts-as-shipped/
        └── *.md                        # Reusable prompt extracts for prompts/
```

## Case Study Narrative Template

Each case study's `README.md` follows this structure:

```markdown
# Case Study — [PROJECT NAME]

## The Brief

[1-2 paragraphs: what was asked for, who asked, what constraints]

## The Approach

[Which workflow recipe was chosen and why]
[Which models were used at each stage]
[Which BHIL conventions applied]

## The Aesthetic Lock

[How the locked aesthetic was established]
[Sref codes captured, parameter stack, profile]
[Image: the locked reference set]

## The Character Library (if applicable)

[Which subjects recurred]
[How references were generated and stored]

## The Shot List

[Walk through each shot: brief description, prompt evolution,
final output]

## The Composite

[How the deliverable was assembled in Figma/InDesign]
[Layer structure, color discipline, brand QA]

## What Worked

[Concrete observations from this project]

## What Didn't

[Honest retrospective: failure modes encountered, surprises, things
to do differently next time]

## Reusable Outputs

[Pointers to any prompts in this project that became repository
prompts in `prompts/`, with attribution and contributor notes]
```

## Anticipated First Case Studies

Subject to NDA clearance, future case studies in this repository will likely include:

- **LOCUS Launch Hero Set** — the announcement deliverable for the LOCUS Framework, including hero plate, executive banner, social tiles, and a 10-second motion teaser. Demonstrates Recipe A and Recipe C in combination.
- **Quarterly Briefing Issue** — a full quarterly briefing visual package including cover, internal hero plates, and persona portraits. Demonstrates Recipe B and Recipe D.
- **Conference Keynote Deck** — a typographic-poster series for a conference keynote, deployed across 16:9 stage, 2:3 program, and 1:1 social. Demonstrates Recipe C and prompt 24's Recraft V3 vector pipeline.
- **Episodic Briefing Series** — multi-issue sequence demonstrating long-running aesthetic and character lock across releases. Demonstrates Recipe D in extended form.

## How to Contribute a Case Study

External contributors who have used this playbook in production work and would like to add a case study:

1. Anonymize/sanitize all client-identifying material before submission.
2. Follow the structure documented above.
3. Open a PR using the `New Prompt Request` issue template (or its forthcoming case-study counterpart).
4. The case study undergoes brand-and-quality review before merge.

See [`CONTRIBUTING.md`](../CONTRIBUTING.md) for the full contribution process.

## Related

- [`templates/deliverable-spec-template.md`](../templates/deliverable-spec-template.md)
- [`workflows/`](../workflows/) — the recipes case studies will demonstrate.
- [`prompts/`](../prompts/) — the prompt library case studies will draw from and contribute back to.
- [`CONTRIBUTING.md`](../CONTRIBUTING.md)
