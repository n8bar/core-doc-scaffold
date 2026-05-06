# Specs

Subordinate specs go here. They describe behaviors and invariants in more detail than the master [`../ProductSpec.md`](../ProductSpec.md) covers.

## Conventions
1. Specs are **content-named**, not milestone-named: `auth.md`, `progress-rollup.md`, `pubsub.md`. They describe the *what*, which outlives any particular milestone.
2. Action lists (milestones, worklists) may reference specs but aren't required to.
3. Specs do not refer back to action lists.
4. Promote a topic from inline-in-milestone to its own file here when:
   - More than one milestone touches it, or
   - The behavior survives the milestone that introduced it and would benefit from a stable canonical home.

When you create a spec, link to it from `../ProductSpec.md` (under "Headline Behaviors" or a related section) rather than only from milestone docs.
