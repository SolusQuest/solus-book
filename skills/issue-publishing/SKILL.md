---
name: issue-publishing
description: Create or update a remote issue from a prepared draft within the task's authorization, preserving identity and unrelated metadata and verifying the requested writes.
---

# Issue publishing

Follow [Issue workflow](../../standards/issue-workflow.md) and the task's actual publication authority. Selecting this skill does not grant authority to write remotely.

## Prepare

Identify the exact repository and existing issue when updating. Read the current target and fields relevant to the request. List the intended text and metadata writes, preserving everything outside their authorized scope.

Prepare the final title and body for the target repository's audience under [Conventions](../../standards/conventions.md#information-and-destination) before any missing approval step. For creation or retyping, verify the enabled native type where the project requires it and an available client that can write and read it. A body-only update preserves the current type without requiring retyping capability.

## Apply and reconcile

Use a structured body argument or body file. Prefer setting required native fields during creation. Update an existing issue in place. Use the actual client's supported operations rather than assuming a particular harness, connector, or CLI version.

Apply relationships and additional metadata only when included in the task. An issue write does not authorize creating tracker categories, changing settings, or closing related work.

For an uncertain response, inspect the actual target or operation state before retrying. Preserve an observed creation identity, reconcile partial writes, and complete only the remaining authorized operations. Do not silently create a replacement or replay an uncertain creation.

## Verify and report

Read back each changed field, including required native type for creation or retyping. Verify the complete changed graph for a bulk structural migration; ordinary text corrections need target and changed-field readback.

Report completion only for verified writes. If capability or permission prevents a required field, preserve the draft or observed partial result and identify the remaining operation. Continue unaffected preparation without substituting title prefixes, body metadata, or unauthorized settings changes.

Return the issue identity, actual changed fields, verification result, and any remaining work. Reuse authorization already established for the requested workflow.
