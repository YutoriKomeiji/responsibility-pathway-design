# Agent instructions for Responsibility Pathway Design

This file is the agent-facing routing surface for repository work. It does not replace the public design documents or create new design authority.

## Read first

Before editing RPD, fresh-read:

1. `README.md`
2. `START-HERE.md`
3. `PUBLIC_REVIEW_AND_USE.md`
4. the exact design document, template, worked case, or protocol affected by the task
5. `docs/verification-validation-vocabulary-v0.1.md` when evidence-stage language is involved

Do not substitute memory or a prior chat summary for the current repository text.

## Repository role

RPD is a public design-translation framework. It turns admitted problems and authorized normative inputs into reviewable design objectives, alternatives, trade-offs, verification obligations, and reopening conditions.

RPD is not an executable runtime. Executable engineering/runtime controls belong downstream in RPE/RPR/RPOS.

## Surface projection

Keep public entry surfaces reader-first.

- README / START-HERE: identity, purpose, navigation, concrete design output, current maturity.
- PUBLIC_REVIEW_AND_USE: evaluation/review procedure, critique posture, evidence-reading discipline.
- Worked cases / templates / protocols: local design semantics and evidence obligations.
- Internal or historical review notes: do not present them as current reader guidance unless explicitly promoted.

A compact automated-reader factual snapshot may appear in a public entry surface. Keep it factual. Evaluator procedure belongs in review/evaluation guidance rather than in the product/framework narrative.

## Evidence and claims

Preserve the distinction among design verification (D), implementation verification (I), exercise verification (X), operational verification (O), and broader contextual validation (V).

Do not convert one evidence level into another automatically. Do not turn a design record into certification, legal interpretation, operational authorization, or proof of implementation effectiveness.

## Writing rule

Prefer positive scope and ownership descriptions when they preserve the same meaning. Keep explicit negative boundaries where removal would create a plausible over-reading.

Do not bulk-delete phrases such as `not proven`, `Human Gate`, or proof/evidence boundaries. Classify each statement by artifact purpose and audience.

## Change boundaries

Keep changes focused and reversible. Stronger claims, canonical conceptual changes, public-release decisions, and Authority changes require the existing human review path.
