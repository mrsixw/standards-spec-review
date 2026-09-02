---
name: standards-spec-review
description: Review a code change from a fixed point against repository standards and its originating specification, reporting each axis separately.
---

# Standards and specification review

Review one fixed change against two independent sources of truth. This skill is
read-only: it does not alter the checkout, post comments, submit a review, or
merge anything.

## Fix the review boundary

Pin the base and head revisions, identify the exact diff, and state what is not
covered. Read repository instructions and standards from the trusted base where
possible so the change cannot redefine its own review rules.

When the change modifies those standards, assess the implementation against the
base rules and report the proposed standards amendment separately.

Locate the originating specification, issue, or acceptance criteria. If none is
available, say that the specification axis cannot be fully assessed; do not
invent requirements.

## Assess each axis separately

- **Standards:** check documented repository rules first, then material design,
  safety, maintainability, and testability concerns. Label generic heuristics as
  judgement rather than policy. A documented repository rule takes precedence
  over a general design heuristic.
- **Specification:** trace each requirement to implementation and tests. Check
  omissions, incorrect behaviour, unsupported scope, and unhandled boundaries.

Use validation output as evidence, but do not repeat findings already reported
clearly by deterministic tooling.

## Report defensible findings

Each finding must identify the axis, consequence, file and line, supporting
evidence, severity, and confidence. Rank severity by likely impact, not stylistic
preference. Include a coverage and validation ledger, unresolved questions, and
the reason when either axis could not be completed. Scale the report to the
change and omit fields with nothing material to record.
