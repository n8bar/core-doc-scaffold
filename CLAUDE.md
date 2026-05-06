# CLAUDE

Always-loaded primer for **<PROJECT_NAME>** — <one-line tagline>.

This file should hold whatever needs to be in context regardless of which part of the project you're working on. It sits above the spec/action split (PLAN.md / ProductSpec.md): not a spec, not an action list, just the primer.

<!--
If you'll use LLM coding agents (Claude Code, Codex, Cursor, etc.) and you
have framework-specific usage rules, drop them in `.agents/` and import here:

    @.agents/<framework>.md

Otherwise delete this comment and the `.agents/` folder.
-->

## Product (primer — see [`docs/ProductSpec.md`](docs/ProductSpec.md) for canonical detail)
- **Core idea:** <one-sentence summary of what this product is>.
- **Vocabulary** (use consistently): <Term1>, <Term2>, <Term3>. <Optional: explicit "what we're not" framing.>
- **Inspiration:** <Optional — name your prior art and the deliberate departures, or delete this bullet>.

## Durable Principles
1. <Principle that should outlast any one milestone>.
2. <Principle that should outlast any one milestone>.
3. <Principle that should outlast any one milestone>.

## Engineering Style
1. Boring, understandable code; small, reviewable changes.
2. Business logic in domain/service modules with tests, not views.
3. <Project-specific structural invariant — keep here only if always relevant>.

## Dev Environment
1. <Top-line setup command — e.g. `docker compose up --build` or `npm run dev`>.
2. <Required host-level installs — keep this list short>.
3. <Anything that should never be required of the host>.

## Working Style
1. Specs first: a milestone doc with acceptance criteria exists before its code lands. If asked to code before a spec exists, pause and recommend writing it first.
2. Keep docs in sync within the same commit when scope shifts.
3. When the user asks for input/feedback ("what do you think?", "should we…?"), answer first; don't change files until they confirm.
4. Use the system date for any dated docs.
5. Don't merge with a dirty tree or unpushed commits without explicit confirmation.

## Branch & Repo
1. New milestone-scoped work: `M##-<slug>` (uppercase M, no padding). Example: `M02-keyboard-nav`.
2. Non-milestone work: semantic prefixes — `fix/<slug>`, `chore/<slug>`, `docs/<slug>`, `spike/<slug>`.
3. `main` is canonical on GitHub.

## Terminal Ownership
The agent drives <build/test/git> commands inside the project's dev environment — assume the user has no shell open unless they say otherwise.

## Subagents
Use only for independent, path-scoped tasks that materially shorten cycle time. The primary agent owns integration and the user-facing summary.
