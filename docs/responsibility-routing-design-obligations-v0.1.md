# Responsibility Routing design obligations v0.1

Status: ACTIVE DESIGN GUIDANCE / public construction

Responsibility Pathway Design should ask where responsibility can validly move next, not only where a human return point exists.

## Route-first design questions

For every consequential handoff or exception path, identify:

- current responsibility holder;
- candidate next holder;
- Authority class required by the next decision;
- delegation scope available to the receiver;
- receiver eligibility, not merely receiver capability;
- unresolved payload, including uncertain external effects;
- evidence available to the receiver;
- allowed next actions;
- prohibited next actions;
- timing / expiry conditions;
- reevaluation or closure condition;
- residual owner if the route cannot complete.

## Required distinctions

- `fail closed` != Human Gate
- Evidence transfer != Authority transfer
- receiver capability != receiver eligibility
- route selection != Authority grant
- state recovery != approval/resume Authority recovery
- unresolved external effect != success or failure
- Human Return = one bounded Responsibility Route

## Valid route shapes

A safe design may route to:

- continue autonomously within unchanged delegation;
- AI resolution within explicit delegation;
- neutral hold;
- hold for reconciliation/readback;
- bounded Human Return;
- stop and preserve unresolved residue.

A human destination must not be selected merely because an evaluator failed or uncertainty exists. Human Return is appropriate when a real human- or institution-held decision/Authority is required and the destination is practically usable.

## Nominal Human Return anti-pattern

A named human reviewer does not make a route valid when the reviewer lacks one or more of:

- decision Authority;
- relevant evidence;
- sufficient time;
- operational access;
- ability to intervene;
- a bounded decision request;
- ownership of the residual consequence.

Designs should distinguish an actual return route from a ceremonial escalation label.

## Falsification / non-necessity

If an existing host workflow already preserves equivalent responsibility semantics across ambiguous effects, readback, repair/resume, routing, restart, and Authority boundaries, adding another RP-specific mechanism may be unnecessary. That is an acceptable design conclusion.

## Assurance-aware design

Design artifacts should also preserve lifecycle identity:

- published/released artifact;
- current source;
- historical evidence;
- migration material;
- authoring/control material.

These must not be collapsed into one apparent "current" state. Evidence gathered from a specific version or integration boundary should stay scoped to that boundary.

## Relationship to existing Human Return patterns

Existing Human or Institutional Return Point patterns remain valid as specialized patterns. They should be composed under the broader responsibility-route question rather than treated as the default answer for every stop, failure, uncertainty, or policy mismatch.
