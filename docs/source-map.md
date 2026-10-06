# Source map

This map records the initial extraction into Solus Book. Sources informed the handbook; their product requirements and publication settings remain owned by the source repositories. Source paths below are repository-relative inventory entries, not dependencies on another local checkout.

## Inspected snapshots

The selected tracked documents were inspected on 2026-10-06 with no tracked modifications to those documents. The revisions identify extraction inputs, not evidence of downstream adoption or remote publication.

| Source | Revision |
| --- | --- |
| SolusAgent (`solus-agent`) | `bc964b288e2fa24becf7c6c410289b6c8592564d` |
| ContractScribe (`contract-scribe`) | `e588e52461b11ca635905652a6ca96b3faec3ca4` |
| Agentic PR Review (`agentic-pr-review`) | `8064da4a638fbd48a7b846a5b6f4acf89d932457` |
| Game (`game`) | `e4d3801c46273d0dd8f6842aeb68c4aaf6ecd46e` |

## Extraction decisions

| Source material | Disposition | Handbook destination and reason |
| --- | --- | --- |
| SolusAgent, ContractScribe, APR: `docs/50_ai/collaboration-layers.md`; Game: `docs/50_AI/AI协作规则分层.md` | Merge and adapt | [Context model](../agents/context-model.md). Preserve three layers and distinguish them from shared/local ownership. Replace per-project copied procedures with one canonical skill body. |
| SolusAgent and ContractScribe: `docs/00_project/source-of-truth.md`; APR: `docs/00_project/source-of-truth.md` and `docs/50_ai/agent-context.md` | Merge and adapt | [Source of truth](../standards/source-of-truth.md). Separate current behavior, selected requirements, living planning, and historical evidence. Exclude current product implementation claims. |
| SolusAgent and ContractScribe: `docs/00_project/conventions.md`; root `AGENTS.md` entries across the sources | Extract common rules | [Collaboration](../standards/collaboration.md) and [Conventions](../standards/conventions.md). Preserve task authority, audience-appropriate information handling, and focused changes. Language, toolchain, naming, and merge-method choices stay project-owned. |
| SolusAgent and ContractScribe: `docs/00_project/pre-release-engineering.md`; Game: `docs/10_Project_Management/里程碑与范围控制.md` and `docs/50_AI/skills/feature-design-refinement.md` | Merge and shorten | [Pre-release engineering](../standards/pre-release-engineering.md). Split by independently acceptable outcomes, keep related invariants together, and justify extra process by a concrete failure. Exclude milestone identities and fixed task-duration budgets. |
| SolusAgent and ContractScribe: `docs/00_project/contract-lifecycle.md` | Extract common lifecycle | [Contract lifecycle](../standards/contract-lifecycle.md). Draft semantics, exact-revision evidence, and real support commitments are separate. Saved-context, patch, audit, and campaign semantics remain local. |
| SolusAgent, ContractScribe, APR: `docs/10_workflow/issue-workflow.md`; Game: `docs/10_Project_Management/Issue与Project规则.md` | Merge with project configuration | [Issue workflow](../standards/issue-workflow.md). Keep focused outcomes, readiness, useful relationships, and native tracker metadata. Enabled types, assignees, labels, board fields, and repository destinations remain local. |
| SolusAgent, ContractScribe, APR: `docs/10_workflow/pr-workflow.md`; Game: `docs/10_Project_Management/PR创建规则.md` and `PR标题规则.md` | Merge with project configuration | [PR workflow](../standards/pr-workflow.md). Preserve reviewable scope, accurate evidence, changed-head review, and operation authority. Keep project release lanes and merge methods local. |
| SolusAgent and ContractScribe: `docs/50_ai/skills/test-validation.md`; APR: validation sections of context and workflow documents | Extract common invariants | [Validation](../standards/validation.md) and [Test validation skill](../skills/test-validation/SKILL.md). Preserve applicable inputs, meaningful execution, process identity, and evidence limits. Exclude build commands, test filters, timing budgets, and CI matrices. |
| SolusAgent and ContractScribe: `docs/50_ai/skills/architecture-design-refinement.md`; APR: `docs/50_ai/skills/runtime-design-refinement.md`; Game: `docs/50_AI/skills/feature-design-refinement.md` | Merge and generalize triggers | [Design refinement skill](../skills/design-refinement/SKILL.md). Keep material decision exposure, bounded alternatives, ownership, and observable acceptance. Do not turn Game-specific confirmation for every design detail into a shared approval rule. |
| SolusAgent, ContractScribe, APR: `docs/50_ai/skills/issue-refinement.md`; Game: `docs/50_AI/skills/solusquest-issue-drafter.md` | Merge and shorten | [Issue refinement skill](../skills/issue-refinement/SKILL.md). Produce a bounded execution or decision draft. Preserve existing issue identity and distinguish drafting from publication. |
| SolusAgent and APR: `docs/50_ai/skills/issue-publishing.md` | Prefer neutral procedure | [Issue publishing skill](../skills/issue-publishing/SKILL.md). Preserve changed-field readback and reconciliation of uncertain writes. CLI flags and API endpoint recipes are tool-specific details, not shared prerequisites. |
| SolusAgent, ContractScribe, APR: `docs/50_ai/skills/pr-publishing.md`; Game: `docs/50_AI/skills/solusquest-pr-publisher.md`; source PR templates | Merge and shorten | [PR publishing skill](../skills/pr-publishing/SKILL.md) and [PR template](../templates/pull-request.md). Preserve task identity, scoped staging, actual validation, and remote readback. Exclude mandatory product checklists. |
| Game: `docs/50_AI/skills/solusquest-public-repo-handoff.md` | Keep workflow project-owned | The dedicated private-to-public handoff arrangement is project-specific. [Collaboration](../standards/collaboration.md) and [Conventions](../standards/conventions.md) retain only general cross-repository authority and information handling for the actual destination. Product profiles, role arrangements, release pins, and any dedicated handoff procedure remain local. |
| Game: `.codex/skills/` and `.claude/skills/` entrypoints | Extract placement lesson | [Context model](../agents/context-model.md). Common procedure belongs in one source; harness details belong at the adapter boundary. No native wrapper copies or downstream links are created here. |

## Differences retained or excluded

- SolusAgent and ContractScribe prefer English repository prose; Game uses its own language convention. Solus Book uses English, while consumers select their own language policy.
- Game has specific cross-repository tracking and commit-pinned documentation requirements. The shared rule distinguishes living references from immutable evidence; stronger project pinning remains local.
- Game's private-to-public handoff workflow remains project-owned. Private repositories can retain necessary private context under their access rules; the handbook does not require all committed content to be publicly disclosable.
- APR's PR documents contain instructions for an earlier delivery interval alongside newer context. Those stage instructions are excluded from the shared handbook rather than repaired in the source repository during extraction.
- Product assembly graphs, platform API versions, provider secrets handling, runtime contracts, release policies, and executable commands retain their source owners. Only independently reusable engineering principles are extracted.
- Task authorization remains decisive. Defaults inherited from a source, including merge restrictions or review stages, do not erase explicit authorization in the current task.
- Personal coordinator, model-selection, quota, and orchestration policies are outside the handbook's scope.

## Consumer feedback incorporated

The maintainer supplied adoption feedback on 2026-10-06. The following clarifications were incorporated without importing product architecture, commands, tracker mappings, release procedures, or product safety requirements.

| Feedback theme | Shared destination |
| --- | --- |
| Minimal adoption guidance and explicit completion conditions | [Downstream adoption](downstream-adoption.md) and [Adoption example](../templates/downstream-adoption.md). |
| Missing source, incomplete resource loading, and revision mismatch | [Context model](../agents/context-model.md#loading-failures). |
| Selected rules versus instructions embedded in processed material | [Collaboration](../standards/collaboration.md#rules-and-task-material). |
| Behavioral validation of documentation and its consumers | [Validation](../standards/validation.md#applicable-checks) and [Test validation skill](../skills/test-validation/SKILL.md). |
| Repeated defects in one coupled path | [Pre-release engineering](../standards/pre-release-engineering.md#corrections). |
| Semantic accounting before removing duplicate documentation | [Downstream adoption](downstream-adoption.md#semantic-deduplication). |

For later changes, follow [Maintenance](maintenance.md). Actual consumer changes follow [Downstream adoption](downstream-adoption.md).
