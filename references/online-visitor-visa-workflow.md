# Online visitor visa workflow / 线上访客签证完整流程

Scope / 范围：mainland Chinese ordinary-passport holders applying from mainland China for UK Standard Visitor, Canada visitor visa, or Australian subclass 600 Tourist stream. This is a case-management process; the government decides the application. Last reviewed: 2026-09-26.

## Route gate / 路由关卡

Ask for nationality and passport type, residence and application location, destination, exact purpose, intended dates, companions/minors, funding, previous immigration problems, and whether an interview has already been requested. Choose exactly one country module. A work, study, immigration, medical, marriage, transit, or sponsored-family route needs its own rules. Do not fit it into a tourist module.

The standard application must have an online form and document review without a routine interview. Exclude US B1/B2 (interviews generally required), Japan tourism from China (designated agency route), and Schengen short-stay (consular or application-centre lodging). These can be researched separately only if the user changes scope. If a UK, Canada, or Australia case is individually called for interview, record `INTERVIEW_REQUIRED`, stop automated case execution for that step, and explain the authority's instructions. Do not coach scripted answers or pretend that biometrics are an interview.

## Nine gates / 九个关卡

1. **Intake 建档:** open a private case with minimal facts and deadline; record missing route facts as `NEEDS_INFORMATION`.
2. **Route and eligibility 路由与资格:** choose category and location; compare actual purpose, temporary intent, funds, return plan, and suitability with the selected authority's rules. Block an ineligible or conflicting route.
3. **Current rules 官方规则:** reopen the exact module sources; check portal, fee, passport, biometrics, evidence, translation, processing time, and local operational instructions. Record URL, scope, date checked, and unknowns.
4. **Plan and matrix 计划与材料矩阵:** generate case-specific required, conditional, optional, and discouraged evidence. Assign owner, due date, dependency, and cost; distinguish government requirements from internal file-naming conventions.
5. **Evidence audit 材料审核:** compare form draft with identity, dates, work/study, finances, trip cost, sponsor, accommodation, travel history, refusals, and translations. Inspect complete pages, provenance, validity, legibility, and applicant control of funds.
6. **Correction 纠错:** create `BLOCKER`, `WARNING`, and `ADVISORY` findings. Obtain truthful explanations or replacement evidence; rerun affected checks. Never alter a source document to make a story match.
7. **Final review 终审:** show the applicant the exact answers, upload package, fees, declarations, unresolved warnings, and items still dynamic. `READY_TO_SUBMIT` requires applicant review and no known blockers.
8. **Action and applicant steps 行动与本人步骤:** obtain immediate approval for each submission, payment, upload, booking, or disclosure. The applicant completes identity checks, biometrics, passport delivery, and medical steps where instructed. An interview request exits this workflow.
9. **Outcome and maintenance 结果与维护:** track authority messages and deadlines; collect additional documents only after checking the request. Record grant conditions or refusal reasons, close the case, and create a rule-change regression item for the module.

At every gate report state, verified facts, blockers, next action, owner, and date. Completion of gate 7 is a preparation milestone; it does not mean the government accepted or approved the application.

## Country review differences / 各国审核重点

| Route | Official review emphasis | Online and personal steps | Exit trigger |
|---|---|---|---|
| UK | genuine visitor, permitted activity, departure, funds and third-party support | online form and evidence; VAC biometrics when instructed | interview or another unsupported purpose |
| Canada | temporary stay, ties and departure, funds, admissibility | IRCC online application; biometrics if required; passport submission after approval | interview request or inadmissibility requiring specialist advice |
| Australia | genuine visitor, sufficient funds, health and character, Tourist stream conditions | ImmiAccount and attachments; biometrics or health checks if requested | interview request or wrong stream |

Translation rules differ by country. Never copy the UK translator declaration into a Canada or Australia case without checking that module.
