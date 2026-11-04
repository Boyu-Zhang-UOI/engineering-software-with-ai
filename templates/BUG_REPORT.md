# BUG REPORT — [Rule or criterion] [what goes wrong, in one line]

> One report per bug, as an issue in the repository (or a section of `BUGS.md`). Write it for a maintainer who has never seen your tests: they should be able to reproduce the bug from this report alone. In an issue, the heading line is the issue's title.
> 🟡 **AI limited:** the report is yours. An agent may help shrink a reproduction or a failing test; log that in `AI_LOG.md`.
> Tag every claim **observed** (you ran or read it: give the command and its output, or the file and line) or **inferred** (you or an AI concluded it). Replace every [square-bracket placeholder].

**Reporter:** [GitHub username] · **Date:** [date] · **Found by:** [a property and its seed, a test, a review, a scanner, by hand] · **Status:** [open / fixed in [commit or PR]]

## 1. Environment and version

- **Code:** [repository, and the commit hash or tag the bug reproduces on, for example `shipped`]
- **Runtime:** [Node or Python version; Codespace, dev container or OS]
- **Settings that matter:** [for example `ROOMLY_NOW=2026-11-09T16:00:00Z`, `FC_SEED=[seed]`, a config value; "none" if none]

## 2. Rule or criterion violated

> [Quote the rule, the acceptance criterion (its ID in `SPEC.md`) or the documented behavior, and say where it's written.]

## 3. Steps to reproduce

From a clean checkout of the version above:

1. [The smallest sequence of commands or requests that shows the bug]
2. [...]

## 4. Expected and actual

- **Expected:** [what the rule requires, in terms anyone can observe: a status, a return value, what's stored]
- **Actual (observed):** [what happens: the command and its output]

## 5. Minimal failing test

[The shortest test that fails because of this bug and nothing else, in the project's test style and file (for `roomly`: a `node:test` case in `tests/regression.test.js`). It fails on the version above and passes after the fix. For a property failure, give the shrunk counterexample and the seed it came from.]

## 6. Severity

[blocker / major / minor, with the reason: who is affected, how badly and how often. For example: "major: two groups can hold the same room at the same time" (inferred from the test above).]

## 7. Notes

- **Suspected location:** [file and function] ([observed / inferred])
- **Related:** [other failing tests or properties, duplicate reports, the fix PR]
- [Anything else: a workaround, what you ruled out]
