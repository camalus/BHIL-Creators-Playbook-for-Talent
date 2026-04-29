# Quick Reference

Copy/paste-ready prompt library for production teams. This directory is a fast-path companion to [`../prompts/`](../prompts/) — it surfaces the most common prompt patterns in a flatter, denser format suitable for stakeholder review documents and for designers who want to ship to first generation in minutes.

## Files

| File | Purpose |
| :--- | :--- |
| [`20-prompt-library.md`](./20-prompt-library.md) | 20 production-ready prompts in a single scannable file. Each prompt: number, title, sub-register, model, aspect ratio, use case, compliance posture, copy/paste code block. The source of truth for Section 11 of the BHIL-branded reference document. |

## How To Use

1. **Pick your deliverable.** The 20-prompt library is grouped by sub-register: A (executive search & retained search), B (platform dashboard), C (employer brand & recruiting marketing), and a fourth group for workforce reports & conference materials.
2. **Copy the prompt code-block.** Each prompt is a fenced code block ready to paste into your model of choice.
3. **Replace every `[PLACEHOLDER]`.** Bracketed UPPERCASE tokens (`[PROJECT CODENAME]`, `[BRAND ACCENT]`, `[ROLE TITLE]`, `[QUOTE]`, etc.) are the fields you customize per project.
4. **Submit with the noted parameters.** Each prompt declares the recommended model, parameters, and aspect ratio.
5. **Apply compliance.** Every prompt includes a one-line compliance note. The full compliance framework lives in [`../compliance/`](../compliance/).

## Relationship to `prompts/`

The full prompt files in [`../prompts/`](../prompts/) contain four-variant libraries, parameter tables, failure modes, and detailed compliance notes per prompt. They are the reference resource for production teams designing complex deliverables.

The `quick-reference/` directory is the fast-path companion — same prompts, denser format, no four-variant libraries or per-prompt failure-mode tables. Use the quick reference for speed; use the full prompt files when you need depth.

## Compliance Posture

The default rule applies across every prompt in this directory:

> AI for abstract concept and environmental/background. Real photography (with consent and C2PA-tagged provenance) for humans wherever a viewer might mistake the subject for a real employee or candidate. Anonymous-silhouette / illustrated / environmental alternatives are the legitimate exits.

Every prompt below assumes this rule is in force. Prompts that produce imagery resembling people are written to produce environmental, illustrated, or clearly archetypal output — never photo-real fabricated employees. If you adapt a prompt and remove the guardrails, you take on the compliance posture of doing so. The add-on's compliance documentation is non-optional for production work — see [`../compliance/`](../compliance/).

## Related

- [Add-on README](../README.md)
- [Full prompt library](../prompts/README.md)
- [Compliance framework](../compliance/README.md)
- [Candidate imagery decision tree](../workflows/candidate-imagery-decision-tree.md)
- [Three sub-registers reference](../docs/01-three-sub-registers.md)
