# DESIGN — [Feature name]

> How the change in `SPEC.md` will be built, and why this way. 🟡 **AI limited:** an agent may help you explore the codebase and propose options (log it in `AI_LOG.md`); the decisions and their reasons are yours.
> One to three pages. Write it before the tasks, revise it when a task teaches you something.
> Replace every [square-bracket placeholder].

**Author:** [name] · **Spec:** [link to SPEC.md] · **Reviewed by:** [teammate] · **Last updated:** [date]

## 1. Current state

[How the relevant part of the codebase works today: modules, data flow, where state lives. Tag each claim **observed** (file and line, or a command you ran) or **inferred**.]

```text
[A small diagram or file tree, if it helps. Describe it in words too.]
```

## 2. Proposed design

[Components you will add or change, how they interact, and the data they exchange. Name the files.]

## 3. Decisions

One row per decision a reviewer could reasonably have made differently.

| # | Decision | Options considered | Chosen because | Revisit if |
|---|---|---|---|---|
| D1 | [e.g. store a series as a rule, not as expanded occurrences] | [rule · expanded rows · both] | [edits to a series stay one write; matches the DST criterion R3] | [queries by date range get slow] |
| D2 | | | | |

## 4. Seams and risks in existing code

- **Seams** where the change plugs in without editing unrelated code: [for example: the `BookingStore` interface]
- **Characterization tests needed first** (behavior to pin down before refactoring): [list]
- **Risky areas:** [god modules, duplicated logic, weak tests you found]

## 5. Test strategy

| Layer | What | How adequacy is measured |
|---|---|---|
| Unit | [functions] | Mutation score of `[module]`, target [n]% |
| Property | [P1, P2 from SPEC.md] | Seeds and shrunk counterexamples recorded |
| Integration | [routes or workflows] | [criteria R1–Rn covered] |
| Security | [inputs an attacker controls] | [checks or tests] |

## 6. Security and privacy

[What untrusted input reaches this code; what it could make the system do; what the change exposes. If an agent or LLM is part of the feature, link `THREAT_MODEL.md`.]

## 7. Rollout and compatibility

[Migrations, flags, backwards compatibility, how to revert.]

## 8. What the agent will and won't do

Specify · Delegate · Verify for the design as a whole: which parts go to an agent (and which agent, with what permissions), which you write yourself, and how each is verified. Details per task are in `TASKS.md`.
