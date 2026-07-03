# 输出格式

默认使用中文分析和中文结构标题，推荐 UI 文案保持目标产品语言。用户明确要求英文报告时，才切换为英文分析与英文结构。

输出前先按 `REVIEW_FRAMEWORK.md` 判断内容类型和用户目标，再从下列模式中选择最轻且足够的格式。视觉输入清晰可读时直接继续，不要仅因来源是截图而拒绝。

## Mode Selection

- **Compact Mode**：单个词、短标签、按钮、标题、空状态或短句；用户需要快速判断“能不能用”或“怎么写更好”。
- **Delivery Mode**：用户提供产品场景，要求从 0 到 1 生成可直接粘贴到 UI、Figma、PPT 或产品文档中的英文。
- **Field Translation Table Mode**：用户只提供中文 UI 字段或可读中文截图，没有当前英文，并要求翻译页面、Figma frame、PPT 或 string table。
- **Localization Review Table Mode**：用户同时提供中文源文案和当前英文，并要求检查正确性、自然度、一致性、术语或风险。
- **Full Review Mode**：整页 UI、完整流程、PPT 页面、产品方案、多模块内容，或用户明确要求 review、audit、一致性检查或风险评估。
- **Extract + Translate**：可读截图、PPT、Figma frame image 或网页截图，主要目标是提取可见中文并翻译；再按内容选择 Delivery 或 Field Translation Table 输出。
- **Extract + Review**：可读 UI 截图包含当前英文，主要目标是判断文案是否准确、自然、适合海外用户；使用 Localization Review Table 或 Full Review Mode。
- **Ask for clearer input**：截图不可读、关键源文案缺失，或高风险内容缺少业务规则时，明确请求清晰图片、源文本或批准规则，不猜测。
- 用户明确指定格式时，按用户要求输出。

## Compact Mode

### 推荐方案

输出一个最推荐的目标语言版本。当前文案可以保留时，直接写“保留：`...`”。

### 判断

- **结论**：可用 / 可用但可优化 / 建议修改 / 必须修改 / 需补充上下文。
- **语义**：是否保留原意。
- **海外常见度**：目标市场是否常见自然。
- **UI 可读性**：是否适合当前组件和长度。
- **风险**：P0 / P1 / P2 / P3，并用中文简述原因。

### 备选方案

只有存在真实的长度、语气、平台或风险差异时才提供；否则省略本节。

### 不建议

只有存在常见直译、机器翻译感或可能误导的表达时才提供；否则省略本节。

## Delivery Mode

### 推荐文案

**Primary**

输出最推荐的目标语言文案。

**Alternative**

仅在存在真实使用差异时输出。

**Not recommended**

列出一个确有代表性的错误方向；没有必要时省略。

### 为什么这样写

- **语义**：是否准确表达功能意图。
- **海外常见度**：是否符合 Global neutral English 和产品惯例。
- **UI 可读性**：是否适合组件、位置和长度。
- **风险**：是否需要业务、法务、合规或运营确认。

### 适用位置

明确标注 Button / Empty state / Modal / Toast / Banner / Card / Form label / Helper text / PPT title 等位置。

## Field Translation Table Mode

用户只提供中文、没有当前英文时使用。保留页面和模块层级；一个页面包含多个模块时，按模块分别输出，不要把字段混在一起。

### 字段级翻译表

| 原中文 | 推荐英文 | 使用位置 / 语境 | 翻译说明 | 需确认项 | 风险等级 |
|---|---|---|---|---|---|
| ... | ... | ... | ... | ... / - | P0 / P1 / P2 / P3 / - |

字段要求：

- **翻译说明**：简要说明选择该英文的原因，不要暗示正在修改已有英文。
- **需确认项**：只用于官方名称、账户类型、业务规则、金额口径、法律、合规、隐私、航班或金融状态；普通字段写 `-`。
- **风险等级**：只有存在实际风险时才标级；普通字段使用 `P3` 或 `-`。

## Localization Review Table Mode

用户同时提供中文和当前英文，或明确要求 review、audit、检查是否正确自然时使用。

### 本地化检查表

| 原中文 | 当前英文 | 推荐英文 | 判断 | 修改原因 | 风险等级 |
|---|---|---|---|---|---|
| ... | ... | ... | 可用 / 可用但可优化 / 建议修改 / 必须修改 | ... | P0 / P1 / P2 / P3 / - |

推荐英文必须可以直接用于 UI；修改原因保持简短。普通字段不要夸大风险，不确定术语写“需业务确认”。

## Table Header Selection Rule

Do not use `修改原因` when the user has not provided existing English copy.

For source-only translation tasks, use:

- `翻译说明`
- `需确认项`
- `风险等级`

For review tasks with existing English copy, use:

- `判断`
- `修改原因`
- `风险等级`

If the task is ambiguous, infer from the input:

- Only Chinese visible → Field Translation Table Mode
- Chinese and English visible → Localization Review Table Mode
- User asks “翻译” → Field Translation Table Mode
- User asks “检查 / 对不对 / 有没有问题 / 是否自然” → Localization Review Table Mode

## Task Intent Routing

- **Review Mode**：单个短字段使用 Compact Mode；多字段、页面或流程使用 Full Review Mode。不要把完整页面重新翻译一遍。
- **Translation Mode**：0-to-1 场景使用 Delivery Mode；只有中文的多个字段使用 Field Translation Table Mode。高风险文案缺少官方来源时只输出占位和风险说明。
- **Localization Review**：同时存在中文和当前英文时使用 Localization Review Table Mode；此时才使用“修改原因”。
- **Rewrite Mode**：单句使用 Compact Mode；需要直接交付的模块使用 Delivery Mode；说明改写原因，不提供无意义备选。
- **Extract + Translate**：先读取可见文字，再使用 Delivery 或 Field Translation Table Mode；Slide 不套用 UI 检查表。
- **Extract + Review / Rewrite**：先读取可见文字并保留层级，再使用 Compact 或 Full Review Mode。

## PPT / Slide 翻译

用户要求翻译 PPT、slide、产品方案页或提案页时，默认使用：

### 可直接替换为

按照原页面层级输出目标语言文案，仅包含原图中存在的层级：

- Step / Section label
- Title
- Subtitle
- Before / After
- Section heading
- Body copy
- Bullet points
- Footer / operation tips

不要默认输出 UI 检查表格。尽量控制译文长度，使其适合原版式。

### 翻译说明

只说明影响专业含义、行业表达或版式长度的关键判断，不要长篇解释。

### 需确认内容

列出看不清、被遮挡、被裁切、上下文不足或专业名词不确定的内容。没有需要确认的内容时写“无”。

## UI / Web 截图

- 用户要求翻译且只有中文：按页面区域或组件分组，使用 Field Translation Table Mode。
- 用户要求检查当前英文：使用 Localization Review Table、Compact 或 Full Review Mode。
- 用户要求优化：输出当前文案、判断、推荐文案和优先级。
- 当前 Agent 无法可靠读取图片时，请用户提供源文字或更清晰的图片。

## Full Review Mode：单条检查或改写

### 结论

使用以下一种判断，并用中文简要说明：

- **可用**：语义准确、表达自然并适合当前组件。
- **可用但可优化**：当前可以上线或交付，但存在明确的小幅体验改进。
- **建议修改**：表达不自然、不清晰或不适合当前组件，但影响尚未达到必须修改。
- **必须修改**：语义错误、明显误导或存在重要业务风险。
- **需补充上下文**：缺少业务规则、组件信息或源文案，无法可靠判断。

### 主要问题

先说明最关键的问题。结论依赖缺失上下文时，明确写出需要确认的事实。

### 维度检查

| 维度 | 判断 |
|---|---|
| 语义准确性 | 是否保留完整原意、条件和例外？ |
| 海外表达习惯 | 是否符合目标市场和行业的常见表达？ |
| UI 可读性 | 是否适合当前组件以及移动端或 Web 端？ |
| 误解 / 客诉风险 | 用户可能误解或争议什么？ |

### 推荐文案

给出最推荐的最终 UI 文案。一个组件包含标题、正文、标签或操作时，分开列出。推荐文案必须保持目标产品语言。

### 备选方案

只有存在真实的平台、长度、语气或风险差异时才提供；否则写“无”。不要为了凑数量列同义词。

### 优先级

按照 `RISK_RUBRIC.md` 使用 **P0 / P1 / P2 / P3**，并用中文说明原因。

### 假设 / 需补充上下文

缺少页面、组件、业务规则、用户状态、行业背景或平台限制时，在这里明确说明；没有缺失信息时写“无”。

## 批量检查

Full Review Mode 检查多条文案时使用：

| 当前文案 | 组件 / 位置 | 问题类型 | 判断 | 推荐文案 | 优先级 | 置信度 |
|---|---|---|---|---|---|---|
| ... | ... | 错误 / 风险 / 可优化 / 轻微润色 / 需补充上下文 | ... | ... | P0-P3 | 高 / 中 / 低 |

只使用以下问题类型：

- **错误**：语义错误、业务含义丢失、动作含义错误，或可能明显误导用户。
- **风险**：可能引发误解、客诉、错误操作、费用争议、资格争议、退款争议、隐私或合规风险。
- **可优化**：基本能理解，但不够自然、不符合海外 UI 习惯，或不适合当前组件。
- **轻微润色**：当前可用，只是可以更短、更自然或更统一；不要标成高优先级。
- **需补充上下文**：缺少页面位置、组件类型、业务规则、用户状态或平台信息，无法准确判断。

置信度只使用：**高 / 中 / 低**。

保留用户提供的编号或标识，方便映射回源数据。Review Mode 默认只列出问题、风险和确有价值的优化项；用户要求完整审计时，可以列出可保留项，但必须明确说明“可保留”。

高风险文案缺少官方源文案时，不填写完整推荐文案，改用 `REVIEW_FRAMEWORK.md` 中的“推荐处理 / 占位文案 / 风险说明”结构。
