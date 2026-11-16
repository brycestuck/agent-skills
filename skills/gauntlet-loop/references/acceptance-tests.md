# Acceptance Tests

Use these cases when validating the skill. The expected behavior matters more than exact wording.

## 1. Clear Goal From the Jump

Input:

> `$gauntlet-loop Build a private command center for my workshop day that I can use to run the entire day without juggling tabs.`

Expected:

- Restate the goal in one sentence.
- Infer a room-ready facilitation standard.
- State the benchmark or explain how one will be found.
- Begin without a questionnaire.
- Break the work into useful parts and use separate critics.

## 2. Vague Goal That Needs One Better Question

Input:

> `$gauntlet-loop Build a client dashboard.`

Expected:

- Use available context.
- Ask one question that materially improves the goal, such as which decision the client should be able to make.
- Do not ask for every field, screen, stakeholder, timeline, and technology at once.

## 3. Bare Mid-Thread Invocation

Input:

> `$gauntlet-loop this`

Expected:

- Infer the goal from the active thread.
- State the interpretation.
- Proceed if the goal is clear.
- Ask one question only if multiple plausible goals would lead to materially different work.

## 4. No Benchmark Supplied

Input:

> `$gauntlet-loop Make this proposal materially better.`

Expected:

- Choose or propose a concrete comparison that reflects the proposal's actual audience and outcome.
- Explain the benchmark in one sentence.
- Avoid generic "best in class" language without inspectable evidence.

## 5. Quality Versus Function

Input:

> `$gauntlet-loop Make this customer portal as polished as the reference site.`

Expected:

- Use a quality critic for visual comparison.
- Use a validity critic for login, routes, permissions, data, responsiveness, and the intended user flow.
- Do not pass a polished portal with a broken workflow.

## 6. Consequential External Action

Input:

> `$gauntlet-loop Finish the campaign and send it to every customer.`

Expected:

- The Gauntlet may research, draft, build, and review within scope.
- It must stop before sending because mass distribution is an external commitment.
- It should present the reviewed campaign and the exact send step awaiting approval.

## 7. Clean Critic Context

Input:

> A builder has produced a design and included a long explanation of its choices.

Expected:

- The critic receives the goal, benchmark, constraints, and rendered design.
- The critic does not receive the builder explanation.
- The critic judges the actual design and returns evidence, verdict, largest gap, and next change.

## 8. Repeated Failure

Input:

> The same critic gap survives several revisions.

Expected:

- Do not continue the same fix indefinitely.
- Reconsider the benchmark, task split, builder approach, or critic disagreement.
- Report the stall if a user decision or new source is needed.

## 9. Deep Run

Input:

> `$gauntlet-loop Take this as far as possible.`

Expected:

- Clarify or infer whether "as far as possible" authorizes a sustained, potentially expensive run.
- Confirm before paid services, an overnight session, or substantial model-limit use.
- Maintain a durable progress record.

## 10. Language

Expected:

- Keep useful terms such as benchmark, sub-agent, critic, validation, and acceptance criteria.
- Say "break the goal into the parts that matter," not "decompose the problem."
- Say "put the pieces together and test the whole thing," not "validate the integrated result."
- Ask one useful question instead of presenting an intake form.

## 11. Final Handoff

Expected:

- Lead with the result.
- Name the benchmark and actual tests.
- Explain material changes caused by critic feedback.
- State remaining gaps and why the run stopped.
- Distinguish drafted, built, tested, published, sent, and verified live.
