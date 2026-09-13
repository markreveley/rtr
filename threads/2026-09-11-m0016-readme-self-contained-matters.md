# Thread — m0016 README maintenance, self-contained matters, quotations, and terminology

Mechanically exported from the saved Codex session on operator direction.
This exchange revises [m0016](../matters/m0016-launch-instructions-policy.md).

**Boundary.** From the initial README question through “export thread
verbatim” / “then commit,” inclusive. Later messages, including the
`:tabnew` exchange and this export's completion report, are outside this
frozen export.

**Method.** User messages and assistant commentary and final answers are
copied from `response_item` message records in source order, retaining
each message separately with its recorded timestamp and phase. System
and developer instructions, injected environment context, reasoning,
tool calls, tool results, and duplicate event records are omitted.

**Redaction.** None. Message text, including original local file links,
is preserved unchanged. Those links are historical transcript text.

**Interpretation.** Statements remain as spoken, including errors and
later-corrected wording. Export does not ratify the proposed changes.

---

## ▸ Mark — human message, 2026-09-10T22:38:36.392Z

does rewriting the readme (which is clearly out of date) require a matter?

---

## ▸ Codex — agent commentary, 2026-09-10T22:38:38.988Z

I’ll check the repository guidance for when a matter is required.

---

## ▸ Codex — agent final answer, 2026-09-10T22:38:56.602Z

Yes—under the current [matter doctrine](/Users/mark/dev/repos/repos_public/rtr/doctrine/matters.md:48), every change to a governed system requires a matter; there’s no documentation exemption.

Updating an outdated README fits **`fix`**, which explicitly covers “defective behavior or text.” It needs a diagnosis and proposed fix. If the rewrite changes normative rules, that portion would instead be **`spec`**.

For a straightforward refresh, the matter can be brief.

---

## ▸ Mark — human message, 2026-09-10T22:42:00.879Z

add a rewrite of the readme to m0016, and it would seem that this could be a policy - readme gets updated with each ratified matter

---

## ▸ Codex — agent commentary, 2026-09-10T22:42:03.435Z

I’ll read m0016 and add the README rewrite, along with a proposed policy to keep it current as ratified matters are executed.

---

## ▸ Codex — agent commentary, 2026-09-10T22:42:16.155Z

The policy will require a README review for every ratified matter, with relevant updates included in execution and a recorded reason when no change is needed. That keeps the README tied to delivered behavior. I’m also adding the full rewrite to m0016’s scope.

---

## ▸ Codex — agent final answer, 2026-09-10T22:42:57.321Z

Added to [m0016](/Users/mark/dev/repos/repos_public/rtr/matters/m0016-launch-instructions-policy.md):

- A full README rewrite.
- Proposed policy requiring README review with every ratified matter’s execution, relevant updates, and a recorded reason if none are needed.
- Matching execution and verification steps.

Regenerated the index; diff checks passed. The policy remains proposed with m0016.

---

## ▸ Mark — human message, 2026-09-10T22:48:37.539Z

with moo16, see the following:

The doctrine makes the ratified matter the execution contract (§3,
§6) and the repository the record (§8), but does not say directly

i think each matter should be self contained. i checked section 3 in doctrine and could not figure out how it relates. instead of pointing to doctrine sections, you should instead say exactly what the relationship is explicitly and self contained and THEN reference each section

this should itself be a doctrinal change to be added to m0016

---

## ▸ Codex — agent commentary, 2026-09-10T22:48:40.856Z

I’ll add a proposed doctrine rule requiring matters to explain each relied-on rule and its relevance before citing the source, and revise m0016 to follow it.

---

## ▸ Codex — agent final answer, 2026-09-10T22:49:53.966Z

Updated [m0016](/Users/mark/dev/repos/repos_public/rtr/matters/m0016-launch-instructions-policy.md) with a proposed doctrinal requirement: **state the relevant rule or fact, explain its relationship to the matter, then cite the source.** Readers should understand the reasoning without following citations.

Rewrote m0016’s opening and other references accordingly, added a vetting check, and preserved the README work. Regenerated the index; diff checks passed.

---

## ▸ Mark — human message, 2026-09-10T22:52:53.397Z

that accepted plan becomes the contract for execution

what does this mean, and why is it followed with sectional references to doctrine?

---

## ▸ Codex — agent final answer, 2026-09-10T22:52:59.127Z

It means: **the agent must carry out the plan the operator approved. If the work requires changing its scope, behavior, interface, or normative text, the agent must stop and obtain approval of the revised plan.**

“Contract for execution” is shorthand that obscures those concrete obligations. I should have written them directly.

The section references were intended to show where those obligations come from, after explaining them. But I attached them to the vague phrase, so you still had to consult the doctrine to understand it. That repeats the problem you asked me to fix.

---

## ▸ Mark — human message, 2026-09-10T22:57:35.407Z

i think that if you are going to reference doctrine.md, you should quote exactly the verbiage that you are referencing. this aids in auditing and is more efficient for traceability
regarding the statement, my objection was that plan and contract are potentially underspecified. obviously the glossary is meant to account for this - which may mean it needs to be introduced at the top and the terms listed below
plan is overloaded in agentic terms, requiring specification for proper restatement/ratification

---

## ▸ Codex — agent commentary, 2026-09-10T22:57:39.013Z

I’ll revise m0016 to require exact doctrine quotations alongside explanations and citations. I’ll also check the glossary proposal and make the distinction between a matter’s proposed execution plan and an agent’s working plan explicit near the top.

---

## ▸ Codex — agent commentary, 2026-09-10T22:57:58.771Z

m0026 proposes a glossary with “Contract,” but no definition of “Plan.” I’ll add explicit definitions to m0016 and proposed glossary additions, distinguishing the text the operator ratifies from an agent’s working checklist. The quotation rule will also require enough source text to preserve qualifications and exceptions.

---

## ▸ Codex — agent final answer, 2026-09-11T00:34:54.680Z

Updated [m0016](/Users/mark/dev/repos/repos_public/rtr/matters/m0016-launch-instructions-policy.md) to require exact doctrine quotations with explanations and source citations.

Added definitions near the top distinguishing:

- **Matter execution plan:** proposed actions and results included in the matter.
- **Agent working plan:** the agent’s organizational checklist.
- **Contract:** the ratified requirements, covering more than the execution-plan section alone.

Added corresponding glossary amendments and a dependency on m0026. Verified the opening quotations against doctrine and regenerated the index; diff checks passed.

---

## ▸ Mark — human message, 2026-09-11T17:32:53.995Z

export thread verbatim
then commit

