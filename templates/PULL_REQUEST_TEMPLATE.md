# Pull request

<!--
To use this in a repository, copy it to .github/PULL_REQUEST_TEMPLATE.md; GitHub then pre-fills
every new pull request with it.

🔴 AI off for the description: write it yourself (LLVM asks the same of its contributors).
An agent may have written code; it did not write this. Delete the guidance comments as you fill
it in. Upstream projects have their own templates and AI policies: when contributing upstream,
use theirs, and follow their policy where it is stricter than the course's.
-->

## What and why

[Two to five sentences in your own words: the problem, the change, and why this approach. Link the issue: "Closes #[n]".]

## Changes

- [File or module]: [what changed]
- [File or module]: [what changed]

## How I verified it

Tag each line **observed** (you ran or read it; paste the command or link the run) or **inferred**.

- [ ] Tests: `[command]` → [result, e.g. "212 passing, 0 failing"] (observed) · CI run: [link]
- [ ] New or changed tests were written before the implementation, and failed first: [commit link]
- [ ] Acceptance criteria covered: [R1, R2 …] by [test names]
- [ ] Mutation score of the changed module (if required): [before → after, tool and command]
- [ ] Manual check: [what you tried by hand, including one edge case]
- [ ] Static analysis and secret scan clean, or findings explained: [link]

## Risks and limits

[What could break, what you didn't test, what a reviewer should look at first. Honest limitations count in your favor.]

## AI disclosure

<!-- Required. The course's rule: if you can't explain it, you didn't build it. -->

- **Tools and models:** [e.g. "Gemini CLI with [model]; Copilot completions"] · or **None**
- **Delegated to AI:** [what the agent wrote or did: files, tests, refactors, investigation]
- **Written by me without AI:** [what you wrote yourself, including this description]
- **How I verified the AI's work:** [what you read, ran, and changed; what you rejected and why]
- **AI_LOG.md entries:** [dates or links]
- [ ] I have read every line of this diff and can explain it without AI.
- [ ] AI-assisted commits carry an `Assisted-by: [tool and model]` trailer; no agent added sign-offs or attribution.
- [ ] No agent posted anything in this pull request or its review thread on my behalf.

The trailer goes at the end of each AI-assisted commit message, after a blank line, one line per tool:

```text
Expand weekly series across daylight-saving changes

Assisted-by: [tool] ([model])
```

## For the reviewer

[Where to start reading; questions you want answered; anything you're unsure about.]
