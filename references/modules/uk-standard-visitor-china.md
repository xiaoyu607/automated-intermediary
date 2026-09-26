# UK Standard Visitor — mainland China / 英国标准访客签证—中国大陆申请

Module ID: `uk-standard-visitor-china`

Last verified / 最后核验：2026-09-25  
Maturity / 成熟度：`M2 DRY_RUN` for the recorded ordinary-tourism baseline and four scripted branches; `M1 OFFICIAL_REVIEWED` for other conditional branches  
Refresh rule / 更新要求：before every live case and immediately before submission

## 1. Trigger and scope / 触发与范围

Use this module when all of the following are true:

- the applicant is a national of the People's Republic of China using an ordinary mainland Chinese passport;
- the applicant is physically applying from mainland China;
- the intended route is Standard Visitor;
- the intended stay is no more than six months;
- the baseline purpose is tourism or visiting family/friends.

Chinese nationals are visa nationals and normally need entry clearance before travelling. The application must be made online while outside the UK, with the required fee, identity document, and biometrics.

Do not use this baseline as the final workflow for:

- ADS Chinese tour groups;
- diplomatic or official passports;
- Hong Kong SAR, Macao SAR, Taiwan, BN(O), British, dual-national, or right-of-abode cases;
- transit, marriage/civil partnership, private medical treatment, organ donation, academics seeking 12 months, or English study lasting more than six months;
- employment, work placements, internships, or providing goods or services in the UK;
- applications made outside mainland China or permission-to-stay applications made inside the UK.

If UKVI requests an individual interview, pause this online-review workflow and hand the interview step to the applicant or a qualified human adviser. A VAC biometric appointment alone is not an interview.

Standard Visitor can include additional permitted activities, including some business, study, research, and permitted paid engagement activities. Detect these purposes and load the exact official activity rules before continuing; they are only M1 in this module.

## 2. Minimum intake / 最小建档问题

Collect only facts that change the route, evidence, timing, or risk:

1. Passport type, nationality, expiry, and whether the passport will be valid throughout the trip.
2. Exact main purpose, proposed arrival/departure dates, cities, accommodation plan, and estimated total cost.
3. Current residence in mainland China and the preferred visa application centre.
4. Employment, self-employment, study, retirement, unemployment, dependants, and ongoing financial commitments.
5. Who will pay; applicant funds and income; sponsor identity, relationship, immigration status, and promised support.
6. UK family or contacts, travelling companions, and whether any applicant is under 18.
7. Ten-year travel history when applicable, previous UK or other immigration refusals/problems, and criminal/civil/immigration offences.
8. Available passport, finance, employment/study/business, sponsor, relationship, itinerary, and accommodation evidence.
9. Language of each document and whether a compliant English/Welsh translation exists.

Do not collect full passport numbers, full bank account numbers, passwords, one-time codes, or payment details in a public or shared case record.

## 3. Eligibility gate / 资格关卡

Before drafting the form, confirm that the applicant can credibly show:

- they will leave the UK at the end of the visit;
- they will not make the UK their main home through frequent or successive visits;
- their main purpose is permitted and their planned activities match it;
- they will not work, access public funds, or do another prohibited activity;
- they can cover all reasonable trip, dependant, and return/onward travel costs, or have qualifying third-party support;
- the form, evidence, sponsor statements, finances, and itinerary tell one consistent story;
- no suitability issue has been hidden.

There is no fixed official minimum bank balance for a Standard Visitor. Assess whether income or savings, after ongoing commitments, reasonably cover the specific trip. Do not invent a universal number, number of months of bank statements, or “safe balance.”

If another person funds the visit, confirm a genuine relationship, what they will fund, their ability and willingness to do so, and their lawful UK status when relevant. Sponsorship does not replace the assessment of the applicant's own circumstances and intention to leave.

## 4. Workflow / 办理流程

1. **Route check** — confirm ordinary passport, main purpose, duration, application location, and exclusions.
2. **Current-rule refresh** — revisit every source in [uk-standard-visitor-china-sources.md](uk-standard-visitor-china-sources.md); update fee, processing time, portal, VAC provider, file restrictions, and policy dates.
3. **Eligibility review** — record `BLOCKER`, `WARNING`, and `ADVISORY` findings before collecting excess documents.
4. **Application timeline** — the earliest normal application point is three months before travel. Build in time for translation, appointment availability, document correction, and a decision delay.
5. **Evidence matrix** — create a tailored matrix from [../../assets/uk-standard-visitor-china-checklist.md](../../assets/uk-standard-visitor-china-checklist.md). Treat recommended evidence as case-dependent, not universally mandatory.
6. **Form drafting** — draft answers from verified facts. Cross-check trip cost, income, sponsor, addresses, family, travel history, refusals, and intended activities against evidence.
7. **Document preparation** — pair every non-English/Welsh document with a compliant full translation. Check legibility, full-page capture, ordering, dates, names, amounts, and source of funds.
8. **Pre-payment review** — show the current fee and refund consequences. As verified on 2026-09-25, the six-month Standard Visitor fee shown by GOV.UK was £135; refresh it before payment.
9. **User approval** — obtain immediate approval for the final form and payment. Do not submit or pay under general case-management permission.
10. **VAC and uploads** — after the visa application, book the instructed mainland China VAC. GOV.UK currently links China applicants to VFS Global. Recheck the live portal for centre, appointment, optional service, file-size, category, and upload rules.
11. **Biometrics** — the applicant attends as instructed with the required passport/travel document and provides fingerprints and a photograph. Each family member has a separate application, fee, and appointment requirement.
12. **Decision tracking** — normal published processing time was three weeks when verified, starting from identity verification/biometrics under the applicable process. Treat this as a service standard, not a guarantee.
13. **Outcome** — follow the decision message. If refused, do not automatically resubmit; map every refusal reason to evidence or facts, check whether circumstances or documentation changed, and identify appropriate professional review where needed.

Do not recommend non-refundable travel purchases before a decision. UKVI states applicants should not book travel until they receive a decision and does not reimburse losses caused by refusal or delay.

## 5. Evidence rules / 材料规则

### Required or process-essential

- valid passport or travel document covering the whole planned stay;
- online application information and truthful declarations;
- required fee;
- biometrics when required;
- any specific evidence generated by the live checklist or required by a special activity branch.

### Case-dependent supporting evidence

- purpose and itinerary information proportionate to the trip;
- employment, study, self-employment, retirement, or other home circumstances;
- finance showing access to funds and their origin;
- sponsor support, relationship, ability, willingness, and lawful UK status when relevant;
- previous passports/travel history;
- evidence of legal residence when applying outside one's nationality country;
- parental relationship, consent, travel, reception, and care arrangements for minors.

Official visitor guidance describes many of these as evidence an applicant “may want to provide,” not a universal mandatory bundle. Build the bundle around claims made in the form.

### Translation

A document not in English or Welsh must have a full translation that can be independently verified by the Home Office. Each translation must include:

- confirmation that it accurately translates the original;
- translation date;
- translator's full name and signature;
- translator's contact details.

Keep the source-language original and translation paired. Do not assume that a partial translation, self-created summary, app translation, or bilingual-looking document is sufficient without checking the complete document and translator declaration.

### Upload and names

The general UKVI self-upload guidance accepts PDF, PNG, JPG, and JPEG, requires the complete document to be visible, and asks for a descriptive filename. Applicants using a VAC may upload through the commercial partner instead, so check the live VFS rules before applying these formats or limits.

Internal naming convention, not a legal format:

`NN_Category_Applicant_Period_Language.ext`

Examples:

- `01_Passport_LI-MING.pdf`
- `10_Bank-Statement_LI-MING_2026-03_to_2026-08_CN.pdf`
- `11_Bank-Statement-Translation_LI-MING_2026-03_to_2026-08_EN.pdf`

Do not include more identity information in filenames than the portal and case management require.

## 6. Pitfall controls / 踩坑控制

### P1 — Unexplained recent deposits / 无法解释的近期大额入账

`WARNING`, upgraded to `BLOCKER` when the funds are necessary for affordability and their origin cannot be verified.

Check every material non-routine deposit against declared income and support. Record source, date, sender, reason, and supporting evidence. Never suggest temporarily borrowing money to inflate a balance.

### P2 — Form and evidence mismatch / 表格与材料不一致

`BLOCKER` until reconciled truthfully.

Cross-check annual income, employer, employment dates, trip cost, payer, accommodation, UK relatives, travel dates, refusals, and sponsor statements. Preserve the real fact and explain legitimate differences; do not edit evidence to force agreement.

### P3 — Sponsor treated as a guarantee / 把担保人当作获签保证

`WARNING`.

A sponsor letter alone does not prove the applicant is a genuine visitor. Review the applicant's own personal and economic circumstances, intention to leave, relationship with the sponsor, and both parties' consistent account of the visit.

### P4 — Trip cost is implausible / 旅行预算与收入不匹配

`WARNING` or `BLOCKER` depending on severity.

There is no fixed minimum balance. Compare trip cost and ongoing home commitments with reliable income, savings, and valid support. Ask for a truthful explanation when the planned spend is disproportionate.

### P5 — Weak or contradictory purpose / 访问目的薄弱或冲突

`BLOCKER` when the real purpose belongs to another route or includes prohibited work.

Make the main reason, duration, itinerary, funding, invitation, and applicant background coherent. Route study, paid engagements, business activities, medical treatment, marriage, and transit to their exact rules.

### P6 — Missing or defective translations / 缺翻译或翻译声明不完整

`BLOCKER` for every relied-upon non-English/Welsh document until the full translation and declaration fields are present.

### P7 — Relying on low-value evidence / 堆积低价值材料

`ADVISORY`.

Official guidance says some evidence is less useful, including ordinary hotel/flight bookings for a normal visit, personal photographs, car ownership, credit-card statements, and documents unrelated to the stated purpose. Do not use document volume as a substitute for relevant evidence.

### P8 — Non-refundable booking before decision / 未出结果先做不可退订

`WARNING`.

Use a plausible itinerary and budget, but do not tell the user to buy non-refundable travel merely to strengthen the application.

### P9 — Family application assumed to be shared / 误以为家庭共用一份申请

`BLOCKER` before submission.

Each family member needs an individual application and fee and must meet appointment requirements, even when evidence can be shared.

### P10 — Treating three weeks as a promise / 把三周处理时间当保证

`ADVISORY`.

The published processing time may be exceeded for verification, interviews, inaccurate information, extra evidence, demand, or outages. Preserve buffer time.

## 7. Confirmation gates / 用户确认点

Require immediate user confirmation before:

- finalising any answer about refusals, offences, family, funds, sponsors, or intended activity;
- submitting the online form;
- paying the visa fee or purchasing an optional VAC service;
- booking, changing, or cancelling the VAC appointment;
- uploading or disclosing personal documents;
- contacting UKVI, VFS, a sponsor, translator, employer, or other third party;
- withdrawing, changing, or resubmitting an application.

## 8. Session output / 每次会话输出

Report the case state, verified claims, missing evidence, blockers, warnings, next action and owner, deadline, fee/processing-time freshness, and sources to refresh. Never state “guaranteed,” “complete,” or “ready to submit” unless the evidence and confirmation state support that wording.

## 9. Tests / 测试

Read [uk-standard-visitor-china-tests.md](uk-standard-visitor-china-tests.md) when changing this module. The current M2 claim is limited to the documented fictional sandbox and scripted branch tests; it is not a real application result. The full recorded trace is linked from the test file.
