# AI_LOG.md

> Required in every repository you submit. It records how AI was used: each significant session, the tool and model, what was delegated, and what was verified and how. It is graded as evidence of process, so be honest and specific; "used AI for everything, checked it" earns nothing.
> This file is in a repository, often public: no keys, no personal data, no classmates' names (graded personal reflection goes on Canvas). Replace every [square-bracket placeholder].

**Repository:** [name] · **Owner(s):** [names or usernames] · **Tools used this term:** [list; models as configured]

## How to log

- One entry per **significant** session: one that produced a commit, a decision, a finding in a report, or a failure worth remembering. Not every prompt.
- Tag each verification **observed** (you ran or read it, with the command or file) or **inferred** (you or the AI concluded it).
- Log **provider and model switches**: a result from a different model is a different result.
- Commits that came out of a session carry `Assisted-by: [tool and model]`, and the entry links them.

## Sessions

<!-- Newest at the bottom. Copy this block for each session. -->

### [date] — [task, e.g. "T1 series expansion"]

| | |
|---|---|
| **Tool and model** | [e.g. Gemini CLI, [model]; or mini-agent → lab Ollama, [model]] |
| **Specify** | [the task as given: link to the issue, TASKS.md entry, or the prompt in a `text` block below] |
| **Delegated** | [what the agent did: files, commands, tests] |
| **Kept for myself** | [what you wrote or decided] |
| **Verified, and how** | [observed: "`npm test` 48/48 at a1b2c3d"; "read the diff, rejected the change to `config.ts`"; inferred: "agent says the DST case is covered; not yet checked"] |
| **What went wrong** | [wrong assumptions, ignored instructions, tests it tried to change, loops] |
| **Cost** | [requests, tokens or minutes, if known; which allowance] |
| **Commits** | [hashes or links] |

```text
[Optional: the key prompt, copied in. No secrets.]
```

## Experiments

<!-- For week 3's AGENTS.md A/B test, Goldfish tests and any other comparison you run. -->

| Date | Question | Conditions | Runs per condition | Model | Result (observed counts) | Conclusion, scoped to the sample |
|---|---|---|---|---|---|---|
| | [Does the agent run the single-test command before finishing?] | [with AGENTS.md / without] | [3] | | [with: 3/3 · without: 1/3] | |

## Summary for submission

Update at each milestone.

- **What I (we) delegated most, and why:**
- **What I never delegated, and why:**
- **The most useful verification habit:**
- **One time the AI was confidently wrong, and how I caught it:**
