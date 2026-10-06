# Downstream adoption boundaries

Solus Book owns the shared engineering handbook. Each consuming repository owns its adoption. Handbook construction is completed here before integration and migration are carried out as separate work in the downstream repositories.

## Ownership

| Area | Solus Book | Consuming repository |
| --- | --- | --- |
| Engineering standards | Maintain reusable team guidance. | Apply it to the project's actual constraints and document explicit exceptions. |
| Agent context and skills | Maintain common instructions, procedures, and templates. | Supply project context, commands, and task-specific requirements. |
| Harness integration | Describe relevant entrypoint and discovery conventions when needed. | Configure and verify the entrypoints and skill discovery used in that repository. |
| Shared source and updates | Maintain the canonical shared content and its Git history. | Choose the source relationship, record the adopted revision, and manage updates. |
| Deduplication and migration | Clarify which guidance is shared and its intended meaning. | Compare existing documents, preserve local requirements, and update or remove duplicated content. |

The three context layers describe who uses the guidance and how it is loaded. Shared versus repository-specific ownership is a separate concern: a consuming repository can have local content in any layer.

See [Context model](../agents/context-model.md) for placement and source-resource resolution. Shared skills are maintained under `skills/<name>/SKILL.md`; the consumer configures and verifies its actual discovery arrangement, including access to referenced standards and templates.

## Follow-up in each repository

Once the shared content is ready, downstream adoption should cover:

1. Identify the applicable shared standards and procedures, and the project requirements that remain local.
2. Choose how to consume and update the shared source, including the location, revision, and any submodule or link arrangements.
3. Connect the repository's agent entrypoints and skill discovery to the selected content.
4. Consolidate duplicated guidance while preserving product decisions, validation commands, authority boundaries, and intentional local exceptions.
5. Verify document links, harness loading, and relevant workflows in the consuming repository, and record the adoption result there.

The concrete changes, validation evidence, and review belong to the consuming repository. A change to Solus Book alone does not establish that a downstream repository has adopted or validated it. Reading shared instructions also does not grant authority to modify another repository or perform external actions.

Shared-source updates can remain frequent. Each consumer owns when to update and how to record the revision actually used. Submodule configuration, link type, native entrypoints, and platform-specific checkout requirements are decided and verified in that consumer's adoption task.

## Minimal adoption record

Use the [adoption example](../templates/downstream-adoption.md) to record the shared-source location, actual adopted revision and acquisition method, entrypoints, local rules and exceptions, project validation commands, and observed loading results. Its thin `AGENTS.md` example combines shared rules with project-owned context. Adapt it in an existing project document when practical; no separate registry or certification record is required.

For missing sources, inaccessible skill resources, or conflicting revisions, follow [Loading failures](../agents/context-model.md#loading-failures).

## Semantic deduplication

Before removing an old document, identify which rules are covered by shared content, which remain local, and which are intentionally changing. A short migration note can be enough:

```text
Covered by shared content: validation evidence rules.
Retained locally: actual test commands and product acceptance requirements.
Intentional semantic changes: none; any proposed changes are handled explicitly in the task.
```

Check incoming entrypoints and links, tests that read document content or paths, and each skill's associated resources. Update affected references and consumers together, preserving unique local requirements. Verify a representative affected workflow; use [Validation](../standards/validation.md#applicable-checks) when documentation is an input to executable behavior.

## Adoption completion conditions

| Condition | Consumer evidence |
| --- | --- |
| Reproducible source | Record the selected revision and acquisition method; verify that a fresh checkout can obtain the required shared content. |
| Complete loading | Verify entrypoint and skill discovery, plus access to the standards, templates, and other resources needed by the selected skill. |
| Local requirements retained | Identify project-owned commands, product constraints, and explicit shared-rule exceptions. |
| Semantics preserved during deduplication | Account for unique requirements and intentional changes, update incoming references and document consumers, and verify a representative affected workflow. |

These conditions collect existing adoption responsibilities. Record actual results and remaining gaps in the consuming repository; handbook construction alone does not satisfy them.

## This phase

The current phase covers extraction, organization, and verification of the shared handbook in Solus Book. Downstream setup scripts, link creation, entrypoint edits, deduplication, and migration are follow-up work in their respective repositories.
