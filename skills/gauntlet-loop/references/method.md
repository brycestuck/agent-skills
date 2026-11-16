# Gauntlet Loop Method

## Source-Derived Core

Matt Shumer's method is a lead-agent workflow:

1. Give the agent an ambitious goal rather than prescribing the implementation.
2. Give it a real example or measurable standard it can inspect.
3. Let the lead agent decide how to split the goal into parts that can be improved separately.
4. Give each part to a builder and a separate critic with fresh context.
5. Make the critic inspect the real output and compare it directly with the standard.
6. When the work loses, identify the biggest remaining gap and send it back for another round.
7. Continue until the result reaches the bar, the user stops, or further improvement is not worth the cost.
8. After parallel work, use a fresh whole-result review to smooth conflicts and test the complete workflow.

The method depends more on the loop and the quality bar than on phrases such as "utterly perfect."

## What Makes a Good Goal

A useful goal describes what should become true without replacing the agent's judgment about how to get there.

Weak:

> Build a dashboard.

Stronger:

> Build a dashboard the client can use in the Monday meeting to understand what changed, see where the problem is, and decide what to do next.

The skill should strengthen a weak goal using current context and, when needed, one useful question.

## What Makes a Good Benchmark

A benchmark must be something the critic can inspect:

- a real product or category leader;
- a visual reference or reference set;
- a test suite or performance target;
- an existing workflow that already works well;
- a source-quality and reproducibility standard;
- a known decision or operating outcome;
- a holdout example the builders did not optimize against.

Use more than visual similarity when the result also needs to function. A reference can set the quality direction while tests and real user flows protect correctness.

## Why the Critic Must Be Separate

Builders know why they made their choices and can explain away weaknesses. A fresh critic should see the goal, standard, rules, and actual work without receiving the builder's defense.

The critic should judge evidence, not effort.

Blind A/B is strongest when:

- the two options can be shown without identifying which is the reference;
- order can be randomized;
- the critic is not told which result the agent made;
- the comparison can be repeated by another independent critic when the decision is close.

When blind A/B is impossible, preserve independence by withholding builder history and requiring a direct comparison against the same standard.

## Preventing False Wins

Gauntlet Loops can over-reward polish, similarity, or whatever is easiest to score. Protect against that with:

- a separate validity critic;
- real tests and user flows;
- negative constraints that cannot be traded away;
- holdout examples;
- source and calculation checks;
- a complete-result review after the parts are combined;
- human review for judgment-heavy or consequential work.

The benchmark is a compass, not permission to copy protected work or ignore the user's actual needs.

## Suitable Problems

Use the Gauntlet Loop when the goal is ambitious, inspectable, and capable of meaningful iteration:

- software and product builds;
- visual design and presentations;
- research and analysis;
- writing with clear quality references;
- operating systems and workflows;
- strategic decisions with explicit evidence, constraints, and outcomes.

Do not use it for:

- trivial tasks;
- questions that need one direct factual answer;
- work with no inspectable output or meaningful standard;
- tasks where more agents would add ceremony without improving the result;
- unsafe or unauthorized activity.

## Additions in This Adaptation

These safeguards extend the original method for real projects with real constraints:

- Goal clarity before fan-out.
- One useful coaching question instead of an intake form.
- A validity critic alongside the quality critic.
- Explicit authority and external-action boundaries.
- A real end-to-end test after the parts are combined.
- Clear depth and stop conditions.
- A final handoff that separates drafted, built, tested, published, sent, and verified live.
