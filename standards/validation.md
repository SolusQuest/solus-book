# Validation

Choose checks from the behavior and failure surface changed by the task. Evidence should support the acceptance claim being made, with its actual inputs and limitations.

## Applicable checks

Start with focused checks that exercise the affected behavior or meaningful invariant. Include actual producer-consumer paths for an interface change. Broaden checks for a shared boundary, failure, or unresolved concern. Once sufficient applicable evidence passes, proceed toward completing the task.

Documentation can be a behavioral input. Normative specifications, Markdown read by tests, executable command examples, and generated content need checks selected from their changed meaning and actual consumers. Do not reduce validation to links and formatting solely because a file ends in `.md`. When moving or removing documentation, include affected reading paths and generated or executable consumers.

Build success proves compilation under the tested inputs. Test discovery or an empty passing test invocation does not prove execution. Formatting and link checks do not prove product behavior, downstream installation, cross-platform operation, or release readiness.

Use the project's real commands and required environments. Native local checks are usually sufficient for an ordinary local question; add another platform for a concrete compatibility question or required qualification. Synthetic fixtures should preserve the failure being tested. Paid or live-service checks follow the task's authorization.

## Input validity

Record the working tree or revision, command, relevant toolchain, configuration, selection, result, and material limitation. Check applicable restore and build prerequisites before using flags that skip them. Changed source, dependencies, project membership, toolchain, or configuration can invalidate cached output.

Do not reuse an old worktree, different configuration, or earlier revision's output as current evidence without establishing its applicability. Retain raw output in the project's appropriate local or CI evidence location; publish a concise result suitable for the destination's audience under [Conventions](conventions.md#information-and-destination).

## Runs and failures

Preserve the original process or operation handle. Inspect an active or uncertain run before starting another. Terminate only the task's identified process when necessary. Do not kill unrelated processes by global executable name.

Distinguish assertion failures from environment or capability failures. Report a blocked check as blocked. A timeout or cancellation is incomplete evidence, not a pass. Diagnose the concrete failure before retrying, and rerun only the affected checks unless a broader concern remains.

## Completion claims

Report what ran, what passed or failed, what remains unverified, and how those results relate to acceptance. Do not infer CI, independent review, harness loading, or downstream qualification from a local result.

The [Test validation skill](../skills/test-validation/SKILL.md) describes execution. Projects own commands, required checks, test selection conventions, performance budgets, and qualification matrices.
