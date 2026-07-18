# RPD Verification and Validation Vocabulary v0.1

## Status

This document defines the repository-wide vocabulary for bounded verification and validation claims in Responsibility Pathway Design (RPD).

It is a research vocabulary, not a certification scale. A label in this document does not establish safety, legality, fairness, compliance, effectiveness, production readiness, or social acceptance.

## Purpose

RPD artifacts have used nearby expressions such as `operational validation`, `operational verification`, `exercise evidence`, and `broader validation`. Without an explicit contract, those terms can blur five different questions:

1. whether a design is structurally coherent;
2. whether it was implemented as specified;
3. whether people and institutions can exercise it in controlled conditions;
4. whether it operated as claimed in live conditions;
5. whether it contributes to acceptable real-world outcomes in its wider context.

The canonical sequence is:

```text
D — design verification
I — implementation verification
X — exercise verification
O — operational verification
V — broader contextual validation
```

The sequence is cumulative only in evidential demand, not in authority. Passing a later stage does not erase limitations, dissent, residual impact, or the need for human or institutional authorization.

## 1. Canonical levels

### D — Design verification

**Question:** Does the design artifact contain the required relationships, constraints, ownership, evidence, fallback, and traceability?

Typical evidence:

- requirements and design records;
- pathway and authority models;
- normative-source traces;
- pattern selections and trade-off records;
- verification obligations and reopening conditions.

Permitted conclusion:

> The stated design criteria are met or not met within the reviewed artifact and scope.

D does not establish implementation, exercisability, operational performance, or contextual acceptability.

### I — Implementation verification

**Question:** Was the approved design implemented as specified for the declared version and scope?

Typical evidence:

- code, configuration, access controls, workflow states, and interfaces;
- deployment and change records;
- evidence-production mechanisms;
- inspection and conformance-test results.

Permitted conclusion:

> The referenced implementation conforms or does not conform to the stated design requirements within the inspected scope.

I does not establish that authorized actors can use the mechanism under pressure or that it works in live operation.

### X — Exercise verification

**Question:** Can the designed response be exercised in controlled, simulated, rehearsed, or failure-injected conditions?

Typical evidence:

- tabletop exercises;
- simulations and controlled rehearsals;
- failure injection;
- timed escalation, fallback, contestation, and recovery tests;
- actor-unavailability and evidence-loss scenarios.

Permitted conclusion:

> The pathway was or was not exercised successfully under the stated scenarios, participants, assumptions, and time limits.

X does not establish routine live performance, affected-party accessibility outside the exercise, or broader social legitimacy.

### O — Operational verification

**Question:** Did the pathway operate as claimed in real conditions over a declared period, population, version, and scope?

Typical evidence:

- live monitoring and incident records;
- actual overrides, appeals, suspensions, recovery, and reopening;
- timing and availability observations;
- operational deviations and exceptions;
- evidence of real authority exercise.

Permitted conclusion:

> Operational evidence supports or does not support the stated claim for the observed period and scope.

O does not establish that the pathway is acceptable, fair, lawful, effective in all contexts, or free of unobserved harm.

### V — Broader contextual validation

**Question:** Does the design contribute to the intended responsibility outcomes in its social, institutional, legal, organizational, and affected-party context?

Typical evidence:

- relevant operational evidence;
- independent review or replication;
- affected-party research, testimony, complaint, or appeal evidence;
- comparative evaluation against credible baselines;
- longitudinal evidence about burden, residual impact, recovery, and institutional change.

Permitted conclusion:

> The stated validation question is supported, unsupported, mixed, or unresolved within the declared methods and context.

V remains bounded. It is not a universal or permanent verdict and does not self-authorize continued operation.

## 2. Evidence-class relationship

The evaluation protocol uses evidence classes E0–E5. The usual minimum relationship is:

| Level | Usual minimum evidence | Core object |
|---|---|---|
| D | E1 | design artifact |
| I | relevant E2 | implementation |
| X | E3 | controlled exercise |
| O | relevant E4 | live operation |
| V | relevant E4 and E5 | contextual outcome question |

These are minimum relationships, not automatic pass rules. Relevance, integrity, independence, scope, and counterevidence still require review.

## 3. Proposition relationship

The assurance interface uses five proposition types. They map as follows:

| Proposition type | Canonical level |
|---|---|
| Design proposition | D |
| Implementation proposition | I |
| Exercise proposition | X |
| Operational proposition | O |
| Broader validation proposition | V |

An assurance level such as A2 or A3 describes the maturity of evidence assembled for a specific claim. It must not replace the D/I/X/O/V proposition label.

## 4. Legacy and compatibility terms

The following compatibility rules apply to existing repository text:

| Existing expression | Canonical interpretation |
|---|---|
| `operational validation` when describing a rehearsal, simulation, exercisability, or realistic controlled condition | X — exercise verification |
| `operational validation` when describing observed live operation | O — operational verification |
| `real-world validation` | V — broader contextual validation, unless the text clearly means only observed operation |
| `structural verification` | D or I; the artifact under review must be named |
| `effectiveness` without a declared outcome, method, and context | not an admissible bounded conclusion |

The phrase `operational validation` is deprecated for new artifacts because it can refer to either X or O. Existing text must be interpreted by its evidence object, not by the word alone.

## 5. Claim-writing rules

Every verification or validation statement should identify:

- the canonical level;
- the exact claim or criterion;
- the object and version;
- pathway, transition, actor, population, and time scope;
- evidence identifiers and classes;
- methods and scenarios;
- assumptions and exclusions;
- failures, deviations, counterevidence, and dissent;
- result status;
- expiry, monitoring, and reopening conditions;
- claim owner and decision authority.

A claim must not move upward in the sequence merely because more documents exist. The evidence object must change.

## 6. Forbidden inferences

The following inferences are invalid without additional evidence and authority:

- D → implemented;
- I → exercisable;
- X → reliable in routine operation;
- O → broadly acceptable or effective;
- V in one context → valid in another context;
- any level → legally compliant, safe, fair, certified, or authorized for deployment;
- absence of observed failure → absence of latent or unreported failure;
- successful technical rollback → completed responsibility recovery.

## 7. Failure and mixed-result language

Use bounded statuses such as:

- not evaluated;
- insufficient evidence;
- criterion met / not met;
- verified / not verified for the declared scope;
- exercised successfully / unsuccessfully under stated conditions;
- operational evidence supports / does not support the claim;
- mixed or conflicting evidence;
- validation question remains open;
- claim expired or reopened.

Avoid unqualified labels such as `validated system`, `responsible system`, `safe`, `compliant`, `effective`, or `production ready`.

## 8. Responsibility and decision boundary

Evaluators classify evidence and assess bounded claims. Assurance reviewers assemble and challenge arguments. Operational governance decides whether to continue, constrain, suspend, redesign, retire, or reopen operation.

No D/I/X/O/V result self-authorizes a state change. Human or institutional authority remains explicit.

## 9. Migration rule

New or materially revised RPD artifacts should use D/I/X/O/V terminology directly.

When an existing artifact uses a compatibility term:

1. identify the evidence object;
2. map the statement to D, I, X, O, or V;
3. preserve the original scope and uncertainty;
4. do not strengthen the claim during renaming;
5. record ambiguity as an open issue when the evidence object cannot be determined.

Historical wording may remain where changing it would obscure provenance, but active templates and current guidance should use the canonical vocabulary.

## 10. Research boundary

The five-level vocabulary is provisional. Its clarity, inter-rater reliability, sector fit, evidence thresholds, and relationship to established verification, validation, assurance, evaluation, and governance practices require external comparison and empirical testing.