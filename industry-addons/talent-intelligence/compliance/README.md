# Compliance

Regulatory and ethics documentation for AI imagery in talent intelligence and recruiting contexts. As of April 2026, this is the tightest compliance envelope in commercial creative.

This directory exists because no major employer-brand team or industry association (SHRM, ATAP) had published a formal AI-imagery disclosure standard at the time of v1.0.0. The files below aim to fill that gap with a defensible default policy that production teams can adapt and counsel can review.

## Files

| File | Purpose |
| :--- | :--- |
| [`ai-imagery-policy.md`](./ai-imagery-policy.md) | Umbrella policy template defining what AI imagery is permitted, what is prohibited, and what governance applies. Adapt and ratify per organization. |
| [`disclosure-standards.md`](./disclosure-standards.md) | C2PA Content Credentials standards plus visible-disclosure requirements. The technical and design implementation of disclosure. |
| [`jurisdiction-matrix.md`](./jurisdiction-matrix.md) | Per-jurisdiction obligations cheat-sheet (EU AI Act, Colorado AI Act, Illinois HB 3773, NYC Local Law 144, Maryland HB 1202, Tennessee ELVIS Act, Ontario Bill 149, Quebec Law 25, UK ICO). |
| [`representation-testing.md`](./representation-testing.md) | Demographic representation testing protocols using the Monk Skin Tone Scale plus intersectional audit. |
| [`consent-and-likeness.md`](./consent-and-likeness.md) | Rules for when imagery depicts people: consent requirements, likeness avoidance, and the distinction between archetypal and identifiable. |

## The Default Posture

The compliance documentation in this add-on is designed to support a single default posture:

> **Defensible-by-default.** Every asset that could be reviewed by an external regulator, plaintiff's counsel, or candidate advocacy group is produced as if it will be — with documented prompts, model versions, reviewer identity, representation test results, consent documentation (where applicable), and C2PA-signed provenance retained for at least five years.

Five-year retention aligns with OFCCP recordkeeping requirements and provides headroom for the EU AI Act's high-risk obligations (effective August 2, 2026 for recruitment) and Colorado AI Act enforcement (effective June 30, 2026 after the August 2025 special-session delay).

## What This Documentation Is Not

- **Not legal advice.** This is the most current public synthesis of regulatory landscape as of April 2026, intended as production guidance to inform a defensible posture. It is not a substitute for review by counsel licensed in your jurisdiction.
- **Not exhaustive of all applicable law.** Anti-discrimination law has been actively enforced in this category for sixty years; this documentation focuses on the AI-specific overlay. Title VII, ADEA, ADA, GINA, EPA, and state equivalents continue to apply to recruiting practices regardless of whether AI is involved.
- **Not static.** The regulatory landscape is changing rapidly. The jurisdiction matrix is dated; updates to this add-on track regulatory developments per the [`CHANGELOG.md`](../CHANGELOG.md) roadmap.

## How To Use The Compliance Documentation

For new projects:

1. **Read the AI imagery policy template** ([`ai-imagery-policy.md`](./ai-imagery-policy.md)) and adapt it to your organization's posture. Have counsel review.
2. **Identify your jurisdictional footprint** ([`jurisdiction-matrix.md`](./jurisdiction-matrix.md)). Multi-jurisdiction projects (US + EU + UK + Canada) require the most stringent applicable obligations across all dimensions.
3. **Apply the candidate imagery decision tree** ([`../workflows/candidate-imagery-decision-tree.md`](../workflows/candidate-imagery-decision-tree.md)) to every imagery decision.
4. **Apply the disclosure standards** ([`disclosure-standards.md`](./disclosure-standards.md)) to every AI-generated asset.
5. **Apply representation testing** ([`representation-testing.md`](./representation-testing.md)) to every asset depicting people.
6. **Document consent** ([`consent-and-likeness.md`](./consent-and-likeness.md)) for every asset depicting real people.
7. **Archive provenance** for five years minimum.

For existing projects:

1. Audit existing AI-generated imagery against the disclosure standards. Add Content Credentials retroactively where possible.
2. Audit existing real-person imagery against the consent requirements. Re-confirm where employment status or usage scope has changed.
3. Document any compliance gaps and remediate.

## Related

- [Add-on README](../README.md)
- [Candidate imagery problem](../docs/03-candidate-imagery-problem.md)
- [Candidate imagery decision tree](../workflows/candidate-imagery-decision-tree.md)
- [AI disclosure statement template](../templates/ai-disclosure-statement-template.md)
