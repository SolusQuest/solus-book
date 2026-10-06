# Conventions

Solus Book uses English, standard Markdown, UTF-8, LF line endings, and final newlines. Write prose as normal paragraphs without manual line wrapping. Consumers own their documentation language, code style, title conventions, and toolchain choices.

## Clear, maintained content

Lead with the concrete problem, resulting behavior, or decision. Scale detail to the task. Use tables for comparisons and lists for parallel or sequential information. Include rationale when it changes a reader's decision; remove repeated rules and unused scaffolding.

Use relative Markdown links for files maintained in the handbook. Keep each rule, procedure, and template in its owning location. A link supplies relevant detail without requiring the whole handbook to be loaded. Accepted terminology should remain consistent across related documents.

Templates are adaptable starting points. Omit irrelevant fields rather than manufacturing risks, dependencies, or validation results to fill them. Keep examples distinguishable from implemented behavior.

## Information and destination

Handle information according to the destination's audience, access rules, and the project's policy. A private repository can retain necessary private source, project context, documents, and tracker references within those rules. Committing to a private repository does not require making its content suitable for public release.

Before transferring or publishing material, check the actual destination and what its audience may access. For a public destination, remove restricted source, private tracker links, prompts, transcripts, provider responses, machine-local paths, actual session identities, and raw execution records that cannot be disclosed. Sanitized excerpts and synthetic fixtures can preserve an observable failure without exposing its original data. Apply equivalent restrictions when another destination's audience lacks access to the source material.

Keep credentials out of source, documents, and tracker records, using the project's secret-handling mechanism. Cross-repository write authority follows [Collaboration](collaboration.md); transferring information does not itself grant it.

For Solus Book itself, keep machine-local records outside maintained handbook content. The shared handbook must remain understandable without a private checkout, agent memory, or expiring log. This requirement does not remove a consuming project's own private context or impose a dedicated publication or handoff workflow on it.

Respect source licenses when copying code or assets. A repository's availability does not establish a license or contribution policy. Solus Book does not select licenses or release policies for consuming projects.

## Honest status

Distinguish proposals, working-tree changes, committed revisions, published changes, and supported releases. State only the validation and review actually performed. Successful formatting or link checks do not demonstrate downstream harness loading or product behavior.
