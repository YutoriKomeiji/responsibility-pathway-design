# Route-choice worked case: an uncertain external write

Status: **proposed design illustration**, not an RPE/RPR/RPOS conformance certificate.

A task agent attempts a consequential write to an external service. The call times out *after dispatch*. The agent has logs and can request readback, but it has no fresh authorization to repeat the write. A reviewer exists, yet has no access to the service and no evidence that a replay is safe.

## What not to do

- Do not classify the timeout as confirmed failure and blindly retry.
- Do not promote a tool receipt, log transfer, route selection or recovered checkpoint into execution Authority.
- Do not assign `HUMAN_RETURN` merely because a human name appears on the workflow. The reviewer is not currently an eligible receiver for effect verification.

## Route decision record (illustrative)

| Field | Bounded design requirement |
|---|---|
| Source holder | Current workflow, retaining responsibility for unresolved outcome |
| Unresolved payload | Write identity, idempotency key if present, dispatch time, uncertain outcome, evidence references |
| Candidate route | **HOLD_FOR_RECONCILIATION** pending independent readback |
| Candidate receiver | Reconciliation process with valid access and declared delegation; otherwise neutral hold |
| Eligibility check | Can perform authorized readback, understands target identity, has access to required evidence, and is within valid delegation and timing |
| Allowed next action | Authorized read-only query for independent effect observation |
| Forbidden next action | Re-dispatch of the write without outcome reconciliation and fresh authorization |
| Reevaluate | On independent readback, expiry or owner intervention |
| Residual owner | Existing accountable workflow/institutional owner until a valid transfer is established |
| Authority effect | **None** from route selection or evidence movement |

### Alternative outcomes

1. **Verified write occurred:** record effect evidence, reconcile; do not dispatch again.
2. **Verified write did not occur:** a new dispatch still requires the applicable execution authorization and policy checks.
3. **Still unknown:** retain reconciliation hold or neutral hold; do not collapse the state to success or failure.
4. **Human-held decision genuinely required:** select a **bounded Human Return** only if the reviewer has appropriate Authority, evidence, access and intervention capacity.
5. **No eligible route:** stop or preserve residue with an identified owner; do not invent a receiver.

## Cross-layer verification obligations

- **RPM:** route selection is a responsibility-bearing transition, not an Authority source.
- **RPD:** the design record distinguishes a real eligible receiver from nominal human escalation.
- **RPE:** non-allow outcomes must be machine-readable without assuming every stop is a Human Gate.
- **RPR:** unresolved effect remains unretried until readback/reconciliation/authorization obligations are satisfied.
- **RPOS:** durable state, restart and recovery must not create approval or resume Authority.
- **Lean / tests:** these invariants are proof/test *candidates*; this design example does not claim they are fully encoded or verified.

See [Responsibility Routing design obligations](responsibility-routing-design-obligations-v0.1.md) for the broader contract. This scenario is intentionally vendor-neutral and has **no live external effect**.
