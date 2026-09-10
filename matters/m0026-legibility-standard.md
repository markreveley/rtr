---
type: spec
title: Legibility standard — record text is written to its ratifier
description: "Text the operator must act on uses plain language, named definition sections before references to bespoke terms, explicit actors, numbered processes, and a fixed review-entry structure; a glossary enters the doctrine."
id: m0026
state: proposed
status: draft
tags: [formic-matters, process, documentation, review]
implements: m0001
sources:
  - doctrine/matters.md
  - threads/2026-08-29-complexity-escape-and-working-text.md
  - threads/2026-09-10-legibility-and-thread-navigation.md
threads:
  - threads/2026-08-29-complexity-escape-and-working-text.md
  - threads/2026-09-10-legibility-and-thread-navigation.md
generated:
  by: claude-code/2026-08-29
  at: 2026-08-29T04:30:36Z
---

# m0026 · Legibility standard — record text is written to its ratifier

Filed on operator direction in the 2026-08-29 session, exported at
[threads/2026-08-29-complexity-escape-and-working-text.md](../threads/2026-08-29-complexity-escape-and-working-text.md)
and cited in `threads`. The `sources` list above identifies the
doctrine and recorded operator direction this proposal rests on.

The 2026-09-10 revisions remove reliance on pending rules and add
named definitions before references, on operator direction in
[the exported session](../threads/2026-09-10-legibility-and-thread-navigation.md).

## Diagnosed reason

On 2026-08-29 the operator read a vetting entry that conformed to
every rule in force — appended per §6 "Vetting and ratification,"
correct trailer, faithful findings — and could not audit it. The
entry used terms of art without definitions ("pin," "clean review,"
"diff shape"), described acts without naming their actors ("the
review" without saying whose), and was written in the register
agents use with each other, modeled on m0001's vetting rounds. The
operator named the resulting state "complexity escape": the point
where the record outruns the one person whose acts give it force.

Every gate in this framework ends at an operator act. An artifact
the operator cannot audit turns that act into trust, and trust at
the gate is the rubber stamp §14 "The bootstrap" records — now with
better-looking paperwork. §4 "Cheap to file, expensive to ratify"
prices filing and ratifying; nothing anywhere prices reading. This
matter adds the missing requirement: text the operator must act on
must be legible to the operator, and that is a property reviewers
check, not a courtesy.

The principles below are extracted from the operator's rulings in
that session, each anchored to the operator's words:

1. **Write to the ratifier.** "I am not qualified to really audit
   your recent contributions" — an entry only agents can read has
   failed its purpose regardless of conformance.
2. **Name the actor of every act.** "When you say 'the review' do
   you mean the operator review, or the agent review of the
   operator's restatement? You need to be more explicit."
3. **No undefined terms of art.** "There should really be a ban on
   using terminology that hasn't been explicitly defined."
4. **Structure what is enumerable.** "This would fit much better
   into a scheme of sorts, some sort of semi-structured data that I
   can cross reference" — the preamble of a review entry is fields,
   not prose.
5. **Plain statement first, detail after.** "This is essentially
   unscrutable" — said of a finding whose first sentence could not
   be understood without the rest.
6. **Processes are numbered steps.** "Break every process down to
   discrete steps: 1 - actor (operator or agent) does x with these
   considerations, 2 - same statement form, next step, 3 -
   completion definition."
7. **Vocabulary drift is challenged on sight.** "Usage of
   terminology outside of this needs to be immediately called out
   by the other and drilled into — either to correctly state with
   existing terminology, or to upgrade the term to a proper defined
   word in the glossary."

## Proposed text

Seven amendments, each defined in its own section below.

### Named definitions before references

**Bespoke terminology** means names given a particular meaning by
this framework or by the document's author, including names for
rules and processes. A reader must be able to locate what each name
means before being asked to accept or carry out an instruction using
it.

In a matter body, review entry, or handoff, the writer gives each
such term its own named section in the same document, before the
first reference to it outside that definition. The heading uses the
term's exact name. The section opens with a plain-language definition
and, for a rule or process, states who does what and when the
requirement is satisfied.

Later references use that exact name and link to its definition
section. The writer does not introduce a shortened or alternative
name in an execution plan. A definition in another document does
not replace the local section: when an existing framework rule is
being explained, the local definition cites its ratified source.

Established technical vocabulary may instead be explained in the
glossary or in bold at first use. Verbatim historical quotations
remain unchanged; the writer explains any term needed to understand
them in the surrounding authored text.

### Glossary

A **glossary** is a collection of definitions. A new doctrine section
holds the framework's definitions, with a named subsection for each
term. Changes to those definitions go through matters. The initial
definitions follow.

#### Pin

The **pin** is the recorded pair that freezes what was accepted: a
commit ID, which preserves the exact text in Git history forever,
plus a hash of the accepted text. Recorded only after the
operator's act, never offered in advance.

#### Hash

A **hash** (also **checksum**) is a short fingerprint computed from a
text; any change to the text changes the fingerprint, so equal
fingerprints mean identical text. The commit remains the source of
truth; the stored hash exists because the matter file legitimately
keeps changing around the accepted text (review entries append,
state fields change), and recomputing one number is a cheaper
drift check than re-deriving which parts were accepted.

#### Ratified region

The **ratified region** is the part of a matter file the
[Pin](#pin) covers: the body minus the frontmatter and the
append-only `## Vetting` and `## Execution` sections. m0001 is
special: its [Pin](#pin) covers the whole doctrine file instead.

#### Contract

The **contract** is a ratified matter's text, in its role after
ratification: the thing execution is held to (§3 "State —
mutable": "the plan is now the contract").

#### Disposition

A **disposition** is a review entry's closing judgment: what the
review concluded and what, if anything, it asks for.

#### Recording agent

The **recording agent** is the agent that writes lifecycle facts into
a matter after an operator act: state changes, the [Pin](#pin). It
records the operator's acts after they occur.

#### In situ

**In situ** is Latin for "in its original place." An exported review
comment is shown in situ: quoted inside an excerpt of the exact
text it responded to, with its file location and carrying commit —
never in a list detached from its context. Already used,
undefined, by §8 "Where discourse lives" and §9.2 "Threads"; the
operator challenged it on 2026-08-29.

#### Thread

A **thread** is a verbatim export of a session, under `threads/`;
never edited after export (§9.2 "Threads").

#### Run

A **run** is an append-only record of a verification actually
executed, under `runs/` (§9.1 "Runs").

### Review-entry structure

The **review-entry structure** is the format a reviewing agent uses
to record a review. Doctrine §6, "Vetting and ratification,"
currently requires "(round, reviewer, findings, disposition)".
That becomes: an introductory field table — reviewer;
date; the commit whose text was reviewed; what was read; deviations
— rendered the same way in every entry; then findings, each opening
with an ID, the section it is about, and one plain-language sentence
stating the problem, with explanation after; then the
[Disposition](#disposition).
Prose stays where judgment lives; fields carry what is enumerable.

### Actor rule

The **actor rule** requires the writer to name who performs each
action described in record text. In that text, "the review," "the
commit," or "approval" without whose is a finding. The
sentence must say who acts: the operator, the reviewing agent, the
[Recording agent](#recording-agent). The requirement is satisfied
when the reader can identify who performs each action from the
sentence describing it.

### Numbered-steps rule

The **numbered-steps rule** requires the writer to describe a
process as a numbered sequence of actions. Each step names who acts
— the operator, or an agent — and what they do, in the same sentence
form throughout. The final step defines completion: the observable
fact that means the process is done.
The requirement is satisfied when every step names who acts and
what they do, and the final step states how completion is recognized.

### Drift-challenge protocol

The **drift-challenge protocol** is the procedure a reader and writer
follow when a term lacks the required definition or is used with a
different meaning from its definition. Either the operator or an
agent may identify the problem.

1. **The reader** identifies the term and explains what is missing
   or inconsistent before relying on the sentence.
2. **The writer** rewrites the sentence using an already-defined
   term, or supplies a definition under
   [Named definitions before references](#named-definitions-before-references).
   A change to a doctrine definition goes through a matter.
3. **The reader** checks that the sentence uses the defined meaning
   and that the required definition precedes the reference.
   The procedure is complete when both checks pass.

### Legibility review duty

The **legibility review duty** requires a reviewer to check whether
the operator could explain a matter, review entry, or handoff in
their own words. Each finding identifies the unclear
passage and explains what needs clarification. The reviewer completes
this duty by reporting the unclear passages found, or stating that
the review found none.

## What this contradicts

No ratified matter. It amends §6, "Vetting and ratification," with
the six requirements defined above and adds the
[Glossary](#glossary). Doctrine §8, "Where discourse lives," already
defines "in-document review" inline in bold. This proposal adds a
stricter form for framework-specific names: a named definition
section before references, as specified in
[Named definitions before references](#named-definitions-before-references).
Nothing is superseded.

## Proposed execution plan

1. The dev agent adds the [Glossary](#glossary) and its term
   subsections to the doctrine.
2. The dev agent adds
   [Named definitions before references](#named-definitions-before-references)
   to doctrine §6, "Vetting and ratification."
3. The dev agent replaces that section's review-entry format with
   [Review-entry structure](#review-entry-structure).
4. The dev agent adds [Actor rule](#actor-rule) and
   [Numbered-steps rule](#numbered-steps-rule) to doctrine §6,
   "Vetting and ratification," under those exact headings.
5. The dev agent adds [Drift-challenge protocol](#drift-challenge-protocol)
   and [Legibility review duty](#legibility-review-duty) to doctrine
   §6, "Vetting and ratification," under those exact headings.
6. The dev agent updates `CLAUDE.md` to direct agents to the resulting
   doctrine sections and explain their requirements in plain language.
   Any bespoke names used there receive local named definitions and
   links as required by
   [Named definitions before references](#named-definitions-before-references).
7. Reviewers check the amended text against all seven sections above,
   including definition placement, reference links, named actors,
   numbered processes, required review-entry fields, and legibility.
8. The dev agent regenerates `matters/index.md` and records the
   verification under doctrine §9.1, "Runs."
9. The operator re-ratifies m0001 over the doctrine amendment using
   the ratification mechanism then in force. The
   [Recording agent](#recording-agent) records the [Pin](#pin) only
   after that act.
10. The dev agent appends this matter's execution record, moves it
    `staged → executed`, regenerates the index, and presents the
    branch for the operator's merge-commit merge. Execution is
    complete when the proposed changes are in the target and the
    execution record is written, under doctrine §3.1,
    "The execution record."
