# Responsibility Pathway Design — Positioning Above Harness Engineering

## Purpose
This document clarifies where Responsibility Pathway Design (RPD) sits relative to recent discussions such as prompt engineering, context engineering, harness engineering, governance, and accountability design.

RPD should not be read as another local optimization technique for AI output.
It is a higher-order design layer for governing how responsibility flows across systems that already use such techniques.

## Short Thesis
Harness engineering asks:
- how should AI execution be structured?
- how should context, tools, checks, and runtime behavior be stabilized?

Responsibility Pathway Design asks:
- whose responsibility is the flow carrying?
- where can the flow be stopped?
- where does responsibility return to a human role?
- where does organizational responsibility begin?
- who owns repair and rollback after failure?

## Why This Layer Is Needed
A system can be excellent at:
- execution stability
- context management
- tool orchestration
- verification loops
- durable state
and still fail at responsibility.

That happens when:
- authority drifts without explicit rebinding
- human return points are unclear
- rollback exists technically but not organizationally
- records exist but cannot reconstruct responsibility flow
- governance exists outside the live pathway rather than inside it

RPD exists to make those pathways legible before failure, during interruption, and after repair.

## Placement Relative to Other Concepts

### Prompt Engineering
Prompt engineering shapes immediate output behavior.
RPD does not compete with it.
RPD asks what responsibility structure surrounds systems that rely on prompts.

### Context Engineering
Context engineering stabilizes memory, retrieval, and working context.
RPD asks how responsibility is carried across those stabilized contexts.
A better context window does not by itself create a safe responsibility pathway.

### Harness Engineering
Harness engineering structures execution through tools, runtime controls, verification, and external state.
RPD stands above that layer.
Harness engineering stabilizes execution.
RPD governs how judgment, delegation, interruption, repair, and ownership flow across that execution.

### Governance
Governance defines rules, roles, committees, and oversight structures.
RPD is not a replacement for governance.
It is the design layer that asks whether responsibility can still be traced, interrupted, rebound, and repaired when governance meets real operating flow.

### Accountability Design
Accountability design often asks who is responsible.
RPD asks how responsibility moves, where it breaks, and how it returns.
That makes it especially relevant in AI-involved environments where execution can be partially delegated, accelerated, or obscured.

## Practical Reading Rule
If a concept explains:
- how to structure AI execution,
then it is below RPD.

If a concept explains:
- how to preserve responsibility continuity, rebinding, interruption, repair, and rollback ownership across that execution,
then it is part of RPD territory.

## One-Sentence Definition
Responsibility Pathway Design is a higher-order design layer for governing how judgment, delegation, execution, interruption, repair, and organizational responsibility flow across AI-involved systems.

## Relationship to Other Documents
This document should be read together with:
- `docs/principles.md`
- `docs/layer-model.md`
- `docs/failure-and-repair-examples.md`
- `docs/terminology-and-nearby-concepts.md`
