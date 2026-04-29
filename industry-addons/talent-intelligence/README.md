# BHIL Creators Playbook — Talent Intelligence Add-On

**Version:** 1.2.0 · April 2026
**Status:** Production-grade reference, MIT licensed
**Parent:** This is an industry add-on to the [BHIL Creators Playbook for Advanced AI Image Generation](../../README.md). The parent playbook is the prerequisite — read it first.

---

## What This Add-On Is

A specialized layer of prompts, templates, compliance documentation, and workflow guidance for AI image generation in the **talent intelligence and recruiting industry** — covering executive search, talent intelligence platforms, recruiting agencies, and in-house talent acquisition / employer brand teams.

The parent BHIL playbook documents the *grammar* of AI image generation — models, parameters, the Universal Creative Director Toolkit, cross-platform workflows. This add-on documents the *industry-specific dialect* required to produce visual deliverables that read as serious talent-industry work rather than generic stock.

## Why a Separate Add-On

Three findings from the April 2026 industry research drove this add-on's creation:

1. **The talent industry's visual register is bifurcated, not unified.** A "talent" prompt that doesn't pick a sub-register reads as off-brand. There are three distinct visual worlds — retained-search editorial, talent-intelligence platform dashboard, and recruiting-agency editorial-illustration hybrid — and serious work requires fluency across all three.
2. **AI imagery in recruiting now sits inside the most regulated visual category in commercial creative.** EU AI Act Article 50 (August 2026), Colorado AI Act (June 2026), Illinois HB 3773 (January 2026), Ontario Bill 149 (January 2026), Tennessee ELVIS Act, an active EEOC litigation pipeline (*Mobley v. Workday* class certified May 2025), and a documented industry trust crisis (Levi's × Lalaland, Mango Teen, Coca-Cola, Google Gemini) all converge on this category. No leading employer-brand team had published a formal AI-imagery disclosure standard as of April 2026 — this add-on aims to fill that gap.
3. **The candidate-imagery problem is the central design constraint.** Every visual decision in talent work routes through one question: when imagery shows a person, who is that person, and where did the likeness come from. This add-on encodes a default rule at the prompt level: AI for abstract concept and environmental/background; real photography (with consent and C2PA-tagged provenance) for humans wherever a viewer might mistake the subject for a real employee or candidate.

## The Three Sub-Registers

Every prompt in this add-on declares its sub-register explicitly. The parent BHIL register (Foreign Affairs × Palantir field brief, navy/ivory/amber/signal-red, Canela Deck/Sectra Bold) maps almost perfectly onto sub-register A — making it the natural default. Sub-registers B and C require explicit deviation toolkits.

| Register | Visual Logic | Anchor Firms / Platforms | When To Use |
| :--- | :--- | :--- | :--- |
| **A — Retained-search editorial** | Single-accent palette, generous white space, soft documentary portraiture, serif/humanist-sans typography, architectural metaphor photography | Korn Ferry, Spencer Stuart, Egon Zehnder, Russell Reynolds, Heidrick & Struggles | Executive search dossiers, leadership briefs, board-search work, executive-grade workforce reports, premium DEI reports |
| **B — Talent-intelligence platform dashboard** | Dark gradient meshes, glowing node graphs, choropleth globes, bento-grid stat tiles, AI-agent chat panels | Eightfold, Gloat, Lightcast, Beamery, Draup, TalentNeuron | Platform dashboard hero plates, vendor pitch deck imagery, conference keynote backdrops, skills/talent-flow visualizations, HR Tech marketing |
| **C — Recruiting-agency editorial-illustration hybrid** | Lower-case sentence-case headlines, illustration libraries, documentary daylight portraiture, single-color chapter dividers | Randstad, Adecco, Robert Half, ManpowerGroup, AMS, Cielo | Career site heroes, LinkedIn recruiter campaigns, EVP visual systems, salary guides, job posting imagery, recruiting agency case studies |

See [`reference/sub-register-a-retained-search.md`](./reference/sub-register-a-retained-search.md), [`reference/sub-register-b-platform.md`](./reference/sub-register-b-platform.md), and [`reference/sub-register-c-agency.md`](./reference/sub-register-c-agency.md) for the full visual specifications.

## Directory Map

```text
industry-addons/talent-intelligence/
├── README.md                      # This file
├── CHANGELOG.md                   # Version history
├── docs/                          # Industry orientation
│   ├── 00-introduction.md
│   ├── 01-three-sub-registers.md
│   ├── 02-deliverable-types.md
│   ├── 03-candidate-imagery-problem.md
│   └── 04-glossary.md
├── compliance/                    # Regulatory + ethics documentation
│   ├── README.md
│   ├── ai-imagery-policy.md
│   ├── disclosure-standards.md
│   ├── jurisdiction-matrix.md
│   ├── representation-testing.md
│   └── consent-and-likeness.md
├── reference/                     # Visual specifications per sub-register
│   ├── README.md
│   ├── sub-register-a-retained-search.md
│   ├── sub-register-b-platform.md
│   ├── sub-register-c-agency.md
│   └── exemplar-library.md
├── prompts/                       # 16 industry-specific prompts (full files)
│   ├── README.md
│   ├── 01-executive-search/        # 4 prompts — sub-register A
│   ├── 02-talent-intelligence-platform/  # 4 prompts — sub-register B
│   ├── 03-employer-brand/         # 4 prompts — sub-register C
│   └── 04-workforce-reports/      # 4 prompts — mixed
├── quick-reference/               # Copy/paste prompt library (NEW in v1.1.0)
│   ├── README.md
│   └── 20-prompt-library.md       # 20 production-ready prompts in one file
├── templates/                     # Talent-specific spec templates
│   ├── README.md
│   ├── candidate-dossier-template.md
│   ├── employer-brand-spec-template.md
│   └── ai-disclosure-statement-template.md
└── workflows/                     # Production tier guidance
    ├── README.md
    ├── three-production-tiers.md
    └── candidate-imagery-decision-tree.md
```

## Quick Start

1. **Confirm you've read the parent playbook.** This add-on assumes fluency with parameter stacks, the Universal Creative Director Toolkit, and the four cross-platform workflow recipes. Without that foundation the prompts here will not produce the documented output.
2. **Identify your sub-register.** Read [`docs/01-three-sub-registers.md`](./docs/01-three-sub-registers.md) and pick A, B, or C for your project. If you need fluency across multiple, read all three reference files.
3. **Read the compliance overview.** [`compliance/ai-imagery-policy.md`](./compliance/ai-imagery-policy.md) is the umbrella policy template; [`compliance/jurisdiction-matrix.md`](./compliance/jurisdiction-matrix.md) is the regulatory cheat-sheet. These are not optional reading for production work.
4. **Pick your deliverable type.** [`docs/02-deliverable-types.md`](./docs/02-deliverable-types.md) maps the 14 canonical talent-industry deliverables to the prompts that produce them.
5. **Generate.**
   - For depth (four-variant libraries, parameter tables, failure modes): use the full prompt files in [`prompts/`](./prompts/).
   - For speed (copy/paste library, 20 ready-to-customize prompts in one scannable file): use [`quick-reference/20-prompt-library.md`](./quick-reference/20-prompt-library.md).

## What's New In This Release (v1.2.0)

**v1.2.0 (current)** — Layout refinement of the BHIL-branded reference document so 3-4 prompt blocks fit per page. The underlying `quick-reference/20-prompt-library.md` source file is unchanged from v1.1.0.

**v1.1.0** — Adds the [`quick-reference/`](./quick-reference/) directory with a 20-prompt copy/paste library. Same prompts as the full files in [`prompts/`](./prompts/), denser format. The source of truth for Section 11 of the BHIL-branded reference document.

**v1.0.0 (foundation)**

- **16 talent-industry-specific prompts** across executive search, platform marketing, employer brand, and workforce reports.
- **Compliance documentation** covering EU AI Act, Colorado AI Act, Illinois HB 3773, Ontario Bill 149, Tennessee ELVIS Act, and EEOC/OFCCP guidance, plus C2PA Content Credentials standards.
- **Three sub-register reference files** documenting the visual conventions of retained-search editorial, talent-intelligence platform dashboard, and recruiting-agency editorial-illustration hybrid.
- **Three production-tier workflow guidance** (fast iteration, mid-tier, archival quality).
- **A candidate-imagery decision tree** that operationalizes the "AI for concept, real photography for humans" default rule.
- **A curated exemplar library** of 15+ benchmark references from Heidrick, Spencer Stuart, Korn Ferry, Lightcast, Eightfold, Symphony Talent, Verizon, Marriott, and others.

## Roadmap

See [`CHANGELOG.md`](./CHANGELOG.md) for the planned roadmap. Highlights:

- **v1.3.0:** Worked case studies — anonymized end-to-end project walkthroughs; 30-prompt library variant.
- **v1.4.0:** Sub-register D — boutique/specialist search firms (life sciences, executive coaching, niche verticals).
- **v2.0.0:** Motion-deliverable additions for talent (recruiter video assets, conference stage motion, animated dashboard demos).

## Contributing

External contributions follow the parent repo's process — see [`../../CONTRIBUTING.md`](../../CONTRIBUTING.md). Add-on-specific notes:

- Talent-industry contributions must declare their sub-register (A/B/C) explicitly.
- Any prompt or example involving people must comply with the rules in [`compliance/consent-and-likeness.md`](./compliance/consent-and-likeness.md).
- Case-study contributions must be anonymized to remove client identification.

## License

MIT — same as the parent repo. See [`../../LICENSE`](../../LICENSE).

## Related

- [Parent repo README](../../README.md)
- [Parent prompts library](../../prompts/README.md)
- [Parent workflow recipes](../../workflows/README.md)
- [Parent reference toolkit](../../reference/README.md)
