# Global online visitor-route screen / 全球线上访客路径筛选

Scope / 范围：mainland Chinese ordinary-passport holder, resident in and applying from mainland China, short tourism. Verified 2026-09-26. This is a **screening register, not a worldwide completeness claim**. Refresh each official source and the live nationality/purpose selector before advising a real applicant.

## Decision sequence / 判断顺序

1. Confirm passport, residence, application country, tourism purpose, dates, entry point, and any existing visa/residence permit that changes eligibility.
2. Check the destination's current official entry rules. Distinguish `VISA_FREE`, `ETA`, `EVISA`, `ONLINE_FULL_VISA`, `ONLINE_FORM_ONLY`, `IN_PERSON_OR_AGENCY`, and `UNKNOWN`. An online form is not proof of online submission.
3. Check for a routinely required **formal individual interview**. If yes, exclude from this automated execution scope; biometrics, ordinary counter questions, and border questioning are not by themselves such an interview. An individual interview request stops the affected case.
4. Select an exact verified module only if its profile matches. Otherwise conduct labelled case research; do not improvise a checklist or claim coverage.
5. Before payment or submission, recheck temporary exemptions, portal eligibility, passport/entry-point conditions, fees and live form prompts. Obtain immediate user confirmation.

中文要点：先确认护照类型、居住地、目的、日期和入境口岸；再按官方来源区分免签、ETA、电子签、完整线上签证、仅线上填表及强制代理。只有完全匹配已核验模块的案件才能使用该模块。任何正式个人面试通知都使自动执行暂停；付款和提交前必须重新核对动态规则并即时征得同意。

## Reviewed routes / 已核对路径

| Destination | Classification for this profile | Skill status | First-party evidence and caveat |
|---|---|---|---|
| New Zealand / 新西兰 | `ONLINE_FULL_VISA` Visitor Visa | [M2 single-profile dry run](modules/new-zealand-visitor-china.md); other profiles M1 | [INZ Visitor Visa](https://www.immigration.govt.nz/visas/visitor-visa/), [China guide](https://www.immigration.govt.nz/process-to-apply/applying-for-a-visa/providing-evidence-and-documents-to-support-your-visa-application/application-guide-for-visitor-visas-for-citizens-of-china/); enhanced Immigration Online became the route for most new visitor applications on 2026-09-24. |
| Saudi Arabia / 沙特阿拉伯 | `EVISA` tourism | [M1 module](modules/saudi-tourist-evisa-china.md) | [Ministry of Tourism eVisa terms](https://visa.visitsaudi.com/Home/TermsConditions) include China and online issue; no work permission. |
| Indonesia / 印度尼西亚 | `EVISA` e-VOA for eligible tourism | [M1 module](modules/indonesia-evoa-china.md) | [Immigration FAQ](https://jakartapusat.imigrasi.go.id/faqs) lists Tiongkok among e-VOA nationalities and [official portal](https://evisa.imigrasi.go.id/); recheck current B1 product and ports. |
| Sri Lanka / 斯里兰卡 | `ETA` short tourism | [M1 module](modules/sri-lanka-tourist-eta-china.md) | [Immigration ETA home](https://eta.gov.lk/slvisa/visainfo/center.jsp?locale=en_US), [application instructions](https://eta.gov.lk/slvisa/visainfo/apply.jsp?locale=en_US); check current China fee in live selector. |
| Kenya / 肯尼亚 | `ETA` tourism for PRC ordinary passports, subject to live eligibility selector | [M1 module](modules/kenya-tourist-eta-china.md) | [Immigration eTA application guide](https://etakenya.go.ke/how-to-apply) exempts specified **Chinese diplomatic/official/service** passports, not ordinary passports; verify current route in the official selector. |
| Cambodia / 柬埔寨 | temporary `VISA_FREE` if stay ≤14 days and entry 2026-06-15 to 2026-10-15; otherwise assess `EVISA` | [M1 conditional module](modules/cambodia-tourist-china.md) | [Official eVisa portal notice](https://www.evisa.gov.kh/) states time-limited Chinese tourist waiver and e-Arrival obligation. Never auto-charge for a waived route. |
| Singapore / 新加坡 | `VISA_FREE` ≤30 days, PRC ordinary passport | entry-preparation only, no visa module | [ICA bilateral arrangement](https://www.ica.gov.sg/news-and-publications/newsroom/media-release/mutual-30-day-visa-exemption-arrangement-between-singapore-and-the-people-s-republic-of-china). |
| Japan / 日本 | `IN_PERSON_OR_AGENCY` tourism eVisa from China | no independent submission module | [MOFA eVisa](https://www.mofa.go.jp/j_info/visit/visa/visaonline.html): accredited agency required for Chinese nationals resident in China; Codex may pre-audit but cannot replace that channel. |
| South Korea / 韩国 | `ONLINE_FORM_ONLY` for relevant short-stay consular route | no online-submission module | [Korea Visa Portal](https://www.visa.go.kr/openPage.do?LLANG=EN&MENU_ID=10204): printed barcode form and documents must be brought to diplomatic mission. |
| United States / 美国 | routine formal interview for first-time B1/B2 | excluded | [State Department interview-waiver update](https://travel.state.gov/content/travel/en/News/visas-news/interview-waiver-update-sept-18-2025.html). Limited renewals may be exempt but are not a validated module. |
| Türkiye / 土耳其 | `UNKNOWN` for online route; do not infer eVisa eligibility | no module | [Official eligible-country list](https://www.evisa.gov.tr/en/info/who-is-eligible-for-e-visa/) did not list China at review. Recheck current ordinary-passport entry arrangements separately. |
| Vietnam / 越南 | `UNKNOWN` for Chinese ordinary **e-passport** | no module | [New eVisa portal](https://evisa.gov.vn/) and [old portal redirect](https://evisa.xuatnhapcanh.gov.vn/) exist, but an [older official nationality PDF](https://evisa.xuatnhapcanh.gov.vn/documents/20181/117155/Vietnam-Evisa-nation-list-Vi.pdf/7611c905-0370-45e9-8080-cd0dec11df95) excludes Chinese e-passports. Do not apply that historical PDF as current law or claim the current eligibility is settled. |

## Further discovery / 后续排查

India, Russia, Azerbaijan, Tanzania, Egypt, Oman, Bahrain, and other destinations have online-entry leads, but this release has **not** completed exact China-passport tourist eligibility, current exemptions, interview routing, portal/entry-point checks, and end-to-end modules for them. Do not promote a search result or general eVisa website into a supported route. Check official portals country by country. Ireland and Cyprus are not Schengen; assess separately.

## Maintenance / 维护

For each route, store the official link, claim, applicant profile, date checked, next review date, and decision/test affected. Recheck dynamic policies immediately before a live case and submission. Time-limited exemptions require an expiry regression: on and after the end date, automatically revert to `UNKNOWN` until the current official route is reverified. No actual applicant identity data belongs in this register.

中文维护规则：每条结论记录官方链接、适用人群、核验日期、下次复核日期及受影响测试。限期免签到期后先恢复为 `UNKNOWN`，不得沿用旧结论。公开台账不保存真实申请人的身份材料。
