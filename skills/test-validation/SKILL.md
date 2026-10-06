---
name: test-validation
description: Select and run checks for a changed behavior or explicit acceptance claim, then report applicable evidence, failures, blocked checks, and limits without unnecessary validation infrastructure.
---

# Test validation

Read the task's acceptance, the actual diff, relevant project commands, and [Validation](../../standards/validation.md). Use the applicable project toolchain and required environments.

## Procedure

1. Identify the changed behavior, failure surface, and important producer-consumer or shared invariants. Include normative documentation, document-reading tests, executable examples, and generated content where affected; the file extension does not determine the checks. Choose focused checks that can demonstrate the relevant acceptance claim.
2. Confirm inputs and prerequisites: working tree or revision, toolchain, configuration, restore/build validity, test selection, and environment. Do not reuse output from another tree or configuration as current evidence.
3. Execute the authorized checks. Confirm tests actually ran; compilation, discovery, or an empty test run supports only its narrower observation. Use synthetic data where it preserves the actual question.
4. Retain the process or operation handle for a long run. Inspect the original state before retrying or terminating the identified process. Avoid overlapping uncertain runs and unrelated process termination.
5. Diagnose failures and classify environment or capability blockers separately. After a correction, rerun affected checks. Broaden or repeat only when changed inputs or unresolved concerns justify it.
6. Report the actual command, relevant inputs, result, acceptance implication, and material limitation. Keep raw records in the project's appropriate evidence location and publish a concise summary suitable for the destination's audience under [Conventions](../../standards/conventions.md#information-and-destination).

## Result

Separate passed, failed, blocked, and unexecuted checks. State what remains unverified and whether it affects acceptance. A local result does not establish CI, downstream harness loading, an untested platform, or release readiness.

Once sufficient applicable checks pass, complete the authorized task. Do not create a test framework, platform matrix, or permanent evidence format merely to certify a low-impact documentation change or initialization.
