# .agents/

Files and guardrails that help LLM coding agents (Claude Code, Codex, Cursor, Aider, etc.) use this project's frameworks, APIs, libraries, and interfaces correctly.

These are **reference materials**, not behavior rules — agent-behavior rules live in the agent's own loader file (`CLAUDE.md` for Claude Code, `AGENTS.md` for Codex, etc.).

## Typical contents
- **`<framework>.md`** — usage rules for a specific framework or library that agents tend to get wrong (HEEx syntax, LiveView streams, Ecto changeset access, React Server Components rules, etc.). Some frameworks ship a generator (e.g. Phoenix's `mix usage_rules.sync`) that produces these files; others you write by hand.
- **`<api>.md`** — usage rules for an internal or external API the agent will frequently hit.
- **`<convention>.md`** — project-wide conventions that aren't covered by linters/formatters.

## How they get loaded
Each agent imports the relevant files from its own loader. For example, `CLAUDE.md` would do:

```
@.agents/<framework>.md
```

If you don't use LLM coding agents, you can delete this folder. The rest of the doc skeleton works fine without it.
