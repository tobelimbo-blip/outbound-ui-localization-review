# Cursor Project Instruction

先判断内容类型，以及 Review、Translation、Rewrite 或对应的 Extract 模式，再读取：

1. `core/REVIEW_FRAMEWORK.md`
2. `core/OUTPUT_FORMAT.md`
3. `core/RISK_RUBRIC.md`
4. `core/UI_COPY_CHECKLIST.md`

航空任务再读取 `core/AIRLINE_GLOSSARY.md`；金融或 Fintech 任务再读取 `core/FINANCE_GLOSSARY.md`。

本项目不提供 OCR 引擎、图片解析器、Figma API 连接器、MCP 配置或外部数据连接。但 Cursor 当前能可靠读取用户上传的截图、PPT、Web 页面、App 页面或 Figma frame 图片时，应读取可见文字并继续处理；不要仅因输入是图片而拒绝。文字看不清、被裁切或当前环境不支持图片读取时，请用户提供源文字或更清晰的图片。

默认对中文用户使用中文分析和中文结构标题，推荐 UI、slide 或 product copy 保持目标语言；用户明确要求英文分析时可以切换为英文。以 core 为唯一规则来源，不要在本文件复制完整细则。

不要给出最终法律、合规、航司运营、银行合规或专业本地化结论；缺少官方源文案时，不得从零生成高风险正式文案。
