# THREAT_MODEL — [Team or setup name]

> A threat model of **your own agent setup**: the agents, tools, tokens and data your team actually uses. Written in week 4, revised at M2 and before the final defense. 🟡 **AI limited:** an AI may help you brainstorm attacks (log it); the analysis and the decisions are yours.
> Tag every claim about your setup **observed** (you checked it: a config file, a token's permissions page, a test) or **inferred**.
> Replace every [square-bracket placeholder].

**Team:** [names] · **Repository:** [link] · **Version:** [week 4 / M2 / final] · **Date:** [date]

## 1. What we're protecting

| Asset | Where it lives | Who or what can reach it | Impact if lost or leaked |
|---|---|---|---|
| [LLM API keys] | [Codespaces secret for repo X] | [any process in that codespace, including the agent] | [free tier, no card: quota loss only] |
| [GitHub token for the agent] | | | |
| [Team fork `main`] | | | |
| [Course work in progress] | | | |

## 2. The agents and their reach

| Agent / tool | Where it runs | Tools it has | Credentials in reach | Network | Approval policy |
|---|---|---|---|---|---|
| [CLI agent] | [Codespace] | [shell, file edit] | [codespace token; LLM key] | [open] | [every command] |
| [MCP server X] | | | | | |
| [AI reviewer] | [GitHub App] | [comment on PRs] | [repo-scoped app token] | | n/a |
| [CI workflow] | | | | | |

## 3. Untrusted input

Everything an agent reads that someone else could have written: issues, PR descriptions and comments, other teams' code (the PR round), dependencies and their READMEs, web pages, tool and MCP results, test fixtures, upstream code.

| Input | Which agents read it | Could it contain instructions? | Mitigation |
|---|---|---|---|
| | | | |

## 4. The lethal trifecta, per session

For each agent session type, tick the legs it has. Any row with all three needs a change before it runs.

| Session | Private data | Untrusted content | A way out (network, posting, writes others read) | Change |
|---|---|---|---|---|
| [Agent fixing an issue from another team] | ☐ | ☐ | ☐ | |
| [AI reviewer on PR-round PRs] | ☐ | ☐ | ☐ | |
| | ☐ | ☐ | ☐ | |

## 5. Threats

Use the OWASP GenAI LLM Top 10 and the MCP specification's security best practices as checklists ([reading list, week 4](../resources/reading-list.md#week-4--securing-agents)).

| # | Threat | Entry point | Likelihood | Impact | Mitigation (control, not instruction) | Tested? |
|---|---|---|---|---|---|---|
| T1 | Indirect prompt injection makes the agent exfiltrate a secret | [a poisoned issue] | | | [no secrets in that codespace; egress allowlist] | [test link / no] |
| T2 | Agent edits its own permissions or CI | | | | | |
| T3 | Hallucinated or hijacked dependency installed | | | | | |
| T4 | Agent posts in another team's fork or upstream | | | | | |
| T5 | Runaway loop or workflow spends an allowance | | | | | |
| T6 | Tool poisoning by an MCP server | | | | | |
| T7 | | | | | | |

A mitigation that is a line in `AGENTS.md` is advice, not a control. Say what enforces it.

## 6. Residual risk

[What you accept, and why. What would make you change your mind.]

## 7. Changes since the last version

| Date | Change | Why |
|---|---|---|
| | | |
