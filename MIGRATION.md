# MIGRATION

Changes to the `core-doc-scaffold` template over time. When the pattern evolves, this file records what changed so older projects can retrofit intentionally instead of guessing.

## How to retrofit a project bootstrapped from an earlier template version

1. Find the template version you started from (check the entry near the top of your project's `docs/CHANGELOG.log` that recorded the bootstrap).
2. Read the changelog below from that version forward.
3. Apply the changes you want; skip what doesn't fit your project.
4. Add an entry to your project's `docs/CHANGELOG.log` noting the date and which template revisions you pulled.

## Changelog

### 2026-05-06 — Initial template
First version. Established:
- The hierarchy: PLAN.md → Milestone → Arc → Worklist → Item → Subitem.
- The spec/action split with `PLAN.md` and `ProductSpec.md` as the two master docs.
- `CLAUDE.md` as the always-loaded primer above the split.
- Numbering and dotted-reference notation (`m##.NN.NN.NN.NN`); strict in filenames, tolerant in prose.
- Branch naming: `M##-<slug>` plus semantic prefixes for non-milestone work.
- Baseline ancillary docs: `BACKLOG.md`, `FINDINGS.md`, `UX_GUARDRAILS.md`, `CHANGELOG.log`.
- Milestone deadline convention.
- The "stay at your altitude" rule.
- The `.agents/` folder convention for LLM-agent guardrails.
