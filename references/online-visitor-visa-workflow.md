# Online visitor visa workflow / 线上访客签证完整流程

Scope / 范围：mainland Chinese ordinary-passport holders applying from mainland China for an exact [reviewed route](global-online-route-screen.md), including UK, Canada, Australian Visitor 600 Tourist, Schengen individual tourism, New Zealand Visitor, and selected eVisa/ETA/temporary-waiver destinations. Codex performs research and evidence review online; the applicant performs any required lodging or identity step. The authority decides the application. Last reviewed: 2026-09-26.

## Route gate / 路由关卡

Ask for nationality and passport type, residence and application location, destination, exact purpose, intended dates, companions/minors, funding, previous immigration problems, and whether an interview has already been requested. First use the [global screen](global-online-route-screen.md) to classify visa-free, ETA, eVisa, full online visa, online-form-only, mandatory agency or unknown; choose exactly one applicable country module. A work, study, immigration, medical, marriage, transit, or sponsored-family route needs its own rules. Do not fit it into a tourist module.

The Skill's review is remote; government submission may be online or at a centre. Exclude US B1/B2 because its ordinary route generally requires a formal interview. Japan tourism from China remains outside independent submission because an accredited agency is required. A Schengen application-centre visit for lodging, routine trip questions, or fingerprints is not itself a consular interview. If any supported case is individually called for a formal interview, record `INTERVIEW_REQUIRED`, stop automated execution for that step, and explain the authority's instructions. Never script answers or treat fingerprints as an interview.

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
| Schengen tourism | competent main-destination country, purpose, funds, accommodation, travel insurance, return intention | country form/appointment; applicant lodges documents and biometrics as instructed | formal interview request or wrong country/purpose |
| New Zealand Visitor | genuine tourist intention, funds/departure, identity, health/character, complete translations | enhanced Immigration Online; medical/police steps if requested | formal interview or wrong visit type |
| Saudi tourist eVisa | eligible passport, purpose, entry date and passport validity | official online eVisa, email result, border biometrics | Hajj/work purpose or formal interview |
| Indonesia e-VOA | current B1 product, eligible nationality, passport and onward travel | official online e-VOA, border inspection | product/port mismatch or formal interview |
| Sri Lanka ETA | ETA purpose, passport, return ticket and funds | online ETA, acknowledgement then decision | referral is not approval; formal interview |
| Kenya ETA | ordinary-passport exemption screen, itinerary/accommodation, passport and photo | official online ETA, border inspection | exemption mismatch or formal interview |
| Cambodia tourism | date-and-duration waiver gate before visa route | e-Arrival even for temporary visa-free tourism | waiver expiry/longer stay needs live recheck |

Translation rules differ by country. Never copy one country's translation or filename rule into another country's case without checking its module and live checklist.
