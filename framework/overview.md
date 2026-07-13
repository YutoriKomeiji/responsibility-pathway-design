# Overview

Responsibility Pathway Design (RPD) is a human-readable design framework for examining how responsibility moves across AI-involved systems.

It helps reviewers ask where judgment, delegation, execution, interruption, repair, rollback, and organizational responsibility are carried, broken, obscured, returned, or rebound.

## Framework role

RPD is positioned between:

- Responsibility Pathway Model (RPM): theoretical and manuscript layer
- Responsibility Pathway Engineering (RPE): specification, template, checker, and implementation-adjacent layer

RPD does not replace either layer. It translates responsibility-pathway concerns into design language, examples, questions, and reviewable boundaries.

## Core questions

RPD asks:

- Where does responsibility originate?
- Where is judgment delegated?
- Where can action be interrupted?
- Where does the case return to a human or institution?
- What evidence remains available?
- Who owns repair, rollback, or reopening?
- Where does responsibility become organizational rather than local?

## Use

Use this framework to discuss, review, or redesign responsibility pathways before or after AI-involved work.

Useful contexts include:

- AI workflow design review
- governance discussion
- incident or near-miss review
- pre-mortem review
- organizational redesign around AI-involved execution

## Non-claim boundary

RPD is not:

- a legal doctrine
- a safety certification
- a compliance certification
- a fairness certification
- a production-readiness proof
- an implementation architecture
- a replacement for harness engineering
- a transfer of final responsibility to AI

RPD is a design and review language. It does not decide legal validity, deployment safety, compliance status, moral accountability, or production approval.

## Reading path

Start with:

1. [`../docs/principles.md`](../docs/principles.md)
2. [`../docs/layer-model.md`](../docs/layer-model.md)
3. [`../docs/failure-and-repair-examples.md`](../docs/failure-and-repair-examples.md)
4. [`../docs/positioning-above-harness-engineering.md`](../docs/positioning-above-harness-engineering.md)
5. [`../docs/terminology-and-nearby-concepts.md`](../docs/terminology-and-nearby-concepts.md)
6. [`../docs/operating-questions.md`](../docs/operating-questions.md)
