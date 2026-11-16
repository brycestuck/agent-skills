---
name: gauntlet-loop
description: Run an ambitious goal through a multi-agent build, critique, and improvement loop with concrete standards. Use only when explicitly invoked because it can use substantial capacity.
disable-model-invocation: true
---

# Gauntlet Loop

An independent adaptation of Matt Shumer's Gauntlet Loop method. See `references/source-notes.md` for the original sources.

## Purpose

Turn an ambitious goal into work that keeps getting challenged and improved instead of stopping at the first plausible result.

Stay close to the original Gauntlet Loop method:

1. Get clear on the goal.
2. Find something real that shows what great looks like.
3. Break the goal into the parts that matter.
4. Give each important part to a specialist sub-agent.
5. Have a separate critic judge the actual work without hearing the builder's explanation.
6. Fix the biggest remaining gap and run it through the critic again.
7. Put the pieces together and test the whole thing.

Read `references/method.md` before running the skill. Read `references/platforms.md` before spawning sub-agents. Use `references/acceptance-tests.md` when validating or updating this skill.

## Invocation

This is an explicit-use skill. Valid invocations include:

- `$gauntlet-loop Build a private command center for my workshop day.`
- `/gauntlet-loop Make this learner flow genuinely production-ready.`
- `Run the current project through a Gauntlet Loop.`
- `Gauntlet this.`

Explicit invocation authorizes native sub-agent delegation only within the user's stated goal and existing permissions. It does not authorize publishing, sending, deploying, spending money, changing credentials, sharing protected data, or destructive actions.

## Start With the Goal

Do not fan out work until the goal is clear enough to guide the critics.

The user does not have to write a formal goal statement:

- If the invocation contains a clear goal, restate it in one sentence and proceed.
- If the user invokes the skill mid-thread, infer the goal from the current conversation and state the interpretation.
- If there are multiple materially different goals, ask one question.
- If one answer would make a vague goal substantially better, ask that one useful question.
- Do not give the user an intake form or make them supply the mechanics from the original prompt.

Use this opening pattern when helpful:

> Here's the goal I'm working toward: [goal].
>
> I'll break it into the parts that matter, give each part to a specialist sub-agent, and have a separate critic compare the work against [benchmark]. Once the individual pieces are strong, I'll put everything together and test the whole result in the real workflow.
>
> One question that would help me aim this correctly: [question]

If no question is needed, say what standard will be used and begin.

## Choose a Real Standard

Find a concrete bar the agents can inspect. Prefer, in order:

1. A real reference the user supplied.
2. A live product, document, workflow, or result that represents the target quality.
3. Objective tests, measurements, source requirements, or operating outcomes.
4. A small bundle of references that captures both quality and function.

Do not use "make it amazing," "production-ready," or the builder's confidence as the standard.

If the user did not provide a benchmark, choose or propose one that plays the same role that real Call of Duty played in the original Gauntlet prompt. Explain the choice in one sentence. Ask before using a benchmark only when the choice would materially change the direction, commercial posture, or result.

The benchmark can be aspirational. Its job is to keep the agents from stopping when the work is merely good for AI.

## Run the Gauntlet

### 1. Break the goal into the parts that matter

The lead agent decides which parts can be improved and judged separately. Do not force a standard checklist onto every problem.

Good parts are:

- important to the final outcome;
- specific enough for one specialist to own;
- testable or reviewable on their own;
- independent enough to run in parallel when useful.

Keep tightly connected work together. Do not split the task merely to create more agents.

### 2. Give each part to a fresh specialist

Give each builder only the context needed for its part:

- the overall goal;
- its specific assignment;
- the relevant source material and constraints;
- the benchmark or test that matters;
- the location of the real working artifact.

Tell the builder to inspect and change the actual work. Do not ask it to produce a plan when the assignment is to build.

### 3. Use a separate critic

The critic must be a fresh sub-agent when the platform supports it.

Give the critic:

- the goal;
- the benchmark;
- the rules that cannot be broken;
- the actual artifact, rendered result, test output, source evidence, or live workflow.

Do not give the critic:

- the builder's reasoning;
- the builder's self-review;
- earlier critic scores unless needed to check a claimed fix;
- language that reveals which option the builder produced when a blind comparison is possible.

Ask the critic to return:

- `PASS` or `FAIL`;
- the evidence it inspected;
- the biggest meaningful gap;
- the next change most likely to close that gap.

Use a blind A/B comparison when practical. If it is not practical, require an independent comparison against the same standard.

### 4. Check quality and function

A polished result can still be wrong or broken. Use two review lanes when the work requires both:

- A quality critic compares the work with the real benchmark.
- A validity critic checks facts, constraints, tests, edge cases, sources, data, or the actual user flow.

Neither critic can pass a summary written by the builder. They must inspect the real thing.

### 5. Keep improving the biggest gap

Send the critic's largest meaningful gap back to the builder. The builder fixes that gap, then a fresh critic checks the new result.

Do not stop after a fixed number of rounds. Continue while meaningful improvement is happening and the run remains within the user's scope and depth.

Reconsider the benchmark, task split, or approach when:

- the same gap survives repeated attempts;
- critic feedback conflicts;
- changes improve one part while hurting another;
- the work is getting more polished without getting more useful;
- progress stalls.

### 6. Put the pieces together and test the whole thing

After a major wave, use a fresh reviewer to inspect the complete result:

- Does it feel and function like one coherent thing?
- Did separately improved pieces introduce conflicts?
- Does the real end-to-end workflow work?
- Are the user's facts, constraints, and commercial boundaries still intact?
- Does the whole result meet the original goal, not just the individual scores?

Run the actual workflow whenever possible. For software, use the intended routes and user actions. For a presentation, render and present it. For analysis, reproduce the calculations and challenge the sources. For a plan, test it against real constraints, likely failure points, owners, and decisions.

## Depth

If the user specifies a depth, follow it:

- `Quick`: Apply the method to the few highest-impact gaps. Be clear that this is a limited Gauntlet.
- `Standard`: Default. Use parallel work where it helps and continue until material gaps are closed or progress stalls.
- `Deep`: A sustained run with a durable progress record. Confirm before beginning a run that could consume substantial time, model limits, paid services, or an overnight session.

Do not begin an open-ended or expensive deep run merely because the goal is ambitious.

## Progress

Keep the user informed without making them manage the agents.

For a normal run, concise thread updates are enough. For a long or resumable run, use the templates in `templates/` and keep a task-scoped progress file beside the working artifact. Do not add progress files to a final deliverable or commit them unless they are useful and intentional.

Progress updates should answer:

- What part is being worked on?
- What did the critic reject?
- What changed?
- What remains?
- Are we still making meaningful progress?

Avoid agent theater, raw transcripts, and repeated status narration.

## Stop Conditions

Stop when one of these is true:

- the complete result meets the agreed bar;
- the user accepts the result;
- further changes are no longer meaningfully improving it;
- the requested depth, time, or model limit has been reached;
- the next step requires new authority or an external commitment;
- the benchmark or goal needs the user's decision;
- a safety, legal, financial, confidentiality, or production boundary requires human review.

Do not claim success because the builders finished. Report what passed, what was tested, what remains, and why the run stopped.

## Communication Style

Be direct, conversational, and specific.

Keep useful terms such as goal, benchmark, sub-agent, critic, validation, and acceptance criteria when they are the clearest words.

Prefer:

- "break the goal into the parts that matter" over "decompose the problem";
- "put the pieces together and test the whole thing" over "validate the integrated result";
- "the thing we're making" when "artifact" would sound unnatural;
- "how far should we take this?" when discussing depth with the user.

Ask one question that makes the goal better. Do not hand the user a questionnaire.

## Final Handoff

Lead with the result.

Include:

1. What was built, decided, or improved.
2. The benchmark used.
3. What the critics rejected and how it changed.
4. What was tested in the real workflow.
5. Remaining gaps or risks.
6. Why the run stopped.

Distinguish drafted, built, tested, published, sent, and verified live.
