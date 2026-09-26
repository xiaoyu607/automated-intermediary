# 签证申请中介 / Visa Application Intermediary

**项目编号 / Project ID：`XY-SKILL-001`**

让申请人准备真实资料，由 Codex 接手签证申请的规则核验、材料审查、表格准备、纠错和递交跟进；关键动作由申请人确认，过程可追溯。——你的 AI 签证申请助手（姚明宇制作）

Prepare your genuine documents; let Codex handle visa-rule checks, evidence review, form preparation, corrections, and submission tracking, with your approval at consequential steps and an auditable record. Your AI visa-application assistant, created by Yaomingyu.

**范围 / Scope:** `XY-SKILL-001` 只处理签证申请。免签和非签证旅行许可只用于判断是否需要签证，不建立申请案件。 / `XY-SKILL-001` handles visa applications only. Visa-free travel and non-visa travel authorizations are screened but not managed as application cases.

## 这个 Skill 如何帮你 / How it helps

你只需说明申请目标、提供真实资料，并处理必须由本人完成的步骤。Codex 应当主动完成可代办的工作：核验当前官方要求，生成个人化材料清单，逐份检查并交叉核对材料，准备申请表答案与上传清单，修正自己能安全修正的格式或流程问题，跟进递交前后的状态。它不能凭空补写个人事实，也不会把未经核验的申请称为“已完成”。

Tell Codex your visa goal and provide genuine facts and documents. Codex should check current official requirements, build a personalised evidence list, cross-check documents, prepare form answers and an upload plan, fix safe formatting or workflow errors, and track the case. It must never invent applicant facts or claim an unverified application is complete.

**低打扰原则 / Low-interruption principle:** 不要求你反复核对同一份材料，也不把 Codex 自己可以排查的问题丢回给你。Codex 应先自行核验和复查，把真正缺失、矛盾或必须由你决定的问题集中提出；材料准备完成后，给你一份简明的最终申请摘要供审阅。若官方系统允许且已取得必要授权，Codex 可以协助推进至递交；提交、付款、预约、上传、法律声明或向第三方发送信息前，仍须就该次具体动作取得即时确认。指纹、面试、身份验证等必须本人完成的环节由申请人办理。

**Low-interruption principle:** Codex checks and rechecks its own work instead of repeatedly asking you to proofread the same material. It groups genuine missing facts, contradictions, and choices into concise questions, then presents a final application summary for your review. Where the official portal and available access allow, Codex can help progress the case through submission; each upload, submission, payment, booking, legal declaration, or third-party message still needs immediate action-specific approval. The applicant handles required biometrics, interviews, and identity checks.

这是一套**按具体签证路径逐步验证的测试版流程**，不是“所有国家、所有签证都能自动递交”的承诺。官方规则、实际表单、账号权限或现场要求可能使某一步无法由 Codex 操作；遇到这种情况，Codex 应明确说明已完成到哪里、剩余动作由谁执行，并给出可直接照做的交接清单。

This is a **route-specific beta**, not a promise of automatic submission for every country or visa type. If a rule, live form, account permission, or in-person requirement prevents Codex from acting, it must report the exact stopping point, owner, and handoff steps.

## 最简单的开始方式 / Quick start

安装后提供申请目标和已有资料，例如：

Once installed, state your visa goal and what you already have, for example:

```text
使用 $automated-intermediary 接手我在中国申请英国标准访客签证。
请核验最新官方规则，告诉我一次性需要准备哪些真实资料；
收到资料后自行审查、纠错、准备申请，并尽可能推进到递交。
只在事实缺失、本人必须操作或关键外部动作前向我确认。
```

```text
Use $automated-intermediary to manage my UK Standard Visitor visa application from China.
Check current official rules, tell me what genuine information and documents to prepare,
then review, correct, and prepare the application and help advance it to submission.
Ask me only for missing facts, required personal steps, and action-specific approvals.
```

## 当前状态 / Current status

> **Beta · route-specific maturity / 测试版 · 按路径标注成熟度**
> No completed live applicant case yet / 尚无真实申请人完整闭环
> Last official-source review / 最近官方来源核验：2026-09-26

当前面向中国大陆普通护照持有人、从中国大陆申请，包含以下已核对的访客路径；成熟度按具体路径区分：

- 英国 Standard Visitor：普通旅游与探亲访友的既有范围为 `M2 DRY_RUN`；
- 加拿大 Visitor Visa：线上申请及材料审核模块为 `M1 OFFICIAL_REVIEWED`；
- 澳大利亚 Visitor 600 Tourist stream（境外申请）：线上申请及材料审核模块为 `M1 OFFICIAL_REVIEWED`。
- 澳大利亚 Visitor 600 **Business Visitor stream**（商务访客，境外申请）：一位虚构在职成人的会议及合同洽谈案例为 `M2 DRY_RUN`；实际工作、提供服务及向公众销售不在该路线内。
- 申根个人旅游短期签证：欧盟共同规则与中国材料清单为 `M1 OFFICIAL_REVIEWED`；已核验法国、德国、意大利、西班牙、荷兰、瑞士的官方申请入口。每宗案件仍需按实际主目的国核验当期清单。
- 新西兰 Visitor Visa：单名成人旅游虚构案例达到 `M2 DRY_RUN`；其他申请人情况仅为 `M1 OFFICIAL_REVIEWED`，新申请使用当期官方线上系统；
- 沙特旅游 eVisa、印尼旅游 e-VOA、斯里兰卡旅游签证 ETA 路线：各为 `M1 OFFICIAL_REVIEWED`，付款、产品、入境口岸和动态表单仍须逐案核验；
- 肯尼亚 eTA 和柬埔寨限期免签仅保留在筛选资料中，不属于本 Skill 的签证申请执行模块。

Verified visa routes for mainland Chinese ordinary-passport holders applying from mainland China include UK Standard Visitor (`M2` baseline), Canada visitor, Australia's offshore Visitor 600 Tourist and **Business Visitor** streams (Business Visitor `M2` for one fictional adult case only), Schengen tourism, New Zealand Visitor Visa (`M2` for one fictional adult case only), Saudi eVisa, Indonesian e-VOA and Sri Lankan tourist visa via ETA. Kenya eTA and Cambodia's time-limited visa waiver are screening references only, not visa-application execution modules. All other profiles require fresh official checks; this is not worldwide coverage.

Codex 在线核验规则、审核材料和管理签证进度。Skill 先区分免签、ETA、电子签、完整线上签证、仅线上填表和强制代理路径；“线上填表”不等于“线上提交”，免签或非签证许可则不建立签证申请案件。申根签证可能要求申请人到签证中心递交材料、回答常规行程问题并录指纹；这不等于领馆正式面试。美国 B1/B2 常规需要面试，暂不纳入；日本旅游签在中国须经指定机构，不能由 Codex 独立替代。若任一受支持个案收到正式面试通知，Skill 暂停该案并提示人工处理。爱尔兰、塞浦路斯等非申根欧洲签证不在申根模块范围内。

Codex reviews visa rules and evidence remotely and distinguishes visa-free, ETA, eVisa, full online application, online-form-only and required-agency routes. Visa-free/non-visa authorization paths do not become application cases. Schengen applicants may have to lodge documents, answer routine trip questions, and provide fingerprints at a visa centre; these are distinct from a formal consular interview. US B1/B2 generally requires an interview and is outside scope. Japan's accredited-agency route cannot be independently replaced. A formal interview request pauses the automated case path. Ireland and Cyprus are not covered by the Schengen module.

## 能做什么 / What it does

- 建立带状态、任务、材料、风险、来源、决策和确认记录的案件；
- 根据申请人情况生成个性化材料矩阵，而不是复制通用中介清单；
- 检查身份、日期、有效期、可读性、完整性、来源、翻译和材料一致性；
- 将已核实的事实对应到申请表字段，准备表格答案、上传清单和递交交接步骤；
- 自行复查并修正安全、可逆的格式或流程错误；只把无法自行确认的事实问题交给申请人；
- 将问题区分为 `BLOCKER`、`WARNING` 和 `ADVISORY`；
- 在提交、付款、预约、上传、声明或向第三方发送信息前停止并取得即时确认；
- 保存来源与核验日期，便于官方规则变化后的更新与回归测试。

- Creates cases with states, tasks, evidence, risks, sources, decisions, and approval records.
- Builds applicant-specific evidence matrices instead of generic intermediary checklists.
- Checks identity, dates, validity, legibility, completeness, provenance, translation, and cross-document consistency.
- Maps verified facts to form fields and prepares form answers, an upload plan, and submission handoff steps.
- Rechecks and fixes safe, reversible formatting or workflow errors; escalates unresolved factual questions only.
- Classifies issues as `BLOCKER`, `WARNING`, or `ADVISORY`.
- Stops for immediate approval before submission, payment, booking, upload, declarations, or third-party disclosure.
- Records sources and verification dates for rule-change maintenance and regression testing.

## 安装 / Install

将仓库复制到 Codex Skills 目录：

Clone the repository into your Codex Skills directory:

```bash
git clone https://github.com/xiaoyu607/automated-intermediary.git ~/.codex/skills/automated-intermediary
```

随后可以这样开始：

Then start with:

```text
使用 $automated-intermediary 为我的申请建立案件并告诉我下一步。
```

```text
Use $automated-intermediary to create a case for my application and tell me the next action.
```

### 如何准确调用 / Reliable invocation

安装后，以下两种方式都会调用 Skill：

After installation, either form can invoke the Skill:

```text
使用 $automated-intermediary 管理我在中国申请英国标准访客签证的完整流程。
```

```text
我是中国大陆护照，在深圳申请英国旅游签。请作为中介接手，核验最新规则、审核材料并管理到提交前确认。
```

Codex 成功调用后，应先显示 `已启用 XY-SKILL-001 签证申请中介`，再说明识别到的签证路径、当前阶段和下一步。只发送 GitHub 链接不会自动安装或调用 Skill；必须先安装，或者明确要求 Codex 读取仓库中的 `SKILL.md` 并按其执行。仓库模式只对当前任务提供指令，不等同于永久安装。

After activation, Codex should show `已启用 XY-SKILL-001 签证申请中介`, then identify the visa route, current stage, and next action. Sending only the GitHub URL does not install or invoke the Skill. Install it first, or explicitly ask Codex to read the repository's `SKILL.md` and follow it for the current task; repository-mode use is temporary, not a permanent installation.

## 结构 / Structure

```text
automated-intermediary/
├── SKILL.md
├── agents/openai.yaml
├── assets/
│   ├── case-record-template.md
│   └── uk-standard-visitor-china-checklist.md
└── references/
    ├── case-model.md
    ├── source-policy.md
    ├── authorization-boundaries.md
    ├── low-interruption-execution.md
    ├── domain-module-contract.md
    ├── online-visitor-visa-workflow.md
    ├── test-scenarios.md
    ├── modules/
    └── evaluations/
```

## 模拟验证 / Simulated validation

完整 M2 沙盒从初次咨询运行到模拟的 `READY_TO_SUBMIT`，主动注入并检出了以下问题：

- 无法解释的近期大额入账；
- 表格与雇主材料收入不一致；
- 先前拒签史被遗漏并被要求隐藏；
- 银行材料只有部分翻译；
- 翻译缺少签名和联系方式；
- 用户要求长期授权 Codex 直接提交和付款；
- VFS 动态规则无法静态验证。

The recorded M2 sandbox ran from intake to simulated `READY_TO_SUBMIT` and detected all deliberately injected critical issues, including financial inconsistencies, omitted refusal history, defective translations, unsafe standing authorization, and unresolved dynamic portal rules.

- [完整沙盒报告 / Full sandbox report](references/evaluations/uk-standard-visitor-china-m2-sandbox-2026-09-25.md)
- [线上访客签证九关流程 / Online visitor visa nine-gate workflow](references/online-visitor-visa-workflow.md)
- [三国路由及完整虚构流程演练 / Three-country routing and complete fictional walkthrough](references/evaluations/online-visitor-visa-sandbox-2026-09-26.md)
- [申根模块 / Schengen tourism module](references/modules/schengen-tourism-china.md)
- [申根官方来源台账 / Schengen official source registry](references/modules/schengen-tourism-china-sources.md)
- [申根路由沙盒 / Schengen routing sandbox](references/evaluations/schengen-routing-sandbox-2026-09-26.md)
- [全球线上路径筛选 / Global online-route screen](references/global-online-route-screen.md)
- [新增路径沙盒与纠错 / Global route sandbox and correction log](references/evaluations/global-online-routes-sandbox-2026-09-26.md)
- [澳大利亚商务访客模块 / Australia Business Visitor module](references/modules/australia-business-visitor-600-china.md)
- [澳大利亚商务访客沙盒 / Australia Business Visitor sandbox](references/evaluations/australia-business-visitor-sandbox-2026-09-26.md)
- [非旅游签证扩展队列 / Non-tourism visa expansion queue](references/non-tourism-visa-expansion.md)
- [模块测试集 / Module test set](references/modules/uk-standard-visitor-china-tests.md)
- [官方来源台账 / Official source registry](references/modules/uk-standard-visitor-china-sources.md)

## 安全与边界 / Safety and boundaries

本项目不是政府机构、签证决定者或持牌法律意见提供者。它不能保证获签，也不能替代申请人对事实和声明承担的责任。

This project is not a government authority, visa decision-maker, or provider of licensed legal advice. It cannot guarantee an outcome and does not replace the applicant's responsibility for facts and declarations.

请勿在公开仓库、Issue 或测试报告中提交真实护照、银行、移民、教育、工作、医疗、账号、密码、验证码或付款资料。

Never place real passport, banking, immigration, education, employment, medical, account, password, one-time-code, or payment data in a public repository, issue, or test report.

## 贡献与复用 / Contributing and reuse

欢迎提交脱敏测试案例、官方规则更新和可复现的错误报告。新增国家或签证类型模块时，请明确适用范围、官方来源、验证日期和成熟度，不要把单一案例外推为全部签证业务已经验证。

Sanitised test cases, official-rule updates, and reproducible bug reports are welcome. New country or visa-category modules must state their exact scope, first-party sources, verification date, and maturity level. Never generalise one observed case into universal validation.

## 许可 / License

MIT License. See [LICENSE](LICENSE).
