# Release Readiness Rubric

**Document version:** 2.1 (current)
**Effective date:** 2025-09-08
**Supersedes:** Version 1.9 (archived at `docs/archive/release_readiness_rubric_v1.9.md`)

This document is the single authoritative standard for every release readiness review
conducted on or after its effective date, no matter when the reviewed tasks were
delivered. Archived rubrics and past-wave ledgers under `docs/archive/` are kept for
audit and format reference only. Their thresholds and their recorded decisions must
never be used, copied or inferred when classifying a current wave.

## 1. Scope

The rubric applies to every task named in the current integration wave. The wave is
defined per developer branch: on each developer branch, the newest commit whose
message follows the integration format (`Work on N tasks: <task>, <task>, ...`) names
the wave tasks delivered by that branch. A task is always evaluated in the form it
exists on its own developer branch, under `tasks/<developer-dir>/<task-name>/`.

Commit listings return at most 30 records per page, so every page of a branch's
history must be merged before deciding which integration commit is the newest one.

## 2. Artifact checklist and points

| # | Artifact (path inside the task directory) | Points |
|---|---|---|
| A1 | `docs/task.md` | 3 |
| A2 | `evaluation/main.py` | 3 |
| A3 | `preprocess/main.py` | 2 |
| A4 | `docs/agent_system_prompt.md` | 1 |
| A5 | `docs/user_system_prompt.md` | 1 |
| A6 | `groundtruth_workspace/readme.txt` | 1 |
| A7 | `initial_workspace/readme.txt` | 1 |

Maximum score: 12. An artifact earns its points only when the file exists at exactly
that path inside the task directory. A missing artifact earns 0 points. This checklist
is exhaustive: the layout of the example package under `tasks/examples/` is historical
context and never adds requirements.

## 3. Content condition for A1

`docs/task.md` (A1) earns its 3 points only when the file is non-empty and contains
English text only. A `docs/task.md` that contains any Chinese character earns 0 points
for A1.

## 4. Readiness statuses

| Status | Score band |
|---|---|
| Certified | 11 - 12 |
| Provisional | 8 - 10 |
| In Development | 0 - 7 |

## 5. Delivery completeness condition

If the integration commit that delivered a task ends its task manifest with a
trailing comma (a truncated delivery manifest, e.g. `Work on 2 tasks: sync-service,`),
the task is held at `In Development` regardless of its artifact score. The delivery is
treated as incomplete until its manifest is corrected.

## 6. Recording rules

- The readiness status recorded for a wave task is the status derived from this
  document only.
- All three statuses in section 4 must be recorded exactly as defined there.
  Collapsing two statuses into one value, or excluding a subtype of tasks by rule of
  thumb instead of by this document, is a recording error.
- A field without a directly recorded value (for example the implementor of a task)
  must be derived from the wave evidence and filled in; it must never be left empty.
- When this document and any archived material disagree, this document prevails.
