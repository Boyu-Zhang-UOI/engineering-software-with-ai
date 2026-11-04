# STUDY_PROTOCOL — [Short study title]

> CS [5xxx] empirical study protocol, due in week 6; interim results in week 11; a 10-minute talk in week 15; the 4–6 page paper (ACM format) in finals week ([graduate/empirical-study.md](../graduate/empirical-study.md)). Individual or a pair.
> Write it as a preregistration: decide the question, the analysis and what would change your mind **before** you see the data. Changes after that are allowed, but recorded in §10.
> 🟡 **AI limited:** AI may help with analysis code (disclosed in `AI_LOG.md`); the protocol's and the paper's prose are your own (🔴 AI off). Replace every [square-bracket placeholder].

**Author(s):** [names] · **Advisor:** [instructor] · **Type:** ☐ replication · ☐ extension · ☐ new question · **Based on:** [paper, with link; for a replication, one of the [Replicable] items in the [reading list](../resources/reading-list.md#replicable-studies)] · **Date:** [date]

## 1. Question

[One research question, specific enough that the data could answer "no". Example: "Do mutation scores of LLM-generated pytest suites predict real-bug detection on BugsInPy as well as they do for developer-written suites?"]

## 2. Hypotheses

- **H1:** [a directional prediction, with the effect size you'd consider meaningful]
- **H0:** [what you'll conclude if H1 isn't supported]
- **What result would surprise you, and what would you then believe?**

## 3. Data

- **Source:** [public dataset with version or commit, e.g. a dated slice of AIDev; your own artifacts]
- **Licence and terms:** [does the licence allow this use? cite it]
- **Inclusion and exclusion criteria:** [decided now]
- **Size:** [n], and why that is enough (a rough power or precision argument)
- **Personal data:** [none / what, and how it is removed]

## 4. Method

- **Procedure:** [step by step, so someone else could rerun it]
- **Models:** [open-weight models via the lab machine, with tags and settings: temperature, context length, seeds] · **Repeats:** [k runs per condition]
- **Tools:** [mutmut, coverage.py, your scripts; versions]
- **Compute budget at $0:** [lab-machine hours you'll request; free-tier calls; what happens if the queue is busy]
- **Artifacts:** code and data in `[repo link]`, with a README that reproduces every number in the paper

## 5. Analysis plan

- **Measures:** [definitions]
- **Statistics:** [tests or intervals, e.g. bootstrap 95% CIs; correlation with CI; paired comparison]
- **Multiple comparisons:** [how handled]
- **For any human or LLM labeling:** two raters on a sample, Cohen's κ reported

## 6. Threats to validity

| Kind | Threat | What you'll do about it |
|---|---|---|
| **Construct** (do you measure what you claim?) | [e.g. "mutation score" from one tool's operators] | |
| **Internal** (could something else explain the result?) | [e.g. model nondeterminism; contamination] | |
| **External** (does it generalize?) | [e.g. 10 Python projects only] | |
| **Conclusion** (are the statistics sound?) | [e.g. small n, wide intervals] | |
| **Reproducibility** | [model versions change; free tiers change] | [pin tags; record dates; recorded outputs] |

## 7. No-human-subjects check

This course's studies use public data and your own artifacts only. **Any "yes" below means stop and talk to the instructor before collecting anything:** the study would need University of Idaho IRB review, which does not fit in a term.

- [ ] Does the study collect data from or about classmates, maintainers, users or any other people (surveys, interviews, observation, their grades or code)? **Yes / No**
- [ ] Does it intervene in a community, for example by submitting PRs, issues or reviews to see how maintainers respond? **Yes / No** (see [case E8](../resources/case-studies.md#e8-hypocrite-commits-when-research-gets-an-institution-banned))
- [ ] Does it use data that identifies people beyond public usernames in public datasets, or link datasets to identify them? **Yes / No**
- [ ] Will anything in the paper single out an identifiable individual? **Yes / No**
- [ ] Does any data you'll send to a model contain personal data or anything you may not share? **Yes / No** ([data rule](../setup/safety-contract.md#1-the-data-rule))

## 8. Timeline

| Week | Milestone |
|---|---|
| 6 | This protocol, approved |
| 7–10 | Pilot on 10% of the data; fix the procedure; full run |
| 11 | Interim results (Canvas) |
| 14 | Paper draft |
| 15 | 10-minute talk |
| 16 | Final paper (Canvas) and artifact repository |

## 9. Risks to the study

[What could stop it: dataset access, lab-machine time, a model that won't do the task. The fallback for each.]

## 10. Deviations from this protocol

| Date | Deviation | Why | Effect on conclusions |
|---|---|---|---|
| | | | |
