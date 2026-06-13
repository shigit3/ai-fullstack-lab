# Unit Completion Contract

Use this contract to decide progress without asking the learner to self-grade.

## Completion Standard

A unit is complete only when all six are true:

1. Artifact: the required code, document, eval, or design exists.
2. Verification: the required command passes, or a manual check is explicitly satisfied.
3. Understanding: the learner can pass a small knowledge check or explain the central concept in their own words.
4. Variation: the learner handled one changed requirement, edge case, failure, debugging moment, or tradeoff.
5. Boundary: the learner knows what this unit does not cover yet.
6. State: progress and state files are updated.

Do not require polish beyond the unit goal. Do not expand the unit into the next unit.

## Evidence Sources

Accept any of these:

- Working code in the workspace.
- Tests, eval results, logs, screenshots, or terminal output.
- A design diagram or written system map.
- A debugging transcript.
- A verbal explanation plus a concrete implementation plan.

Prefer real artifacts when the unit is implementation-heavy.

## Completion Status

Use only:

- `completed`: all required boundary conditions are met.
- `in progress`: the unit has started but still has required work.

Do not use `paused`. Unfinished work is simply `in progress`.

## Review Rubric

Use this silently unless the learner asks for scoring:

- 0: Not started.
- 1: Concept described but no artifact.
- 2: Artifact exists but is brittle or copied without understanding.
- 3: Artifact works and learner can explain it.
- 4: Artifact works, handles a variation, and learner understands tradeoffs.

Complete at level 4.

## If Incomplete

State:

- What is already good.
- The single smallest missing item.
- The next action.
- The verification command or check.

Update state before ending.

If the learner is overwhelmed, do not add a new concept while marking the unit incomplete. Narrow the same checkpoint instead.

## If Complete

Do this in order:

1. Update `AI_FULLSTACK_PROGRESS.md`.
2. Update `ai-fullstack-labs/LEARNING_STATE.md`.
3. Write `UNIT_COMPLETION.md`.
4. Say `Unit complete / 本单元完成`.
5. Summarize what the learner can now do.
6. Name one remaining risk or blind spot.
7. Name the next unit for orientation, without starting it in the same conversation.

Post-completion polish should not reopen the unit unless it reveals that a completion criterion was false.
