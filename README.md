# Solus Book

Solus Book is the shared engineering handbook for SolusQuest repositories. It maintains reusable engineering standards, harness-neutral procedures and skills, context guidance, and templates.

## Scope

The handbook organizes guidance into three layers, described in [Context model](agents/context-model.md):

1. Engineering standards used by humans and agents.
2. Harness-neutral agent instructions and task procedures.
3. Harness-specific entrypoints and discovery guidance where needed.

Shared guidance is maintained here. Product architecture, project context, build and test commands, and repository-specific requirements remain owned by each project.

Personal workflows, including hybrid coordinator policies, model routing, and Relay orchestration, belong in a separate personal workflow library.

## Downstream adoption

Downstream integration, links, deduplication, and migration are handled in each consuming repository after the shared handbook is established. See [Downstream adoption boundaries](docs/downstream-adoption.md) for responsibilities and follow-up work.

## Reading the handbook

Start with the current task and the project's own context. [Task routing](agents/task-routing.md) selects the relevant standards and procedures. Agents maintaining this repository enter through [AGENTS.md](AGENTS.md).

| Standards | Covers |
| --- | --- |
| [Collaboration](standards/collaboration.md) | Task authority, working-tree identity, and communication. |
| [Source of truth](standards/source-of-truth.md) | Current behavior, selected requirements, durable decisions, and evidence. |
| [Conventions](standards/conventions.md) | Clear content and information handling for the destination's audience. |
| [Pre-release engineering](standards/pre-release-engineering.md) | Coherent outcomes and proportional process. |
| [Contract lifecycle](standards/contract-lifecycle.md) | Draft changes, historical evidence, and support commitments. |
| [Issue workflow](standards/issue-workflow.md) | Focused execution contracts, readiness, and tracker changes. |
| [PR workflow](standards/pr-workflow.md) | Reviewable changes, publication, and readiness claims. |
| [Validation](standards/validation.md) | Applicable inputs, meaningful checks, process state, and evidence limits. |

| Skills | Typical result |
| --- | --- |
| [Design refinement](skills/design-refinement/SKILL.md) | Bounded decision proposal. |
| [Issue refinement](skills/issue-refinement/SKILL.md) | Execution or decision draft. |
| [Issue publishing](skills/issue-publishing/SKILL.md) | Verified authorized tracker changes. |
| [PR publishing](skills/pr-publishing/SKILL.md) | Reviewable PR and honest remote state. |
| [Test validation](skills/test-validation/SKILL.md) | Applicable checks and evidence summary. |

Adaptable templates are available for a [design note](templates/design-note.md), [issue](templates/issue.md), [PR](templates/pull-request.md), and [downstream adoption](templates/downstream-adoption.md), including an illustrative thin agent entrypoint.

## Maintaining shared content

[Maintenance](docs/maintenance.md) describes placement, semantic changes, source history, and validation. [Source map](docs/source-map.md) records initial extraction and the project-specific or historical content retained outside the handbook. Each rule and procedure has one canonical source.

## Current state

The initial shared content is assembled locally. [Initial validation](docs/validation.md) records its checks and limits. Downstream discovery, resource loading, integration, deduplication, and migration remain consumer-owned follow-up work.
