# Pull request workflow

Prepare one coherent change for review, preserving the requested issue, branch or worktree, base, and publication scope. Respect instructions to keep work local or uncommitted. An authorized initialization does not require creating a remote review process first.

## Reviewable result

Use the project's title convention and a self-contained body explaining the concrete problem and resulting behavior, tracking reference when useful, actual validation, and material limitations. Describe the final implementation for a reviewer who has not seen the conversation.

Keep acceptance-critical code, contracts, tests, and documentation together. Update affected consumers and state any actual compatibility consequence. Inspect the diff and staged content for unrelated files, generated output, credentials, information outside the repository's permitted access, and unsupported claims. Private project material can remain in a private PR under [Conventions](conventions.md#information-and-destination).

The [PR template](../templates/pull-request.md) is a starting point. Project templates and required fields take precedence when the task uses them.

## No-issue path

A separate issue is unnecessary when the outcome is bounded and complete in one review cycle, needs no independent scheduling or coordination, and leaves no unresolved product decision, external commitment, authority change, dependency-graph change, or multi-PR delivery boundary.

If scope grows beyond those conditions, refine the added work before claiming readiness. A no-issue explanation should be brief.

## Publication and readiness

Publish as a draft by default unless the task or project workflow selects ready-for-review status. Respect authorization already given for the whole requested workflow under [Collaboration](collaboration.md).

Verify the actual remote target, base, head, text, and state after publication. Before claiming readiness, inspect current required checks and review feedback for that head. Local checks, CI, independent review, and release acceptance are different kinds of evidence.

A queued review, acknowledgement, timeout, cancellation, old-head result, or green check by itself does not establish completed review and readiness. Report the actual state and any outstanding requirement. Required reviewers and checks remain project-owned; ordinary changes do not acquire an extra review gate from this handbook.

Preserve finding history. Correct the admitted failure and affected neighboring cases, then refresh the evidence invalidated by the change. Reuse evidence that remains applicable. Follow [Validation](validation.md).

Merge, closure, release, deployment, and settings changes follow the task's authority; PR publication alone does not authorize them. Use the [PR publishing skill](../skills/pr-publishing/SKILL.md) for the operational procedure.
