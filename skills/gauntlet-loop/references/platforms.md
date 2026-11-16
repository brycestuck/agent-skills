# Platform Guidance

## Shared Rule

The main session is the conductor. Keep it responsible for:

- the overall goal;
- the benchmark;
- deciding which parts can run independently;
- assigning builders and critics;
- tracking scope, authority, and progress;
- putting the result back together;
- the final real-world test and handoff.

Do not run the entire skill inside a worker that cannot create other workers.

## Codex and ChatGPT Work

Use Codex's native collaboration tools when they are available.

- Explicit invocation of `$gauntlet-loop` authorizes sub-agent use for the stated task.
- Create bounded tasks that can run independently.
- Use clean-context workers when critic independence matters. When supported, start them without inherited conversation turns.
- Pass only the goal, the worker's assignment, relevant sources, constraints, benchmark, and artifact location.
- Do not preload the Gauntlet skill into builders or critics.
- Keep one slot available for the main conductor and respect the session's concurrency limit.
- Use isolated worktrees when parallel builders would otherwise edit overlapping repository files.
- Do not let multiple agents edit the same files without an ownership plan.

If native sub-agents are unavailable, disclose that the review cannot be fully independent. Use the freshest isolated session available or run a limited single-agent review without pretending it is blind.

## Claude Code

Use Claude Code's Agent tool for fresh sub-agents.

- Keep the main Claude Code session as the conductor.
- Use fresh general-purpose sub-agents for builders and critics.
- Do not preload this skill into their context.
- Give each sub-agent a concise assignment packet.
- Run independent work in parallel or in the background when permissions and file ownership allow.
- Remember that Claude Code sub-agents cannot spawn their own sub-agents. The main session must manage every builder-critic round.
- Use worktrees for parallel code changes that could overlap.
- Use agent teams only when the work genuinely needs sustained coordination across independent sessions and that feature is enabled.

Claude Code sub-agents may still inherit project memory such as `CLAUDE.md`. Treat them as fresh relative to the current conversation, not as completely blank models. Keep critic prompts independent of builder history.

If the user invokes the skill in Claude.ai, Cowork, or another Claude surface without local sub-agent support, use the surface's available agent capability. If there is no independent worker context, explain the limitation before claiming a true blind-critic loop.

## Builder Assignment Packet

Give a builder:

```text
Overall goal:

Your part:

What great looks like:

Rules you cannot break:

Sources and files:

Make changes to the real working result. Return the result, evidence, and anything that blocked you. Do not grade your own work.
```

## Critic Assignment Packet

Give a critic:

```text
Goal:

Benchmark:

Rules that cannot be broken:

Actual result to inspect:

Inspect the real result. Do not infer quality from a builder summary.

Return:
- PASS or FAIL
- Evidence inspected
- Biggest meaningful gap
- Next change most likely to close that gap
```

For blind A/B, randomize labels and do not reveal which option is the reference or agent-produced result until the critic has chosen.
