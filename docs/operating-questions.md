# Responsibility Pathway Design — Operating Questions

## Purpose
This document turns RPD into a compact working checklist for design review, deployment review, incident review, and organizational discussion.

It is not a governance checklist in the usual sense.
It is a pathway review tool.
The point is not only to ask who is responsible, but whether responsibility can still move, return, stop, and repair under real operation.

## Core Review Questions

### 1. Intent
- What is this system actually trying to optimize?
- Who defined that objective?
- Is the intended objective still the real operating objective?

### 2. Decision
- Where is decision authority actually located?
- Is authority delegated anywhere?
- After delegation, where is accountability rebound?

### 3. Execution
- Who or what executes the action?
- Can execution continue without visible human ownership?
- What happens if the system behaves fluently but incorrectly?

### 4. Human Return
- At which point can a human role take authority back?
- Is that return point explicit, visible, and practical?
- Does the human role have real override power or only nominal approval power?

### 5. Interruption
- Who can stop the flow?
- Under what conditions must the flow be paused?
- Is interruption cheap enough to be used in practice?

### 6. Record
- Can the pathway be reconstructed afterward?
- Are approvals, overrides, and handoffs visible?
- Is there enough trace to show where responsibility moved?

### 7. Repair
- Who owns repair after failure?
- Who can rebind authority?
- Who owns rollback?
- Who records the repair and the new binding state?

### 8. Organizational Transition
- At what point does responsibility stop being a local operator issue and become an organizational responsibility?
- Is that transition explicit?
- Is there a named owner for that transition?

## Interpretation Rule
If a design cannot answer these questions clearly, the pathway is underdesigned.
If a deployment cannot answer them under pressure, the pathway is fragile.
If an incident review cannot answer them afterward, the pathway was not sufficiently legible.

## Practical Use Cases
This document can be used in:
- AI deployment review meetings
- governance workshops
- incident post-mortems
- pre-mortems for new AI workflows
- role-boundary redesign sessions
- executive review of AI operating risk

## Relationship to Other Documents
This document should be read together with:
- `docs/principles.md`
- `docs/layer-model.md`
- `docs/failure-and-repair-examples.md`
- `docs/positioning-above-harness-engineering.md`
- `docs/terminology-and-nearby-concepts.md`
