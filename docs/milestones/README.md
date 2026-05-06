# Milestones

Milestone docs go here, one folder per milestone:

```
milestones/
  m01-<slug>/
    m01-<slug>.md         ← the milestone doc
    m01.01-<arc>.md       ← optional Arc breakout
    m01.01.01-<wl>.md     ← optional Worklist breakout
```

Default: keep Arc and Worklist content **inline** within the milestone doc. Break out into separate files only when a section gets long enough to warrant its own file.

If a single milestone's breakouts get crowded, introduce arc subfolders:

```
milestones/
  m02-<slug>/
    m02-<slug>.md
    m02.01-<arc>/
      m02.01-<arc>.md
      m02.01.01-<worklist>.md
      m02.01.02-<worklist>.md
```

See [`../PLAN.md`](../PLAN.md) § Conventions for the full numbering and reference rules.
