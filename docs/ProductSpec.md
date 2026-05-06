# Product Spec
_Last updated: <YYYY-MM-DD>_

The canonical specification of **<PROJECT_NAME>** — what the product is, the vocabulary used to describe it, the principles it must hold to, and the headline behaviors that define it.

This is the master spec. Milestone docs and subordinate specs (under `docs/specs/`) narrow or extend it but do not contradict it. [`PLAN.md`](PLAN.md) tracks how we get there; this doc tracks what "there" means.

## Core Idea
**<one-sentence summary — the product's elevator pitch>**

<One paragraph elaborating: what users do with this, what makes it different, what it explicitly is *not*.>

## Product Inspiration
<Optional section — keep if the product is visibly inspired by prior art and the relationship matters. Otherwise delete this section.>

Heavily inspired by **<reference product>**, with these deliberate departures:
1. <Departure>.
2. <Departure>.
3. <Departure>.

## Vocabulary
- **<Term>** — <one-line definition>.
- **<Term>** — <one-line definition>.
- **<Term>** — <one-line definition>.
- (...add as many as needed; keep definitions short)

## Durable Principles
- **<Principle>** — <why it matters in one line>.
- **<Principle>** — <why it matters in one line>.
- **<Principle>** — <why it matters in one line>.
- (...3–7 works well; more starts to feel performative)

## Headline Behaviors
<Use this section for the central behaviors that define the product. Keep
each at altitude — describe the principle and the canonical rule, but push
edge cases down into the milestone doc that owns the behavior.>

### <Behavior name>
<One-paragraph description.>

```
<canonical rule, formula, or invariant if there is one>
```

Detailed edge cases live in [`<milestones/m##-<slug>/m##-<slug>.md>`](milestones/<slug>/<slug>.md).

## Cross-Feature Requirements
<Optional section for invariants that span features — security posture,
data ownership, multi-user behavior, accessibility floors, etc. Delete
the section if there's nothing of this shape yet.>

- <Requirement>.
- <Requirement>.

## Constraints (current release line)
<Optional section. Lists what the product explicitly is *not* doing right
now. Useful for scoping arguments. Delete if not needed yet.>

- No <thing>.
- No <thing>.
