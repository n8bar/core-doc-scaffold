<!-- ──────────────────────────────────────────────────────────────────────── -->
<!--  TEMPLATE NOTES — DELETE THIS WHOLE BLOCK AFTER USING THIS TEMPLATE       -->
<!-- ──────────────────────────────────────────────────────────────────────── -->

# core-doc-scaffold

Opinionated project documentation skeleton. Bootstrap a new repo with a coherent doc hierarchy on day one, instead of drifting toward an `R/notes.md` and a stale `TODO.txt` six months in.

## What's inside

```
CLAUDE.md            — always-loaded primer (working style, engineering rules)
docs/
  README.md          — doc-folder index: roles, hierarchy, conventions
  PLAN.md            — master action list (milestones, current status, deferred decisions)
  ProductSpec.md     — master spec (vocabulary, principles, behaviors)
  BACKLOG.md         — work for releases after the current target
  FINDINGS.md        — numbered observation log
  UX_GUARDRAILS.md   — universal UX/a11y baseline + project-specific section
  CHANGELOG.log      — chronological scope/structure record (plain text)
  milestones/        — milestone docs in m##-<slug>/ subfolders
  specs/             — content-named subordinate specs
.agents/             — files & guardrails for LLM coding agents (optional)
```

## How to use

1. Click **"Use this template"** above (or `gh repo create --template n8bar/core-doc-scaffold ...`).
2. In the new repo, search for `<` to find every placeholder. Most live in `CLAUDE.md`, `README.md`, `docs/PLAN.md`, and `docs/ProductSpec.md`.
3. Set the date in each `_Last updated:_` line to today.
4. Decide whether you want `.agents/` (it's for LLM coding agents — keep it if you'll work with Claude Code, Codex, Cursor, etc.; delete it otherwise).
5. Delete this template-notes block from the top of `README.md`.
6. Initial commit. Done — your project has a working doc skeleton.

## Philosophy

- **Two master docs:** `PLAN.md` (action — *how* and *when*) and `ProductSpec.md` (spec — *what* and *why*). They never overlap.
- **Stay at your altitude.** Higher-level docs name the thing and link down; they don't catalog the same detail as their child docs.
- **Hierarchy:** PLAN.md → Milestone → Arc → Worklist → Item → Subitem. Docs stop at Worklist; Items and Subitems are inline checklist content.
- **Numbering:** filenames strict (`m02.01.01-slug.md`), references tolerant in prose (`m02.1.1` and `m02.01.01` both legal).
- **Branches:** `M##-<slug>` for milestone work; `fix/`, `chore/`, `docs/`, `spike/` for non-milestone work.
- **Specs are content-named, not milestone-named** (`docs/specs/auth.md`, not `docs/specs/m02-auth.md`). Action lists may reference specs but aren't required to.
- **Milestones carry deadlines** (approximate is fine, marked with `~`).
- **CLAUDE.md sits above the spec/action split** as the always-loaded primer — anything that should be in context regardless of which part of the project you're working on.

Full convention text lives in [`docs/README.md`](docs/README.md). `docs/PLAN.md` itself is kept lean — it's the operational dashboard, not a reference manual.

## Refresh / migration

When the template pattern improves, [`MIGRATION.md`](MIGRATION.md) records what changed and how to retrofit projects that were bootstrapped from earlier versions.

<!-- ──────────────────────────────────────────────────────────────────────── -->
<!--  END TEMPLATE NOTES                                                       -->
<!-- ──────────────────────────────────────────────────────────────────────── -->


# <PROJECT_NAME>

<PROJECT_TAGLINE>

<One-paragraph project pitch. What is this, who is it for, and what makes it
different? Keep it short — anyone reading should know within 30 seconds
whether this project is relevant to them.>

The execution dashboard lives in [`docs/PLAN.md`](docs/PLAN.md); the canonical product spec lives in [`docs/ProductSpec.md`](docs/ProductSpec.md).

## Stack

- <stack item>
- <stack item>

## Run it

```
<command>
```

## Run the tests

```
<command>
```
