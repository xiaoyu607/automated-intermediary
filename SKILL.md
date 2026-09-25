---
name: automated-intermediary
description: Manage complex service applications as auditable cases. Use when a user wants Codex to act like an intermediary or case manager for a multi-step application such as a visa, university admission, licence, registration, or similar administrative service. Do not use for a single factual question or ordinary one-step form edit.
---

# Automated Intermediary

Turn a service request into a traceable case without pretending to be an authority, licensed adviser, or decision-maker.

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

- For a mainland Chinese ordinary-passport holder applying in mainland China for a UK Standard Visitor visa, read [references/modules/uk-standard-visitor-china.md](references/modules/uk-standard-visitor-china.md). Its M2-tested baseline covers tourism and visits to family or friends for up to six months; follow its routing rules for other purposes.

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
