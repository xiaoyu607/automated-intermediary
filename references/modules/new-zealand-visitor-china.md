# New Zealand Visitor Visa / 新西兰访客签证（中国大陆申请）

Module ID: `new-zealand-visitor-china` · Maturity: `M2 DRY_RUN` **only for the fictional single-adult tourism profile recorded in the [sandbox](../evaluations/global-online-routes-sandbox-2026-09-26.md)** · Verified: 2026-09-26. No live portal submission, applicant observation, or independent end-to-end user test.

## Scope / 适用范围

Mainland Chinese ordinary-passport holder resident in mainland China, applying there online for a short tourist visit. If the trip's real purpose is business, study, work, medical treatment, joining family, or a special NZeTA eligibility route, stop and re-route. A group-tour/ADS route is not this individual module. An individual formal interview request pauses execution.

## Intake and eligibility / 建档与资格

Ask purpose, dates, travel companions/minors, passport validity, prior New Zealand stays, funds and payer, accommodation, departure plan, employment/study/family ties, immigration/refusal history, health/character issues, and language of every document. Check genuine visit, ability to fund stay and departure, identity, health, character, and the live visitor conditions; do not promise a grant or invent a universal bank-balance threshold.

## End-to-end / 完整路径

1. Run the [shared nine gates](../online-visitor-visa-workflow.md) and check the [official Visitor Visa page](https://www.immigration.govt.nz/visas/visitor-visa/) plus [China guide](https://www.immigration.govt.nz/process-to-apply/applying-for-a-visa/providing-evidence-and-documents-to-support-your-visa-application/application-guide-for-visitor-visas-for-citizens-of-china/). Check the [2026 portal migration notice](https://www.immigration.govt.nz/about-us/news-centre/important-visitor-visa-application-form-changes/); new applications for most visitor visas moved to enhanced Immigration Online on 2026-09-24.
2. Generate the exact online checklist. Matrix: passport/photo and identity; travel purpose/itinerary; funds and outward travel; ties and leave/employment where relevant; sponsor/relationship/minor documents only when triggered; health/police documents only when required or requested. Use the [China tourism-only checklist](https://www.immigration.govt.nz/assets/inz/documents/checklists/china/checklist-for-china-visitor-visa-less-than-6-months.pdf) only within its stated <6-month tourism scope. Distinguish checklist guidance from live portal-required uploads.
3. Translate **every** non-English supporting document fully and retain the source. [INZ translation rules](https://www.immigration.govt.nz/process-to-apply/applying-for-a-visa/providing-evidence-and-documents-to-support-your-visa-application/providing-english-translations-of-supporting-documents/) say visitor supporting translations generally need not be certified, but medical/police certificates do. The applicant, family member, or adviser on the case must not translate; record translator name, address, phone, and language qualifications/experience. Check name spelling and aliases. Partial bank-statement translation is a blocker.
4. Audit form answers against evidence: passport spelling, dates, intended stay, family, employment, source of funds, refusals and departure means. Recheck file formats, fee and current prompts in the live portal; filename pattern is internal practice only.
5. Show the applicant the exact draft and attachments. Obtain fresh confirmation for upload, submission and payment. No real action occurs in a dry run.
6. Track status and official requests. Applicant completes any personal medical/identity step. Stop at a formal interview. On written decision, record eVisa conditions or refusal reasons; verify passport linkage and departure/arrival instructions.

## Failure controls / 踩坑

- `BLOCKER`: wrong visitor category; omitted refusal; identity/date mismatch; incomplete translation; missing mandatory portal item; purported permission for work.
- `WARNING`: assuming a health/police document or in-person step is always/never needed; relying on the old portal after migration; paying or booking non-refundable travel before decision.
- `ADVISORY`: `Category_Applicant_Date_Language.ext` is an internal filing convention, not an INZ rule.

Refresh portal, fees, processing times, translations, checklist and any interview/medical request before a live case. See [source policy](../source-policy.md) and [authorization boundaries](../authorization-boundaries.md).

## 中文执行摘要

适用于在中国大陆申请个人旅游访客签证的中国普通护照持有人；团队旅游、商务、工作、学习及特殊 NZeTA 路径需另行分流。依次核对官方签证页、中国申请指南、当期线上系统和材料提示；建立身份、行程、资金、离境能力、国内联系及条件材料矩阵；逐项比对表格与证据。所有非英文材料都需完整英文翻译并附原件，普通访客支持材料通常不要求认证翻译，但医疗和无犯罪证明例外；申请人、家属及本案顾问不能自行翻译。材料问题改正后，仍须由申请人审阅，并在上传、提交、付款前分别即时确认。收到正式面试通知即暂停。这里的 `M2` 仅证明单名成人虚构案例的流程模拟，不证明真实门户或获签结果。
