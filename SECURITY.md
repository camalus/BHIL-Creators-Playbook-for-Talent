# Security and Sensitive Asset Policy

This repository is a public-facing reference. It must never contain:

## Hard exclusions

- **Real Sref codes** authored by BHIL or used in client work. The numeric codes that appear in this repository (e.g. `1742826451`) are illustrative placeholders and should not be treated as live brand codes.
- **Real moodboard IDs or personalization profile codes.** Use placeholders like `[BHIL PROFILE]`, `[BHIL COVER SREFS]`, `[BHIL FRAMEWORK PROFILE]`.
- **Omni-Reference URLs** (`https://s.mj.run/XXXX`). These are character/asset locks and must remain in the access-controlled brand vault.
- **Client identifiers** — names, codenames, sector tags that could deanonymize an engagement.
- **API keys, tokens, or credentials** for any image generation service or downstream pipeline component (Runway, Veo via Vertex AI, Gemini API, OpenAI, Black Forest Labs).
- **Trained-model artifacts** — LoRA weights, embeddings, or fine-tunes derived from BHIL or client data.
- **Cover-art file outputs** that are part of an unreleased deliverable.

## Reporting a leak

If you find any of the above committed to this repository — in current code or in git history — do **not** open a public issue.

Contact Barry Hurd directly via the channel listed in the BHIL internal directory. The repository will be force-pushed and the asset rotated.

## Pipeline security

Operational guidance for client-confidential work:

- **Do not use cloud-hosted models** for engagements with data residency or sovereignty constraints. Use Flux.2 [dev] or [klein] open weights running in the BHIL air-gapped environment. See [`frameworks/flux/`](frameworks/flux/).
- **Do not feed client-identifiable text or imagery into multi-image fusion pipelines** unless the engagement contract explicitly permits cloud processing.
- **Treat SynthID and C2PA Content Credentials as features, not bugs.** They make non-disclosure of AI use untenable; therefore disclose AI use in methodology notes by default. See [`frameworks/nano-banana/synthid-c2pa.md`](frameworks/nano-banana/synthid-c2pa.md).

## Supply-chain notes

- The `.github/workflows/` files in this repository run on public GitHub Actions runners against repository content only. They do not call external image-generation APIs and do not require secrets.
- If the workflows are extended in the future to call generation APIs (for prompt validation or example regeneration), do so via OIDC-federated credentials, not long-lived tokens.
