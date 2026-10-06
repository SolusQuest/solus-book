# Downstream adoption example

Adapt this example in an existing project document or a small adoption note. It illustrates an arrangement, not an installed configuration or a verified adoption. The consuming repository chooses its paths, acquisition method, local rules, and harness setup under [Downstream adoption](../docs/downstream-adoption.md).

## Minimal adoption record

| Field | Record in the consuming repository |
| --- | --- |
| Shared source | Actual source location and repository identity. The example below uses `docs/shared/`. |
| Adopted revision and acquisition | Actual full source commit and how a fresh checkout obtains it. Include the required initialization or retrieval instructions. |
| Entrypoints and skill discovery | Actual entrypoint links and discovery configuration, with the source location used to resolve skill resources. |
| Project rules and exceptions | Links to local context, product constraints, and deliberate exceptions to shared defaults. |
| Validation commands | The project's actual commands and required environments, or the document that owns them. |
| Loading and workflow results | What was actually checked, relevant harness/version, entrypoint and resource loading results, and a representative workflow result. Mark missing or unexecuted checks explicitly. |

## Thin AGENTS.md example

The following block is an illustrative consuming-repository root file. `docs/project-context.md`, `docs/development.md`, and `docs/shared-adoption.md` stand for project-owned documents; rename them and the shared-source path to fit the actual repository. Link shared rules directly rather than adopting Solus Book's own maintenance entrypoint.

```markdown
# Agent entrypoint

Read [Project context](docs/project-context.md) and [Development](docs/development.md) for this project's architecture, constraints, commands, and validation requirements.

Use [Collaboration](docs/shared/standards/collaboration.md), [Source of truth](docs/shared/standards/source-of-truth.md), and [Conventions](docs/shared/standards/conventions.md) for shared defaults. Use [Task routing](docs/shared/agents/task-routing.md) to select the applicable skill and supporting rules.

[Shared adoption](docs/shared-adoption.md) records the selected source revision, resource mapping, local exceptions, and loading results. Relative references inside shared files resolve from their source location.

The current task, applicable instructions, working directory, and existing authorization remain in force. Project documents supply local requirements and explicit exceptions. Surface material unresolved conflicts before dependent work; continue independent authorized work using available applicable guidance.
```

Verify the actual entrypoint, skill discovery, and referenced resources in the consuming harness. Resolving the illustrative links alone does not prove that the harness loads them.
