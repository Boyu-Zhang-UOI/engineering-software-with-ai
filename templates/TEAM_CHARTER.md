# TEAM_CHARTER — [Team name]

> Agreed in week 2, before the team writes any code; revisited after M1 (week 8). Every member signs off in the team fork by committing their name below. It is about how you work, not about grades: **peer evaluations go on Canvas**, never here.
> Replace every [square-bracket placeholder].

**Members:** [name (GitHub username)] · [name] · [name] · [name] · **Team fork:** [link] · **Feature area in the class codebase:** [to be set at M0]

## 1. Goals

- What we want to have contributed by the final presentation: [one or two sentences]
- What each of us wants to learn: [one line each]

## 2. Roles

Rotate at each milestone, so everyone does each role once. Every member writes code, reviews, and operates agents.

| Role | M0–M1 | M1–M2 | M2–Final |
|---|---|---|---|
| **Coordinator** (runs meetings, tracks `TASKS.md`, flags risks) | | | |
| **Integration lead** (owns CI, the merge points, branch protection) | | | |
| **Security lead** (owns `THREAT_MODEL.md`, token scopes, dependency checks) | | | |
| **Upstream liaison** (reads the parent project's policies; contact with maintainers if the team goes upstream) | | | |

## 3. Communication and meetings

- **Channel:** [where] · **Expected response time:** [e.g. within 24 hours on weekdays]
- **Standing meeting:** [day, time, place or link, length]
- **Notes:** [where they live; who writes them]
- **When someone can't make a deadline:** tell the team by [how long before], with what's done and what isn't.

## 4. How we work

- **Branches:** one per task, named `[t3-short-name]`; `main` is protected; merges only through PRs with green CI.
- **Reviews:** every PR is reviewed by a teammate who didn't operate the agent on it ([REVIEW.md](REVIEW.md)); reviews within [n] hours on weekdays.
- **PR size:** aim for under [n] changed lines; larger needs a reason in the description.
- **Definition of done:** criteria covered by tests that failed first; CI green; mutation score of changed modules at least [n]% where required; PR description self-written with the AI section filled in; `AI_LOG.md` updated.
- **Parallel work:** before two people (or agents) work at once, the coordinator records the merge point in `TASKS.md`.

## 5. AI use in the team

- Agents run only in sandboxes, with approvals on, under each operator's own keys ([safety contract](../setup/safety-contract.md)). No shared keys; no shared accounts.
- **Free allowances:** who uses which pool, so the team doesn't run dry in the same week ([TOOLS.md](../TOOLS.md#spreading-the-work-across-free-allowances)): [plan]
- **Lab machine:** the team's batch window, if staff assign one: [time]
- Agents never post comments, reviews or PRs in another team's fork or upstream ([rule 10](../setup/safety-contract.md#10-no-unattended-agents-in-other-peoples-spaces)).
- Our team's own rules, beyond the course's: [e.g. "no agent edits to test files without a second reviewer"]

## 6. Decisions and disagreements

- Technical decisions: [e.g. proposer writes a row in `DESIGN.md` §3; decided by consensus, or by the feature owner after 24 hours]
- If we disagree about workload or quality: talk as a team first; if that fails within [n] days, any member may ask the instructor to mediate.
- If a member stops contributing: [what the team does, and when it tells the instructor]

## 7. Sign-off

<!-- Each member adds their own line in their own commit. -->

- [name], [date]
- [name], [date]
- [name], [date]

## Revisions

| Date | Change | Why |
|---|---|---|
| | | |
