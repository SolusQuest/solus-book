---
name: design-refinement
description: Resolve material design choices and produce a bounded decision proposal before implementation depends on unresolved product, contract, ownership, or authority decisions.
---

# Design refinement

Use the current task and relevant project design documents. Consult [Pre-release engineering](../../standards/pre-release-engineering.md) and [Contract lifecycle](../../standards/contract-lifecycle.md) for durable or supported boundaries.

## Procedure

1. Identify the concrete unresolved decision, affected consumer, accepted constraints, and actual implementation state. Preserve already accepted naming and boundaries.
2. Present the recommended option and meaningful alternatives. Explain the evidence, tradeoffs, and practical consequence if the choice is wrong. Include ownership, state, compatibility, security, or side-effect consequences when affected.
3. For a durable external boundary, inspect bounded relevant precedent. For uncertain executable behavior, use an authorized small experiment that can discriminate the choices; state what it cannot prove.
4. Keep the scope at the boundary needed now. Split independently useful outcomes and retain jointly enforced invariants. Defer speculative extension and compatibility mechanisms without a real requirement.
5. Determine which choices are already authorized, ordinary implementation decisions, or material owner decisions still needed. Complete a reviewable proposal before requesting a missing decision. Continue independent authorized work while it is pending.
6. Record accepted conclusions in the owning document or work record when that write is authorized. A discussion or proposal request alone leaves the result as a draft.

## Result

Return the decision, recommendation, rationale, affected boundaries, acceptance and validation, unresolved choices, and intended decision owner. The [Design note](../../templates/design-note.md) is an optional structure; scale it to the choice.

Do not present unsettled material decisions as implementation-ready. Refinement does not itself authorize tracker publication, product scope expansion, or writes in another repository. Ordinary choices within an authorized implementation task do not acquire a new approval step.
