# The Human Manual

**A Science-informed, Rigorously Designed Approach for Thinking and Living**

An evidence- and reason-first curriculum for understanding reality, understanding ourselves,
thinking clearly, navigating society, and living a meaningful life.

This repository holds the project's source of truth: an [Obsidian](https://obsidian.md) vault in
[`vault/`](vault). Open that folder as a vault, or read the Markdown directly — every note is plain
text.

## What this is

The project is built as a **knowledge system first and a book second**. Each concept is written once
as a canonical note that stands alone, links to its prerequisites and consequences, and is reusable
across every output channel:

```text
Concept note
  ├── Website
  ├── Book
  ├── YouTube
  ├── Instagram
  ├── Newsletter
  └── Chatbot / AI tutor
```

Derivative content is expected to **simplify the explanation, not distort the underlying idea**.

## The spine

The curriculum runs in one direction, each layer resting on the one before it:

```text
REALITY → LIFE → MIND → THINKING → SOCIETY → LIVING WELL → PRACTICE
```

| Layer | Question it answers | Territory |
|---|---|---|
| Reality | What is the world like? | Physics, causality, information, probability, complexity, emergence |
| Life | Why are living systems different? | Evolution, selection, adaptation, cooperation, competition |
| Mind | What kind of creature is a human? | Predictive processing, active inference, perception, emotion, consciousness |
| Thinking | How can we reason better? | Logic, epistemology, Bayesian reasoning, biases, decision theory, game theory |
| Society | What happens when humans interact? | Markets, incentives, institutions, inequality, norms, collective action |
| Living Well | What should we do with our lives? | Values, ethics, meaning, purpose, flourishing, wisdom |
| Practice | How do we actually live it? | Mindfulness, reflection, habits, decision journals, deliberate practice |

Cross-cutting principles recur at every layer: evolution, feedback loops, incentives, tradeoffs,
adaptation, information, uncertainty, cooperation and competition, emergence, agency, constraints,
selection effects, path dependence.

**The key idea:** the Manual should not merely tell people *what to believe*. It should teach them
*how to investigate, reason, decide, and revise*.

## Vault layout

```text
vault/
  00 - Start Here/            Orientation: README, Master Map, Curriculum, Questions Index,
                              Content Pipeline, Source Evaluation, Publishing Dashboard
  01 - Questions/             The human-facing navigation layer — discovery by question, not discipline
  02 - Foundations/           Physics & Reality · Life & Evolution · Complexity & Emergence
  03 - Mind & Human Nature/   Predictive processing, active inference, emotion, consciousness
  04 - Thinking & Rationality/ Logic & Epistemology · Probability & Bayesian Reasoning ·
                              Cognitive Biases · Decision Making · Game Theory
  05 - Society & Civilization/ Economics · Institutions
  06 - Living Well/           Meaning & Purpose · Values & Ethics
  07 - Practice/              Mindfulness & Reflection
  10 - Maps of Content/       MOCs for Mind, Thinking Tools, Society, Living Well
  12 - Projects/              Build Roadmap
  99 - Templates/             Concept, Question, Source, YouTube, Instagram, Decision Journal
```

Start with [`vault/00 - Start Here/README.md`](vault/00%20-%20Start%20Here/README.md), then the
[Master Map](vault/00%20-%20Start%20Here/The%20Human%20Manual%20-%20Master%20Map.md) and
[Curriculum](vault/00%20-%20Start%20Here/Curriculum.md).

## How a note is structured

The **Concept Note** is the canonical artifact. Every one follows
[`99 - Templates/Concept Template.md`](vault/99%20-%20Templates/Concept%20Template.md): a
one-sentence explanation, why it matters, the idea, mechanism, example, counterexample, common
misconceptions, what it does *not* imply, evidence, limitations and uncertainty, connections
(prerequisites / related / applications), the human question it answers, and drafted content for
each channel.

Frontmatter carries the machine-readable state:

```yaml
type: concept        # concept | question | source | content | practice
status: seed         # seed → researching → drafted → reviewed → published → needs-update → archived
domain:
question:            # the human question this concept serves
importance: high
confidence: provisional
prerequisites:
related:
sources:
youtube: false       # per-channel publishing flags
instagram: false
newsletter: false
website: false
book: false
chatbot: false
```

The per-channel booleans drive the
[Publishing Dashboard](vault/00%20-%20Start%20Here/Publishing%20Dashboard.md), which uses Dataview
queries to surface concepts by status and to find concepts still missing YouTube or Instagram
treatments. Dataview is optional — without it the folders, links, graph view, and backlinks still
work.

## Content workflow

1. Create or discover a concept
2. Write the concept note
3. Add sources
4. Connect prerequisites and consequences
5. Add examples
6. Check for misconceptions
7. Create derivative content
8. Publish
9. Record feedback
10. Revise the canonical note

See [Content Pipeline](vault/00%20-%20Start%20Here/Content%20Pipeline.md).

## Editorial standard

Prefer:

- Evidence over authority
- Reason over rhetoric
- Explicit uncertainty over false certainty
- Mechanisms over slogans
- Examples over abstraction
- Steelmanning over caricature
- "I don't know" when warranted

Avoid presenting philosophical or scientific claims as established fact merely because they are
interesting.

Every important claim gets interrogated — what exactly is claimed, what supports it, how strong is
the evidence, what would falsify it, are there competing explanations, is it causal or
correlational, how large is the effect, does it generalize, what uncertainty remains — and is then
marked **Established**, **Well supported**, **Plausible**, **Contested**, **Speculative**, or
**Unknown**. See [Source Evaluation](vault/00%20-%20Start%20Here/Source%20Evaluation.md), which also
sets out the evidence hierarchy from primary research down to anecdote.

## Current state

The scaffolding is complete; the writing has barely begun.

- 25 concept notes and 12 question notes exist. **All are `status: seed`** — frontmatter and a
  one-sentence explanation, with the remaining sections empty.
- The Questions Index and the MOCs deliberately link ahead to notes that do not exist yet (Causality,
  Entropy, Attention, Memory, Markets, Public goods, Wisdom, and others). These unresolved links are
  the backlog, not errors.
- The source library is empty — only the source template exists.
- Domain, prerequisites, related, and sources fields are largely unfilled.

Per the [Build Roadmap](vault/12%20-%20Projects/Build%20Roadmap.md):

| Phase | Status |
|---|---|
| 1 — Foundation (architecture, templates, curriculum) | mostly done; source library and foundational concepts outstanding |
| 2 — Knowledge graph (prerequisites, "leads to", MOCs, question maps) | not started |
| 3 — Content engine (YouTube, Instagram, newsletter, website, review, analytics) | not started |
| 4 — Book (narrative sequence, chapters, exercises, diagrams, bibliography, export) | not started |
| 5 — AI tutor (chunking, retrieval, citations, Socratic and learning-path modes) | not started |
| 6 — Interactive Manual (concept explorer, learning paths, decision tools, simulations, quizzes) | not started |

## Contributing to the vault

- New concept, question, or source notes start from the matching file in `99 - Templates/`.
- File them under the layer folder they belong to, and add the wiki-link to the relevant MOC and to
  the Questions Index.
- Advance `status` only as the note earns it; leave sections empty rather than filling them with
  filler.
- Record uncertainty explicitly — an empty "Limitations and uncertainty" section on a `reviewed` note
  is a defect.
