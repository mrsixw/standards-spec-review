---
name: standards-spec-review
description: Review a code change from a fixed point against repository standards and its originating specification, reporting each axis separately.
---

# Standards and Spec Review

This is a read-only review core. It does not post comments, approve changes, merge branches, or alter the checkout.

## Workflow

1. Pin the fixed point and identify the exact diff.
2. Locate the originating issue, specification, or explicitly record that none exists.
3. Locate repository standards and applicable validation results.
4. Review the Standards axis for documented rule violations and material design smells.
5. Review the Spec axis for missing requirements, scope creep, and incorrect behavior.
6. Report the two axes separately with file and line evidence, severity, and confidence.

Documented repository standards override generic heuristics. Treat design smells as judgement calls, not hard violations. Skip findings already enforced by tooling.
