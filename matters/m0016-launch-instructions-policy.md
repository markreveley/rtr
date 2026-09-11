---
type: spec
title: Self-contained matters and entry points aligned with the ratified record
description: "Require defined terms, self-contained explanations, and exact doctrine quotations, ground launch instructions in ratified authority, and rewrite and maintain the README."
id: m0016
state: proposed
status: draft
tags: [formic-matters, process, execution, provenance]
implements: m0001
depends_on: [m0020, m0018, m0026]
threads:
  - threads/2026-09-11-m0016-readme-self-contained-matters.md
  - threads/2026-08-26-m0012-execution.md
  - threads/2026-08-29-minimal-handoff-and-declared-sources.md
generated:
  by: codex/2026-08-26
  at: 2026-08-26T23:55:08-07:00
---

# m0016 · Self-contained matters and entry points aligned with the ratified record

Doctrine quotations below reproduce `doctrine/matters.md` at repository
commit `e3f7195c5cd0339b3c07cc2ccef281a67ef38df9`. Proposed amendments are labeled separately. Quoted
terms retain their source wording; the definitions below explain how
this matter uses them.

## Terms used in this matter

The glossary proposal would collect framework definitions, including
“Contract,” but does not yet define “Plan”
([m0026](m0026-legibility-standard.md#glossary)). It remains proposed.
The definitions below state exactly how this matter uses those terms;
its proposed glossary additions appear later for ratification.

### Matter execution plan

A **matter execution plan** is the written set of actions and intended
results proposed in a matter for the executing agent to carry out.
Before ratification it is proposed work. After ratification, its
accepted wording is part of the text against which execution is
checked. It is not the entirety of what the operator ratifies: the
matter's other accepted requirements and proposed normative text also
constrain execution.

### Agent working plan

An **agent working plan** is an agent's task breakdown or checklist for
organizing its work, whether held in a planning tool, session, or file.
Creating or editing one does not itself constitute operator
ratification or change the accepted requirements. If such a breakdown
is included in the text submitted for ratification, its inclusion must
be explicit; it cannot silently replace the matter execution plan.

### Contract

**Contract** means the accepted requirements in the ratified text
against which execution is checked. It is not a separate document or
an agent working plan. This matter uses “ratified requirements” in its
own instructions; “contract” is explained here because the doctrine
uses it in the quotation below.

### Ratified region

The **ratified region** identifies the text whose acceptance is
recorded. Ordinary matters use the body excluding frontmatter and
append-only review and execution records. The doctrine states:

> the body minus the frontmatter and the append-only record sections
> (`## Vetting`, `## Execution`), so lifecycle appends and frontmatter
> transitions never invalidate it.

Source: [doctrine §6, “Vetting and ratification”](../doctrine/matters.md#6--vetting-and-ratification).

Where the proposed text is a separate document, that document is
covered as specified by the doctrine; m0001 covers the whole doctrine
file. This matters because approval is not limited to a heading named
“plan.” The same section states:

> Where a matter's proposed text is a
> separate document (m0001 → this specification, which has no
> frontmatter), the hash is that document's whole file at the same
> commit.

Source: [doctrine §6, “Vetting and ratification”](../doctrine/matters.md#6--vetting-and-ratification).

## Diagnosed reason

The operator accepts specific text, and the executing agent must carry
out the requirements in that text. This prevents an agent's working
checklist from being mistaken for the approved scope. The doctrine's
`ratified` state describes that acceptance as:

> the operator has accepted the exact text; the plan is now the contract

Source: [doctrine §3, “State — mutable”](../doctrine/matters.md#3--state--mutable).

The words “plan” and “contract” in this sentence need explicit
boundaries: the statement must not be restated as approval of whatever
an agent happens to call its plan. The proposed glossary definitions
make those boundaries explicit.

If execution would change accepted behavior, scope, interface, or
normative text, the agent must stop and obtain re-ratification of the
changed matter execution plan. A launch prompt cannot silently add
such changes. The doctrine states:

> A deviation that changes what was ratified — behavior, scope,
> interface, normative text — is an execution failure, not a recordable
> deviation: the dev agent stops, the matter takes `staged → proposed`
> (§3), and the changed plan is re-ratified before work resumes.

Source: [doctrine §3.1, “The execution record”](../doctrine/matters.md#31-the-execution-record).

Review, rulings, and decisions must live in repository files. An
instruction supplied only in a launch prompt would leave part of the
requirements outside that record. The doctrine states:

> The repository is the record. Review, rulings, and decisions live in
> the tree: vetting entries on matters (§6), threads (§9.2), runs (§9.1).

Source: [doctrine §8, “Where discourse lives”](../doctrine/matters.md#8--where-discourse-lives).

The doctrine does not directly specify what belongs in a launch
instruction. The first
consumer follow-through exposed the omission: the framework execution
thread records two checked launch prompts being delivered outside the
file, while their operative text is absent from the repository
([thread R13](../threads/2026-08-26-m0012-execution.md)). One of those
agent-authored handoffs repeated doctrine, supplied an unfiled
containment plan, made execution-sequencing choices, and carried
repository facts that then needed a second out-of-record prompt review.
The prompt had become a parallel specification whose corrections could
not accrete on the matter it purported to govern.

An operator act still has to reach an agent. The defect is not that a
launch instruction exists; it is that the instruction can silently
become the only place substantive scope or execution policy exists.
That defeats exact-text ratification and makes the repository cease to
be the operative channel at the moment execution begins.

The README is another entry point into the repository's process. Its
overview, status, and workflow guidance need a full rewrite against the
operative record. Without an ongoing maintenance obligation, later
matters can leave that guidance stale again. Keeping both entry points
aligned with the authoritative record is part of this matter's scope.

The earlier opening of this matter called the ratified matter the
“execution contract” and cited sections without explaining their rules
or how those rules supported the diagnosis. A reader had to reconstruct
that relationship from another document. Matters need to define ambiguous terms before using them, explain each
rule's bearing on the proposal, and quote the exact source wording
before giving its citation. A paraphrase alone makes the reader leave
the matter to audit whether the rule was restated faithfully.

## Proposed text

Add a `### Launch instructions` subsection to doctrine §8 containing
this policy verbatim:

> Launch instructions are pointers, not shadow specifications. They identify the repository, matter, operator act, and necessary external authority. Scope and execution instructions come from the repository’s ratified record. Any substantive instruction absent from that record is filed or amended and ratified before execution.
>
> Authority resides in ratified text and in the operator’s acts, live or recorded, and nowhere else. A `proposed` matter is a candidate: it may be pointed to — a dependency, a supersession target, a coordination reference — but it is never citable as the basis for a rule, an assumption, or an act. Text that treats a proposed matter as operative is a shadow specification, wherever it lives.

Add the same two paragraphs verbatim to `CLAUDE.md` as standing
rules. The
doctrine is the authority; `CLAUDE.md` makes the rule present at the
agent's first read and continues to distill, never override, per
[m0015](m0015-agent-instructions.md).

Add a `### README maintenance` subsection to doctrine §8 containing
this policy verbatim:

> Every matter must identify its README impact before ratification. During execution of each ratified matter, the executing agent reviews the governed repository's README and updates it wherever the delivered change affects its description, setup, usage, workflow, or status. These updates belong to the same matter and execution branch. Before the matter enters `executed`, its execution record identifies the README changes or explains why none were needed.
>
> The README summarizes and points to the authoritative record; it does not establish independent rules. Ratification alone must not be described as completed implementation. Pending changes, if mentioned, are explicitly identified by their lifecycle state. Listings and rollups remain derived under §12 rather than being maintained as duplicate inventories in the README.

Add the same two README-maintenance paragraphs verbatim to `CLAUDE.md`
as standing rules, subordinate to doctrine.

Rewrite the root `README.md` as part of this matter's execution. Cover
the framework's purpose, repository layout, governing sources, matter
lifecycle, ratification and execution responsibilities, launch
instructions, README maintenance, and available tooling. Verify each
instruction against the operative record and actual tooling. Replace
stale status and workflow prose; link to the derived matter index for
collection state and to historical records for provenance. Any pending
proposal mentioned must remain clearly labeled as pending. The rewrite
must introduce no rule beyond the ratified record and this matter's
ratified amendments.

Add a `### Self-contained matters` subsection to doctrine §4, “Cheap to file, expensive to ratify,” containing
this policy verbatim:

> Each matter must be understandable on its own. When its diagnosis, proposal, constraints, or execution plan relies on an external rule or fact, state the relevant rule or fact explicitly, explain how it supports or constrains this matter, and then cite the source. A section number, document title, link, or shorthand label alone does not supply that explanation. Citations provide provenance and allow verification; they do not replace the reasoning the reader needs in the matter itself.
>
> When referencing doctrine, quote the exact passage relied upon after explaining its relevance, then cite its source section with its exact heading and a link. Include enough surrounding wording to preserve qualifications and exceptions. Clearly separate quotations from restatements and proposed amendments. Do not silently edit quoted wording. Before ratification, verify each quotation against the identified source version and check that it supports the accompanying explanation.
>
> Introduce a terms section near the top of each matter, before substantive use of specialized or ambiguous terms, with named definitions for the terms used below. Use the framework glossary where applicable, quoting its definitions and citing their source; explicitly identify proposed definitions or refinements. Distinguish a matter execution plan from an agent working plan, and specify which text is submitted for ratification. Unqualified “plan” or “contract” must not leave the object of approval ambiguous.
>
> Include the substance needed to assess the matter, without copying entire source documents. Distinguish existing authority from proposed changes, and keep restatements faithful to their sources; a restatement does not acquire independent authority. Before ratification, vetting checks that the matter's reasoning and proposed work can be understood without following its citations, and that each citation supports the explanation preceding it. Incomplete proposals remain cheap to file, but missing explanations must be supplied before ratification.

Add the same four self-contained-matter paragraphs verbatim to
`CLAUDE.md` as standing rules, subordinate to doctrine. Apply this
writing requirement to m0016 during preparation and vetting. The rule
becomes a general obligation only through ratification and execution
of the proposed doctrine amendment.

### Proposed glossary additions

Add the following definitions to the framework glossary proposed by
[m0026](m0026-legibility-standard.md#glossary), once that glossary is
operative. Replace its “Contract” definition with the wording below.
These are proposed normative definitions, not claims that the pending
glossary already governs. Before ratification of m0016, reconcile this
wording with the glossary's accepted text and resolve any conflict.

> **Matter execution plan:** The actions and intended results written in a matter for the executing agent to carry out. Before ratification they are proposed; after ratification their accepted wording constrains execution along with the rest of the ratified requirements. The execution-plan section alone is not the full object of ratification.
>
> **Agent working plan:** An agent's task breakdown or checklist used to organize work. It does not itself authorize changes or replace ratified requirements. If it is to be ratified, it must be explicitly included in the text submitted to the operator.
>
> **Contract:** The requirements in the ratified text against which execution is checked. This term does not name a separate artifact or an agent working plan. Identify the ratified text when using the term; prefer “ratified requirements” where that wording is sufficient.

The README rewrite must introduce the glossary near the top and explain
the terms needed to understand its workflow. The distinction between
matter execution plans and agent working plans must survive any
restatement submitted for ratification.

## Enforcement

- Before acting, an agent resolves the named repository and matter,
  reads the repository's governing instructions and normative
  specification, verifies the matter's state and ratification record,
  and maps the requested operator act to a transition or lifecycle
  action the doctrine permits.
- A filing or vetting launch may introduce information into a
  `proposed` matter. That information becomes operative only after it
  is written into the matter and ratified. It is never execution scope
  merely because it appeared in the launch instruction.
- An agent that finds an act, assumption, or rule resting on a
  `proposed` matter stops and reports: the content enters force only
  through ratification. Coordination references — `depends_on`,
  supersession links, pointers — remain ordinary and carry no
  authority.
- A launch against a ratified or staged matter cannot extend or replace
  its ratified region. Material additional direction takes the normal
  re-open or execution-failure path: before staging, the operator
  returns the matter to `proposed`; during execution, the agent stops,
  records the failure, and returns it to `proposed`. The revised matter execution plan
  must be ratified before work resumes (source wording: “- `ratified → proposed` — the operator re-opens a ratified matter whose plan is found broken before staging. The ratification fields are cleared, their values recorded in the vetting section. - `ratified → staged` — the operator slots it into the pipeline. - `staged → executed` — only through a dev agent the operator launched against the matter. Delegating that trigger to an orchestration agent would be its own future matter, never an inference.” — doctrine §3, “State — mutable,” in [doctrine/matters.md](../doctrine/matters.md), source wording: “A deviation that changes what was ratified — behavior, scope, interface, normative text — is an execution failure, not a recordable deviation: the dev agent stops, the matter takes `staged → proposed` (§3), and the changed plan is re-ratified before work resumes. Entering `executed` requires a final `## Execution` section on the matter: what actually landed (commits, PR), deviations from the ratified plan, date, actor.” — doctrine §3.1, “The execution record,” in [doctrine/matters.md](../doctrine/matters.md)).
- Necessary external authority may be stated in the launch — for
  example permission to push a named matter branch or open a pull
  request. Authority changes what operations the agent may perform; it
  does not change the ratified deliverable.
- The session export preserves human and agent turns verbatim,
  including the launch turn, omits reasoning and tool traffic, and
  applies redaction before publication. This keeps the operator act
  and attempted shadow instructions auditable (source wording: “`threads/` holds verbatim session exports — primary sources, like goldens: human and agent turns verbatim, reasoning and tool traffic omitted, redaction applied before publication.” — doctrine §9.2, “Threads,” in [doctrine/matters.md](../doctrine/matters.md)). The matter, not the thread, remains the source of execution
  scope.
- This rule is judgment-enforced by the agent and operator. A validator
  cannot inspect an unpersisted prompt. Mechanically checkable facts
  belong to deterministic checks, while assessing scope and meaning
  remains agent judgment (source wording: “Anything in this process checkable by deterministic code is checked by deterministic code — schema, transitions, links, cycles, hashes, staleness, derived views (the validator, m0008). Agents are reserved for judgment: whether a diagnosis is correct, whether a plan is good, whether scope is right. Ratification is the operator's alone.” — doctrine §10, “Deterministic wherever possible,” in [doctrine/matters.md](../doctrine/matters.md)). Future orchestration or launch tooling may make the repository,
  matter, state, and pin checks deterministic; that is not introduced
  here.

## What this contradicts

The launch policy contradicts no ratified text. Changes must begin as
matters, subject to the defined bootstrap and retroactive exceptions;
this explains why a prompt cannot create an unfiled change (source wording: “Nothing lands in any governed system that did not begin as a matter, with two defined exceptions: the bootstrap of an installation (§14) and the retroactive path (§11).” — doctrine §1, “What a matter is,” in [doctrine/matters.md](../doctrine/matters.md)). The operator accepts exact text as the requirements for execution, and
material departures require stopping and re-ratification; the policy
applies those constraints to launch instructions (source wording: “- `ratified → proposed` — the operator re-opens a ratified matter whose plan is found broken before staging. The ratification fields are cleared, their values recorded in the vetting section. - `ratified → staged` — the operator slots it into the pipeline. - `staged → executed` — only through a dev agent the operator launched against the matter. Delegating that trigger to an orchestration agent would be its own future matter, never an inference.” — doctrine §3, “State — mutable,” in [doctrine/matters.md](../doctrine/matters.md), source wording: “A deviation that changes what was ratified — behavior, scope, interface, normative text — is an execution failure, not a recordable deviation: the dev agent stops, the matter takes `staged → proposed` (§3), and the changed plan is re-ratified before work resumes. Entering `executed` requires a final `## Execution` section on the matter: what actually landed (commits, PR), deviations from the ratified plan, date, actor.” — doctrine §3.1, “The execution record,” in [doctrine/matters.md](../doctrine/matters.md), source wording: “**Ratification is the operator's act alone, over the exact text.** The operator reads the matter as it stands at a specific commit and states ratification. Where a matter's proposed text is a separate document (m0001 → this specification, which has no frontmatter), the hash is that document's whole file at the same commit.” — doctrine §6, “Vetting and ratification,” in [doctrine/matters.md](../doctrine/matters.md)). Decisions belong in repository records, so operative scope cannot
exist only in a prompt (source wording: “The repository is the record. Review, rulings, and decisions live in the tree: vetting entries on matters (§6), threads (§9.2), runs (§9.1).” — doctrine §8, “Where discourse lives,” in [doctrine/matters.md](../doctrine/matters.md)). The operator may still direct new
substantive work, which must enter the record and be ratified before
execution. The doctrine describes its own unratified text as a
candidate; the authority paragraph extends that distinction explicitly
to every proposed matter (source wording: “This text becomes normative when the operator ratifies it as a whole document (§6).” — introduction to [doctrine/matters.md](../doctrine/matters.md)).

The README policy adds a maintenance obligation that the doctrine does
not currently state. Execution records already
must identify what landed, deviations, date, and actor; this policy adds
the README outcome to that record (source wording: “A deviation that changes what was ratified — behavior, scope, interface, normative text — is an execution failure, not a recordable deviation: the dev agent stops, the matter takes `staged → proposed` (§3), and the changed plan is re-ratified before work resumes. Entering `executed` requires a final `## Execution` section on the matter: what actually landed (commits, PR), deviations from the ratified plan, date, actor.” — doctrine §3.1, “The execution record,” in [doctrine/matters.md](../doctrine/matters.md)). Collection listings
and rollups must be regenerated from their source rather than manually
maintained; the README therefore points to those views (source wording: “**Views are derived.** The flat collection is the only source of truth; every listing, worklist, and rollup is regenerated (`tools/gen-index.py` today, m0008 properly) and never hand-edited.” — doctrine §12, “Storage and format,” in [doctrine/matters.md](../doctrine/matters.md)). The rewrite replaces the existing
README's explanatory prose, not the historical records it cites. Routine
README updates needed to describe a matter's delivered change are part
of that matter; new substantive policy still requires ratified scope.

The pending thread-persistence proposal addresses which session
exchanges persist and by what mechanism
([m0011](m0011-thread-persistence.md)); this matter governs where
execution authority and scope reside even when every launch turn is
perfectly preserved. It also does not select the next matter or launch
agents autonomously: the operator slots a ratified matter into the
pipeline and launches the executing agent (source wording: “- `ratified → proposed` — the operator re-opens a ratified matter whose plan is found broken before staging. The ratification fields are cleared, their values recorded in the vetting section. - `ratified → staged` — the operator slots it into the pipeline. - `staged → executed` — only through a dev agent the operator launched against the matter. Delegating that trigger to an orchestration agent would be its own future matter, never an inference.” — doctrine §3, “State — mutable,” in [doctrine/matters.md](../doctrine/matters.md)).

The self-contained-matter policy adds a writing and vetting requirement.
The pending heading-citation proposal supplies section names but does
not require the relied-on passage itself; this proposal adds exact
quotations and explanations ([m0018](m0018-doctrine-heading-citations.md)).
The pending glossary proposal defines Contract but not Plan; this
proposal adds the two explicit plan definitions and refines Contract
([m0026](m0026-legibility-standard.md#glossary)). Neither pending proposal
is treated as existing authority.
A proposal may already be filed as a single sentence, while its type's
required content must be complete before ratification. This amendment
preserves that low filing threshold and adds explanatory completeness
to the ratification requirements (source wording: “The required sections in §2 gate **ratification**, not filing. A matter may be filed as a single sentence: a defect can be reported before it is understood, and producing the diagnosis is what vetting is for — it may take several rounds. No matter reaches `ratified` without its type's required sections complete.” — doctrine §4, “Cheap to file, expensive to ratify,” in [doctrine/matters.md](../doctrine/matters.md)). It does not transfer
authority from cited sources to a matter's restatements.

## Proposed execution plan

1. Insert the launch and README subsections in doctrine §8, “Where discourse lives,” and the
   self-contained-matter subsection in doctrine §4, “Cheap to file,
   expensive to ratify,” without changing
   the proposed paragraphs' text. Add the proposed glossary definitions
   and replace its Contract definition as specified above.
2. Insert all eight standing-rule paragraphs verbatim in `CLAUDE.md` under its standing
   rules, subordinate to doctrine as that file already declares.
3. Rewrite `README.md` to the scope above. Review its claims and commands
   against the ratified record and actual tooling, distinguish pending
   from delivered changes, and verify that collection listings are
   pointers to derived views rather than duplicate inventories.
4. Regenerate `matters/index.md` and write an append-only verification
   run with claims, environment, commands, expected and observed
   results, verdict, date, and actor (source wording: “`runs/` holds append-only verification records: one file per run, stating the claim(s) tested (with links to the matters they support), the environment (OS, kernel, architecture, toolchain and tool versions), the exact commands, expected versus observed results, the verdict, the date, and the actor.” — doctrine §9.1, “Runs,” in [doctrine/matters.md](../doctrine/matters.md)). Verify each
   standing-rule paragraph occurs once in doctrine and once in
   `CLAUDE.md`, each glossary definition matches its proposed wording, the
   index regenerates byte-identically, repository links resolve, and the
   rewritten README meets the preceding checks. Record the review of
   m0016's self-contained explanations, defined terms, exact quotation
   fidelity, source versions, and citation support.
5. Because doctrine changes, present the amendment commit for the
   operator's m0001 re-ratification. Record the new whole-file pin only
   after that act, on the same execution branch. The pin identifies the
   commit the operator read and hashes the whole doctrine file, because
   that file is m0001's ratified deliverable (source wording: “**Ratification is the operator's act alone, over the exact text.** The operator reads the matter as it stands at a specific commit and states ratification. Where a matter's proposed text is a separate document (m0001 → this specification, which has no frontmatter), the hash is that document's whole file at the same commit.” — doctrine §6, “Vetting and ratification,” in [doctrine/matters.md](../doctrine/matters.md)).
6. Export the human and agent session turns verbatim, including the
   launch turn, excluding reasoning and tool traffic, and applying
   redaction before publication (source wording: “`threads/` holds verbatim session exports — primary sources, like goldens: human and agent turns verbatim, reasoning and tool traffic omitted, redaction applied before publication.” — doctrine §9.2, “Threads,” in [doctrine/matters.md](../doctrine/matters.md)).
7. Append this matter's execution record, including its README changes,
   move it `staged → executed`,
   remove its `branch`, regenerate the index, and put the completed
   branch before the operator for a merge-commit merge.
