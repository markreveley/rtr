---
type: feature
title: Automated checks for terminology and review-entry structure
description: "Preserve the proposed legibility lint: flag undefined terminology and missing review-entry fields, while leaving judgments about clarity to reviewers."
id: m0031
state: proposed
status: draft
tags: [formic-matters, documentation, review, tooling]
implements: m0001
depends_on: [m0026, m0008]
sources:
  - doctrine/matters.md
  - threads/2026-09-10-legibility-and-thread-navigation.md
threads:
  - threads/2026-09-10-legibility-and-thread-navigation.md
generated:
  by: codex/2026-09-10
  at: 2026-09-10T21:58:41Z
---

# m0031 · Automated checks for terminology and review-entry structure

## Why this is filed

Filed on operator direction on 2026-09-10 to preserve useful work
removed while making m0026 self-contained. That direction is preserved
in [the exported session](../threads/2026-09-10-legibility-and-thread-navigation.md).

The earlier proposal is preserved in
`matters/m0026-legibility-standard.md` at commit
`e68a1a9bf219a2dace6f2c4e934b75d07db27639`, execution-plan step 3:

> Forward to m0008, once it exists: a lint that flags terms of art
> absent from the glossary and entries missing preamble fields.
> Whether text is legible stays a judgment check.

This records the origin of the idea. Neither that draft nor this
filing establishes a rule. Doctrine §10, “Deterministic wherever
possible,” supplies the existing principle: code performs checks it
can determine; agents exercise judgment.

## Proposed feature

A **lint** is a tool that reads text and reports specific problems
without rewriting it. This proposal would add two checks:

- Flag specialized terms that lack the definitions required by the
  ratified rules. Intended checks cover glossary entries, bold
  first-use definitions, and named local definition sections with
  links from later references.
- Flag review entries missing required introductory fields, such as
  the reviewer, date, reviewed commit, material read, and deviations.

Each finding identifies the file, location, and missing definition or
field. Reviewers still judge whether the text is understandable.

## Decisions required before ratification

1. Define how the tool identifies specialized terms. A glossary alone
   cannot identify every unfamiliar term absent from it; any heuristic
   must report its limits and leave uncertain cases to reviewers.
2. Specify the exact document scope, definition syntax and placement,
   reference-link checks, entry format, and required fields against
   the ratified rules then in force.
3. Choose the implementation interface and whether findings are
   advisory or block a check, with examples of valid and invalid input.

## Execution dependencies

`depends_on` requires the legibility standard (m0026) and matter
tooling (m0008) to execute before this feature can be staged or
executed, under doctrine §7, “Composition — no containers.” Their
current drafts do not supply binding rules for this feature. The
implementation plan must be completed against their accepted results
before this matter is ratified.
