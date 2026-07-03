# Outbound UI Localization Review

给中国 UX/UI 设计师、产品经理和运营人员使用的出海 UI 英文文案 Skill。

你可以用它翻译中文 UI、检查已有英文、改写产品文案，也可以处理可读的 App、Web、Figma 和 PPT 截图。默认回复使用中文解释，推荐文案使用 Global neutral English，方便直接交付设计和开发。

适用行业包括旅行、航空、金融、电商、会员、SaaS 和企业工具。

## 解决的问题

中文 UI 逐字翻译后，常见问题不只在语法。

| 问题 | Skill 如何处理 |
|---|---|
| 英文能读，但不像产品文案 | 结合海外产品惯例和组件语境给出推荐表达 |
| 保留中文语序或内部术语 | 改成海外用户能理解的说法，不改变业务含义 |
| 文案不适合组件 | 按按钮、空状态、弹窗、Toast、表单等组件控制长度和信息量 |
| 状态或规则容易误解 | 检查费用、退款、支付、航班、账户和用户权益等信息 |
| 只给译文，无法判断能否使用 | 区分可用、可优化、建议修改、必须修改和需补充上下文 |

## 适用对象

- 中国 UX/UI、交互和视觉设计师
- 出海产品经理与运营人员
- 需要交付英文界面的产品团队

## 支持的内容

### UI 与产品文案

- Button、Tab、Menu、Empty state
- Modal、Toast、Snackbar、Tooltip
- Form label、Helper text、Error message
- Status tag、Table column、Card、Banner
- 运营活动、会员权益、积分和优惠券
- 产品方案、PPT 标题和说明文字

### 输入形式

- 中文或中英对照文本
- App 与 Web 页面截图
- Figma frame image
- PPT、Keynote 或 Slide 截图
- Markdown、CSV、JSON 或 string table

当前 Agent 能可靠读取图片文字时，Skill 会继续翻译或检查。文字模糊、被裁切或关键字段无法辨认时，Skill 会要求清晰图片或源文本。

## 判断维度

| 维度 | 检查内容 |
|---|---|
| 语义准确性 | 是否保留业务含义、动作、条件和限制 |
| 海外常见度 | 是否符合目标用户和行业惯例 |
| UI 可读性 | 是否适合组件、端类型和空间限制 |
| 误解与业务风险 | 是否可能引发错误操作、客诉或状态误解 |
| 敏感度 | 是否涉及支付、退款、隐私、身份、航班或合规信息 |

Skill 不会因为存在另一个更自然的说法，就把当前文案判成错误。已经准确、常见且适合组件的文案会标记为可用。

## 工作模式

Skill 根据输入内容和用户目标选择最轻且足够的模式。

| 模式 | 适用场景 | 主要输出 |
|---|---|---|
| Compact Mode | 单个词、按钮、标题或短句 | 推荐方案与简短判断 |
| Delivery Mode | 根据中文场景从 0 到 1 生成英文 | Primary、Alternative、Not recommended |
| Field Translation Table Mode | 只有中文字段或中文截图 | 字段级翻译表 |
| Localization Review Table Mode | 同时提供中文和当前英文 | 本地化检查表 |
| Full Review Mode | 页面、流程、方案或风险审查 | 完整检查报告 |
| Extract + Translate | 可读截图需要翻译 | 按页面层级输出译文 |
| Extract + Review | 可读截图包含待检查英文 | 按字段或模块检查 |
| Ask for clearer input | 图片不可读或关键规则缺失 | 请求清晰输入或业务规则 |

## 两种字段表格

用户只提供中文时，Skill 使用字段级翻译表：

```text
| 原中文 | 推荐英文 | 使用位置 / 语境 | 翻译说明 | 需确认项 | 风险等级 |
```

用户提供中文和当前英文，并要求检查时，Skill 使用本地化检查表：

```text
| 原中文 | 当前英文 | 推荐英文 | 判断 | 修改原因 | 风险等级 |
```

纯翻译任务不会使用“修改原因”。普通 UI 字段通常标记 `-` 或 P3。官方名称、账户类型、金额口径、支付、退款、隐私和航班状态等内容才需要更高风险等级或业务确认。

## 推荐输入方式

提供页面、组件和业务含义，可以减少来回确认。

```text
产品：航空公司海外网站
页面：My Trips
组件：空状态
中文含义：部分渠道订单不会自动显示，用户可以手动添加
当前英文：No trips yet
限制：移动端，标题和辅助说明各一行
任务：检查当前英文
```

你也可以直接上传截图：

```text
把这张中文 App 首页翻译成英文，按页面模块输出。
```

```text
检查这张 Figma 截图里的英文，保留可用文案，只列需要改的内容。
```

```text
把这页 PPT 改成自然、克制的英文，保留原有层级。
```

## 安装

### Codex

Codex adapter 已包含运行所需的 `SKILL.md` 和 `references/`，可以独立安装：

```bash
cp -R adapters/codex/.agents/skills/outbound-ui-localization-review \
  "${CODEX_HOME:-$HOME/.codex}/skills/"
```

也可以把该目录复制到项目的 `.agents/skills/`。

### Claude、Cursor 和 Trae

- Claude：保留项目根目录的 `core/`，安装 `adapters/claude/outbound-ui-localization-review/`。
- Cursor：保留 `core/`，使用 `adapters/cursor/AGENTS.md` 和对应 `.mdc` 规则。
- Trae：保留 `core/`，把 `adapters/trae/rules.md` 加入项目规则。
- 其他 Agent：读取根目录 `AGENTS.md`，再按说明加载 `core/`。

## 仓库结构

```text
outbound-ui-localization-review/
├── core/                         # 核心规则与 glossary，唯一 source of truth
├── adapters/
│   ├── codex/                    # 自包含 Codex Skill
│   ├── claude/
│   ├── cursor/
│   └── trae/
├── evals/                        # 11 个回归案例
├── examples/                     # 完整输出示例
├── AGENTS.md                     # 跨 Agent 入口
└── README.md
```

### Core

`core/` 包含：

- `REVIEW_FRAMEWORK.md`
- `OUTPUT_FORMAT.md`
- `RISK_RUBRIC.md`
- `UI_COPY_CHECKLIST.md`
- 通用产品、UI、运营营销和垂直行业 glossary

### Codex references

`adapters/codex/.agents/skills/outbound-ui-localization-review/references/` 是 `core/` 的安装副本。修改核心规则后需要同步并检查差异：

```bash
cp core/*.md adapters/codex/.agents/skills/outbound-ui-localization-review/references/
diff -qr core adapters/codex/.agents/skills/outbound-ui-localization-review/references
```

## Glossary 使用原则

Glossary 提供语境参考，不强制替换已经可用的文案。Skill 会根据组件、用户动作、行业惯例和风险选择术语。

例如：

- `Login` 可以作为名词，动作按钮通常使用 `Log in`。
- `Promo code` 和 `Promotion code` 都可用，组件空间和产品语气决定选择。
- `Authorized`、`Approved` 与 `Settled` 表示不同金融状态，不能互换。
- `Scheduled`、`Estimated` 与 `Departed` 表示不同航班状态，不能互换。

## Evals

`evals/` 包含 11 个回归案例，覆盖：

- 短文案判断与防止过度纠错
- 中文首页字段翻译和中英稿检查
- PPT、Figma 与网页截图
- 航空和金融状态
- 电商、会员与 SaaS 权限文案
- 不可读截图和高风险文案处理

每个案例包含 `Expected Mode`、`Expected Output Shape` 和禁止行为。使用干净的 Agent 会话运行案例，可以检查 Skill 更新后是否退化。

## 能力边界

| 事项 | 处理方式 |
|---|---|
| 图片文字 | 使用当前 Agent 已有的视觉能力；本项目不提供 OCR 引擎 |
| Figma 数据 | 处理可读的 frame image；本项目不配置 Figma API 或 MCP |
| 法律与合规 | 翻译或检查官方源文案；最终结论由法务或合规人员确认 |
| 航空与银行规则 | 根据已确认规则检查措辞；运营和业务团队负责最终定义 |
| 官方名称 | 使用企业、机构或产品的批准英文名，不自行创造 |

高风险内容缺少官方源文案时，Skill 会输出占位和风险说明，不生成可直接上线的正式条款。

## 维护说明

- `core/` 是规则源文件。
- Codex `references/` 必须与 `core/` 保持一致。
- Adapter 只保留入口和加载说明，不复制整套规则。
- 新 glossary 需要重复案例支持，避免为单次任务扩展分类。

## License

仓库尚未选择开源许可证。公开复用前，请由仓库所有者补充合适的 License。
