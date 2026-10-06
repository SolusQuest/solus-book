# Agent entrypoint

Solus Book maintains the shared engineering handbook for SolusQuest. Follow the current task and [Collaboration](standards/collaboration.md), [Source of truth](standards/source-of-truth.md), and [Conventions](standards/conventions.md).

Read [Context model](agents/context-model.md) for placement and [Task routing](agents/task-routing.md) for task-specific reading. Load only the standards and skills relevant to the work.

## Maintaining this repository

- Put human-and-agent rules in `standards/`, task execution in `skills/<name>/SKILL.md`, context routing in `agents/`, and adaptable output structures in `templates/`.
- Preserve one canonical body for each rule and procedure. Add supporting resources only when they help an actual task.
- Keep product architecture, commands, current implementation status, and project exceptions with their owning repositories. Personal coordinator, model-routing, quota, and Relay orchestration policies stay outside this handbook.
- Use [Source map](docs/source-map.md) when adapting source guidance and [Maintenance](docs/maintenance.md) when changing shared meaning or paths. Do not import a source project's stage, tooling, or approval rule as a universal default.
- Follow [Downstream adoption](docs/downstream-adoption.md). Changes to consumers, their entrypoints, links, duplicated documents, and migration are handled in those repositories under their task authority.
- Validate changed links, formatting, skill metadata where applicable, and meaningful decision scenarios. Report actual limits; local handbook checks do not establish downstream harness loading.

Use English and normal unwrapped Markdown paragraphs in this repository. Preserve existing task authorization and unrelated working-tree changes. A local handbook task does not by itself authorize commit, push, remote tracker changes, or publication.
