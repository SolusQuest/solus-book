# Context model

The handbook separates guidance by audience and execution role. Shared versus project-specific ownership is an independent dimension.

## Three layers

| Layer | Handbook source | Project-owned additions |
| --- | --- | --- |
| Human-and-agent rules | `standards/`: engineering principles and workflow requirements. | Product purpose, architecture, terminology, commands, support commitments, and local workflow requirements. |
| Harness-neutral agent context and procedures | `agents/` for routing; `skills/<name>/SKILL.md` for task execution. | Project context and task-specific procedures that do not depend on one harness. |
| Harness-specific entrypoints | The placement guidance in this document; actual adapters only when a maintained need exists. | Discovery configuration, native entrypoints, tool-specific instructions, and permission or capability handling. |

A rule affecting human work belongs in the first layer. An agent execution procedure belongs in the second. A particular harness's loading or tool behavior belongs in the third. All three can contain project-local material.

## Canonical content

Standards own rules. Skills own the common steps for producing a task result and link to applicable standards. Templates supply output structure. A skill can restate an essential operational constraint when needed to prevent misuse, but should not copy an entire standard.

Each skill has one maintained `SKILL.md` body with a concise name and description. Supporting references are added only for substantial conditional detail. A native adapter should route to this body and add only its actual harness requirements.

This repository maintains source skills under `skills/`. Downstream discovery directories and native entrypoints are configured and verified during [adoption](../docs/downstream-adoption.md); their loading behavior is not inferred from the existence of these source files.

## Composing task context

Start with the current task, the consuming repository's context, and its documented shared-source location. Read applicable shared rules and the relevant skill, then the product documents needed for the specific change. Distinguish accepted boundaries from unresolved choices and current behavior from plans.

Project documents supply local values and explicit exceptions. The handbook supplies shared defaults for decisions left open. Current task instructions and established authority remain in force under [Collaboration](../standards/collaboration.md). Surface a material unresolved conflict to its owner; do not silently replace a product decision with a shared example.

## Paths and resources

Relative links in Solus Book resolve from their owning file in the handbook source tree. An adoption arrangement must preserve access to referenced standards and templates, or provide a verified mapping to their actual source location. Exposing only a copied skill folder does not establish that those dependencies remain accessible.

When a harness exposes a linked entrypoint, use the consuming repository's documented handbook location to resolve source references. Do not guess it from a machine-specific absolute path. Verify the chosen arrangement, including resource access, in the consuming repository.

## Loading failures

Report the unavailable resource, the entrypoint or skill that required it, the documented source location, and the expected versus observed revision when known. Distinguish a missing source from a readable skill whose dependencies fail. Do not report loading or adoption complete while a required resource remains unavailable.

| Failure | Locate and resolve |
| --- | --- |
| Shared source or required rule is missing | Inspect the consumer's documented acquisition and initialization instructions and selected location. Restore the selected source within task authority, or report the missing capability. |
| Skill is discoverable but a dependency cannot be read | Inspect the actual skill source location, resource mapping, link target, and access to the referenced standard or template. Discovery alone does not prove complete loading. |
| Loaded content differs from the adopted revision | Report both identities and the affected paths. Reconcile them with the consumer's adoption record and authorized update scope before relying on the conflicting content. |

Continue independent work covered by the current task and available applicable rules, such as inspecting local context, collecting evidence, or preparing a bounded draft. Pause only operations whose required rules, resource semantics, or acceptance depend on the missing or conflicting content. Obtain that guidance or the necessary owner decision before those operations; do not silently substitute guessed instructions, a stale copy, or the latest revision. Recheck the affected loading path after correction.

Use [Task routing](task-routing.md) for selective reading and [Maintenance](../docs/maintenance.md) for changing placement or semantics.
