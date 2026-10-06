---
name: issue-refinement
description: Turn a task or existing issue into a focused execution or decision draft with bounded scope, acceptance, validation, and dependencies, before tracker publication.
---

# Issue refinement

Read the task or existing issue, relevant project rules, [Issue workflow](../../standards/issue-workflow.md), and [Pre-release engineering](../../standards/pre-release-engineering.md).

## Procedure

1. Decide whether separate tracking adds coordination, scheduling, dependency, or acceptance value. A bounded complete change may use the no-issue path.
2. Identify one primary outcome and an outcome-focused title. Select a proposed native type from the project's convention where applicable; verify available types at publication.
3. State scope and exclusions, observable acceptance, applicable validation, real dependencies, useful code and document references, and the expected review boundary.
4. Resolve material design choices before dependent implementation, or frame a bounded decision or experiment with its resolving evidence. Ordinary implementation choices can remain with the implementer.
5. Keep implementation with its acceptance-critical contracts, tests, and docs. Split independently useful and verifiable outcomes, not file names or coding order.
6. For an existing issue, preserve its identity and distinguish proposed text from proposed relationship or metadata changes. Keep historical acceptance and local project requirements intact.
7. Return the refined draft and remaining material decisions. Record it locally or in owning docs only within the task's scope.

Use the [Issue template](../../templates/issue.md) as needed. Do not add planning parents, milestones, readiness labels, or extra reviews merely to fill a template.

## Result and publication boundary

An implementation draft is ready when scope, dependencies, acceptance, and validation are clear and no required owner decision remains unresolved. An experimental draft instead states the question and evidence needed.

Drafting does not authorize remote creation, metadata changes, or closure. If publication is already authorized, continue through the [Issue publishing procedure](../issue-publishing/SKILL.md) using the same target and existing authority.
