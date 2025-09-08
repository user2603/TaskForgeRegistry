# Release Readiness Rubric

**Document version:** 1.9 [ARCHIVED - SUPERSEDED]
**Effective period:** 2025-07-01 to 2025-09-07
**Status:** Superseded by Version 2.1 (effective 2025-09-08), located at
`docs/release_readiness_rubric.md`. This copy is retained for audit and format
reference only. DO NOT use it to classify current waves.

## 1. Scope

The rubric applied to every release readiness review conducted during its effective
period. The wave definition is unchanged from later versions: on each developer branch,
the newest commit whose message follows the integration format
(`Work on N tasks: <task>, <task>, ...`) names the wave tasks of that branch.

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

Maximum score: 12. An artifact earns its points when the file exists at exactly that
path inside the task directory.

## 3. Content condition

None in this version: all artifacts earn their points on file existence only.

## 4. Readiness statuses

| Status | Score band |
|---|---|
| Certified | 9 - 12 |
| Provisional | 7 - 8 |
| In Development | 0 - 6 |

## 5. Delivery completeness condition

None in this version: the delivery manifest in the commit message is not evaluated.

## 6. Recording rules

- Decisions recorded under this version keep their original scores and statuses in the
  audit trail; they are never rewritten when a newer version takes effect.
