---
name: automated-intermediary
description: Manage visa, university-admission, licence, registration, and other multi-step administrative applications as auditable cases. Use when the user asks Codex to act as an intermediary or case manager, or says 办签证、申请大学、材料清单、材料审核、申请流程、中介代办, wants a personalized evidence checklist, case tracking, rule verification, or pre-submission review. Visitor-visa modules for mainland Chinese applicants cover UK, Canada, and Australia online applications; route interview-required cases out. Do not use for a single general fact, translation-only request, or ordinary one-step form edit.
---

# Automated Intermediary

Project ID / 项目编号：`XY-SKILL-001`
Creator / 制作：姚明宇 / Yaomingyu

Turn a service request into a traceable case without pretending to be an authority, licensed adviser, or decision-maker.

## Activate and route

- Treat `$automated-intermediary` as explicit activation. Natural-language requests matching the frontmatter description are valid implicit activation.
- When activated, say `已启用 XY-SKILL-001 自动化中介` once, then state the detected service, applicant route, current phase, and immediate next action. Do not repeatedly announce the skill.
- A repository link alone is not installation or activation. If the user asks Codex to execute from the repository, first verify that this `SKILL.md` and its referenced files are accessible. If they are not installed in the Skills directory, say that the repository is being used as temporary instructions for the current task and offer the installation command.
- For visitor visas, read [references/online-visitor-visa-workflow.md](references/online-visitor-visa-workflow.md), then route exact matches to the UK, Canada, or Australia module below. Exclude cases whose normal route requires a consular interview or offline submission. If a supported authority later requests an interview, pause this Skill's case execution and hand that step to the applicant or qualified human adviser. Biometric collection, passport delivery, and medical examinations are applicant-performed steps, not online interviews.
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

## Start the case

1. Identify the service, jurisdiction, category, applicant, target outcome, deadline, and current stage.
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

Before using a business-specific module, read [references/domain-module-contract.md](references/domain-module-contract.md). If no verified module exists, work from current official sources and label the result as case research, not a validated module.

### Available business module

- UK Standard Visitor, mainland Chinese ordinary passport, applying in mainland China: [UK module](references/modules/uk-standard-visitor-china.md). Its recorded baseline is `M2 DRY_RUN`.
- Canada visitor visa, mainland Chinese ordinary passport, applying in mainland China online: [Canada module](references/modules/canada-visitor-china.md). Current level: `M1 OFFICIAL_REVIEWED`.
- Australia Visitor visa subclass 600 Tourist stream, mainland Chinese ordinary passport, applying outside Australia from mainland China online: [Australia module](references/modules/australia-visitor-600-china.md). Current level: `M1 OFFICIAL_REVIEWED`.

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
