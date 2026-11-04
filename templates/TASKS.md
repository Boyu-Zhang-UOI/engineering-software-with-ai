# TASKS — [Feature name]

> The design split into agent-sized tasks. Each task fits one agent session and one reviewable diff, and states Specify · Delegate · Verify before anyone starts ([safe-loop.md](../resources/safe-loop.md#specify--delegate--verify)).
> **Goldfish test:** a fresh session given only this file and `SPEC.md` should be able to start any task without asking you. Replace every [square-bracket placeholder].

**Spec:** [link] · **Design:** [link] · **Owner:** [name] · **Last updated:** [date]

## Rules for this list

- A task names its files, its check and its "done when". If it needs a design decision, it goes back to `DESIGN.md` first.
- The check is written and seen failing **before** the implementation (check first).
- Parallel tasks name their **merge point**: where their branches meet, and who resolves conflicts.
- Status: ☐ not started · ◐ in progress · ☑ merged · ✗ dropped (say why).

## Tasks

### T1 — [Short imperative title]

- **Criteria:** [R1, R2 from SPEC.md]
- **Specify:** [what must be true afterwards, in one or two sentences]
- **Delegate:** [agent and mode, e.g. "CLI agent in plan mode"] · **Files in scope:** `[src/recurrence.js]`, `[tests/recurrence.test.js]` · **Commands allowed without asking:** `[npm test]` · **Step limit:** [n]
- **Keep for myself:** [e.g. the property test; the DST edge case]
- **Verify:** [the test or command, and what passing looks like; mutation score if relevant; what you'll check by hand]
- **Depends on:** [none / T0] · **Merge point:** [n/a / "rebases onto T2 before merge; Alex resolves"]
- **Branch / worktree:** `[t1-series-expansion]`
- **Status:** ☐ · **PR:** [link] · **AI_LOG entry:** [date]

### T2 — [Short imperative title]

- **Criteria:**
- **Specify:**
- **Delegate:** · **Files in scope:** · **Commands allowed without asking:** · **Step limit:**
- **Keep for myself:**
- **Verify:**
- **Depends on:** · **Merge point:**
- **Branch / worktree:**
- **Status:** ☐ · **PR:** · **AI_LOG entry:**

## Summary

| Task | Criteria | Owner | Agent | Status | PR |
|---|---|---|---|---|---|
| T1 | R1, R2 | [name] | [agent] | ☐ | |
| T2 | | | | ☐ | |

## Learned while building

[Anything a task taught you that changed the spec, the design or the next tasks. Link the change in `SPEC.md` §8 if the spec moved.]
