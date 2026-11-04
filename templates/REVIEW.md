# REVIEW — [PR title]

> A checklist and defect log for reviewing a pull request, especially an AI-authored one. 🔴 **AI off for the comments you sign:** review comments posted under your name are your own writing. You may run an AI reviewer separately and compare (week 9), and you may ask an AI to explain code you don't understand (log it in `AI_LOG.md`).
> Be specific and kind: file and line, what you observed, what you suggest. Graded peer evaluations of teammates go on Canvas, not here.
> Replace every [square-bracket placeholder].

**Reviewer:** [name] · **PR:** [link] · **Author:** [name or team] · **Date:** [date] · **Time spent:** [minutes]

## 1. Before reading the diff (5 min)

- [ ] The PR links an issue and acceptance criteria; I can say in one sentence what it should do.
- [ ] The PR is small enough to review in one sitting. If not, ask for it to be split before reviewing.
- [ ] The AI disclosure section is filled in.
- [ ] CI is green, or the failures are explained.

## 2. Correctness

- [ ] Each acceptance criterion has a test that would fail without the change. (Check one by reverting the change locally.)
- [ ] Edge cases: boundaries, empty and maximum input, time zones, concurrency, error paths.
- [ ] Tests check expected behavior, not just the current output (an oracle copied from the code proves nothing).
- [ ] No test was weakened, skipped, deleted or edited to match the new code without a stated reason.
- [ ] I ran it: `[command]` → [result].

## 3. Fit with the codebase

- [ ] Follows the project's conventions (`AGENTS.md`, `CONTRIBUTING.md`); no unrelated reformatting or renames.
- [ ] No duplicated logic that already exists elsewhere; no dead code; no leftover debugging.
- [ ] Names and structure a maintainer would accept.

## 4. Security and supply chain

- [ ] Untrusted input is validated; no injection, path traversal or unsafe deserialization.
- [ ] No secrets, tokens, internal URLs or personal data in code, tests, fixtures or logs.
- [ ] New dependencies: planned, real, maintained, pinned; lockfile updated consistently.
- [ ] Changes to CI, agent config, prompts or instruction files read as carefully as code (a prompt is code).

## 5. Defect log

Severity: **blocker** (must fix) · **major** · **minor** · **nit** (optional). Type: logic · security · test gap · style · docs · other.

| # | File:line | Severity | Type | Observed | Suggestion |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |

## 6. Decision

☐ Approve · ☐ Approve with nits · ☐ Request changes · ☐ Needs discussion

**Summary for the author** (2–4 sentences, your own words):

---

## Comparing with an AI reviewer (week 9)

Score both reviews against the defect key (staff provide it for the lab's seeded PRs). A comment is a **true positive** if it identifies a defect in the key, a **false positive** if it doesn't.

- **Only findings count.** Praise, questions and summaries aren't findings: they don't count as comments, for you or the AI reviewer, when reviews are scored.
- **A disputed false positive.** If you think a comment the key doesn't list is a real problem, mark it **disputed** and argue it in your write-up (`COMPARISON.md` in week 9) with evidence you observed: a command and its output, or a failing test. Report precision with and without it; staff decide.

| | Me | AI reviewer: [tool] |
|---|---|---|
| Comments | | |
| True positives | | |
| False positives | | |
| Defects in key found | / [n] | / [n] |
| **Precision** (TP ÷ comments) | | |
| **Recall** (found ÷ defects in key) | | |
| Time | [min] | [min, plus setup] |

- What did the AI find that I missed? What did I find that it missed?
- Which AI comments would I have acted on? (Deployed AI reviewers' comments lead to changes less often than humans': see the [reading list](../resources/reading-list.md#week-9--review-at-scale).)
