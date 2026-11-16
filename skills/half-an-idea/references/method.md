# Half an Idea Method

## The Core Idea

Most weak AI requests are not primarily writing problems. They are incomplete briefs.

The user often knows more than they have stated:

- why the work matters;
- who it is for;
- what a good result feels like;
- which facts are fixed;
- what would make the result unusable;
- whether they want exploration, a decision, a deliverable, or an external action.

This skill converts that tacit context into the minimum amount of explicit structure needed to act.

## 1. Find the Result Behind the Request

Do not anchor too tightly on the first noun or deliverable the user mentions.

Examples:

- “I need a deck” may mean “I need the leadership team to approve a pilot.”
- “I need a prompt” may mean “I want you to complete this research.”
- “I have an idea for a dashboard” may mean “I need weekly visibility into stalled accounts.”
- “Help me respond” may mean “Protect the relationship without accepting the premise.”

Identify both:

- the requested output;
- the operational result that output should create.

The output should serve the result.

## 2. Distinguish Four Modes

### Do

The outcome is clear enough to act. Build the brief internally and complete the task.

### Prompt

The user needs a portable instruction for another AI, agent, project, or tool. Return the prompt as the primary artifact.

### Brief

The work needs stakeholder alignment, delegation, or later execution. Produce a concise brief with decision points, owner, dependencies, definition of done, and validation.

### Explore

The user has a direction but not yet a destination. Surface the few meaningful options, explain the tradeoffs, recommend a path, and convert the selected or recommended path into an actionable next step.

Do not stay in Explore mode merely because some details are unknown.

## 3. Diagnose Ambiguity, Not Length

Prompt depth should follow the number and consequence of plausible interpretations.

A short request is sufficient when:

- the task has one conventional meaning;
- the output is reversible;
- the source is authoritative and complete;
- format and audience are obvious from context.

More structure is needed when:

- different audiences require materially different choices;
- commercial or emotional posture matters;
- the owning company, client, or account is unclear;
- facts must come from a named source;
- the output will be repeated or automated;
- errors could affect customers, money, legal exposure, personal data, or production systems.

Longer is not inherently better. Every instruction should remove a plausible failure or encode a real requirement.

## 4. Ask One High-Leverage Question

Ask only when the answer would change the result materially.

Good questions resolve:

- which of two outcomes matters;
- who the actual decision-maker or audience is;
- whether the work is exploratory or ready for commitment;
- which company, client, or account owns the request;
- whether an external action is authorized;
- which authoritative source should control.

Weak questions ask the user to do the agent's job:

- “What tone do you want?” when a voice guide, prior writing, or the audience makes it clear;
- “Can you provide more context?” without naming the missing fork;
- a list of fields that can be inferred;
- preferences that affect polish but not the decision.

If one question cannot resolve every unknown, ask the most consequential one and make safe assumptions for the rest.

## 5. Translate Tacit Judgment

When examples exist, identify the qualities that make them useful:

- structure;
- level of specificity;
- evidence;
- voice;
- decision logic;
- exclusions;
- emotional temperature;
- action requested.

Use those qualities as acceptance criteria. Do not imitate superficial formatting while missing the underlying purpose.

## 6. Build for Reuse Only When Reuse Exists

For a recurring task, separate:

- stable instructions;
- company, client, or role context;
- task-specific inputs;
- authoritative sources;
- validation criteria.

Use variables for task-specific inputs. Do not convert a one-time request into an elaborate template without evidence that it will recur.

## 7. Validate the Result, Not the Prompt

A polished prompt is not the outcome.

Validation should answer:

- Did the resulting work satisfy the user's real objective?
- Are facts traceable to the correct sources?
- Did the output preserve the intended voice and posture?
- Can the intended user understand and act on it?
- Did any assumption create an avoidable risk?
- If repeatable, does the prompt work with a second representative example?

Prefer direct inspection, tests, rendered artifacts, and real workflows over confidence statements.

## Compact Internal Pattern

Use this only as an internal aid:

```text
Outcome:
Audience or user:
Owning account:
Authoritative context:
Deliverable or action:
Constraints:
Quality bar:
Consequential assumptions:
Validation:
```

Do not automatically expose this block to the user in `Do` mode.
