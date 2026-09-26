# Schengen tourism routing sandbox / 申根个人旅游路由沙盒

Date: 2026-09-26. All applicant facts, evidence and authority messages are fictional. This text exercise made no appointment, application, payment or government submission and did not test a live centre or portal. It checks the common route and interview boundary; the Schengen module remains `M1 OFFICIAL_REVIEWED`.

## Fictional case / 虚构案件

`TEST-SCH-CN-001`: adult ordinary PRC-passport holder residing in Shenzhen. Planned ten-day individual tourism: France six nights, Germany four nights, departing from China and entering Schengen through Germany. Initially asks to apply to Germany because its appointment appears earlier. Works in Shenzhen, pays for the trip, has bank statements and a Chinese employer letter. The first draft includes a cancelled hotel reservation and insurance covering only France. No prior Schengen stay in the past 180 days is stated; that claim still requires applicant confirmation.

| Gate | Decision and correction | Result |
|---|---|---|
| 1. Intake | Collect passport, residence, all destinations/nights, purpose, dates, travel history, job, funds, companions and evidence languages. | PASS |
| 2. Route | France is the longest stay and main destination. German first entry does not make Germany competent. Switch to France and verify the applicable French consular district and TLS centre. | Wrong-country `BLOCKER` detected; PASS |
| 3. Sources | Check EU common rules, 2024 China harmonised list and France-Visas China. Leave the live France-Visas generated checklist, TLS appointment stock and fee display for action-time refresh. | No unsupported live claim; PASS |
| 4. Matrix | Require the passport/form/photo, itinerary, accommodation, travel medical insurance and financial/return evidence under applicable sources. Check used hukou pages, recent current-account statements and employer letter with translation for this employed profile. | PASS |
| 5. Evidence | Detect cancelled accommodation and France-only insurance; compare hotel dates, transit and flight reservations to the ten-day route. | Two `BLOCKER`s; PASS |
| 6. Correction | Fictional applicant supplies valid accommodation covering both countries and Schengen-wide insurance with the required cover; employment translation is paired with the original. | Text-level blockers resolved; PASS |
| 7. Final review | Present the corrected route and document matrix to the fictional applicant; mark the live France checklist and centre instructions `UNKNOWN` until opened in a real case. | No claim of real submission readiness; PASS |
| 8. Applicant action | Applicant would personally sign/lodge documents and provide fingerprints at the centre after immediate appointment/payment approval. Routine trip questions at the counter are not treated as a formal interview. | No actual external action; PASS |
| 9. Outcome | A mock written refusal would trigger reason-by-reason review and France-specific appeal instructions; a mock grant would trigger visa-sticker checks. A separate formal interview notice stops automated execution. | Both branches routed; PASS |

## Correction log / 纠错记录

| Risk | Change made | Check |
|---|---|---|
| Earlier release excluded every Schengen case because lodging was in person. | Scope now distinguishes remote Codex review from the applicant's centre visit. | Gates 2 and 8 |
| First entry could be mistaken for the application country even when another state is the main destination. | Competent-state gate precedes checklist generation. | Gate 2 |
| A single EU checklist could be mistaken for every country's full operational list. | Destination source and live generated checklist are required. | Gates 3 and 7 |
| Routine counter questions could be mistaken for a formal interview. | Only a specific formal interview request exits the workflow. | Gate 8 and outcome branch |

This run supports routing and document-review logic only. It does not establish portal compatibility, appointment availability, real-world completion, or visa outcome.
