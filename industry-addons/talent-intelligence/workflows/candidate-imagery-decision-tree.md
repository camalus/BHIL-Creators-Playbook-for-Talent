# Candidate Imagery Decision Tree

The operational version of the decision tree from [`../docs/03-candidate-imagery-problem.md`](../docs/03-candidate-imagery-problem.md). Every imagery request — regardless of production tier — passes through this tree before generation begins. The tree is fast in practice (most decisions take seconds) but its documentation requirement ensures defensible-by-default posture.

## The Tree

```text
START — IMAGERY REQUEST RECEIVED

╭─────────────────────────────────────────────────────────────────────╮
│ NODE 1 — Does this asset need to depict a person?                   │
╰─────────────────────────────────────────────────────────────────────╯
   │
   ├── NO ─→ NODE 6 (proceed with non-person AI generation)
   │
   └── YES ─→ NODE 2

╭─────────────────────────────────────────────────────────────────────╮
│ NODE 2 — Does the depicted person represent a real, named           │
│         individual?                                                 │
╰─────────────────────────────────────────────────────────────────────╯
   │
   ├── YES ─→ NODE 3 (real person — consent path)
   │
   └── NO ─→ NODE 4 (fabricated person — composite path)

╭─────────────────────────────────────────────────────────────────────╮
│ NODE 3 — Real person path: Do you have documented consent for       │
│         this asset's use?                                           │
╰─────────────────────────────────────────────────────────────────────╯
   │
   ├── YES ─→ Use real photography. AI generation of likeness PROHIBITED.
   │           Apply C2PA. Apply representation testing. Document.
   │
   └── NO ─→ STOP. Initiate consent process. Do not proceed with this
            asset until consent is documented OR substitute with a
            non-real-person alternative (NODE 4 or NODE 6).

╭─────────────────────────────────────────────────────────────────────╮
│ NODE 4 — Fabricated person path: Will the asset be candidate-       │
│         facing or public-facing?                                    │
╰─────────────────────────────────────────────────────────────────────╯
   │
   ├── NO (internal / template / explainer) ─→ NODE 5
   │
   └── YES ─→ NODE 5 (proceed with caution)

╭─────────────────────────────────────────────────────────────────────╮
│ NODE 5 — Could a viewer reasonably mistake the depicted person      │
│         for a real employee or candidate?                           │
╰─────────────────────────────────────────────────────────────────────╯
   │
   ├── YES (photo-real or near-photo-real) ─→
   │     STOP. AI generation of fabricated person PROHIBITED for this
   │     use case. Path options:
   │       • Use real photography with consent (NODE 2 → NODE 3 YES)
   │       • Use anonymous-silhouette / illustrated / environmental
   │         alternative (NODE 6 with explicit "no faces" or
   │         illustrated register)
   │
   └── NO (clearly stylized illustration; deliberately abstract) ─→
        Proceed. Generate with explicit illustration / abstract register.
        Apply representation testing (Test 1, Test 2, Test 3).
        Apply visible AI disclosure.
        Apply C2PA.
        Document in provenance archive.

╭─────────────────────────────────────────────────────────────────────╮
│ NODE 6 — Non-person path: AI generation permitted.                  │
╰─────────────────────────────────────────────────────────────────────╯
   │
   ├── Apply C2PA Content Credentials.
   ├── Apply visible AI disclosure if photorealistic AND in
   │   candidate-facing channel.
   ├── Document prompt, model, references, reviewer, output.
   └── Archive per recordkeeping requirements.

END
```

## Documentation Requirements At Each Node

Every traversal of the tree produces a documentation record. Even fast Tier 1 decisions create a record (typically a single line in a project log).

### NODE 1 Documentation

Record:
- Asset description.
- Decision (depicts person YES / NO).

### NODE 2 Documentation

Record (if NODE 2 reached):
- Whether person is real or fabricated.
- If real, the named individual.

### NODE 3 Documentation

Record (if NODE 3 reached):
- Consent status.
- If consent documented: reference to release file, scope, period, withdrawal terms.
- If consent not documented: the substitution decision and the path forward.

### NODE 4 Documentation

Record (if NODE 4 reached):
- Audience scope (internal / candidate-facing / public-facing).
- Use case (template / explainer / final asset).

### NODE 5 Documentation

Record (if NODE 5 reached):
- Visual register (photo-real / near-photo-real / clearly stylized illustration / abstract).
- Reviewer assessment of "could be mistaken for real."
- Decision (proceed / substitute).
- If substituting, the substitution path.

### NODE 6 Documentation

Record (if NODE 6 reached):
- Prompt used.
- Model and version.
- Reference images.
- Reviewer name.
- Representation test results (where applicable).
- Disclosure language and placement.
- C2PA manifest reference.

## The Substitution Paths

When the tree directs substitution, three paths are available:

### Substitution Path 1 — Real Photography With Consent

The gold standard. Documented model release per [`../compliance/consent-and-likeness.md`](../compliance/consent-and-likeness.md). Real employee in real workplace context. Requires lead time for consent process and photography commissioning.

### Substitution Path 2 — Anonymous-Silhouette / Environmental Alternative

The "no-faces" register. Workplace environmental detail with no people, hands-on-keyboard close-ups with no face, anonymous silhouettes (industry standard in executive search dossiers), or back-of-head / over-the-shoulder framing.

Use prompt patterns from:
- [`../prompts/03-employer-brand/12-job-posting-environmental.md`](../prompts/03-employer-brand/12-job-posting-environmental.md) (workplace environmental)
- [`../prompts/01-executive-search/03-anonymized-market-map.md`](../prompts/01-executive-search/03-anonymized-market-map.md) (anonymous silhouettes)

### Substitution Path 3 — Illustrated Alternative

The "clearly stylized illustration" register. GitLab / Notion / Mailchimp / Octocat / Salesforce Trailblazer aesthetic — illustration that is unmistakably illustrated rather than photo-real.

Use prompt patterns from:
- [`../prompts/03-employer-brand/09-career-site-hero.md`](../prompts/03-employer-brand/09-career-site-hero.md) (illustrated career-site hero)
- [`../prompts/03-employer-brand/11-evp-pillar-treatment.md`](../prompts/03-employer-brand/11-evp-pillar-treatment.md) (illustrated EVP icon system)

## Common Tree-Traversal Patterns

Examples of how typical projects traverse the tree:

### Pattern A — Career Site Hero (Engineering)

```text
NODE 1: Does asset need to depict a person? YES (engineering team).
NODE 2: Real or fabricated? Decision: REAL employees (with consent).
NODE 3: Consent documented? YES — releases on file for two named engineers.
RESULT: Real photography. AI generation of likeness PROHIBITED.
        C2PA applied to the layout (typography, color treatment).
        Documentation archived.
```

### Pattern B — EVP Pillar Icon System

```text
NODE 1: Does asset need to depict a person? NO (abstract icons).
NODE 6: Non-person path. AI permitted.
RESULT: Recraft V3 generates the icon set.
        C2PA applied. Disclosure on toolkit colophon. Documentation archived.
```

### Pattern C — Job Posting Environmental Header

```text
NODE 1: Does asset need to depict a person? NO (workplace environmental).
NODE 6: Non-person path. AI permitted.
RESULT: NB Pro generates the workplace environmental scene.
        C2PA applied. Disclosure on job posting page. Documentation archived.
```

### Pattern D — DEI Report Cover (Architectural Path)

```text
NODE 1: Does asset need to depict a person? NO (architectural metaphor).
NODE 6: Non-person path. AI permitted.
RESULT: MJ v7 generates the architectural restraint cover.
        C2PA applied. Visible disclosure on colophon. Documentation archived
        with extra stringency given DEI category compliance stakes.
```

### Pattern E — DEI Report Cover (Named-Employee Path)

```text
NODE 1: Does asset need to depict a person? YES (one named employee).
NODE 2: Real or fabricated? REAL.
NODE 3: Consent documented? YES — full release for DEI report use.
RESULT: Real photography of named employee.
        AI generation of likeness PROHIBITED.
        Layout typography may use AI (Ideogram).
        C2PA applied to the layout. Visible disclosure on cover with
        named-employee attribution. Documentation archived.
```

### Pattern F — Template / Explainer Composite Person

```text
NODE 1: Does asset need to depict a person? YES (training material example).
NODE 2: Real or fabricated? FABRICATED.
NODE 4: Candidate-facing? NO (internal training only).
NODE 5: Could be mistaken for real? Generated as photo-real → YES → STOP.
        Substitute with clearly stylized illustration.
        Re-generate with illustration register.
        Re-traverse: NODE 5 NO.
RESULT: Illustrated archetypal figure for training.
        Representation testing applied. C2PA applied. Disclosure applied.
        Documentation archived.
```

## Failure Modes

| Failure Mode | What Happens | Mitigation |
| :--- | :--- | :--- |
| **Tree skipped** | Asset generated without traversal; documentation gap | Tree traversal mandatory at brief stage; logged in project workspace |
| **NODE 5 misclassification** | Photo-real output classified as "stylized" by producer; published as candidate-facing | Independent reviewer assessment at NODE 5; reviewer rejection authority |
| **Consent assumed** | NODE 3 answered YES without verifying release | Reviewer verifies release before sign-off; release file linked in documentation |
| **Substitution skipped** | Tree directs substitution but producer proceeds with AI generation under deadline pressure | Reviewer enforcement; escalation to project lead |
| **Documentation gap** | Tree traversed but record not created | Documentation template integrated into production workflow; non-completion blocks publication |

## Related

- [Workflows README](./README.md)
- [Candidate imagery problem (overview)](../docs/03-candidate-imagery-problem.md)
- [AI imagery policy](../compliance/ai-imagery-policy.md)
- [Consent and likeness](../compliance/consent-and-likeness.md)
- [Disclosure standards](../compliance/disclosure-standards.md)
- [Representation testing](../compliance/representation-testing.md)
- [Three production tiers](./three-production-tiers.md)
