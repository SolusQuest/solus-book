# Source of truth

Keep current behavior, selected requirements, planning, and evidence distinct. A design can be accepted before implementation exists; a historical passing result applies to the revision and conditions that produced it.

| Surface | Owns |
| --- | --- |
| Current source and current-state documentation | Available behavior and artifacts in the inspected tree. |
| Engineering and architecture documents | Long-lived rules, selected boundaries, and requirements. |
| Issues or equivalent work records | Focused outcomes, unresolved decisions, acceptance, and dependencies. |
| Pull requests and their validation records | Proposed implementation and evidence for the actual reviewed revision. |
| Released artifacts and support policies | The compatibility and support commitments made to consumers. |
| Project boards and dashboards | Planning views derived from the owning records. |

## Durable decisions

Chats, prompts, agent memory, scratch files, and expiring logs can inform work. Record accepted decisions in the owning repository document, issue, or PR. Preserve the decision and useful rationale without pasting the conversation.

Update affected current specifications and implementation together. Historical acceptance remains true for its original inputs; it does not automatically govern the current implementation or prove a later change.

Solus Book owns the shared text. Consumers own its adoption, local requirements, and explicit exceptions. A source repository's product rules do not become shared rules merely because a document is linked or inspected.

## References and evidence

Use a current path for a living reference where the project allows it. For an immutable historical claim, identify the exact revision and conditions. When citing a Git commit, use its full SHA and verify it belongs to the history relevant to the claim. Project rules can require stronger pinning for particular transfers or execution contracts.

Identify uncommitted evidence as working-tree evidence. Do not assign it an invented commit, CI run, release, or remote review result. Tracker URLs remain mutable references even when they include a stable issue number.

A validation record explains what was observed and its limits. Current acceptance uses applicable evidence under [Validation](validation.md), with compatibility interpreted through [Contract lifecycle](contract-lifecycle.md).
