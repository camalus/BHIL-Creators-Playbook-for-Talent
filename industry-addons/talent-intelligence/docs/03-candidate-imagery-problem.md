# The Candidate Imagery Problem

Every visual decision in talent work routes through one question: when imagery shows a person, who is that person, and where did the likeness come from. This file documents the four solutions, their failure modes, and the default rule this add-on encodes.

## The Four Solutions

### 1. Stock Photography

**The default for a generation of recruiting work.** Generic Getty / iStock photography, often featuring conspicuous demographic variety in a workplace setting.

**Failure modes:**
- **Demographic stereotyping.** The composition of stock libraries skews toward stylized representations of "diverse workplace" that don't reflect any actual workforce.
- **Image recurrence.** The same Getty images appear across competitor career sites, dating internal teams' work and undermining brand differentiation.
- **The "iStock register."** Stock photography signals lack of investment to candidates. Universum's 2025 finding that 75% of candidates evaluate employer brand before compensation makes this register genuinely costly.

**When still acceptable:**
- Internal documents not customer-facing (training decks, internal HR materials).
- Quick LinkedIn recruiter posts where speed-to-publish exceeds brand investment.
- Conceptual or generic deliverables (a slide titled "Talent Acquisition" needs nothing more than illustrative imagery).

**When unacceptable:**
- Career site hero (the highest-stakes employer-brand asset).
- DEI report cover (synthetic-diversity stock is the central failure mode).
- Executive search dossiers (bottom of register; reads as outsourced).
- Premium workforce reports.

### 2. Real Employees With Consent

**The gold standard for top-of-funnel candidate-facing content.** Photography of actual employees in real workplace contexts, with documented consent and defined usage rights.

**Requirements:**
- A signed model release **separate from the employment agreement**. Employment relationship does not constitute consent for marketing imagery use.
- Defined usage scope (channels, geographies, time period).
- GDPR / CCPA-aligned withdrawal rights (the employee can revoke consent at any time, with operational implications for asset removal).
- Post-2024 AI-training language explicitly addressing whether the imagery may be used to train AI systems (default: no).
- Continued consent on employment status changes (an employee leaves the company; the imagery should be retired or re-confirmed).

**Failure modes:**
- **Consent gaps.** Employee imagery used after departure without re-confirmation.
- **Scope creep.** Imagery licensed for career site reused in social ads without re-licensing.
- **Demographic over-curation.** Selecting employees for visibility based on demographic representation rather than authentic narrative.

**Anchor exemplars:**
- Atlassian "Team Anywhere" — location-stamped portraits of named employees in their actual remote work locations.
- Airbnb "Live & Work Anywhere" — authentic distributed-workforce imagery.
- GitLab Handbook public photo briefs.
- Mollie commissioned signature photographer-filter approach.
- Microsoft DigiGirlz with real participants in technical contexts.
- Salesforce Equality Trailblazer Award profiles with full career narratives.

**This is the default for human imagery in this add-on.**

### 3. AI-Generated Imagery

**Adoption surged 2024-2026 but has produced documented backlash.** AI-generated images of fabricated employees, candidates, or workplace scenes.

**Documented failure cases:**

- **Levi's × Lalaland.ai (March 2023).** Levi's announced AI-generated diverse models for its e-commerce site. Drew immediate criticism for "artificial diversity." Levi's revised within six days that the pilot was *"not a means to advance diversity or as a substitute for the real action that must be taken."*
- **Mango Teen Sunset Dream Collection (July 2024).** Photorealistic AI-generated campaign drew consumer pushback over fabricated young models.
- **Guess / Vogue US (2025).** AI-generated print campaign in Vogue triggered backlash over fashion-industry job displacement and fabricated models.
- **Coca-Cola Christmas (2024 + 2025).** AI-generated holiday spots drew criticism in successive years, with the 2025 ads particularly scrutinized.
- **Toys "R" Us (2024).** AI-generated brand short film criticized for technical artifacts and uncanny-valley register.
- **Google Gemini (February 2024).** Gemini suspended image generation after over-correction produced historically inaccurate diverse Nazi soldiers — a high-profile case of representation testing failing badly.
- **Aerie pledge (October 2025).** Aerie pledged not to use AI-generated bodies, explicitly positioning the pledge as a brand differentiator.
- **Dove "Real Beauty Prompt Playbook."** Dove published an open prompting playbook explicitly designed to reduce demographic bias in AI image generation.

**Where AI imagery is still appropriate:**
- **Abstract concept illustration.** Skills graphs, talent-flow diagrams, dashboard hero plates with no human subjects.
- **Environmental and background scenes.** Workplace details (a desk, a window, a hallway) with no faces.
- **Architectural metaphor photography.** A mountain summit (Heidrick), a building exterior, a sky.
- **Clearly stylized illustrations.** Mailchimp's outsider art, GitLab's open-source illustrations, GitHub's Octocat — these are obviously not photo-real.
- **Document props and editorial textures.** Paper grain, topographic engravings, abstract data art for backgrounds.

**Where AI imagery is inappropriate:**
- **Career site heroes featuring fabricated "employees."**
- **DEI reports featuring synthetic diversity.**
- **Executive bio plates featuring AI-generated portraits of real or fabricated executives.**
- **Recruiter campaign tiles featuring AI-generated quoted "employees."**
- **Any context where a viewer might mistake the AI-generated person for a real employee or candidate.**

### 4. Anonymous-Silhouette / Illustrated / Environmental Alternatives

**The third path that sidesteps the problem.** Anonymous silhouettes (long-standing in executive search dossiers), back-of-head and over-the-shoulder framing, hands-on-keyboard close-ups with no face, environmental workplace details without people, and illustrated alternatives.

**Anchor exemplars:**
- GitLab open-source illustrated style.
- GitHub Octocat character.
- Notion hand-illustrated peach/cream system.
- Mailchimp Collins-designed outsider art.
- Canva Canvanaut gradient illustrations.
- Salesforce Astro Trailblazer characters.
- Anonymous silhouette avatars in executive search dossiers (industry standard).

**When this register works:**
- DEI report covers (architectural restraint or illustrated alternative).
- Career site hero secondary plates (environmental detail accompanying a real-employee primary).
- Job posting hero (the workplace detail register is now standard).
- Anonymized market mapping (anonymous silhouettes with role-and-industry labels).
- EVP pillar treatments (illustrated icon system over photography).

**When this register doesn't work:**
- Where a real person's authentic story is the deliverable's core (executive bio, employee testimonial).

## The Default Rule

This add-on encodes a single default rule across all prompts:

> **AI for abstract concept and environmental/background. Real photography (with consent and C2PA-tagged provenance) for humans wherever a viewer might mistake the subject for a real employee or candidate. Anonymous-silhouette / illustrated / environmental alternatives are the legitimate exits.**

Every prompt in this add-on declares its compliance with this rule. Where a prompt produces imagery that *could* be mistaken for a real person, the prompt either:

1. Generates clearly archetypal/composite people (with explicit no-real-person-resemblance language and visible AI disclosure), used for templates and explainers, never as final candidate-facing assets.
2. Generates the asset *without* people (environmental, illustrated, or typographic), with the human element added separately via real photography.

## The Decision Tree

A practical decision tree for any imagery request:

```text
Does this asset need to depict a person?

├── No → Proceed with AI generation (abstract, environmental, illustrated).
│         Apply compliance: C2PA, AI disclosure if photorealistic.
│
└── Yes → Continue.

  Does the depicted person represent a real, named individual?

  ├── Yes → Real photography only. Documented consent required.
  │         AI generation of real-person likeness is prohibited.
  │
  └── No  → Continue.

    Will the asset be candidate-facing or public-facing?

    ├── Yes → Continue with caution.
    │
    └── No  → AI generation may be permitted for archetypal/composite
              persons. Apply representation testing. Apply visible AI
              disclosure. Document in asset provenance.

      Could a viewer reasonably mistake the depicted person for a real
      employee or candidate?

      ├── Yes → AI generation prohibited. Use real photography with consent
      │         OR anonymous-silhouette / illustrated / environmental
      │         alternative.
      │
      └── No  → AI generation permitted (clearly stylized illustration,
                deliberately abstract figure). Apply representation testing
                and visible AI disclosure.
```

The full operational version of this tree, with documentation requirements at each node, is in [`workflows/candidate-imagery-decision-tree.md`](../workflows/candidate-imagery-decision-tree.md).

## The Trust Crisis Context

The candidate-imagery problem sits inside a larger industry trust crisis with two directions of suspicion:

1. **Candidates suspect employer-brand AI imagery.** Documented backlash cases have made consumer audiences attuned to AI-generated marketing imagery. Aerie's "no AI bodies" pledge is now a competitive position.
2. **Employers suspect AI-fabricated candidates.** Pindrop's "Ivan X" deepfake-candidate case and Gartner's forecast that 1 in 4 candidates globally will be AI-fabricated by 2028 (CNBC, April 2025) mean recruiters are increasingly wary of candidate-side AI.

In this environment, **visible C2PA Content Credentials disclosure on production-side AI imagery functions as a competitive trust signal** as well as a regulatory hedge. The add-on's compliance documentation treats this as a default, not an option. See [`compliance/disclosure-standards.md`](../compliance/disclosure-standards.md).

## Related

- [Add-on README](../README.md)
- [Three sub-registers](./01-three-sub-registers.md)
- [Deliverable types](./02-deliverable-types.md)
- [Candidate imagery decision tree (operational)](../workflows/candidate-imagery-decision-tree.md)
- [AI imagery policy](../compliance/ai-imagery-policy.md)
- [Disclosure standards](../compliance/disclosure-standards.md)
- [Representation testing](../compliance/representation-testing.md)
- [Consent and likeness](../compliance/consent-and-likeness.md)
