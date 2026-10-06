# Maintenance

Maintain shared guidance at its canonical location. Keep the handbook useful for actual engineering decisions without accumulating another layer of compulsory process.

## Placement and scope

Use [Context model](../agents/context-model.md) to choose the layer. Human-and-agent rules belong in `standards/`; common agent execution belongs in `skills/`; routing belongs in `agents/`; adaptable output structure belongs in `templates/`.

Before extracting a rule, identify the reusable principle, its applicability, and the product details that remain local. Check nearby content for duplication. Preserve substantive exceptions instead of flattening different project requirements into a misleading universal rule.

Update [Source map](source-map.md) for material new extraction or a changed extraction decision. Record a suitable source identity and concise disposition without importing private working records. The initial map is an extraction record, not a continuously synchronized mirror of the source repositories.

## Changing shared meaning

State the concrete problem and resulting guidance. Distinguish a wording clarification from a changed default, authority assumption, resource dependency, or task result. Amend affected standard, skill, routing entry, and template together where the change actually affects them.

Keep essential constraints easy to find. Move substantial conditional detail to skill references only when it improves selective reading. Do not add empty resource directories, harness-specific metadata, or helper scripts without an actual use.

When moving or renaming content, update incoming references in the same change and state the changed paths in its review record. A real consumer can require a coordinated transition; speculative future consumers do not justify permanent aliases. Follow [Contract lifecycle](../standards/contract-lifecycle.md).

## Source history and consumers

Use ordinary Git history when a Git baseline exists. Record material semantic or path changes in the owning review record. Initial handbook construction does not introduce a tag scheme, release automation, or a separate compatibility registry.

Shared content can evolve continuously. Each consumer chooses when to update, records the source revision actually adopted, and verifies its own arrangement. A shared-source change alone does not prove consumer adoption. Follow [Downstream adoption](downstream-adoption.md); consumer changes are separate tasks in those repositories.

## Validation

For affected content, verify relative references and anchors, UTF-8/LF/final-newline hygiene, and consistency with canonical placement. For a changed skill, validate its frontmatter, name, folder identity, concise trigger description, and absence of unfinished scaffold text. The skill-creator validator checks structural metadata, not decision quality.

Review meaningful scenarios when semantics change: ordinary authorized work, a material unresolved decision, partial external writes, invalid evidence, or a transfer across ownership boundaries. Check whether the instructions preserve task intent and produce an honest result. A document walkthrough is editorial evidence; actual harness discovery and downstream operation are verified in the consumer.

Use [Validation](../standards/validation.md) for proportional checks. Do not add a CI platform, validation framework, or permanent script merely to certify this initial document set. Report actual results and limits, and keep the [Initial validation record](validation.md) historical once the initial handbook is accepted.
