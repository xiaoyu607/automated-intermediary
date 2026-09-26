# Australia Business Visitor 600 sandbox / 澳大利亚商务访客沙盒纠错

Run date: 2026-09-26. All identities and evidence are invented. No ImmiAccount login, upload, submission, payment, appointment, biometrics or real immigration decision occurred. M2 applies only to the case-management behavior of the fictional profile below, not to live portal compatibility or a visa grant.

## Fictional profile / 虚构人物

Chinese ordinary-passport holder living and employed in Shenzhen, applying from China while outside Australia; 8-day Sydney trip in January 2027 for an unpaid industry conference and two genuine contract-discussion meetings; employer funds the trip; applicant plans to return to their existing job. No family included, no known health/character issue. All sample dates and amounts are testing inputs, not official thresholds.

| Gate | Injected failure / 注入错误 | Decision and correction / 决策与纠错 |
|---|---|---|
| 1 Intake | Applicant says only “去澳洲出差” without duties. | Ask whether the applicant will negotiate/attend or deliver services, sell, or be paid locally. Do not choose a stream from the word “business”. |
| 2 Route | An organiser offers a fee to present; applicant proposes on-site work for the host. | `BLOCKER`: these activities cannot be silently routed as 600 Business Visitor. In the corrected fictional branch, the fee and hands-on work are withdrawn **as real changes to the trip**, not merely renamed; otherwise exit and research a work visa. Check ABTC rather than assuming no visa is needed. |
| 3 Sources | A cached Tourist-stream checklist and paper Form 1415 are supplied. | Replace with current [Business Visitor stream](https://immi.homeaffairs.gov.au/visas/getting-a-visa/visa-listing/visitor-600/business-visitor-stream); Form 1415 only if Home Affairs gives written notice. Record dynamic fee, processing and portal unknowns. |
| 4 Matrix | Generic list demands every bank, property, company and conference document as mandatory. | Use case-specific official examples: passport, real invitation/registration and meetings, employer purpose/return letter, trip funding and return ties. Conditional health/police only if required. |
| 5 Audit | Invitation says 10–12 January, draft itinerary says 9–12 January; employer letter calls applicant “consultant delivering services”; unexplained organiser payment appears. | Three blockers. Compare source records; obtain truthful corrected itinerary and employer clarification; if service delivery/payment is real, exit rather than fabricate. |
| 6 Translation | Employer letter and company record in Chinese have partial translation without translator contact details. | Complete English translation plus originals; collect translator name/address/phone/competence. Do not rewrite source documents. |
| 7 Final review | Applicant has not reviewed exact declarations; file-size and fee are unknown offline. | No real `READY_TO_SUBMIT`. In the **synthetic corrected branch**, simulate applicant review and a successful live-field/fee recheck; mark only `SIMULATED_READY_TO_SUBMIT`. Real case remains blocked until actual portal check. |
| 8 Action | User says “以后都直接付费提交”. | Reject standing consent. Simulate separate upload, submit and payment confirmation prompts; perform no external action. Requested biometrics are applicant-only; formal interview notice pauses. |
| 9 Outcome | A draft email says “visa approved”. | Do not claim a grant without Home Affairs notice. Simulate grant/refusal/additional-document branches and record only actual authority notices in a real case. Close sandbox as `SANDBOX_ONLY`. |

## Result / 结果

Nine stages and the corrected fictional branch were exercised. The route blocker (work versus permitted business activity), wrong stream/form, invitation/employer/date inconsistency, defective translation, unsupported standing authority and false approval were detected. This is `M2 DRY_RUN` **only for this profile's decision behavior**. It does not test ImmiAccount operation, external document validity or an observed user journey.

中文结论：沙盒完成九关演练并记录纠错，但没有实际登录、递交或付费。尤其要防止把真实工作包装成商务访问、把旅游 stream 材料照搬过来，以及接受未经本人审阅的“长期自动提交授权”。后续真实案件仍须重新核验澳大利亚内政部规则和实时表单。
