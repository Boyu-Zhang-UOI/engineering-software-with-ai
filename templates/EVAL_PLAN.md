# EVAL_PLAN — [Feature name]

> How you will measure an LLM feature before, and after, you change it. An eval is an experiment: give it a sample, a metric, error bars and a decision rule. Written in week 11, completed in week 12, required at M2 if your contribution uses an LLM.
> Replace every [square-bracket placeholder].

**Owner:** [name] · **Feature:** [link] · **Model(s) and provider(s):** [as configured; log changes] · **Date:** [date]

## 1. What the feature must do

[One paragraph, linking the SPEC.md criteria it serves. Example: "Turn a natural-language booking request into a booking JSON object that validates against the schema, or say which field is missing."]

## 2. Failure modes

List them **after** reading at least 30 real outputs, not before: some criteria only appear once you look ("criteria drift": [Shankar et al.](https://arxiv.org/abs/2404.12272)).

| # | Failure mode | Example (case ID) | Frequency in first 30 |
|---|---|---|---|
| F1 | [wrong time zone on start time] | [c017] | |
| F2 | [invents a room that doesn't exist] | | |
| F3 | [invalid JSON after retries] | | |

## 3. Dataset

- **Cases:** [n] in `evals/cases.jsonl` · **Sources:** [hand-written, sampled from logs with no personal data, adversarial]
- **Split:** [dev set for iterating; held-out set touched only for the final number]
- **Labels:** [expected fields per case; who labeled; how disagreements were settled]
- **Contamination check:** [are any cases copied from public examples a model may have seen?]

## 4. Metrics

| Metric | Definition | Target | Why this target |
|---|---|---|---|
| Schema validity | share of outputs that validate, after retries | | |
| Field accuracy | per field, exact or normalized match | | |
| Task success | all required fields correct | | |
| pass^k | all of k repeated runs succeed (reliability) | | |
| Cost | tokens or credits per request (mean, p95) | | |
| Latency | seconds per request (median, p95) | | |

**Error bars.** Report a 95% interval for every rate (bootstrap, or the formulas in [Miller](https://arxiv.org/abs/2411.00640)), and compare two versions on the **same** cases (a paired comparison). State how many cases you would need to detect the difference you care about.

## 5. LLM-as-judge (if a metric needs judgment)

- **Judge model and prompt:** [model] · `[where the judge prompt lives, e.g. JUDGE_PROMPT in src/judge.js]`
- **Human labels:** [n] cases labeled pass/fail by [you], with a one-line critique each, **before** looking at the judge's grades
- **Calibration:** report percent agreement **and** Cohen's κ, plus true-positive and true-negative rates. A judge that always says "pass" can agree 95% of the time with labels that are 95% passes ([Husain](https://hamel.dev/blog/posts/llm-judge/))
- **Bias checks:** [answer order, verbosity, self-preference]
- **Decision rule:** the judge is used only if κ ≥ [value] on held-out labels

| | Judge pass | Judge fail |
|---|---|---|
| **Human pass** | | |
| **Human fail** | | |

## 6. Regression gate in CI

- **Recorded responses:** `[evals/recordings-[name]/]`, so CI runs offline with no key and no cost
- **Gate:** CI fails if [task success on the recorded set drops below n%] or [any case in `evals/must-pass.jsonl` fails]
- **Refreshing recordings:** [when and by whom; the refresh is its own reviewed PR]

## 7. Results

| Version | Date | Cases | Task success (95% CI) | Validity | Cost/request | p95 latency | Notes |
|---|---|---|---|---|---|---|---|
| baseline | | | | | | | |
| | | | | | | | |

## 8. Error analysis

[Group the failures by mode; one representative example each; what you changed in response and whether it worked. Say what the eval does *not* measure.]
