# Sharing and provenance

This portable package is an original synthesis of the requested review workflow. It contains no personal deployment configuration, credentials, private conversation/memory, or copied assistant platform policies. It is not installed, scheduled, or granted external write permissions by creating or sharing these files.

## Public references checked on 2026-10-16

- OpenAI Codex [review-agent](https://github.com/openai/codex/blob/main/codex-rs/skills/src/assets/samples/review-agent/SKILL.md), [Apache-2.0 license](https://github.com/openai/codex/blob/main/LICENSE), [notice](https://github.com/openai/codex/blob/main/NOTICE). Copyright 2025 OpenAI. Ideas used: defect-focused read-only review, real regression evidence, surrounding code/test checks, narrow locations and impact-based priority.
- Jesse Vincent's Superpowers [requesting-code-review](https://github.com/obra/superpowers/blob/main/skills/requesting-code-review/SKILL.md), [MIT license](https://github.com/obra/superpowers/blob/main/LICENSE). Copyright (c) 2025 Jesse Vincent. Ideas used: independent reviewer with limited context and explicit comparison SHAs, verification against requirements, evidence-based disagreement.

No upstream source file or substantial prose excerpt is redistributed. Upstream licenses apply to their respective projects, not automatically to this original package. This package is publicly available without a license grant. The owner has not selected distribution terms; public availability does not itself grant permission to use, modify, or redistribute it. References track upstream main as observed on the date above; they are not immutable pins. Source fetches and license inspection succeeded, while commit-metadata lookup was unavailable.

## Deliberate improvements

- Evidence hypotheses and counter-checks reduce plausible but false findings.
- Separate verifier/publisher roles isolate judgment from external write permission.
- Three outcomes distinguish a validated pass from missing evidence.
- Per-write identity/head/thread checks and live deduplication reduce race and retry mistakes.
- Focused finding follow-ups avoid unauthorized repeated broad reviews.
- Browser proof is tied to the tested head and privacy-checked before sharing.

This is a review workflow, not a security audit guarantee. Scenario tests are described in VALIDATION.md; they do not replace integration tests against a deployment's actual tools and permissions.
