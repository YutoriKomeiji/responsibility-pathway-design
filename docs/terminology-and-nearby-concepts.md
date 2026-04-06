# Responsibility Pathway Design — Terminology and Nearby Concepts

## Purpose
This document clarifies how Responsibility Pathway Design (RPD) relates to nearby concepts that may sound similar but do not center the same design problem.

The goal is not to reject these concepts.
It is to prevent conceptual flattening.
RPD becomes less useful when it is reduced to a generic label for accountability, governance, or architecture.

## Core Distinction
RPD centers:
- responsibility flow
- breakpoints
- rebinding points
- stop points
- human return points
- repair paths
- rollback ownership
- transition into organizational responsibility

Many nearby concepts overlap partially.
Few center all of these at once.

## Nearby Concepts

### Responsibility Engineering
Close in motivation, but not identical.

Responsibility Engineering tends to emphasize:
- structuring responsibility
- assigning or clarifying responsibility
- engineering traceability and protocol

RPD goes further by treating responsibility as a pathway that:
- moves
- breaks
- returns
- is rebound
- must remain repairable

Practical distinction:
Responsibility Engineering asks how responsibility should be structured.
RPD asks how responsibility should flow.

### Responsibility Architecture
This can be a useful neighboring term when the focus is on static structure.
RPD is compatible with it, but places more emphasis on continuity under live operation.

Practical distinction:
Responsibility Architecture asks what the structure looks like.
RPD asks what happens when the structure is under pressure, delegation, interruption, and repair.

### End-to-End Accountability Design
This is one of the closest neighboring concepts.
It captures continuity better than many governance terms.
However, RPD is still more explicit about:
- rebinding after delegation
- stop points
- human return points
- repair ownership
- rollback authority

Practical distinction:
End-to-End Accountability Design stresses continuity.
RPD stresses continuity plus diagnosable breakpoints and repair authority.

### Sociotechnical Governance
This is broad and often useful.
It captures the fact that responsibility failures occur across humans, institutions, interfaces, and systems.
RPD fits inside that concern, but is more operationally specific.

Practical distinction:
Sociotechnical Governance asks how mixed human-technical systems should be governed.
RPD asks where responsibility breaks inside those systems and how it should be repaired.

### AI Governance
AI governance provides policies, roles, committees, controls, and review structures.
RPD depends on governance, but does not collapse into it.

Practical distinction:
Governance sets rules.
RPD asks whether responsibility still remains legible, interruptible, and repairable when those rules meet live operation.

### Human-in-the-loop
Human-in-the-loop is often treated as a safety answer by itself.
RPD treats it as insufficient unless the human role clearly owns:
- review authority
- interruption authority
- override authority
- rebound responsibility after delegation

Practical distinction:
Human-in-the-loop asks whether a human is present.
RPD asks whether that human actually carries meaningful return authority.

### Logging and Auditability
Logs and audits matter, but they are not the pathway itself.
RPD treats records as part of the pathway only when they allow reconstruction of how responsibility moved and where it broke.

Practical distinction:
Auditability asks whether something was recorded.
RPD asks whether the responsibility pathway can be reconstructed and acted upon.

## Summary Table

| Concept | Primary focus | What RPD adds |
|---|---|---|
| Responsibility Engineering | structure and traceability | flow, break, return, rebinding, repair |
| Responsibility Architecture | static accountability structure | live continuity under delegation and interruption |
| End-to-End Accountability Design | continuity of accountability | explicit breakpoints, return points, rollback ownership |
| Sociotechnical Governance | broad human-technical governance | operational pathway diagnosis and repair |
| AI Governance | rules, oversight, committees | responsibility continuity during live execution |
| Human-in-the-loop | human presence in loop | meaningful authority return and override ownership |
| Logging / Auditability | recordability | reconstructable responsibility pathway |

## Interpretation Rule
If a term can explain responsibility only after the fact, it is not enough for RPD.
If a term cannot explain where responsibility should return during live failure, it is not enough for RPD.
If a term cannot define who owns repair and rollback, it is not enough for RPD.

## Relationship to Other Documents
This document should be read together with:
- `docs/principles.md`
- `docs/layer-model.md`
- `docs/failure-and-repair-examples.md`
- `docs/positioning-above-harness-engineering.md`
