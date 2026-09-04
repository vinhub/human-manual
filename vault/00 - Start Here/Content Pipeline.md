# Content Pipeline

The canonical artifact is the **Concept Note**. Everything else is a derivative.

```text
Concept
  ├── Website
  ├── Book
  ├── YouTube
  ├── Instagram
  ├── Newsletter
  └── Chatbot
```

## Status values

Use these in frontmatter:

- seed
- researching
- drafted
- reviewed
- published
- needs-update
- archived

## Content workflow

1. Create or discover a concept.
2. Write the concept note.
3. Add sources.
4. Connect prerequisites and consequences.
5. Add examples.
6. Check for misconceptions.
7. Create derivative content.
8. Publish.
9. Record feedback.
10. Revise the canonical note.

## Domain vocabulary

Every `type: concept` and `type: question` note carries exactly one `domain`, matching its layer in
the [[The Human Manual - Master Map|Master Map]] spine:

`reality` · `life` · `mind` · `thinking` · `society` · `living-well` · `practice`

Two placements are deliberate and worth knowing: **Probability** is filed under `reality` (the
Curriculum places it in Part I, though it is also a thinking tool), and **How can we know what is
true?** is filed under `reality` because the [[Questions Index]] groups it there, though it is
epistemology. Templates leave `domain` empty.

## Citing a source

Source notes live in `08 - Sources/`, named `Author Year - Short Title`.

- A concept note lists its sources as wiki-links in the `sources:` frontmatter list, and links them
  inline at the specific claim they support — not in a bibliography at the bottom.
- Every empirical claim in an Evidence section carries a marking from [[Source Evaluation]]
  (Established / Well supported / Plausible / Contested / Speculative / Unknown).
- Source notes carry a `verified:` field recording **what was actually checked** — citation only,
  abstract, or full text. Do not let an unread paper masquerade as a read one.
- A source at level 5–7 of the evidence hierarchy (expert explanation, popular summary, anecdote) may
  be used as a placeholder, but must say so in its caveats and name the primary work that should
  replace it.

## Important rule

Social content should **simplify the explanation, not distort the underlying idea**.
