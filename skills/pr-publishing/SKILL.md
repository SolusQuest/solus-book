---
name: pr-publishing
description: Prepare or publish a reviewable pull request for a coherent change, preserving task identity and publication scope and reporting actual validation, feedback, and remote state.
---

# Pull request publishing

Follow [PR workflow](../../standards/pr-workflow.md), [Collaboration](../../standards/collaboration.md), and the consuming repository's required checks and title convention.

## Prepare

Inspect the actual repository, issue or task, branch or worktree, base, working changes, and diff. Preserve specified identities and unrelated edits. Confirm the change fits the accepted outcome; use a brief no-issue explanation when appropriate.

Select validation from the affected behavior under [Validation](../../standards/validation.md). Record actual results and limitations. Prepare a self-contained title and body describing the concrete problem and final behavior. The [PR template](../../templates/pull-request.md) is optional when the project has its own template.

Inspect the intended diff and staging for unrelated files, credentials, generated output, and unsupported claims. Check other restricted material against the target repository's audience and policy under [Conventions](../../standards/conventions.md#information-and-destination); private project context can remain in a private PR. Respect a task instruction to leave work uncommitted or local. Reuse authority already given for necessary steps in a requested publication workflow; obtain only missing authority after the concrete preparation is ready.

## Publish

Use the requested branch and remote target. Publish as a draft by default unless the task or project selects ready-for-review status. Use a structured body or body file to preserve literal content.

Preserve an existing PR identity. Read back an uncertain publication before retrying. Verify repository, base, actual head, title, body, and state after the requested writes. Add a task attachment when the current environment provides and requires it.

## Report readiness

Inspect current required checks and review feedback for the actual head before claiming remote readiness. Distinguish local validation, CI, completed independent review, and outstanding findings. Pending work, acknowledgements, timeouts, or old-head results do not prove completion.

After a correction, verify affected findings and refresh invalidated evidence. Preserve finding history and reuse applicable unchanged results. Do not introduce extra review cycles without a concrete need.

Return the PR identity, resulting behavior, actual evidence, current state, and remaining decisions. Merge, release, deployment, closure, and settings changes need their own task authority; publication alone does not grant it.
