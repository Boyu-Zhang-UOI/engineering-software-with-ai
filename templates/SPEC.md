# SPEC — [Feature name]

> 🟡 **AI limited:** write the problem, the criteria and the out-of-scope list yourself. You may ask an AI to *critique* the spec ("what is ambiguous? which edge cases are missing?"), and record that in `AI_LOG.md`, but not to write it.
> **Goldfish test** before you build: give only this file to a fresh agent session and ask what it would build, what it would ask, and what it would assume ([how](../resources/agent-patterns.md#the-goldfish-test)). Every question or wrong assumption is a defect here.
> Replace every [square-bracket placeholder].

**Owner:** [name] · **Issue:** [link] · **Status:** [draft / agreed / changed in beat 2] · **Approved by:** [GitHub username], [date] · **Last updated:** [date]

## 1. Problem

[Who needs what, and why it matters, in 2–4 sentences. Link the issue or discussion it came from.]

## 2. Context

[The part of the codebase this touches, the existing behavior that must not change, and any constraints from maintainers or the project's policies. Tag claims about current behavior **observed** (you ran or read it) or **inferred**.]

## 3. Acceptance criteria (EARS)

Write each criterion in one of the EARS patterns. The default is event-driven: **WHEN** *trigger*, **THE SYSTEM SHALL** *observable response*. Each one must be checkable by a test or a reproducible command. Include the edge cases: boundaries, empty and maximum inputs, time zones, concurrency, failure of a dependency.

| Pattern | Form |
|---|---|
| Event-driven | WHEN [trigger], THE SYSTEM SHALL [response] |
| State-driven | WHILE [state], THE SYSTEM SHALL [response] |
| Unwanted behavior | IF [condition], THEN THE SYSTEM SHALL [response] |
| Optional feature | WHERE [feature is enabled], THE SYSTEM SHALL [response] |
| Ubiquitous | THE SYSTEM SHALL [response] |

| ID | Criterion | Priority | Verified by | Status |
|---|---|---|---|---|
| R1 | WHEN a user requests a booking that ends exactly when another begins, THE SYSTEM SHALL accept it. | MUST | `tests/bookings.test.js` "adjacent bookings" | ☐ |
| R2 | IF a requested booking overlaps an existing one by any amount, THEN THE SYSTEM SHALL reject it with status 409 and name the conflicting booking. | MUST | property test P1 | ☐ |
| R3 | WHEN a weekly series crosses a daylight-saving change, THE SYSTEM SHALL keep each occurrence at the same local start time. | MUST | | ☐ |
| R4 | | | | ☐ |

## 4. Properties

Invariants that must hold for *all* inputs, for property-based tests (week 6).

- **P1:** [For example: no two accepted bookings for the same room overlap.]
- **P2:** [For example: expanding a series and then cancelling it leaves the store as it was.]

## 5. Out of scope

What this change deliberately does not do (this list stops you, and the agent, from wandering).

- [ ]
- [ ]

## 6. Interfaces

[API routes, function signatures, CLI flags or file formats that change, with one example request and response each. Mark anything public that other code depends on.]

## 7. Non-functional constraints

- **Compatibility:** [what must keep working]
- **Performance:** [for example: series expansion of 52 occurrences under 50 ms]
- **Security and privacy:** [inputs to validate; no personal data; what an attacker controls]
- **Cost** (if it calls an LLM): [budget per request; see `EVAL_PLAN.md`]

## 8. Spec changes

When the specification changes (a beat, a maintainer's request, something learned while building), record it here instead of silently editing above.

| Date | What changed | Why | Criteria affected |
|---|---|---|---|
| | | | |

## 9. Open questions

- [ ]
