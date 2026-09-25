# Case model / 案件模型

Read this reference when creating, resuming, or changing a case.

## Required case fields

- `case_id`: non-sensitive stable identifier.
- `service`: requested service.
- `jurisdiction`: authority or institution responsible.
- `category`: exact application category when known.
- `applicant_profile`: only facts needed for the workflow.
- `target_outcome`: the user's desired result, not a promised result.
- `current_state`: one state from the state machine.
- `target_date` and `hard_deadlines`.
- `tasks`, `evidence`, `risks`, `sources`, `decisions`, and `approvals`.
- `last_updated` and `next_review`.

## State machine

`NEW → INTAKE → NEEDS_INFORMATION → RESEARCHING → ELIGIBILITY_REVIEW → PLANNING → COLLECTING_DOCUMENTS → DRAFTING → QUALITY_REVIEW → USER_APPROVAL → READY_TO_SUBMIT → SUBMITTED → WAITING → ADDITIONAL_DOCUMENTS → APPROVED / REFUSED → CLOSED`

Use only states supported by evidence. `READY_TO_SUBMIT` means all known blockers are resolved and the user has reviewed the final package; it does not authorize submission. Preserve earlier state changes in the decision log.

## Task fields

Each task should have: identifier, description, owner, dependency, due date, status, proof of completion, and whether user confirmation is required.

## Evidence fields

Each item should have: identifier, requirement it supports, owner, source file or location, issue date, expiry date, language, translation status, verification status, sensitivity, and notes. Do not duplicate evidence merely to make a checklist look complete.

## Risk fields

- `BLOCKER`: proceeding would violate a requirement or create a high likelihood of invalid submission.
- `WARNING`: the case may proceed, but the issue could materially weaken or delay it.
- `ADVISORY`: operational improvement that is not presented as mandatory.

Each risk needs a trigger, consequence, prevention or fix, evidence/source, owner, and status.

## Session checkpoint

Every pause or handoff should preserve the state, completed work, unresolved items, next action, responsible person, deadline, and rules that must be refreshed.

