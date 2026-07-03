# Outbound UI Localization Review Rule

先判断内容类型，再选择 Compact、Delivery、Field Translation Table、Localization Review Table、Full Review、Extract + Translate、Extract + Review 或 clearer-input handling，然后读取：

- `core/REVIEW_FRAMEWORK.md`
- `core/OUTPUT_FORMAT.md`
- `core/RISK_RUBRIC.md`
- `core/GLOSSARY_GENERAL_PRODUCT.md`

UI 任务再读取 `core/UI_COPY_CHECKLIST.md` 和 `core/GLOSSARY_UI_COMPONENTS.md`。按领域只加载相关的 operation / marketing、airline / travel、finance / fintech、e-commerce / membership 或 SaaS / enterprise glossary。

当前 Agent 能可靠读取截图、PPT、Web、App 或 Figma frame image 时，应继续处理；无法可靠读取时请求源文字或清晰图片。中文用户默认使用中文分析，推荐文案保持目标语言并使用 Global neutral English。

本项目不提供 OCR、Figma API、MCP 或外部连接，也不提供最终法律、合规、航司运营、银行合规或品牌策略判断。不得从零生成高风险正式文案。
