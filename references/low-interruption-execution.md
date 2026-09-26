# Low-interruption execution / 低打扰执行契约

This contract applies to a supported, exact-match visa route. It describes who does what after an applicant asks Codex to manage the case. It does not override current official instructions, the selected visa module, or [authorization boundaries](authorization-boundaries.md).

## Division of work / 分工

| Applicant / 申请人 | Codex / AI 中介助手 |
| --- | --- |
| State the travel purpose and provide truthful personal facts and available original evidence. | Identify the exact route, verify current first-party rules, and create a personalised requirement matrix. |
| Answer material questions that cannot be established from evidence; obtain genuinely missing documents. | Extract and cross-check facts, maintain an evidence-to-form-field map, and explain only real gaps or contradictions. |
| Review the final material declarations and approve each consequential action immediately before it occurs. | Prepare form answers and upload plan, self-check them, execute authorised actions when access and rules allow, and retain an action log. |
| Complete applicant-only identity, biometric, in-person, signature, or interview steps. | Track outcomes, deadlines, official requests, and next steps; provide a precise handoff for steps it cannot perform. |

## Execution rules / 执行规则

1. **One intake, then focused exceptions.** Ask for only the facts needed to route and plan. Once materials arrive, inspect them before asking for more. Group related missing facts and conflicts into a concise numbered request. Do not repeatedly ask the applicant to confirm already evidenced facts merely because Codex has not completed its own review.
2. **Trace every material answer.** Link each identity, travel, employment, finance, immigration-history, and declaration answer to the supplied evidence, a direct applicant statement, or an official rule. Mark unsupported answers `UNKNOWN`; never silently infer or fabricate them. Keep sensitive case records private.
3. **Self-repair safe defects.** Codex can reorganise a checklist, correct a copied field in its own draft against verified evidence, rename its own working files, improve legibility where content remains unchanged, or retry a failed read. Record what changed and recheck affected fields. Never alter original evidence, translate or certify beyond actual capability, or change applicant facts to make documents agree.
4. **Escalate only consequential ambiguity.** Ask the applicant or pause when a fact is disputed, evidence conflicts, a required document is absent, an official rule is unresolved, or a choice changes cost, eligibility, or risk. Explain the effect of each unresolved item and what would clear it. Do not make the applicant debug a prompt, tool, or model error.
5. **One clear final review.** Present the proposed route, important declarations, evidence inventory, unresolved warnings, costs/deadlines as verified, and intended external actions in a compact application summary. Ask the applicant to review material facts and declarations. If a later change affects them, show the changed portion again; do not require a full re-review of unchanged content.
6. **Action-by-action approval.** A general request to “handle everything” is not permission to upload, submit, pay, book, sign, make a legal declaration, or send data to a third party. Show the exact target and proposed action immediately before it occurs and obtain explicit confirmation under [authorization boundaries](authorization-boundaries.md). This may require more than one approval when the portal separates actions.
7. **Truthful completion state.** Use the states in [case-model.md](case-model.md): a prepared draft remains `DRAFTING` or `QUALITY_REVIEW`; final applicant review is `USER_APPROVAL`; `READY_TO_SUBMIT` is not submitted; only an observed submission advances to `SUBMITTED` and then `WAITING`. Store receipt or reference numbers only after observing them. If portal access or policy prevents a step, identify the exact field/action, owner, and copy-ready handoff; do not claim submission.

## Acceptance checks / 验收点

A supported case is low-interruption only if Codex can show: a current official-source record; a personalised requirement matrix; material form answers tied to evidence or direct statements; cross-document checks and correction/recheck logs; a concise exception list; a final applicant review; action-specific approvals where applicable; and an observed submission receipt or an explicit applicant handoff. A dry run proves only the tested scenario, not a live portal or every applicant profile.
