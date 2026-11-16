# Agent Skills

A few skills I use every day with Claude and other AI agents. Each one is a folder with a `SKILL.md` and supporting references, so it works anywhere that supports the Agent Skills format.

| Skill | What it does | How to use it |
| --- | --- | --- |
| [Half an Idea](skills/half-an-idea/SKILL.md) | Turns a rough thought into a minimum-sufficient brief, asks at most one question, and then does the work. It returns a reusable prompt only if you ask for one. | Explicit only: `/half-an-idea` or "wrangle this idea for me" |
| [Gauntlet Loop](skills/gauntlet-loop/SKILL.md) | Pushes an ambitious goal through specialist builders and independent critics, measured against a real benchmark, until the work stops improving. | Explicit only: `/gauntlet-loop`. It can use a lot of capacity. |
| [AI Ambition Coach](skills/ai-ambition-coach/SKILL.md) | Places an idea or workflow on a ten-level AI adoption ladder, explains why, and lays out stronger pathways with copyable prompts. | `/ai-ambition-coach`, or ask whether an idea is ambitious enough with AI |

## Install

### Claude Code

Add this repository as a plugin marketplace, then install the skills:

```text
/plugin marketplace add brycestuck/agent-skills
/plugin install agent-skills@agent-skills
```

Or copy any skill folder into `~/.claude/skills/` for personal use, or into `.claude/skills/` inside a project.

### Claude apps

Zip a single skill folder (for example `skills/gauntlet-loop`) and upload it as a custom skill in Claude's settings.

### Codex and other agents

Copy the skill folder into your agent's skills directory, for example `~/.codex/skills/`. Each skill includes `agents/openai.yaml` metadata for Codex.

## Credits

- **Gauntlet Loop** adapts Matt Shumer's Gauntlet Loop method. Original sources are listed in [source-notes.md](skills/gauntlet-loop/references/source-notes.md).
- **AI Ambition Coach** builds on [The Eight Levels of AI Adoption](https://every.to/guides/the-eight-levels-of-ai-adoption) by Mike Taylor, Laura Entis, and Claude, and [The Next Two Levels of AI Adoption](https://every.to/also-true-for-humans/the-next-two-levels-of-ai-adoption) by Mike Taylor, both published by Every. The skill paraphrases the framework and adds its own coaching method.

Neither skill is affiliated with or endorsed by the original authors.

## License

[MIT](LICENSE). The license covers the skill text and files in this repository. It does not grant rights to the underlying frameworks, which belong to their authors.
