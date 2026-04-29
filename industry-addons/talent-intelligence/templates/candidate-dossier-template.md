# Candidate Dossier Spec Template

Project-level brief for a retained-search candidate dossier. Instantiate by copying this template to your project workspace and filling in the bracketed fields.

---

## Project: [PROJECT CODENAME]

| Field | Value |
| :--- | :--- |
| **Project codename** | [e.g., "Project Aurora"] |
| **Search type** | [CEO / CFO / CXO / Board / GM / VP / Practice Leader] |
| **Practice area** | [CEO & BOARD OF DIRECTORS / FINANCIAL OFFICERS / TECHNOLOGY OFFICERS / etc.] |
| **Client firm** | [Client name — confidential within team] |
| **Client code name** | [Client codename used in dossier — anonymized] |
| **Search slate** | [Slate I / Slate II / Slate III / Final Recommendations] |
| **Dossier version** | [v1.0 / v2.0 / v3.0] |
| **Production date** | [YYYY-MM-DD] |
| **Engagement lead** | [Lead consultant name] |
| **Project manager** | [PM name] |
| **Designer / producer** | [Designer / agency name] |

## Register Declaration

**Sub-register:** A — Retained-search editorial.

This project uses the BHIL parent brand register applied to retained-search editorial register (sub-register A).

| Element | Value |
| :--- | :--- |
| **Palette primary** | Deep navy `#0F1A2E` |
| **Palette ground** | Warm ivory `#F5EFE3` |
| **Accent — gold** | Warm amber `#C9A24A` |
| **Accent — alert** | Signal red `#A82A2E` |
| **Display typeface** | Canela Deck (or GT Sectra Bold register) |
| **Body typeface** | [Editorial body type — typically a humanist sans] |
| **Photography register** | Documentary, soft single-source, slight desaturation, tight framing |

If client-firm register override applies (Spencer Stuart, Korn Ferry, Egon Zehnder, etc.), document the substitution here:

| Element | BHIL Default | Client Override |
| :--- | :--- | :--- |
| Primary accent | `#A82A2E` (signal red) | [e.g., Spencer Stuart `#C8102E`] |
| Display typeface | Canela Deck | [e.g., Rotis Serif Regular] |
| Photography register | [BHIL] | [Client-specific] |

## Asset Inventory

The dossier comprises the following assets:

| Asset | Prompt Reference | Aspect Ratio | Notes |
| :--- | :--- | :--- | :--- |
| Cover | [`../prompts/01-executive-search/01-candidate-dossier-cover.md`](../prompts/01-executive-search/01-candidate-dossier-cover.md) | 8.5×11" portrait | Architectural metaphor + STRICTLY CONFIDENTIAL stamp + project codename |
| Section dividers (4-6) | Variant of cover | 8.5×11" portrait | Section name overlay |
| Executive bio plates | [`../prompts/01-executive-search/02-executive-bio-plate.md`](../prompts/01-executive-search/02-executive-bio-plate.md) | 8.5×11" portrait | Real photographs of consenting candidates; AI imagery prohibited for candidate likenesses |
| Anonymized longlist | [`../prompts/01-executive-search/03-anonymized-market-map.md`](../prompts/01-executive-search/03-anonymized-market-map.md) | 11×17" tabloid | Gray silhouette avatars, hatched-circle company replacements, lock icons |
| Market map | [`../prompts/01-executive-search/03-anonymized-market-map.md`](../prompts/01-executive-search/03-anonymized-market-map.md) | 11×17" tabloid | Bubble cluster or org-tree |
| Colophon | (typographic only) | 8.5×11" portrait | Confidentiality notice + AI disclosure if applicable |

Asset count target: [N] assets.

## Anonymization Rules

This dossier follows the standard retained-search anonymization conventions:

- **Cover anonymizes the client.** The client firm is referred to by codename only on the cover; revealed inside.
- **Longlist redacts identities.** Candidates on the longlist are represented by gray silhouette avatars with role-and-industry descriptors only ("CFO – Top-5 Global Bank"). No names, no photographs.
- **Company logo replacement.** Real company logos are replaced with hatched neutral monogram circles in any anonymized context.
- **Lock icons.** Confidential nodes in market maps and org charts carry small lock icons.
- **STRICTLY CONFIDENTIAL stamp.** Cover carries diagonal "STRICTLY CONFIDENTIAL" stamp in signal red, rotated -15°, with hairline rules above and below.
- **Codename in footer.** Project codename and dossier version in footer of every page.

## AI Imagery Compliance

| Question | Decision |
| :--- | :--- |
| **AI imagery on cover?** | [YES — abstract architectural metaphor only / NO — real photography only] |
| **AI imagery on section dividers?** | [YES / NO] |
| **AI imagery in market map / org chart?** | [YES — anonymized silhouettes and hatched circles only / NO] |
| **AI imagery for any candidate likeness?** | **NO. Tennessee ELVIS Act / state right-of-publicity exposure.** Real photographs only with documented consent. |
| **C2PA Content Credentials applied?** | YES — to all AI-generated assets |
| **Visible AI disclosure on cover?** | [YES — colophon / NO — confidential context exemption] |
| **Visible AI disclosure on colophon?** | YES |

## Consent Inventory

| Asset | Real Person Depicted | Consent Documented | Notes |
| :--- | :--- | :--- | :--- |
| Cover | None | N/A | Architectural metaphor |
| Bio plate — [Candidate 1 name] | [Candidate 1] | [YES — release on file] | Consent for client-search-committee use only; not for further distribution |
| Bio plate — [Candidate 2 name] | [Candidate 2] | [YES — release on file] | Same scope |
| ... | ... | ... | ... |

## Representation Testing

For assets depicting people:

| Asset | Test 1 (MST) | Test 2 (Intersectional) | Test 3 (Bias amplification) | Failure-Mode Review | Result |
| :--- | :-: | :-: | :-: | :-: | :-: |
| Bio plates (real photography) | N/A — real | N/A — real | N/A — real | Pass | Pass |
| Anonymized longlist (gray silhouettes) | N/A — abstract | N/A — abstract | N/A — abstract | Pass | Pass |

Real photography of consenting candidates does not require Test 1, 2, or 3 (these tests apply to AI-generated imagery). Failure-mode review still applies.

## Production Workflow

| Stage | Owner | Target Date |
| :--- | :--- | :--- |
| Brief approved | [PM] | [Date] |
| Cover generated and reviewed | [Designer] | [Date] |
| Bio plate photography scheduled | [PM + photographer] | [Date] |
| Bio plates reviewed | [Engagement lead + designer] | [Date] |
| Market map drafted | [Researcher + designer] | [Date] |
| Anonymization review | [Engagement lead] | [Date] |
| Compliance review | [Compliance reviewer] | [Date] |
| Final approval | [Engagement lead] | [Date] |
| Delivered to client | [PM] | [Date] |

## Recordkeeping

The following are archived for **five years from the dossier's last delivery date**:

- This template, completed.
- All prompts used (with iteration history).
- Model versions used.
- All reference images.
- All generated assets (final + variants).
- Reviewer identities and notes.
- Representation test results (per asset).
- Consent documentation (per real person depicted).
- Disclosure language and placement.
- Delivery records (date, version, recipient).

Archive location: [project workspace path or DAM identifier].

## Confidentiality Notice

This template, the assets it documents, and all associated material are STRICTLY CONFIDENTIAL. Disclosure outside the engagement team and the client search committee is prohibited.

## Related

- [Templates README](./README.md)
- [Executive search prompts](../prompts/01-executive-search/README.md)
- [AI imagery policy](../compliance/ai-imagery-policy.md)
- [Consent and likeness](../compliance/consent-and-likeness.md)
- [Sub-register A specification](../reference/sub-register-a-retained-search.md)
