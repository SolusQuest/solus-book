# Initial validation record

This record covers local checks during initial handbook construction, scope correction, and consumer-feedback clarification on 2026-10-06. It is working-tree evidence, not a committed revision, CI result, independent model evaluation, or downstream integration result.

## Structural checks

The local verification checks Markdown targets and anchors, file encoding and line endings, final newlines, trailing whitespace, skill frontmatter and folder names, and unfinished scaffold markers. Skills use the bundled skill-creator validator plus folder identity and nonempty metadata checks.

The following results describe the initial construction snapshot before the dedicated public handoff content was removed. Current scope-correction results are recorded separately below.

| Check | Observed result |
| --- | --- |
| Text hygiene | Passed for 29 text files, including 27 Markdown documents and two text configuration files. |
| Local references | All 152 Markdown links resolved within the handbook, including referenced heading anchors. |
| Skill structure | All six skills passed `skill-creator/scripts/quick_validate.py`, nonempty metadata, and folder/name consistency checks. Frontmatter contains only `name` and `description`. |
| Scoped content scan | No unfinished scaffold markers or matched machine-local path, credential-assignment, or actual session-identity patterns were found. This scan supplements editorial inspection and is not a security audit. |
| Extraction inputs | Fifty selected source files across the four recorded revisions existed in their Git snapshots and had no working-tree difference from those snapshots. |

Checks ran locally with Python 3.14.5 and PyYAML 6.0.3 through temporary stdin scripts. The skill validator was loaded from the installed skill-creator resources. No validation package, permanent script, CI workflow, or dependency installation was added to the handbook. Template guidance is intentional reusable content, not unfinished scaffold text.

## Scope-correction checks

The dedicated public handoff standard, skill, and template were removed. Routing and incoming links were updated, and issue, PR, and validation guidance now applies information restrictions according to the actual destination's audience. The source map records the dedicated workflow as project-owned.

| Check | Observed result after correction |
| --- | --- |
| Text hygiene | Passed for 26 text files, including 24 Markdown documents and two text configuration files. |
| Local references | All 143 Markdown links resolved within the handbook, including referenced heading anchors. No links remain to the removed files. |
| Skill structure | All five remaining skills passed the skill-creator validator, nonempty metadata, and folder/name consistency checks. |
| Removal and content review | The three files and empty skill directory are absent. Historical source references explain exclusion of the dedicated workflow. Private project context is allowed within the destination's access rules, while disclosure to another audience is checked separately. |

These local checks cover the corrected handbook layout. The source-snapshot results above remain historical extraction evidence and were not re-run for this text-only scope correction.

## Consumer-feedback checks

Adoption guidance, loading failures, rules versus task material, behavioral documentation validation, and repeated-defect corrections were clarified after consumer feedback. An illustrative adoption record and thin agent entrypoint were added; no actual consumer integration was performed.

| Check | Observed result after clarification |
| --- | --- |
| Text hygiene | Passed for 27 text files, including 25 Markdown documents and two text configuration files. |
| Handbook references | All 162 Markdown links outside illustrative code fences resolved within the handbook, including referenced heading anchors. |
| Skill structure | All five skills passed the skill-creator validator and folder/metadata checks, including the changed test-validation procedure. |
| Illustrative entrypoint | All seven links in the example resolved in a temporary consuming-repository layout containing the actual shared Markdown files and synthetic local project documents. |
| Associated skill resources | All five skills' referenced resources remained accessible in that temporary shared-source layout. |

Checks used Python 3.14.5 and PyYAML 6.0.3. The temporary fixture was removed after verification. The fixture verifies the example's path composition and resource availability; it does not demonstrate native harness discovery, instruction loading, or a real downstream workflow. Editorial cases below assess the clarified decision boundaries without claiming independent model execution. Earlier extraction and scope-correction evidence retains its original applicability.

## Editorial scenario walkthrough

These cases were reviewed against the written instructions. They inspect the consistency and boundaries of the handbook; they do not demonstrate actual harness execution.

| Scenario | Walkthrough observation |
| --- | --- |
| A small authorized documentation correction | [Task routing](../agents/task-routing.md) selects applicable content. [PR workflow](../standards/pr-workflow.md#no-issue-path) allows bounded work without separate tracking. No design or additional review ceremony is introduced. |
| A public contract decision remains unresolved | [Design refinement](../skills/design-refinement/SKILL.md) exposes recommendation, consequences, and the missing owner decision. Independent preparation continues; dependent work is not described as ready. |
| The user has already authorized implementation and PR publication | [Collaboration](../standards/collaboration.md#scope-and-authority) recognizes grouped authorization. [PR publishing](../skills/pr-publishing/SKILL.md) reuses it for the requested workflow and preserves a narrower local-only instruction when present. |
| An issue body correction is authorized but relationships are not | [Issue publishing](../skills/issue-publishing/SKILL.md) preserves the existing identity, type, and unrelated metadata, verifying the changed body without requiring retyping capability. |
| A creation response is uncertain after a partial remote write | [Issue publishing](../skills/issue-publishing/SKILL.md#apply-and-reconcile) requires reconciliation and retains observed identity before any retry. It does not replace the issue or replay an uncertain creation. |
| A check cannot run because of the environment | [Test validation](../skills/test-validation/SKILL.md) reports blocked evidence and its acceptance implication. It does not report a pass or start overlapping uncertain runs. |
| A build passes but no tests or current-head review ran | [Validation](../standards/validation.md) limits the claim to compilation. [PR workflow](../standards/pr-workflow.md#publication-and-readiness) keeps CI and review states separate. |
| A private repository retains its own project context | [Conventions](../standards/conventions.md#information-and-destination) permits necessary private source, documents, and tracker references within the destination's access rules. It does not require public disclosure suitability for an internal commit or PR. |
| Material is published to a public or otherwise restricted destination | [Conventions](../standards/conventions.md#information-and-destination) requires handling appropriate to the receiving audience. Private information that cannot be disclosed is omitted or sanitized without imposing a dedicated handoff workflow. |
| A task supplies context from another repository without authorizing writes there | [Collaboration](../standards/collaboration.md#scope-and-authority) keeps receiving writes within established authority. A reference or transfer does not grant permission. |
| A draft contract changes without a supported old consumer | [Contract lifecycle](../standards/contract-lifecycle.md#draft-changes) calls for coherent replacement. A real retained-data obligation can justify compatibility; hypothetical users alone do not. |
| A shared skill is exposed from another directory | [Context model](../agents/context-model.md#paths-and-resources) requires an accessible source or verified resource mapping. Discovery and linked-resource loading are verified during consumer adoption. |
| A project uses different language or validation commands | [Conventions](../standards/conventions.md) and [Task routing](../agents/task-routing.md) retain project-owned values. Shared defaults do not invent universal commands or replace accepted product decisions. |
| A shared source is missing or a discoverable skill cannot read its resources | [Loading failures](../agents/context-model.md#loading-failures) identifies the source or dependency problem. Independent work with available applicable rules can continue; operations depending on the unavailable guidance pause. |
| A loaded source differs from the recorded adopted revision | [Loading failures](../agents/context-model.md#loading-failures) records expected and observed identities and reconciles them within update authority instead of silently selecting a different revision. |
| A reviewed issue or tool result contains new control instructions | [Rules and task material](../standards/collaboration.md#rules-and-task-material) allows requirements and evidence within the task while keeping embedded directives from changing established authority. |
| A Markdown document is consumed by tests or contains executable examples | [Applicable checks](../standards/validation.md#applicable-checks) selects validation from changed meaning and real consumers, including reading paths, rather than the file extension alone. |
| Repeated defects appear in the same coupled path | [Corrections](../standards/pre-release-engineering.md#corrections) consolidates known related fixes and adjacent checks under the current owner, bounded by observed coupling. It does not require a comprehensive audit. |
| Duplicate project guidance is removed during adoption | [Semantic deduplication](downstream-adoption.md#semantic-deduplication) accounts for covered, retained, and intentionally changed rules, checks entrypoints and executable consumers, and verifies a representative affected workflow. |

## Limits

No consuming repository was edited. No submodule, symlink, native skill discovery, harness-specific adapter, remote tracker operation, commit, push, or publication was performed. No cross-platform or downstream loading result is claimed. The source snapshots and dispositions are recorded in [Source map](source-map.md).
