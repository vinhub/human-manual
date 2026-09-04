---
type: question
status: drafted
domain: thinking
importance: high
concepts:
  - "[[Probability]]"
  - "[[Bayesian Reasoning]]"
  - "[[Decision Theory]]"
  - "[[Cognitive Biases]]"
  - "[[Sunk Cost Fallacy]]"
  - "[[Prisoner's Dilemma]]"
---

# How should I make decisions?

## Short answer

Separate the three questions you are actually asking — *what do I want*, *what will happen*, and
*what should I therefore choose* — because they have different methods and conflating them is what
makes decisions feel impossible.

Then: compute expected value where you can, use robust rules where you cannot, and refuse to bet
anything you cannot afford to lose regardless of how good the odds look. Most of the available
improvement is not in better calculation. It is in **process** — writing down what you predict and
what would change your mind, then actually looking back.

## Why this is difficult

- **Three problems wear one costume.** Values, prediction, and choice get bundled into "what should I
  do?" No amount of analysis resolves a values question, and no amount of soul-searching resolves a
  prediction question.
- **Good decisions can have bad outcomes.** Under uncertainty, outcome quality is a noisy signal of
  decision quality. Judging your process by its results — sometimes called *resulting* — teaches you
  the wrong lesson roughly as often as the right one.
- **You usually don't know the probabilities.** Textbook decision theory assumes you can put numbers
  on outcomes. Most real decisions offer no such numbers, and inventing them can produce false
  precision rather than clarity.
- **The evaluating machinery is itself biased.** You are running the assessment on the hardware that
  produces [[Sunk Cost Fallacy]] and the rest of [[Cognitive Biases]].
- **Feedback is slow and confounded.** The decisions that matter most resolve over years, once, with
  no control condition. This is the worst possible environment for learning from experience.

## Concepts needed

In reading order:

1. [[Probability]] — the language for saying how sure you are
2. [[Bayesian Reasoning]] — how belief should move when evidence arrives
3. [[Decision Theory]] — combining belief with what you value to pick an action
4. [[Cognitive Biases]] — the systematic ways this goes wrong
5. [[Sunk Cost Fallacy]] — the most common single failure, worked in detail
6. [[Prisoner's Dilemma]] — what changes when the other party is also deciding

For the *what do I want* half of the question, see [[Ethics]] and [[Flourishing]].

## Best current explanation

**Expected value is the normative core.** Weight each outcome by how good it is and how likely it is;
prefer the option with the best total. Everything else is an amendment for the fact that you are not
a calculator with perfect information.

Three amendments do most of the practical work:

**Avoid ruin first.** Expected value is indifferent between a steady gain and a coin-flip with the
same average. Your life is not indifferent, because some losses end the game and you do not get to
keep playing the average. Rule out the absorbing outcomes before optimising anything else.

**Prefer robust to optimal.** An option that is fine across many possible futures usually beats one
that is excellent if your probability estimate is right. Your estimate is usually not right.

**Buy information when it is cheap relative to the stake.** Many agonising decisions are really
requests for a cheap test that nobody ran. Before choosing, ask what observation would change the
answer and what it would cost to obtain.

## Alternative explanations

There is a real, unsettled dispute here, and it is worth knowing that the field has not resolved it.

- **Expected utility theory** — the classical normative standard. Coherent, but demands probabilities
  and a utility function you rarely have.
- **Bounded rationality and satisficing (Simon)** — real agents have limited time and computation, so
  the right target is *good enough*, not optimal. Optimising is itself a cost.
- **Ecological rationality and fast-and-frugal heuristics (Gigerenzer)** — simple rules are not
  defective approximations of the correct calculation; in noisy, low-information environments they
  can *outperform* complex models, because complex models fit noise. This directly contests the
  heuristics-and-biases framing that treats deviation from expected utility as error.
- **Robust and adversarial approaches** — under deep uncertainty, minimise worst-case regret rather
  than maximise expected value.
- **Character-based** — ask what kind of person you intend to be and decide as they would. Sidesteps
  the calculation entirely, and is more defensible than it sounds for decisions that recur.

The heuristics-and-biases and ecological-rationality programmes disagree about whether a heuristic is
a bug or a feature. **This is genuinely contested**, and any source presenting either as settled is
overselling.

## Evidence

Question notes route; the sourced detail lives in the concept notes. Marked per
[[Source Evaluation]].

- **Simple formal rules match or beat expert intuitive judgement in predicting human behaviour** —
  *Well supported.* Mechanical prediction averaged ~10% more accurate than clinical judgement and was
  substantially better in 33–47% of studies, versus 6–16% the other way, holding across judgement
  tasks and expertise levels ([[Grove et al 2000 - Clinical versus Mechanical Prediction]]).
- **Forecasting accuracy is measurable and trainable** — *Plausible, pending primary sources.*
  Supported by the Good Judgment Project, but currently cited here through a popular summary
  ([[Tetlock & Gardner 2015 - Superforecasting]]); the primary papers must replace it before any
  number is published.
- **People systematically violate expected-value reasoning in predictable directions** —
  *Well supported.* Worked in detail at [[Sunk Cost Fallacy]].
- **Structured process (written predictions, explicit falsifiers, outcome review) improves individual
  decision quality** — *Plausible.* This is the project's operating assumption and the basis of the
  Decision Journal template. It is weaker evidentially than the confidence with which it is usually
  asserted, and it needs its own sources.

## Practical implications

1. **Name which question you are on.** Values, prediction, or choice. Answer them separately.
2. **Write the decision down before you make it** — the options, what you expect to happen, your
   rough confidence, and *what would tell you that you were wrong*. Use the Decision Journal template.
3. **Set the review date at the same time.** A prediction with no scheduled look-back teaches nothing.
4. **Check for ruin before optimising.** Can any branch end the game?
5. **Ask what would change your mind.** If nothing would, you are defending, not deciding.
6. **Strike out what you have already spent and re-argue it.** ([[Sunk Cost Fallacy]])
7. **Judge the process, not the outcome.** A good decision that turned out badly is still a good
   decision, and this is the hardest one to actually do.

## Related questions

- [[Why do I make predictable reasoning errors?]]
- [[How can we know what is true?]]
- [[When should I cooperate?]]
- [[What should I value?]] — the values half of this question
- [[How do I change my behavior?]] — deciding is not doing
