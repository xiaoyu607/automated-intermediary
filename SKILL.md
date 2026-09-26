---
name: automated-intermediary
description: Manage visa applications as auditable cases for mainland Chinese applicants. Use for 签证申请、旅游签、商务签、学生签、材料清单或审核、签证流程、中介代办 when the user wants eligibility screening, official-rule verification, case tracking, or pre-submission review. Execute only exact verified visa modules; pause if an individual formal interview is required. Do not use for university admission, licences, registrations, visa-free travel planning, translation-only, or one-step facts.
---

# Automated Intermediary

Project ID / 项目编号：`XY-SKILL-001`
Creator / 制作：姚明宇 / Yaomingyu

Turn a **visa application** into a traceable, low-interruption case without pretending to be a visa authority, licensed immigration adviser, or decision-maker. The applicant supplies genuine facts and evidence; Codex owns rule research, document checks, draft preparation, safe corrections, and case tracking. Other application types are outside this Skill.

## Activate and route

- Treat `$automated-intermediary` as explicit activation. Natural-language requests matching the frontmatter description are valid implicit activation.
- When activated, say `已启用 XY-SKILL-001 签证申请中介` once, then state the detected visa category, applicant route, current phase, and immediate next action. Do not repeatedly announce the skill.
- A repository link alone is not installation or activation. If the user asks Codex to execute from the repository, first verify that this `SKILL.md` and its referenced files are accessible. If they are not installed in the Skills directory, say that the repository is being used as temporary instructions for the current task and offer the installation command.
- For visitor visas, read [references/online-visitor-visa-workflow.md](references/online-visitor-visa-workflow.md) and [references/global-online-route-screen.md](references/global-online-route-screen.md), then route exact matches to a module below. First distinguish visa-free, ETA, eVisa, full online visa, online-form-only and mandatory agency/in-person submission. If the traveller is visa-free or only needs a non-visa travel authorization, state that no visa application is needed and end this Skill's case-management path; the screen remains a historical decision aid, not authorization to manage entry-card/eTA tasks. The Skill's research and evidence review can be online even when the applicant must personally lodge documents, answer routine counter questions, give biometrics, or deliver a passport. Exclude routes with a routine formal consular interview. If an authority requests an individual interview, pause this Skill's execution for that case and hand the interview step to the applicant or qualified human adviser.
- For non-tourism visas, identify the exact country, category, applicant and application location. Read [references/non-tourism-visa-expansion.md](references/non-tourism-visa-expansion.md). Use a verified module only on an exact match; otherwise provide labelled source research and a proposed test plan, never a completed application workflow.
- Read [references/test-scenarios.md](references/test-scenarios.md) when changing discovery, activation, routing, or core behavior.

## Use the workflow contract

Keep every case within this sequence. Do not skip a stage merely because the user asks for a final checklist:

1. Intake and scope.
2. Route and eligibility screen.
3. Current official-rule verification.
4. Personalized plan and evidence matrix.
5. Evidence review and consistency checks.
6. Blocker correction and recheck.
7. Final package review with the applicant.
8. Immediate confirmation for each submission, payment, booking, upload, declaration, or third-party message.
9. Closure, outcome recording, and rule-update follow-up.

At each response, expose the current stage, verified facts, unresolved blockers, and one concrete next action. Ask only questions that are necessary for the current decision gate.

## Minimize applicant effort without hiding risk

- Read [references/low-interruption-execution.md](references/low-interruption-execution.md) for the handoff contract. Do not ask the applicant to repeatedly proofread the same evidence or repair Codex's own checklist, formatting, or routing errors.
- Extract facts from supplied evidence, map every material form answer to its source, and cross-check dates, names, finances, travel plans, and declarations. Re-run affected checks after each correction. Never invent, alter, or silently reconcile applicant facts.
- Resolve safe, reversible formatting and workflow errors yourself. Batch unresolved factual questions and choices into one concise request when practical; ask again only if new evidence or rules create a new material issue.
- Before final review, show a concise application summary, source-linked exceptions, and the exact remaining personal steps. Let the applicant review material declarations without forcing line-by-line reapproval of unchanged fields.
- If the official portal, account access, or applicant-only requirement prevents Codex from completing an action, state the exact stopping point and provide a precise applicant handoff. Do not describe a prepared draft as submitted.

## Start the case

1. Identify the visa jurisdiction, category, applicant, application location, target outcome, deadline, and current stage.
2. Ask only for missing facts that materially change eligibility, required evidence, timing, cost, or risk. Never ask the user to paste passwords, one-time codes, full payment credentials, or unnecessary identity data.
3. If this is a new case, offer to create a private case record from [assets/case-record-template.md](assets/case-record-template.md). Do not create files unless the user asks to begin or manage the case.
4. Read [references/case-model.md](references/case-model.md) when creating, resuming, or changing a case state.

## Establish the rule set

Before giving case-specific requirements or executing a live case:

1. Find current first-party sources for the exact jurisdiction, service category, application location, and applicant profile.
2. Separate binding requirements, official operational guidance, and internal best practice. Never present a convention or community report as law.
3. Record the source URL, page title, applicable scope, publication/update date when available, and verification date.
4. If rules may have changed, browse again even when a local reference exists. Read [references/source-policy.md](references/source-policy.md) for source ranking, conflict handling, and freshness.
5. State uncertainty and stop the affected branch when an important fact cannot be verified.

## Build and run the plan

Produce only the detail useful at the current stage:

- a personalized requirement and eligibility summary;
- a staged task plan with owners, dependencies, deadlines, costs, and status;
- an evidence register showing required, optional, missing, invalid, expiring, translated, and verified items;
- risks classified as `BLOCKER`, `WARNING`, or `ADVISORY`;
- a decision log that explains why the next action is appropriate;
- a concise next-action list.

For each evidence item, check identity, date, validity, legibility, completeness, provenance, translation, and consistency with forms and other evidence. Do not infer facts merely to make documents agree.

Before using a visa-specific module, read [references/domain-module-contract.md](references/domain-module-contract.md). If no verified module exists, work from current official sources and label the result as case research, not a validated module.

### Available visa modules

- UK Standard Visitor, mainland Chinese ordinary passport, applying in mainland China: [UK module](references/modules/uk-standard-visitor-china.md). Its recorded baseline is `M2 DRY_RUN`.
- Canada visitor visa, mainland Chinese ordinary passport, applying in mainland China online: [Canada module](references/modules/canada-visitor-china.md). Current level: `M1 OFFICIAL_REVIEWED`.
- Australia Visitor visa subclass 600 Tourist stream, mainland Chinese ordinary passport, applying outside Australia from mainland China online: [Australia module](references/modules/australia-visitor-600-china.md). Current level: `M1 OFFICIAL_REVIEWED`.
- Australia Visitor visa subclass 600 **Business Visitor stream**, mainland Chinese ordinary passport, applying outside Australia from mainland China online for permitted business visitor activities: [Business Visitor module](references/modules/australia-business-visitor-600-china.md). `M2 DRY_RUN` only for the recorded fictional employed-adult conference/contract-meeting case; no live portal or real applicant tested.
- Schengen short-stay individual tourism, mainland Chinese ordinary passport, applying in mainland China: [Schengen module](references/modules/schengen-tourism-china.md). The common EU/China rules and official entry points for France, Germany, Italy, Spain, Netherlands and Switzerland are `M1 OFFICIAL_REVIEWED`; each live case must open the competent country's current checklist.
- New Zealand Visitor Visa, mainland Chinese ordinary passport, individual tourism from China: [New Zealand module](references/modules/new-zealand-visitor-china.md), `M2 DRY_RUN` only for its recorded fictional single-adult tourism profile; broader route remains first-party reviewed, not live tested.
- Saudi tourist eVisa, same applicant profile: [Saudi module](references/modules/saudi-tourist-evisa-china.md), `M1 OFFICIAL_REVIEWED`.
- Indonesia tourist e-VOA, same applicant profile: [Indonesia module](references/modules/indonesia-evoa-china.md), `M1 OFFICIAL_REVIEWED` for route screening; live product/portal details must be rechecked.
- Sri Lanka tourist ETA, same applicant profile: [Sri Lanka module](references/modules/sri-lanka-tourist-eta-china.md), `M1 OFFICIAL_REVIEWED`.
- Kenya eTA and Cambodia's time-limited visa waiver are **screening-only historical references**, not visa-application execution modules. Do not open a visa application case solely to complete those travel authorizations or entry cards.

Read the selected module's official-source registry before giving case-specific requirements. A completed cross-country fictional walkthrough does not upgrade an untested portal or a real case to `M2`.

## Control consequential actions

Read [references/authorization-boundaries.md](references/authorization-boundaries.md) before any external write, submission, payment, booking, signature, legal declaration, or message to a third party.

Always show the exact proposed action and obtain the user's confirmation immediately before a consequential or irreversible step. Earlier permission to manage the case is not standing permission to submit, pay, book, sign, or send. Stop when an action legally or operationally requires the applicant in person.

## Complete or pause

At the end of each working session, report:

- current case state;
- what was verified or changed;
- unresolved blockers and warnings;
- the next action, owner, and deadline;
- sources that need rechecking before submission.

Match the user's language. For reusable public artifacts, provide Chinese and English unless the user requests another language policy. Never place real applicant data, credentials, or unredacted evidence in a public repository.
