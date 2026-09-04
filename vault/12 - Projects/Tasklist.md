# Tasklist

Operational work queue for The Human Manual. [[Build Roadmap]] says *what phases exist*; this file
says *what to do next and how I will know it is done*.

**Roles:** Claude is the producer and the primary consumer of this file. Vin is reviewer and guide.

## How to use this file

- Work top-down within the lowest-numbered open priority band. Do not start a P1 task while a P0
  task is open unless it is explicitly marked `parallel-ok`.
- Update `status` in place as work proceeds. Never delete a task — set it to `done` or `dropped`
  with a one-line reason.
- `GATE` tasks stop the queue: produce the work, then hand it to Vin and wait for sign-off before
  starting anything that depends on it. Everything else proceeds without asking.
- `done-when` is the acceptance test. If every bullet is not literally true, the task is not done.
- Keep `NEXT` accurate — it is how a cold session resumes without re-deriving context.

**Status values:** `todo` · `doing` · `blocked` · `review` (awaiting Vin) · `done` · `dropped`
**Size:** S (single sitting) · M (a few sittings) · L (multi-session)

## NEXT

> **Awaiting review.** T-001 and T-003 are done. T-002 and T-004 (both GATE) are written and sitting
> at `status: drafted` for Vin. T-005 is deliberately held — a style guide must encode what was
> *approved*, not what was proposed. On sign-off: mark both notes `reviewed`, do T-005, then open P1.

---

## P0 — Calibration

Nothing should be produced at volume until "good" is defined once and approved. These tasks exist to
make every later task mechanical.

### T-001 — Define the `domain` vocabulary and backfill all frontmatter
`status: done` · `size: S` · `deps: —` · `parallel-ok`

Every note has an empty `domain:` field, so the [[Publishing Dashboard]] queries group by nothing.

**done-when**
- A controlled vocabulary of domain values is written into [[Content Pipeline]] (one value per
  curriculum layer: reality, life, mind, thinking, society, living-well, practice).
- Every `type: concept` and `type: question` note has a non-empty `domain` matching that vocabulary.
- ~~The Publishing Dashboard's three Dataview queries return correctly grouped rows.~~
  **Not verified** — Dataview cannot be executed from the CLI. The underlying data is present and
  well-formed (37/37 notes populated, vocabulary consistent); the queries need one look inside
  Obsidian. Doing so surfaced a real defect, now tracked as T-017.

### T-002 — Write one concept note to full `reviewed` quality (GATE)
`status: review` · `size: M` · `deps: T-001`

The exemplar that calibrates depth, voice, length, and evidence handling for all 25+ remaining notes.
Proposed subject: **Sunk Cost Fallacy** — well-evidenced, has a real replication story, has genuine
limitations, and is small enough to finish properly.

**done-when**
- Every section of the Concept Template is filled, including *Counterexample*, *What this does NOT
  imply*, and *Limitations and uncertainty*.
- Every empirical claim carries an evidence marker (Established / Well supported / Plausible /
  Contested / Speculative / Unknown) per [[Source Evaluation]].
- It cites at least three real source notes created under T-003.
- `prerequisites`, `related`, and `sources` frontmatter are populated with resolving links.
- Handed to Vin with a short note on the calls I made (length, voice, how hard I leaned on hedging).

### T-003 — Build the source-note workflow on real sources
`status: done` · `size: S` · `deps: —` · `parallel-ok`

The source library is empty; only the template exists. The editorial standard is unenforceable
without it.

**done-when**
- A `08 - Sources/` folder exists with at least 3 real source notes backing T-002. **9 written**,
  every citation checked against journal metadata via web search.
- Each records what it supports, key claims, caveats, and a `quality` rating tied to the evidence
  hierarchy.
- The convention for citing a source from a concept note is documented in [[Content Pipeline]].

### T-004 — Write one question note to full quality (GATE)
`status: review` · `size: S` · `deps: T-002`

Questions are the navigation layer and use a different template; they need their own calibration.
Proposed subject: **How should I make decisions?**

**done-when**
- Short answer, why it is difficult, concepts needed (resolving links), best current explanation,
  alternatives, evidence, practical implications, related questions — all filled.
- It reads as an entry point that routes to concepts, not as a concept note in disguise.
- Handed to Vin for sign-off.

### T-005 — Distil the approved exemplars into a house style guide
`status: blocked` · `size: S` · `deps: T-002, T-004` — blocked on sign-off, by design

Encode what the gates approved so later notes do not drift.

**done-when**
- `00 - Start Here/Style Guide.md` exists covering: target length per section, voice, how to hedge,
  when to mark a claim contested, how examples are chosen, what belongs in a concept vs a question.
- It is written as rules I can check myself against, not as prose advice.
- Linked from the Start Here README.

### T-017 — Fix `importance` sorting in the Publishing Dashboard
`status: todo` · `size: S` · `deps: —` · `parallel-ok`

Found while doing T-001. All three dashboard queries `SORT importance DESC`, but `importance` holds
strings, so DESC sorts alphabetically and puts `medium` above `high` — the dashboard ranks the
backlog exactly wrong.

**done-when**
- Ordering is correct. Either a numeric `importance_rank` is added alongside the label, or the
  queries sort on an explicit expression. Vin picks — this changes frontmatter across 37 notes.

---

## P1 — Make the graph real

The vault currently promises more than it contains: 35 wiki-links resolve to nothing and the
Curriculum names ~35 concepts that appear in no map or file. This band makes the structure honest and
navigable before content volume lands on top of it.

### T-010 — Create the 20 missing concept stubs
`status: todo` · `size: M` · `deps: T-005`

Attention · Causality · Collective action · Creativity · Cultural evolution · Economics ·
Externalities · Free energy principle · Game theory · Hope · Language · Learning · Markets · Memory ·
Motivation · Perception · Public goods · Relationships · Values · Wisdom

**done-when**
- Each exists in the correct layer folder with complete frontmatter and a real one-sentence
  explanation (not a placeholder).
- Each is `status: seed` with `importance` set deliberately, not defaulted.
- No MOC link to a concept resolves to nothing.

### T-011 — Create the 15 missing question stubs
`status: todo` · `size: S` · `deps: T-005`

How can I become more attentive? · How can I learn from my mistakes? · How do incentives change
behavior? · How should I live with uncertainty? · How should I reason when I am uncertain? · How
should I update my beliefs? · What is consciousness? · What should I value? · Why do institutions
matter? · Why do markets work? · Why do organisms compete? · Why do organisms cooperate? · Why do we
have emotions? · Why does complexity emerge? · Why does life adapt?

**done-when**
- Each exists in `01 - Questions/` with frontmatter and a real short answer.
- Every link in [[Questions Index]] resolves.

### T-012 — Reconcile Curriculum ↔ MOCs ↔ files
`status: todo` · `size: M` · `deps: T-010, T-011`

The Curriculum names roughly 35 concepts that reach no MOC and no file — Scientific method, Entropy,
Information, Complexity, Systems and feedback, Natural selection, Mutation, Adaptation, Kin
selection, Sexual selection, Competition, Evolutionary game theory, Base rates, Correlation vs
causation, Confirmation bias, Availability heuristic, Regression to the mean, Expected value, Value
of information, Supply and demand, Social mobility, Network effects, Norms, Property rights,
Autonomy, Contribution, Mastery, Reflection, Habit formation, Behavioral design, Feedback,
Journaling, Deliberate practice, Decision journals, Experiments.

**done-when**
- Every Curriculum concept is either (a) a note, (b) listed in a MOC as deliberately deferred, or
  (c) removed from the Curriculum with a reason.
- The three lists agree. A reconciliation summary is handed to Vin — this is a scope decision he
  should see even though it is not a hard gate.

### T-013 — Add MOCs for Reality and Practice; normalise naming
`status: todo` · `size: S` · `deps: T-010` · `parallel-ok`

Four MOCs exist for seven layers. Reality, Life, and Practice have none, and MOC links use sentence
case (`[[Predictive processing]]`) while files use title case.

**done-when**
- `MOC - Reality`, `MOC - Life`, and `MOC - Practice` exist and cover their layers.
- A single casing convention is chosen, documented in the Style Guide, and applied to every wiki-link
  in the vault.

### T-014 — Wire prerequisites and consequences across all concepts
`status: todo` · `size: M` · `deps: T-010, T-013`

Roadmap Phase 2. This is what turns a folder of notes into a curriculum with a traversal order.

**done-when**
- Every concept note has non-empty `prerequisites` and `related` frontmatter with resolving links.
- Each note's Connections section names at least one prerequisite and one application.
- The dependency graph is acyclic across layers — nothing in Reality depends on Society.

### T-015 — Build question → concept maps
`status: todo` · `size: S` · `deps: T-014`

**done-when**
- Every question note's "Concepts needed" lists the concepts that actually answer it, in reading
  order.
- Every concept note's `question` frontmatter points at a real question note.

### T-016 — Add a link-health check
`status: todo` · `size: S` · `deps: —` · `parallel-ok`

**done-when**
- A script in `tools/` reports dangling wiki-links, notes missing required frontmatter, and status
  distribution.
- It runs from the repo root with no dependencies beyond a shell.
- Current output is clean or its remaining failures are tracked as tasks here.

---

## P2 — Prove the pipeline end to end

One vertical slice carried all the way from concept to published derivative, before scaling. This
surfaces pipeline problems while the cost of fixing them is one slice, not thirty.

### T-020 — Complete one full vertical slice to `reviewed`
`status: todo` · `size: L` · `deps: T-014`

One question plus every concept it needs. Proposed: **How should I make decisions?** → Decision
theory, Expected value, Probability, Bayesian reasoning, Sunk cost fallacy.

**done-when**
- Every note in the slice is `status: reviewed` with full sections, sources, and evidence markers.
- A reader can start at the question and follow prerequisites through to an answer without hitting a
  seed note.

### T-021 — Produce the first derivative content set (GATE)
`status: todo` · `size: M` · `deps: T-020`

Tests the core claim of [[Content Pipeline]] — that derivatives simplify without distorting.

**done-when**
- One YouTube script and one Instagram carousel exist as `type: content` notes linked to their
  concept.
- Each is checked against the source concept for distortion, and the check is recorded.
- The concept's channel booleans are updated.
- Handed to Vin — voice on social is a brand decision, not mine to settle.

### T-022 — Write the editorial review checklist
`status: todo` · `size: S` · `deps: T-021`

**done-when**
- A checklist exists that gates `drafted → reviewed`, covering evidence markers, falsifiability,
  misconceptions, effect sizes, and generalisation.
- It was applied retroactively to the T-020 slice and caught at least one real defect.

### T-023 — Bring all remaining concepts to `drafted`
`status: todo` · `size: L` · `deps: T-022`

**done-when**
- No `type: concept` note is still `status: seed`.
- Work proceeded in `importance` order, with progress reported per batch rather than in one dump.

---

## P3 — Channels and products

Roadmap Phases 3–6. Deliberately unelaborated: these depend on decisions that should be made with a
real corpus in hand, not now. Each becomes its own P0/P1 band when promoted.

- **T-030** — Website publishing path (static export from the vault). `deps: T-023`
- **T-031** — Newsletter workflow and cadence. `deps: T-022`
- **T-032** — Book narrative sequence: order the corpus into chapters, identify what only exists for
  the book (exercises, diagrams, bibliography). `deps: T-023`
- **T-033** — AI tutor: chunking, retrieval, citation support, Socratic and learning-path modes.
  `deps: T-023`
- **T-034** — Interactive Manual: concept explorer, learning paths, decision tools, simulations.
  `deps: T-030`

---

## Open questions for Vin

Answers change the work; I will proceed on the stated default until told otherwise.

1. **Depth-first or breadth-first?** Default: depth — finish one vertical slice properly (T-020)
   before drafting everything shallowly. The alternative gets a complete-looking vault faster but
   risks 40 notes written to the wrong standard.
2. **How opinionated should the Manual be?** The editorial standard says evidence over authority, but
   Living Well cannot be written without taking positions. Default: argue positions explicitly and
   mark them as positions, rather than hiding them behind hedging.
3. **Scope of the Curriculum.** T-012 will likely propose cutting concepts rather than writing 35 more
   notes. Default: cut aggressively, keep the spine.
4. **Audience.** Default assumption: a curious generalist who can handle a graph and an equation but
   is not an academic. This drives length and how much I define.

## Working agreements

- I proceed without asking on everything except `GATE` tasks and anything that deletes or restructures
  existing notes.
- I will not mark a note `reviewed` on my own judgment once T-022 exists — that checklist is the gate.
- When I hit a genuine fork mid-task, I finish everything that does not depend on it and surface the
  fork here under Open questions rather than stalling.
- Status in this file is the truth. If it says `done`, the `done-when` bullets were checked.
