# MIGRATION

Changes to the `core-doc-scaffold` template over time. When the pattern evolves, this file records what changed so older projects can retrofit intentionally instead of guessing.

## How to retrofit a project bootstrapped from an earlier template version

1. Find the template version you started from (check the entry near the top of your project's `docs/CHANGELOG.log` that recorded the bootstrap).
2. Read the changelog below from that version forward.
3. Apply the changes you want; skip what doesn't fit your project.
4. Add an entry to your project's `docs/CHANGELOG.log` noting the date and which template revisions you pulled.

## Changelog

### 2026-05-07 — Tighten heading and item-numbering conventions
Two tightenings to `docs/README.md` § Numbering:
- §1.2: Arc headings inside a milestone doc must use the local number only (`### 1 — <name>`), not the full dotted form (`### m02.01 — <name>`).
- §1.4: Items must not prefix themselves with their own dotted reference. Position in the doc gives the reference; self-labels are forbidden. Cross-references between items remain fine.

To retrofit: scan your milestone docs for `### m##.NN —` Arc headings and `**m##.NN.NN** —` item prefixes; convert to `### N —` and drop the prefix.

### 2026-05-06 — Slim PLAN, conventions moved to `docs/README.md`
PLAN.md was carrying ~80 lines of structural reference (Doc Roles, hierarchy diagram, numbering, doc layout, specs-vs-actions, branches, repo, deadlines) ahead of operational content (Current, Milestones). Opening PLAN to "get to work" meant scrolling past the reference block every time.

Changes:
- New file: `docs/README.md` — owns Doc Roles, action-list hierarchy, the "stay at your altitude" rule, and conventions §1 Numbering, §2 Doc Layout, §3 Specs vs. Actions, §4 Milestone deadlines.
- `docs/PLAN.md`: structural sections deleted; replaced with a 3-line pointer to `docs/README.md`, `../CLAUDE.md`, and `ProductSpec.md`. PLAN now opens directly to Deferred Decisions / Current / Milestones.
- Old PLAN §4 Branches and §5 Repo deleted as duplicates — those rules already live canonically in `CLAUDE.md`'s Working Style and Branch & Repo sections.
- `CLAUDE.md`: one-line pointer added directing agents to `docs/README.md` when adding any doc or making a structural decision.
- Working Style gained two collaboration rules from a separate revision the same day: explicit-approval gate after writing an execution doc, and document-order execution with no skip-ahead without per-item approval.

To retrofit:
1. Create `docs/README.md` from the current scaffold.
2. Delete the Doc Roles and Conventions blocks from your `docs/PLAN.md`; replace with the 3-line pointer.
3. Add the `docs/README.md` pointer line to your `CLAUDE.md`.
4. (Optional) Add the two new Working Style rules.

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
