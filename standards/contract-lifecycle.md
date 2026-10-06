# Contract lifecycle

APIs, data formats, packages, and other interfaces can have different support boundaries. Apply lifecycle decisions to the boundary that has an actual consumer or obligation.

| Concept | Meaning |
| --- | --- |
| Draft semantics | The current selected shape before a supported commitment exists. |
| Repository revision | The exact source semantics and implementation at a commit. |
| Artifact or package version | A compatibility family or published artifact identity under its owning policy. |
| Historical evidence | Observations at a recorded revision and conditions. |
| Supported commitment | A stated obligation to consumers of a released or otherwise supported surface. |

## Draft changes

Change an unreleased draft together with affected producers, consumers, specifications, validators, tests, and references. Update only surfaces actually affected. A version number alone does not identify every draft revision or promise cross-revision compatibility.

Do not retain superseded readers, aliases, or fallback behavior solely for hypothetical future consumers. An existing downstream integration, retained data that cannot be discarded, or an explicit support promise can justify coexistence. Record the obligation, boundary, owner, supported lifetime, and removal condition.

Unsupported or incompatible input should fail according to the owning contract. A fresh start or substitute input is a separate caller decision when it changes the requested semantics; it should not be hidden as recovery.

## Evidence and supported surfaces

A milestone acceptance or passing experiment remains evidence for its original revision. It is not an additional compatibility state or proof that current code still behaves the same way.

When a surface becomes supported, document its compatibility and support policy. Breaking changes follow that policy and include migration or rejection behavior where the real obligation requires it. Public source availability alone does not establish a support commitment.

Package versions, wire-format versions, and repository revisions need not advance together. Add transfer provenance only where an actual artifact transfer or retained state cannot be protected through the existing source and run identities.

Use [Pre-release engineering](pre-release-engineering.md) for proportional process and [Validation](validation.md) for current evidence. Specific version schemes, persisted-state semantics, and release lanes remain project-owned.
