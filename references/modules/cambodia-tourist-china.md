# Cambodia tourism: temporary waiver or eVisa / 柬埔寨旅游：限期免签或电子签

Module ID: `cambodia-tourist-china` · Maturity: `M1 OFFICIAL_REVIEWED` for **2026-09-26 routing**, not post-expiry policy · Verified: 2026-09-26.

Scope: mainland Chinese ordinary-passport holder, individual tourism from China. First determine intended arrival date and stay length. The [Cambodia official eVisa portal](https://www.evisa.gov.kh/) currently announces a Chinese-passport tourist visa exemption **only from 2026-06-15 through 2026-10-15, for stays up to 14 days per entry**. It says an e-Arrival card is still required. Outside those exact conditions, do not extend the waiver: re-open the official eVisa nationality and Visa T route before giving a checklist or taking payment. Business/other purposes and formal interview requests exit this module.

Follow the [shared nine gates](../online-visitor-visa-workflow.md). For an in-window ≤14-day case, classify `VISA_FREE`, build an entry-preparation matrix (passport, itinerary, stay, e-Arrival, live border requirements), and **do not** direct the user to pay for a tourist eVisa. For an out-of-window or >14-day case, classify `UNKNOWN_PENDING_LIVE_CHECK`; if official portal confirms Visa T eligibility, use its live application, fee, document and checkpoint rules, with immediate consent for submission/payment. Check the issued eVisa and entry point where relevant. A sandbox must not actually file e-Arrival or an eVisa.

`BLOCKER`: assuming the temporary waiver applies after 2026-10-15 or to a longer stay; misclassifying e-Arrival as a visa; charging for an exempt case. `WARNING`: temporary-policy changes; reverify at case intake and just before travel. `ADVISORY`: internal file naming is not a Cambodian rule.

## 中文执行摘要

先核对入境日期与停留时长：仅在官方公告的 2026 年 6 月 15 日至 10 月 15 日、每次不超过 14 天的中国游客路径，按临时免签处理，但仍需填写电子入境卡；不要让符合条件者支付旅游签费用。超出日期或时长时先标 `UNKNOWN_PENDING_LIVE_CHECK`，再核对当期官方 Visa T 或其他政策，不能自动套用旧规则。
