# Responsibility Pathway Design — Layer Model

## Purpose
This document introduces a layered model for analyzing where responsibility is carried, broken, obscured, or repaired.

RPD is not limited to a single handoff between actor A and actor B.
In AI-involved environments, responsibility often travels across multiple layers simultaneously.
A pathway may appear intact at one layer while already broken at another.

## Why a Layer Model is Needed
Modern systems combine:
- policy
- organization
- software
- workflow
- model outputs
- interfaces
- records

A failure may be visible only at the surface while its cause lives in another layer.
RPD therefore treats responsibility as a multi-layer pathway.

## Proposed Layer Model

### Layer 1: Intent Layer
What was the system or organization trying to achieve?

Key questions:
- What was the intended objective?
- Who defined it?
- Was the objective explicit or only assumed?

Typical break:
- execution follows a pattern that no longer matches the real objective

### Layer 2: Decision Layer
Where was authority to decide actually located?

Key questions:
- Who had decision authority?
- Was authority delegated?
- Was delegation explicit?
- Was accountability rebound after delegation?

Typical break:
- decision moved, responsibility did not

### Layer 3: Execution Layer
Who or what performed the action?

Key questions:
- Which human role, team, or AI system executed?
- Was execution supervised?
- Could execution be interrupted?

Typical break:
- execution continued under weak or unclear ownership

### Layer 4: Interface Layer
How was action surfaced to the human operator?

Key questions:
- Was the human aware of what the system was doing?
- Did the interface make authority clear or hide it?
- Were override paths visible?

Typical break:
- fluent interface behavior masks authority drift or automation creep

### Layer 5: Model / System Behavior Layer
How did the underlying AI or software behave?

Key questions:
- What role did model output play?
- Was the behavior bounded?
- Were limitations understood?
- Did the system amplify ambiguity?

Typical break:
- model behavior becomes functionally authoritative without explicit ownership

### Layer 6: Record Layer
What trace was left behind?

Key questions:
- What was logged?
- Can the pathway be reconstructed?
- Are approvals, overrides, and rollback actions visible?

Typical break:
- failure cannot be reconstructed because record design was too weak

### Layer 7: Repair Layer
How can the pathway be stopped, repaired, rebound, or rolled back?

Key questions:
- Who can stop the flow?
- Who can rebind responsibility?
- What is the rollback path?
- Who records the repair?

Typical break:
- nominal accountability exists, but no repair path exists in practice

## Interpretation Rule
A responsibility pathway should not be evaluated only by its visible surface behavior.
It should be checked layer by layer.

A system is not well-designed merely because:
- it appears efficient
- the AI output looks reasonable
- one owner can be named afterward

A pathway is sound only when responsibility remains legible and repairable across layers.

## Example Diagnosis Pattern
A common modern failure might look like this:
- Intent layer: deliver faster decisions
- Decision layer: authority partially delegated to AI-assisted workflow
- Execution layer: staff rely on recommendation without active rebinding
- Interface layer: system presents recommendation as seamless next step
- Model layer: AI output becomes de facto authority
- Record layer: no clear trace of human confirmation
- Repair layer: no one clearly owns rollback

In such a case, the failure is not only "human error" or "AI error."
It is a pathway design failure across layers.

## Practical Use
This layer model can be used to:
- diagnose incidents
- design governance flows
- review AI deployment plans
- evaluate role boundaries
- define override and rollback structures
- improve organizational accountability design

## Relationship to Principles
This document should be read together with:
- `docs/principles.md`

The principles define the core logic of RPD.
The layer model defines where that logic should be inspected and applied.
