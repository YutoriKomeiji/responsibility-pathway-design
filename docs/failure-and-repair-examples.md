# Responsibility Pathway Design — Failure and Repair Examples

## Purpose
This document provides compact example patterns showing how Responsibility Pathway Design (RPD) can be used to interpret failure and define repair.

These are not legal case analyses.
They are framework-oriented examples meant to show how pathway breaks can be located and how repair / rebinding can be designed.

## Why Examples Matter
A principles layer explains what RPD is.
A layer model explains where responsibility should be examined.
Examples help show how those ideas work in practice.

RPD becomes more useful when it can answer not only:
- what responsibility is
but also:
- where it broke
- how it can be repaired
- how authority should be rebound afterward

---

## Example 1: AI recommendation adopted without explicit ownership

### Situation
An AI-assisted workflow produces a recommendation used by staff in a high-impact operational decision.
The output is presented as the next obvious action.
No explicit human owner rebinds responsibility before execution.

### Pathway break
- Decision authority drifted into system fluency
- Execution continued without explicit accountability rebinding
- Record layer did not preserve a clear confirmation point

### Failure reading
The failure is not only "the AI was wrong" or "the operator clicked too quickly."
The deeper issue is that delegation occurred without a visible authority handoff.

### Repair path
- restore explicit human confirmation before execution
- bind decision ownership to a named role
- require a visible override / approval checkpoint
- preserve confirmation trace in the record layer

### Design lesson
Smooth recommendations must not erase the point where responsibility is rebound.

---

## Example 2: Organization delegates monitoring to AI but keeps no rollback owner

### Situation
An organization deploys AI-assisted monitoring for anomaly detection and automated alert handling.
The system reduces human review load, but no clearly assigned role owns rollback when misclassification causes harm.

### Pathway break
- execution and escalation moved into system flow
- repair authority was never assigned
- rollback existed technically, but not organizationally

### Failure reading
This is not only a tooling failure.
It is a repair-layer design failure.
A system that has no practical rollback owner is not responsibility-complete.

### Repair path
- define who can pause automated handling
- define who can reverse incorrect escalations
- define who records the repair event
- define which signals require manual authority rebinding

### Design lesson
Repairability must be owned, not merely available.

---

## Example 3: Executive intent and operational execution diverge

### Situation
Leadership states that AI should be used only as decision support.
At the operational layer, teams begin treating AI output as a default answer because throughput pressure rewards compliance speed.

### Pathway break
- intent layer and execution layer diverged
- interface and workflow normalized passive acceptance
- authority drift occurred without explicit policy update

### Failure reading
The pathway is broken between declared intent and actual operating behavior.
This is not solved by naming a single guilty individual.

### Repair path
- inspect where workflow incentives pushed passive adoption
- restore explicit policy-to-operation binding
- add review checkpoints where output becomes action
- measure whether staff still exercise judgment in practice

### Design lesson
A declared policy is not a sound pathway if the operating layer silently rewrites it.

---

## Example 4: Responsibility appears assigned after the fact, but cannot be reconstructed

### Situation
After an incident, the organization points to a nominal owner.
However, logs do not clearly show who approved, who overrode, or whether the decision path passed through a required checkpoint.

### Pathway break
- record layer is too weak to reconstruct authority flow
- nominal assignment exists, but inspectability does not

### Failure reading
Responsibility that cannot be reconstructed is structurally incomplete.
Naming an owner afterward does not repair a missing pathway trace.

### Repair path
- improve logging of approvals and overrides
- preserve decision checkpoints in system records
- define minimum reconstruction requirements for high-impact decisions

### Design lesson
Record design is part of responsibility design.

---

## Example 5: Human override exists in theory but is unusable in practice

### Situation
The deployment documentation says that humans can always override the AI.
In practice, the interface makes override difficult, costly, or socially discouraged.

### Pathway break
- interface layer conceals practical authority
- execution layer favors system continuation over human interruption
- human authority exists nominally but not operationally

### Failure reading
This is not a simple UX problem.
It is a responsibility accessibility failure.
The pathway claims reversibility but does not support real exercise of authority.

### Repair path
- redesign interface to make override visible and cheap enough to use
- define protected conditions for interruption
- ensure override use does not require heroic effort

### Design lesson
A pathway is unsound if authority exists only on paper.

---

## General Interpretation Pattern
When analyzing a case with RPD, ask in order:
1. What was the intended objective?
2. Where was decision authority supposed to be?
3. Where did delegation occur?
4. Who or what executed?
5. Did the interface clarify or hide authority?
6. Can the record reconstruct the pathway?
7. Who could stop, override, repair, or roll back?
8. After failure, where should responsibility be rebound?

## Practical Use
These examples can be used as:
- workshop material
- policy discussion prompts
- governance review aids
- deployment pre-mortem prompts
- incident post-mortem structure seeds

## Relationship to Other Docs
This document should be read together with:
- `docs/principles.md`
- `docs/layer-model.md`

The principles define the logic.
The layer model defines the analytical space.
These examples show how the framework begins to operate on real patterns.
