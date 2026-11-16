---
name: half-an-idea
description: Turn a half-formed idea into a minimum-sufficient brief, then do the work or produce a reusable prompt. Use only when explicitly invoked; ask at most one material question.
disable-model-invocation: true
---

# Half an Idea

## Purpose

Turn "I have half an idea" into useful work without making the user complete an intake form or learn prompt engineering.

The skill is a briefing method, not a prompt-lengthening trick. Its job is to identify the real outcome, supply the missing structure, resolve the one ambiguity that matters most, and move the work forward.

Read `references/method.md` before using this skill. Use `references/acceptance-tests.md` when validating or updating the skill.

## Invocation

This is an explicit-use skill. Valid invocations include:

- `/half-an-idea I have half an idea for a client workshop...`
- `$half-an-idea Turn this into something usable.`
- `Wrangle this idea for me.`
- `Use the half-an-idea skill on this.`
- `Build me a prompt from this rough thought.`

Invocation authorizes analysis, drafting, research, and in-scope execution. It does not authorize sending, publishing, deploying, spending money, changing credentials, sharing protected information, or destructive actions.

## Default Behavior

Default to doing the work, not merely returning a prompt.

Use the mode implied by the user's request:

- `Do`: Build the minimum-sufficient internal brief, complete the work, and verify it. This is the default.
- `Prompt`: Return a paste-ready prompt when the user explicitly wants to use another AI, agent, project, or tool.
- `Brief`: Return a decision or execution brief when the user wants alignment before action.
- `Explore`: Help the user narrow the idea when the desired outcome itself is still uncertain.

If the request could reasonably mean `Do` or `Prompt`, choose `Do` unless the user specifically asks for a prompt.

## Start With the Kernel

Extract the smallest set of facts that makes the idea actionable:

1. The result the user is trying to create or make true.
2. Who will use, receive, approve, or be affected by it.
3. The company, client, team, or account the work belongs to.
4. The most authoritative available source.
5. The deliverable or action that moves the idea forward.
6. The boundaries that cannot be violated.
7. What a good result must accomplish.

Do not ask the user to provide all seven. Infer them from the current request, connected sources, files, conversation, and durable context.

## Run the Ambiguity Test

Imagine giving the current idea to two capable operators with no additional context.

- If they would produce substantially the same useful result, proceed.
- If they would make materially different decisions about the outcome, audience, commercial posture, owning account, or external commitment, ask one question.
- If the difference is cosmetic or easily reversible, make a reasonable assumption, state it only when useful, and proceed.

Ask at most one question for the whole invocation. Ask the question that collapses the largest consequential fork. Never ask for information that can be discovered safely from available sources.

## Build the Minimum-Sufficient Brief

Create only the instructions the work actually needs:

- `Outcome`: what should be true when the work is done.
- `Audience or user`: who the result is for and what they need.
- `Context`: facts and sources the work must rely on.
- `Deliverable`: the thing to produce or action to complete.
- `Constraints`: facts, tone, boundaries, exclusions, and permissions.
- `Quality bar`: observable criteria for a strong result.
- `Assumptions`: only consequential assumptions not confirmed by evidence.
- `Validation`: how to check that the result works.

Treat this as an internal working brief in `Do` mode. Do not make the user read a large meta-prompt before seeing the result.

## Prompt Construction

When `Prompt` mode is requested:

- Write for the intended model, tool, or agent when known.
- Put stable context and rules before the task-specific request.
- Separate instructions from source material.
- Use examples only when they encode a real quality requirement.
- Use variables such as `[AUDIENCE]` or `[SOURCE FILE]` when repeat use is likely.
- Tell the receiving system what to produce and how the result will be judged.
- Require source checking or explicit uncertainty when factual accuracy matters.
- Include a completion or validation check for consequential work.

Do not:

- inflate a simple request into a long prompt;
- add role-play personas that do not change the result;
- request hidden chain-of-thought;
- use arbitrary confidence percentages;
- repeat the same instruction in multiple sections;
- add frameworks, headings, or steps merely to make the prompt look sophisticated;
- silently strengthen commitments, certainty, criticism, or commercial posture.

## Execute and Verify

In `Do` mode:

1. State the interpreted goal briefly when it helps alignment.
2. Use available sources before asking the user for facts.
3. Complete the work within the existing permissions.
4. Check the result against the quality bar and real user flow.
5. Lead the final response with the finished result or decision.
6. Distinguish drafted, built, tested, published, sent, and verified live.

If a reusable prompt would help after the work is complete, include it only when the user asked for it or when it is a concise, material part of the handoff.

## Source Discipline

When the user works across several companies, clients, or accounts, keep each one separate. Shared access is not permission to combine them.

Use this source order:

1. The user's current direction.
2. The authoritative live system or task document.
3. The current project files or knowledge base.
4. Recent conversation and memory.
5. Older material, clearly treated as dated.

Do not replace an inaccessible named source with an older related source without saying so. Do not invent facts, stakeholders, goals, access, status, or commitments.

## Communication

Be direct, conversational, and useful.

- Ask one good question, not a questionnaire.
- Keep useful technical terms when they improve precision.
- Preserve the user's hedges, such as `I think`, `I believe`, and `I'm hoping`, when writing on their behalf.
- Name a consequential assumption before it can distort the work.
- Avoid narrating the mechanics of prompt engineering unless the user asks.

The experience should feel like handing a rough thought to a strong operator who understands how to clarify it and move.
