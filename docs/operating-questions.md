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

### 4. Responsibility Routing
- When the current actor or process should no longer continue, where can responsibility legitimately move next?
- Is the next receiver eligible for this specific unresolved payload, decision scope, and time window?
- What Authority does the receiver actually hold, and what Authority is explicitly not transferred with evidence, context, or technical capability?
- Is the route a bounded Human Return, an organizational/institutional return, an authorized process, an AI resolution within explicit delegation, or a reconciliation/neutral hold?
- If a human role is selected, does that role have usable authority, information, time, and intervention capacity rather than nominal presence only?
- Can the pathway remain safely held when no eligible receiver is currently available, instead of inventing a Human Return or continuing autonomously?

### 5. Interruption
- Who can stop the flow?
- Under what conditions must the flow be paused?
- Is interruption cheap enough to be used in practice?

### 6. Record
- Can the pathway be reconstructed afterward?
- Are approvals, overrides, route selections, and handoffs visible?
- Is there enough trace to show where responsibility moved?
- Does the record distinguish observed evidence from Authority, authorization, and receiver eligibility?

### 7. Repair
- Who owns repair after failure?
- Who can rebind authority?
- Who owns rollback?
- Who records the repair and the new binding state?
- After repair, is resume Authority established separately rather than inferred from recovery success?

### 8. Organizational Transition
- At what point does responsibility stop being a local operator issue and become an organizational responsibility?
- Is that transition explicit?
- Is there a named owner for that transition?
- Does crossing the organizational boundary preserve unresolved obligations, evidence provenance, receiver eligibility, and residual ownership?

## Interpretation Rule
If a design cannot answer these questions clearly, the pathway is underdesigned.
If a deployment cannot answer them under pressure, the pathway is fragile.
If an incident review cannot answer them afterward, the pathway was not sufficiently legible.

A generic fail-closed state is not automatically a Human Gate. Human Return is one bounded Responsibility Route. Evidence transfer, technical capability, successful recovery, or route selection must not silently create Authority.

If an existing host system already preserves the same responsibility contract across uncertainty, routing, readback, repair/resume, and restart boundaries, adding another RPD/RP* mechanism may provide little or no additional value. That is a valid design result, not a failure of the review.

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
- `docs/responsibility-routing-design-obligations-v0.1.md`
