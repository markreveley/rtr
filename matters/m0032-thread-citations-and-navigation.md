---
type: spec
title: Stable thread-message citations and derived navigation
description: "Define direct citations to individual thread messages and generated navigation between matters and their evidence, including older exports without changing their text."
id: m0032
state: proposed
status: draft
tags: [formic-matters, provenance, documentation, tooling]
implements: m0001
depends_on: [m0011]
sources:
  - doctrine/matters.md
  - threads/2026-09-10-legibility-and-thread-navigation.md
threads:
  - threads/2026-09-10-legibility-and-thread-navigation.md
generated:
  by: codex/2026-09-10
  at: 2026-09-10T22:20:50Z
---

# m0032 · Stable thread-message citations and derived navigation

## Why this is filed

Filed on operator direction on 2026-09-10, following discussion of
whether thread evidence belongs in this repository. The operator
asked to preserve the navigation proposal and place it in the
handoff's working order, then asked about parsing older threads and
whether this work should be expedited. The direction is preserved
in [the exported session](../threads/2026-09-10-legibility-and-thread-navigation.md).

A link to a whole conversation does not identify which message
supports a claim. A reviewer checking “the operator required this”
must search the conversation and distinguish the operator's words
from the agent's interpretation. The repository should make that
comparison direct.

Doctrine §9.2, “Threads,” establishes verbatim primary sources and
derived views; §12, “Storage and format,” requires generated listings;
§10, “Deterministic wherever possible,” separates mechanical checks
from judgment. This proposal supplies a citation format and the
navigation those existing principles permit.

## Proposed text

Amend doctrine §9.2, “Threads,” and §12, “Storage and format,” with
the following requirements. The exact schema and export integration
must be completed before ratification, as listed below.

### Message identifier

A **message identifier** is a permanent name for one retained human
or agent message within an exported thread. The exporter assigns it
once; later messages never cause it to be renumbered or reused.
The thread's path and the identifier together locate the message.

New exports give each message a heading such as `### turn-0024`.
The speaker is recorded separately, so a citation can use
`thread-file.md#turn-0024` without depending on the spelling of the
speaker's name. The original message follows verbatim. This proposal
does not change which messages an export retains or how publication
redactions are applied.

### Message citation

A **message citation** identifies the particular source message
supporting an authored statement. For a new export, the author links
directly to its [Message identifier](#message-identifier). The reader
can inspect the original words and the surrounding exchange.

An author records the relationship explicitly: for example, operator
direction, an agent proposal, or a review finding. Those labels are
claims for a reviewer to check. A label does not ratify a matter or
establish that every statement in the cited message was accepted.

The exact source and relationship also enter structured matter
frontmatter, allowing tooling to collect them. The author writes
that metadata; a generator does not infer agreement from message
text, speaker identity, or the presence of a link.

### Derived navigation index

A **derived navigation index** is a listing generated from recorded
[Message citation](#message-citation) entries. It provides two views:

- For each matter: the cited messages and the author's stated
  relationship between each message and the matter.
- For each thread message: the matters that cite it.

The generator checks that source files and message targets exist,
identifiers are unique within a thread, and citation metadata is
well-formed. Reviewers determine whether a message supports the
claim and whether an operator act occurred. No index entry means
only that no structured citation was recorded; it does not prove
there is no relevant evidence.

The index is regenerated, never edited by hand. It links to original
evidence and introduces no generated interpretation of what the
operator approved.

### Legacy thread parsing

**Legacy thread parsing** means recovering message boundaries and
speaker labels from an existing export without modifying that file.
The parser records the source path, full commit ID, and message line
range. Those coordinates identify the exact text even if a parser
is later corrected.

The existing exports use speaker headings such as `## ▸ Mark` and
`## ▸ Claude`, sometimes with dates or turn descriptions. They also
contain ordinary Markdown headings inside messages. The parser must
recognize export-specific speaker delimiters and report ambiguous
boundaries for review; it must not treat every heading as a message
or invent missing timestamps or speaker identities.

Generated navigation can expose these older messages through their
recorded source coordinates or a derived view with message anchors.
Existing thread bytes and citations remain intact. Adding heading
identifiers to old primary-source files is outside this proposal.
Mechanical parsing locates messages; an author or reviewer still
identifies which messages substantiate each matter.

## Decisions required before ratification

1. Specify the exact matter-frontmatter citation schema, allowed
   relationship labels, and representation of legacy source ranges.
   Define how it coexists with the existing `threads` field.
2. Specify identifier assignment and source-message mapping during
   export, including interrupted sessions and continuation exports.
3. Specify the generated index's path, rendering, and link format,
   including how a reader opens a legacy range in its exact source.
4. Define parser behavior for each existing export format, quoted
   speaker headings, and ambiguous boundaries. Provide examples
   whose expected segmentation can be checked against the source.
5. Define citation-maintenance review: citation metadata lies outside
   a matter's ratified body, so an edit must not silently substitute
   different evidence for a claim in accepted text.

## Proposed execution plan

1. The dev agent adds the completed citation and export requirements
   to doctrine §9.2, “Threads,” and the completed metadata schema to
   §12, “Storage and format.”
2. The dev agent records the deterministic implementation requirements
   in the matter-tooling plan, m0008, if it is still proposed. If
   that plan is already ratified or executed, the dev agent files a
   separate implementation matter instead of rewriting accepted work.
3. Reviewers check the specified new-export and legacy examples,
   source preservation, direct links, and the separation between
   mechanical checks and judgments about authority.
4. The dev agent regenerates `matters/index.md` and records the
   verification under doctrine §9.1, “Runs.”
5. The operator re-ratifies m0001 over the doctrine amendment using
   the mechanism then in force; the recording agent records the
   accepted commit and content hash after that act.
6. The dev agent writes the execution record, marks this matter
   executed, regenerates the index, and presents the branch for the
   operator's merge-commit merge. This specification is complete
   when its requirements are in doctrine and the execution record
   exists. The generator and parser become available only when
   their implementation matter executes.

## What this changes and depends on

The proposal adds an export-heading convention and citation metadata.
It preserves doctrine §9.2's verbatim evidence and §9.4,
“Immutability.” It introduces neither a new source repository nor an
automatic ratification mechanism. Search and summaries are outside
this proposal.

`depends_on: [m0011]` requires the thread-persistence policy to execute
before this matter is staged or executed, under doctrine §7,
“Composition — no containers.” Its eventual export policy must be
checked against this design before ratification; its current draft
supplies no binding requirement here. m0008 names the intended
implementation work, not an operating mechanism.

Existing preserved threads can be indexed later. Capture of otherwise
unavailable session evidence is the time-sensitive task. The planned
order therefore keeps the current legibility and authority work first,
then the persistence policy, this specification, and its implementation.
