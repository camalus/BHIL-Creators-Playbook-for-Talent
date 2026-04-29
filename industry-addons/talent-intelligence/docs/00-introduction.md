# Introduction

The talent intelligence and recruiting industry has a visual identity problem that is rarely named explicitly: most generated imagery in the industry reads as generic stock because the industry's actual visual vocabulary is **bifurcated**, not unified. The high end of the industry — Korn Ferry, Spencer Stuart, Egon Zehnder, Russell Reynolds, Heidrick & Struggles — is converging on an austere editorial idiom that is closer to *Foreign Affairs* than to a tech startup. The platform layer — Eightfold, Gloat, Lightcast, Beamery — is converging on a dark-gradient agentic-AI dashboard idiom. The agency middle — Randstad, Robert Half, Adecco, ManpowerGroup — sits between the two, leaning illustration-led with single-color chapter dividers and lower-case sentence-case headlines.

A "talent" prompt that doesn't pick a sub-register reads as nothing in particular. This add-on exists to make that choice explicit and to provide the production-grade dialect for each register.

## Three Compounding Constraints

Beyond the register problem, three other industry-specific constraints shape every visual decision:

### 1. The Candidate-Imagery Problem Is the Central Design Constraint

When recruiting imagery shows a person, the question of *who that person is* and *where the likeness came from* is the question that determines whether the deliverable is appropriate, legal, ethical, and effective. Four solutions are in active use across the industry, and each one has documented failure modes:

- **Stock photography** fails on demographic stereotyping, image recurrence across competitor sites, and the iStock/Getty register that signals lack of investment.
- **Real employees with consent** is the gold standard for top-of-funnel content, but requires a model release separate from the employment agreement, defined usage scope, GDPR/CCPA-aligned withdrawal rights, and post-2024 AI-training language.
- **AI-generated imagery** has produced documented backlash — Levi's × Lalaland.ai (March 2023), Mango Teen Sunset Dream Collection (July 2024), Guess/Vogue US (2025), Coca-Cola Christmas (2024 + 2025), Toys "R" Us (2024), Google Gemini Nazi-soldier over-correction (February 2024) — and faces an active industry trust crisis from the Pindrop/Gartner forecast that 1 in 4 candidates globally will be AI-fabricated by 2028.
- **Anonymous-silhouette / illustrated alternatives** sidestep the problem entirely and are now an authentic-feeling exit (GitLab's open-source illustration system, GitHub's Octocat, Notion's hand-illustrated peach/cream, Mailchimp's Collins-designed outsider art).

This add-on encodes a default rule across all prompts: **AI for abstract concept and environmental/background; real photography (with consent and C2PA-tagged provenance) for humans wherever a viewer might mistake the subject for a real employee or candidate.** See [`docs/03-candidate-imagery-problem.md`](./03-candidate-imagery-problem.md) and [`workflows/candidate-imagery-decision-tree.md`](../workflows/candidate-imagery-decision-tree.md).

### 2. AI Imagery in Recruiting Sits Inside the Tightest Compliance Envelope in Commercial Creative

No statute in any jurisdiction directly governs AI-generated imagery in recruiting, but three overlapping regulatory vectors converge on this category:

- **Anti-discrimination law** — Title VII, ADEA, ADA, GINA, EPA in the United States; EEOC Compliance Manual Section 15 treats imagery as part of recruiting practices. *Mobley v. Workday* (N.D. Cal., No. 3:23-cv-00770) was conditionally certified as an ADEA collective on May 16, 2025 with potential reach in the hundreds of millions of applicants.
- **AI / automated-decision-making law** — Colorado AI Act (effective June 30, 2026 after the August 2025 special-session delay), Illinois HB 3773 (effective January 1, 2026), Illinois AI Video Interview Act, NYC Local Law 144, Maryland HB 1202, EU AI Act (high-risk obligations August 2, 2026 for recruitment under Annex III §4), Quebec Law 25 §12.1, Ontario Bill 149 (effective January 1, 2026).
- **Synthetic-content law** — Tennessee ELVIS Act (civil and Class A misdemeanor liability for unauthorized AI replicas of voice or likeness), EU AI Act Article 50 deepfake disclosure obligations, the EU Code of Practice on AI Labelling and Transparency final version expected June 2026.

No leading employer-brand team had published a formal AI-imagery disclosure standard as of April 2026. This add-on aims to fill that gap with a defensible default policy — see [`compliance/`](../compliance/).

### 3. The Industry Is in an Active Trust Crisis

The *production* side of recruiting (employer brand teams using AI imagery) faces consumer pushback. The *applicant* side (AI-fabricated candidates with deepfake profiles, AI-assisted interviews, ghost candidates) is now subject to a Gartner-cited forecast that 1 in 4 job candidates globally will be AI-fabricated by 2028 — meaning recruiters and employer-brand teams are operating under a presumption of AI suspicion from candidates, and candidates are operating under a presumption of AI suspicion from employers. Visible C2PA disclosure, demographic-representation testing, and provenance-by-default are not just regulatory hedges in this environment; they are competitive trust signals.

## What This Add-On Is Not

- **Not a replacement for the parent playbook.** This add-on assumes fluency with the four foundational rules, the Universal Creative Director Toolkit, the parameter stacks, and the cross-platform workflow recipes. Read [`../../README.md`](../../README.md) and [`../../docs/`](../../docs/) first.
- **Not legal advice.** The compliance documentation in this add-on is the most current public synthesis of regulatory landscape as of April 2026, and is intended as production guidance to inform a *defensible* posture. It is not a substitute for review by counsel licensed in your jurisdiction.
- **Not a diversity policy or hiring policy.** This add-on covers visual production. Hiring policy, sourcing strategy, and diversity strategy live in your firm's HR governance.
- **Not exhaustive.** The industry is large. This add-on covers the highest-leverage 80% of canonical talent-industry deliverables. Vertical specializations (life sciences exec search, climate-tech recruiting, niche staffing) are flagged for v1.2.0 and beyond.

## How To Read This Add-On

1. Start with this introduction.
2. Read [`docs/01-three-sub-registers.md`](./01-three-sub-registers.md) and identify which register your project requires.
3. Read [`docs/03-candidate-imagery-problem.md`](./03-candidate-imagery-problem.md) before any prompt that involves people.
4. Read the relevant compliance file: [`compliance/ai-imagery-policy.md`](../compliance/ai-imagery-policy.md) (umbrella) and [`compliance/jurisdiction-matrix.md`](../compliance/jurisdiction-matrix.md) (per-jurisdiction obligations).
5. Identify your deliverable type from [`docs/02-deliverable-types.md`](./02-deliverable-types.md) and select the appropriate prompt from [`prompts/`](../prompts/).
6. Use [`templates/`](../templates/) for project-level briefs.
7. Use [`workflows/`](../workflows/) for the production-tier guidance.

## Related

- [Add-on README](../README.md)
- [Three sub-registers](./01-three-sub-registers.md)
- [Deliverable types](./02-deliverable-types.md)
- [Candidate imagery problem](./03-candidate-imagery-problem.md)
- [Glossary](./04-glossary.md)
- [Parent playbook foundational rules](../../../docs/01-foundational-rules.md)
