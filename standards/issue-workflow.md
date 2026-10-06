# Issue workflow

An issue is a focused execution or decision contract. Create one when it adds useful planning, scheduling, coordination, dependency, or acceptance information. A bounded change can use the [no-issue path](pr-workflow.md#no-issue-path).

## Content and readiness

State one primary outcome, useful context, scope and exclusions, observable acceptance, applicable validation, actual dependencies, and relevant owning documents or code. Identify an expected review boundary when it helps execution. A parent or milestone should add useful coordination information.

Split independently useful and acceptable outcomes. Keep shared invariants and acceptance-critical tests and documentation together under [Pre-release engineering](pre-release-engineering.md).

An implementation issue is ready when material product and architecture decisions are settled, scope and dependencies are clear, and acceptance can be checked. Ordinary internal implementation choices can remain with the implementer. An experiment instead states the question and the evidence needed to resolve it.

Use the [Issue template](../templates/issue.md) selectively. Drafting or refining an issue does not itself publish it or change tracker metadata.

## Tracker conventions

Use the repository's enabled native type for the primary outcome where its tracker supports types and the project requires them. Verify available types for creation or retyping. Preserve an existing type for a body-only update. Do not duplicate a native type with a title prefix or parallel body field.

The project owns language, enabled types, labels, readiness markers, assignees, milestones, board fields, and repository destinations. Do not invent missing categories or change tracker settings merely to complete a text edit.

## Publication and changes

Read the target and fields relevant to the intended writes before mutation. Preserve the identity of an existing issue and unrelated metadata. Use a structured body or body file to preserve actual newlines and literal text.

Read back the changed fields after publication. A bulk relationship or milestone migration also verifies the complete changed graph. Reconcile an uncertain result before retrying; preserve observed identifiers and avoid duplicate creations.

Long-lived planning decisions belong in their owning docs. A board view is not the sole execution contract. Follow [Collaboration](collaboration.md) for authority and the [Issue publishing skill](../skills/issue-publishing/SKILL.md) for execution.
