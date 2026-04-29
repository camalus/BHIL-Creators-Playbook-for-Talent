# Consent and Likeness

Rules for when imagery depicts people. The compliance underpinning of [`docs/03-candidate-imagery-problem.md`](../docs/03-candidate-imagery-problem.md).

## Two Distinct Questions

When imagery depicts a person, two distinct compliance questions apply:

1. **Is this a real person?** If so, consent is required.
2. **Could this be mistaken for a real person?** If so, the AI generation rules in [`ai-imagery-policy.md`](./ai-imagery-policy.md) Section 4 apply.

These questions interact: AI-generated imagery resembling a real, identifiable individual without consent is the worst-case scenario, exposing Tennessee ELVIS Act, state right-of-publicity, EU AI Act Article 50 deepfake, and consumer-protection liability simultaneously.

## Real People — Consent Requirements

When imagery depicts a real, identifiable individual (an employee, a candidate, a board member, an executive), [Organization Name] obtains and documents:

### Written Model Release

A **written model release** signed by the depicted individual, separate from any employment agreement. The employment relationship does not constitute consent for marketing imagery use; this is a recurring failure mode.

The release defines, at minimum:

**Scope of use:**
- Channels where the imagery may appear (career site, social media, paid advertising, internal materials, conference materials, vendor partner materials).
- Geographies where the imagery may be deployed.
- Time period of use (typically 1-3 years; longer periods require renewal).
- Whether the imagery may be cropped, color-corrected, or composited (typically yes within the brand register).
- Whether the imagery may be modified by AI tools (e.g., background removal, lighting correction) (typically yes for technical adjustments).
- Whether the imagery may be used to train AI systems (default: **no**, given evolving regulatory landscape and trust considerations).
- Whether the imagery may be licensed to third parties.

**Withdrawal rights:**
- The depicted individual may revoke consent at any time.
- Revocation triggers operational removal: the imagery is retired from active use within [N] business days.
- Revocation does not require the individual to provide a reason.

**Compensation:**
- Whether compensation is provided for the imagery (talent fees, gift cards, charitable donations on behalf of the individual).
- If no compensation, the consideration is documented (typically the consideration is the individual's voluntary participation; this should be explicit).

**Privacy:**
- The imagery is processed under documented lawful basis (typically "consent" for marketing purposes under GDPR / equivalent).
- Data subject rights under the applicable privacy regime (access, deletion, portability) are honored.
- The individual is informed of how their data is processed.

### Re-Confirmation Triggers

Consent is re-confirmed when:

- **Employment status changes** — departure, role change to a different team or function, promotion to a more senior role.
- **Usage scope expands** — imagery licensed for career site is reused in social ads.
- **Imagery modification material** — imagery is edited beyond technical adjustments.
- **Time period elapses** — initial consent period ends.

When re-confirmation cannot be obtained (departed employee unreachable; refusal upon request), the imagery is retired.

### Special Case — Executive Search Candidates

Candidate dossiers in retained search depict candidates' identities and likenesses by their nature. The consent posture differs from employer-brand consent:

- Candidates have provided consent to the search firm to share their identity and credentials with the client search committee.
- This consent is typically not consent for broader marketing use; the dossier is confidential to the client.
- Reuse of candidate likeness or identity in any non-confidential context (e.g., a search firm's marketing materials) requires separate consent.
- AI-generated portraits of candidates are prohibited regardless of consent status — the candidate's actual photograph is the appropriate representation.

### Special Case — Public Figures

Public figures (executives in their public-figure capacity, politicians, recognized industry leaders) have reduced expectations for consent in journalistic and editorial contexts. However:

- This add-on's scope is recruiting and talent communications, which are commercial uses, not editorial.
- Commercial use of a public figure's likeness without consent is exposed (right of publicity).
- AI-generated likeness of a public figure without consent compounds the exposure (Tennessee ELVIS Act, EU AI Act Article 50).
- Default: even for public figures, obtain written consent for commercial recruiting use.

### Special Case — Group Photography

Imagery depicting groups (team photos, conference photography, event photography) requires consent from each individual depicted to a degree that allows them to be reasonably identified.

- Wide-angle group shots where individuals are not reasonably identifiable may not require individual consent (jurisdiction-dependent).
- Close-up group shots where individuals are identifiable require individual consent.
- Photography in public spaces follows jurisdictional rules (e.g., expectation of privacy in workplace settings vs. public events).

## Fabricated People — Likeness Avoidance

When imagery depicts a fabricated person (an AI-generated archetypal/composite person used in templates, explainers, or training materials per [`ai-imagery-policy.md`](./ai-imagery-policy.md) Section 3.5), the imagery must:

### Not Resemble a Real, Identifiable Individual

This is operationally enforced by:

1. **Prompt language that produces composite/archetypal results.** Prompts use compositional descriptors ("a 35-year-old field operator with athletic build, mid-length dark hair pulled back, charcoal field jacket") rather than language that could echo specific real people.
2. **Avoidance of real-person reference.** Prompts do not include names of real people, references to specific public figures, or attributes that uniquely identify a real individual.
3. **Resemblance check.** Generated outputs are checked against a reverse-image-search baseline to confirm they do not closely resemble a recognizable real individual.
4. **Documentation.** The prompt and the resemblance check result are archived per [`ai-imagery-policy.md`](./ai-imagery-policy.md) Section 9.

### Not Be Mistaken for a Real Employee or Candidate

This is operationally enforced by:

1. **Visible AI disclosure.** Per [`disclosure-standards.md`](./disclosure-standards.md), visible disclosure is applied so that the viewer is informed.
2. **Stylization or context cues.** Where possible, the imagery is rendered in a register that signals "this is a template / explainer / illustration" rather than "this is an actual employee."
3. **Confined scope of use.** Templates and explainers are typically internal or training-context use; not deployed as final candidate-facing assets.

### Pass Representation Testing

Per [`representation-testing.md`](./representation-testing.md), all imagery depicting people undergoes representation testing regardless of whether the depicted person is real or fabricated.

## Anonymous-Silhouette Convention

The anonymous-silhouette convention — long-standing in executive search dossiers, increasingly used in DEI and talent intelligence work — sidesteps both consent and likeness concerns:

- Silhouettes / back-of-head / over-the-shoulder framing depicting no identifiable individual.
- Hands-on-keyboard, hands-holding-document, hands-on-conference-table close-ups.
- Workplace environmental detail with no faces.
- Stylized geometric avatars (industry-standard gray silhouettes in dossiers).

These conventions do not require consent (no real person depicted) and do not raise likeness concerns (no fabricated person could be mistaken for real). They are appropriate for:

- Anonymized longlists and market maps.
- DEI report imagery where the focus is data, not individuals.
- Job posting environmental imagery.
- Career site secondary plates.

## Group Imagery and Composition

When designing imagery depicting multiple people:

- **Document each individual's consent separately.**
- **Apply representation testing to the group as well as to each individual.**
- **Avoid composite imagery that combines real people into fabricated groupings** (e.g., AI-compositing real employees from different photographs into a "team" that doesn't exist as depicted) unless explicitly disclosed.
- **Be cautious with stock-photo composites that read as real teams.** Stock photography is licensed for use but may not be licensed for representation as a specific organization's team.

## Failure Modes

| Failure Mode | What Happens | Mitigation |
| :--- | :--- | :--- |
| **Consent for employment, not marketing** | Employee imagery used in recruiting; employee unaware or withdrew. Litigation, reputational. | Separate written model release. Re-confirmation upon status change. |
| **Scope creep** | Imagery licensed for one channel reused in another. Privacy, contract. | Defined scope in release; channel additions require re-confirmation. |
| **Departed employee** | Employee leaves; imagery still in market. Right of publicity, contract. | Re-confirmation triggers; operational removal process. |
| **AI-generated likeness leak** | Generated imagery resembles a real individual. Tennessee ELVIS, right of publicity. | Reverse-image-search check; archetypal-only prompt language. |
| **AI-generated employee fabrication** | Career site shows AI "employees." Consumer protection, trust. | Default rule applied; real photography for humans on candidate-facing assets. |
| **Group composite** | Real employees AI-composited into fictional team. Privacy, contract, deception. | Document each individual's photograph and consent; no AI-compositing of real-person groupings. |

## Related

- [Compliance README](./README.md)
- [AI imagery policy](./ai-imagery-policy.md)
- [Disclosure standards](./disclosure-standards.md)
- [Representation testing](./representation-testing.md)
- [Candidate imagery problem (overview)](../docs/03-candidate-imagery-problem.md)
- [Candidate imagery decision tree (operational)](../workflows/candidate-imagery-decision-tree.md)
