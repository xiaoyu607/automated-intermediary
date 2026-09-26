# 自动化中介 / Automated Intermediary

**项目编号 / Project ID：`XY-SKILL-001`**

将签证和大学申请等中介业务封装为可审计的 Codex Skill：完整沙盒模拟、官方规则持续更新、材料审查与提交前确认。——你的 AI 中介助手（姚明宇制作）

Turn visa, university admission, and other intermediary services into an auditable Codex Skill with complete sandbox simulations, continuously updated official rules, evidence review, and pre-submission confirmation — your AI intermediary assistant, created by Yaomingyu.

## 当前状态 / Current status

> **Beta · route-specific maturity / 测试版 · 按路径标注成熟度**
> No completed live applicant case yet / 尚无真实申请人完整闭环
> Last official-source review / 最近官方来源核验：2026-09-26

当前包含三条面向中国大陆普通护照持有人、从中国大陆申请的线上访客签证路径：

- 英国 Standard Visitor：普通旅游与探亲访友的既有范围为 `M2 DRY_RUN`；
- 加拿大 Visitor Visa：线上申请及材料审核模块为 `M1 OFFICIAL_REVIEWED`；
- 澳大利亚 Visitor 600 Tourist stream（境外申请）：线上申请及材料审核模块为 `M1 OFFICIAL_REVIEWED`。

Three online visitor-visa routes now cover mainland Chinese ordinary-passport holders applying from mainland China: UK Standard Visitor (`M2 DRY_RUN` baseline), Canada Visitor Visa (`M1 OFFICIAL_REVIEWED`), and Australia's offshore Visitor 600 Tourist stream (`M1 OFFICIAL_REVIEWED`). Maturity applies only to each route and tested scenario.

这轮只覆盖正常流程无需面试的线上申请与审核。美国 B1/B2、经指定机构申请的日本旅游签、需要窗口递交的申根短期签证暂不纳入。录指纹、体检或递交护照由申请人按官方通知完成；若某一英/加/澳个案收到面试通知，Skill 暂停该个案并提示人工处理。

This release covers online applications whose ordinary process does not require an interview. US B1/B2, Japan tourism through designated agencies, and Schengen short-stay lodging are outside scope. The applicant completes biometrics, medical checks, or passport delivery when instructed. An individual interview request pauses the Skill's automated case path.

## 能做什么 / What it does

- 建立带状态、任务、材料、风险、来源、决策和确认记录的案件；
- 根据申请人情况生成个性化材料矩阵，而不是复制通用中介清单；
- 检查身份、日期、有效期、可读性、完整性、来源、翻译和材料一致性；
- 将问题区分为 `BLOCKER`、`WARNING` 和 `ADVISORY`；
- 在提交、付款、预约、上传、声明或向第三方发送信息前停止并取得即时确认；
- 保存来源与核验日期，便于官方规则变化后的更新与回归测试。

- Creates cases with states, tasks, evidence, risks, sources, decisions, and approval records.
- Builds applicant-specific evidence matrices instead of generic intermediary checklists.
- Checks identity, dates, validity, legibility, completeness, provenance, translation, and cross-document consistency.
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

Codex 成功调用后，应先显示 `已启用 XY-SKILL-001 自动化中介`，再说明识别到的申请路径、当前阶段和下一步。只发送 GitHub 链接不会自动安装或调用 Skill；必须先安装，或者明确要求 Codex 读取仓库中的 `SKILL.md` 并按其执行。仓库模式只对当前任务提供指令，不等同于永久安装。

After activation, Codex should show `已启用 XY-SKILL-001 自动化中介`, then identify the route, current stage, and next action. Sending only the GitHub URL does not install or invoke the Skill. Install it first, or explicitly ask Codex to read the repository's `SKILL.md` and follow it for the current task; repository-mode use is temporary, not a permanent installation.

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
- [模块测试集 / Module test set](references/modules/uk-standard-visitor-china-tests.md)
- [官方来源台账 / Official source registry](references/modules/uk-standard-visitor-china-sources.md)

## 安全与边界 / Safety and boundaries

本项目不是政府机构、签证决定者或持牌法律意见提供者。它不能保证获签，也不能替代申请人对事实和声明承担的责任。

This project is not a government authority, visa decision-maker, or provider of licensed legal advice. It cannot guarantee an outcome and does not replace the applicant's responsibility for facts and declarations.

请勿在公开仓库、Issue 或测试报告中提交真实护照、银行、移民、教育、工作、医疗、账号、密码、验证码或付款资料。

Never place real passport, banking, immigration, education, employment, medical, account, password, one-time-code, or payment data in a public repository, issue, or test report.

## 贡献与复用 / Contributing and reuse

欢迎提交脱敏测试案例、官方规则更新和可复现的错误报告。新增国家、签证类型或学校模块时，请明确适用范围、官方来源、验证日期和成熟度，不要把单一案例外推为全部业务已经验证。

Sanitised test cases, official-rule updates, and reproducible bug reports are welcome. New country, visa, or institution modules must state their exact scope, first-party sources, verification date, and maturity level. Never generalise one observed case into universal validation.

## 许可 / License

MIT License. See [LICENSE](LICENSE).
