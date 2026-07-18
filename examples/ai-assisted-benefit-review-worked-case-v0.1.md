# RPD Worked Case v0.1: AI-Assisted Benefit Review

## Status

This is a synthetic research case for method testing. It does not describe a real authority, claimant, legal regime, deployed system, or validated outcome.

- Case ID: `RPD-WC-BENEFIT-001`
- Case version: `0.1`
- Study ID: not assigned (worked example only)

## Case question

How should responsibility remain connected when an AI-assisted workflow recommends that a public-benefit claim be delayed or rejected, while relevant evidence may be incomplete and the affected person may face immediate hardship?

## Study purpose

The case compares three design alternatives against the same pathway diagnosis. It demonstrates how RPM findings can be translated into RPD requirements, composed patterns, observable propositions, and an RPE handoff without treating the worked example as proof of effectiveness.

## Synthetic setting

A caseworker reviews applications with assistance from a model that predicts inconsistency and missing documentation. A flagged application may enter enhanced review. The organization has a general appeal channel, but the appeal may occur after the payment window has expired.

Actors:

- applicant;
- frontline caseworker;
- reviewing supervisor;
- model and workflow service team;
- payment operations;
- appeal unit;
- institutional policy owner;
- external support representative where available.

## Initial pathway

```text
application
  → automated flag
  → caseworker review
  → delay or rejection recommendation
  → supervisor confirmation for selected cases
  → notice
  → appeal
  → correction or continued rejection
  → payment, restoration, compensation, or unresolved residual impact
```

## RPM-style findings

| Case finding ID | Candidate kernel class | Finding | Pathway consequence |
|---|---|---|---|
| BF-01 | F1 authority-capability mismatch | The person detecting immediate hardship cannot authorize temporary payment | authority and capability are separated |
| BF-02 | F5 contestation failure | The normal appeal can complete after the critical payment window | remedy may arrive after option expiry |
| BF-03 | F2 evidence discontinuity | Model rationale, caseworker notes, and policy assumptions are stored separately | evidence continuity is weak |
| BF-04 | F4 return-point failure; F5 contestation failure | The notice names an appeal route but not an accessible human return point | nominal contestability may not be exercisable |
| BF-05 | F6 recovery ownership failure | Reversal of the decision does not assign ownership for consequential losses | rollback is treated as recovery |
| BF-06 | F7 assumption expiry failure | Temporary enhanced-review rules have no expiry review | temporary delegation may become permanent |

Case finding IDs are local to this example. Candidate kernel classes remain reviewable mappings and may be revised without changing the observed finding.

## Design objectives

1. Preserve a usable intervention before severe hardship becomes irreversible.
2. Align stop, suspend, and provisional-support authority with actors who can detect urgent conditions.
3. Maintain a reconstructable evidence chain across model, human, policy, and workflow transitions.
4. Provide an accessible and time-bounded contestation path.
5. Assign recovery and residual-stewardship ownership beyond decision reversal.
6. Expire or reauthorize temporary review rules.

## Testable requirements

| ID | Requirement |
|---|---|
| R1 | A named actor shall be able to suspend adverse execution before the payment deadline when declared hardship criteria are met. |
| R2 | The workflow shall expose a human return point reachable through the decision notice and assisted channels. |
| R3 | Model output, material inputs, human reasoning, policy version, overrides, and timestamps shall be linked in one review trace. |
| R4 | An urgent challenge shall receive an initial human decision within a declared maximum time. |
| R5 | A corrected decision shall trigger a separate recovery assessment covering restoration, consequential loss, and residual impact. |
| R6 | Enhanced-review rules shall expire unless explicitly reviewed and reauthorized. |
| R7 | Actor absence and unavailable-system scenarios shall be exercised before operational claims are made. |

## Alternative A — Documentation-centered control

Components:

- detailed model and caseworker logging;
- standard supervisor sampling;
- ordinary appeal route;
- periodic policy review.

Strengths:

- lower implementation burden;
- improved reconstructability relative to the initial state.

Limitations:

- no guaranteed intervention before option expiry;
- appeal remains temporally weak;
- no provisional support;
- no explicit recovery owner;
- risks the anti-patterns Logging Without Remedy and Responsibility by Documentation.

## Alternative B — Urgent human return and scoped suspension

Pattern composition:

- Human / Institutional Return Point;
- Scoped Approval;
- Contestation Hold;
- Assumption Expiry;
- Cross-Organization Handoff Contract.

Components:

- named urgent-review officer;
- authority to suspend delay or rejection for defined hardship cases;
- linked evidence packet;
- maximum response time;
- rule expiry and reauthorization;
- handoff contract between review and payment operations.

Strengths:

- improves timely contestability and intervention;
- preserves a human decision point;
- limits authority by scope and duration.

Limitations:

- continued operation depends on staffing and reachable authority;
- suspension alone does not complete recovery;
- may shift workload to a scarce review team.

## Alternative C — Urgent return, provisional support, and recovery ownership

Pattern composition:

- all Alternative B patterns;
- Progressive Commitment;
- Evidence-Preserving Rollback;
- Recovery Ownership;
- Residual Stewardship;
- Time-Bounded Delegation.

Additional components:

- provisional support under bounded eligibility and recovery rules;
- staged commitment before final adverse execution;
- named recovery coordinator;
- residual-impact register;
- post-correction review of consequential losses;
- monitoring of unresolved hardship and challenge accessibility.

Strengths:

- addresses timing, recovery, and residue rather than decision correction alone;
- creates observable operational obligations.

Limitations:

- highest administrative and financial burden;
- provisional support may create overpayment and recovery concerns;
- requires careful proportionality, legal, policy, and affected-party review outside RPD.

## Comparative assessment

Scores are illustrative prompts, not validated measurements. Use `0 = absent`, `1 = weak`, `2 = partial`, `3 = strong within declared design scope`.

| Dimension | A | B | C | Evidence needed before any stronger claim |
|---|---:|---:|---:|---|
| authority–capability alignment | 1 | 3 | 3 | role and authority test |
| intervention before option expiry | 0 | 2 | 3 | timed exercises and field observation |
| evidence continuity | 2 | 3 | 3 | trace completeness audit |
| accessible contestability | 1 | 3 | 3 | accessibility testing with representative users |
| recovery capacity | 0 | 1 | 3 | completed recovery cases and burden review |
| residual stewardship | 0 | 1 | 3 | ownership and closure records |
| implementation burden | 3 | 2 | 1 | staffing, cost, and workflow study |
| risk of documentation theatre | high | medium | medium | exercise and operational counterevidence |

## Provisional selection

Alternative C is selected for research testing because it most completely addresses the diagnosed pathway discontinuities. This is not a claim that it is legally authorized, economically optimal, socially accepted, or superior in real operation.

Alternative B remains a credible comparator. Alternative A remains a baseline rather than a straw alternative because many real governance programs emphasize logging, review, and appeal without redesigning intervention timing or recovery ownership.

## Exercise scenarios

1. urgent hardship detected during normal staffing;
2. urgent-review officer unavailable;
3. model service unavailable but adverse workflow continues;
4. notice inaccessible to the applicant;
5. evidence packet missing the applicable policy version;
6. challenge submitted minutes before option expiry;
7. provisional support later found excessive;
8. decision reversed but consequential loss disputed;
9. payment and review organizations disagree on authority;
10. temporary rule reaches expiry without completed review;
11. repeated overrides indicate a design defect;
12. affected-party representative challenges the hardship criteria themselves.

## Observable propositions

- P1: Compared with Alternative A, Alternatives B and C reduce the proportion of exercised scenarios in which intervention authority is unavailable before option expiry.
- P2: Alternative C increases documented recovery ownership compared with A and B.
- P3: Alternative C may increase administrative burden and delay in low-stakes cases.
- P4: Linked evidence improves reconstruction completeness but does not by itself improve remedy.
- P5: A human return point that is unreachable, inaccessible, or under-resourced will not improve practical contestability.

## Defeaters and revision triggers

The selected design should be restricted, revised, or rejected if evidence shows that:

- provisional support creates greater unmanaged harm than the timing problem it addresses;
- the urgent route is systematically inaccessible;
- authority exists on paper but cannot be exercised;
- recovery ownership produces no completed recovery;
- burden is transferred disproportionately to applicants or frontline workers;
- an alternative design performs as well with substantially less burden;
- pathway improvements disappear outside the exercise setting.

## RPE handoff

RPE specifications should define:

- exact authority boundaries and fallback actors;
- workflow states and suspension semantics;
- evidence schema and version linkage;
- response-time measurement;
- accessibility and assisted-channel requirements;
- provisional-support execution and correction;
- recovery and residual-impact records;
- monitoring signals, thresholds, and reopening actions;
- change control and rule-expiry implementation.

## Human gate

Any real field use would require explicit institutional, legal, policy, operational, affected-party, and human authorization. This synthetic case authorizes none of those actions.
