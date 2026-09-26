# Cambodia tourism: temporary waiver or eVisa / 柬埔寨旅游：限期免签或电子签

Archive status: `SCREENING_ONLY` for the dated visa-waiver decision, verified 2026-09-26. The waiver branch is not a visa application and is not executable under this visa-only Skill. A post-waiver Visa T application is **unbuilt** and must not inherit `M1`.

Scope: mainland Chinese ordinary-passport holder, individual tourism from China. First determine intended arrival date and stay length. The [Cambodia official eVisa portal](https://www.evisa.gov.kh/) currently announces a Chinese-passport tourist visa exemption **only from 2026-06-15 through 2026-10-15, for stays up to 14 days per entry**. It says an e-Arrival card is still required. Outside those exact conditions, do not extend the waiver: re-open the official eVisa nationality and Visa T route before giving a checklist or taking payment. Business/other purposes and formal interview requests exit this module.

For an in-window ≤14-day case, classify `VISA_FREE` and state that no tourist visa application should be opened under this Skill; e-Arrival is separate and not executed here. For an out-of-window or >14-day case, classify `UNKNOWN_PENDING_LIVE_CHECK`. Do **not** use this archived note to execute Visa T: a new official-source review, visa-specific module and sandbox are needed first.

`BLOCKER`: assuming the temporary waiver applies after 2026-10-15 or to a longer stay; misclassifying e-Arrival as a visa; charging for an exempt case. `WARNING`: temporary-policy changes; reverify at case intake and just before travel. `ADVISORY`: internal file naming is not a Cambodian rule.

## 中文执行摘要

先核对入境日期与停留时长：仅在官方公告的 2026 年 6 月 15 日至 10 月 15 日、每次不超过 14 天的中国游客路径，按临时免签处理，不建立签证案件；电子入境卡属于本 Skill 范围之外。超出日期或时长时标 `UNKNOWN_PENDING_LIVE_CHECK`，先核对当期官方 Visa T 或其他政策，尚不能启动自动办理。
