# Task routing

Begin with the actual user request and the repository's current context. Read the [collaboration](../standards/collaboration.md), [source-of-truth](../standards/source-of-truth.md), and [content conventions](../standards/conventions.md) relevant to the task. Once loaded, reuse them unless the source or task changes.

Choose the smallest useful reading set below. Routine implementation does not automatically require design refinement, issue creation, or an extra review workflow.

| Task | Shared rules | Procedure or output |
| --- | --- | --- |
| Resolve a material design choice | [Pre-release engineering](../standards/pre-release-engineering.md); [Contract lifecycle](../standards/contract-lifecycle.md) when compatibility is affected. | [Design refinement](../skills/design-refinement/SKILL.md); [Design note](../templates/design-note.md). |
| Refine scope or an implementation issue | [Issue workflow](../standards/issue-workflow.md); [Pre-release engineering](../standards/pre-release-engineering.md). | [Issue refinement](../skills/issue-refinement/SKILL.md); [Issue template](../templates/issue.md). |
| Create or update a remote issue | [Issue workflow](../standards/issue-workflow.md). | [Issue publishing](../skills/issue-publishing/SKILL.md). |
| Implement a bounded change | [Pre-release engineering](../standards/pre-release-engineering.md); affected project rules and contracts. | The current task or issue defines acceptance; use relevant project implementation procedures. |
| Select or perform validation | [Validation](../standards/validation.md). | [Test validation](../skills/test-validation/SKILL.md). |
| Prepare or publish a PR | [PR workflow](../standards/pr-workflow.md); [Validation](../standards/validation.md). | [PR publishing](../skills/pr-publishing/SKILL.md); [PR template](../templates/pull-request.md). |
| Maintain shared guidance | [Context model](context-model.md); [Maintenance](../docs/maintenance.md). | [Source map](../docs/source-map.md) and the affected canonical content. |
| Adopt the handbook in a consumer | [Downstream adoption](../docs/downstream-adoption.md). | A separately scoped task in the consuming repository. |

Load project architecture, commands, release policy, or harness instructions only when the task needs them. A missing material input requires a targeted lookup or clarification; independent authorized preparation can continue. Keep unknown requirements visible rather than inventing a universal command or approval gate.
