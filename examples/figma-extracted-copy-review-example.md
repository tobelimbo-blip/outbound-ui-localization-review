# Figma 已提取文案检查示例

本示例假设宿主 Agent 已经从 Figma 获取文本。本项目不提供 Figma API 连接器或 MCP 配置；如果当前 Agent 能读取用户上传的 Figma frame 图片，也应读取其中清晰可见的文字并继续检查。

## 页面上下文

- 产品：跨境支付 Web 应用
- 页面：转账确认
- 目标语言：English (US)
- 输入：宿主 Agent 提供的组件名称和可见文案

## 批量检查

| 当前文案 | 组件 / 位置 | 问题类型 | 判断 | 推荐文案 | 优先级 | 置信度 |
|---|---|---|---|---|---|---|
| `Exchange price` | 表单标签 | 错误 | 数字表示货币兑换关系，应使用 rate 而不是 price。 | `Exchange rate` | P1 | 高 |
| `Actual arrival amount` | 汇总行 | 风险 | 直译不自然，也不清楚费用是否会改变到账金额。 | 确认费用规则后再定稿；若表示收款人最终所得，可用 `Recipient gets` | P0 | 中 |
| `Confirm to transfer` | 主按钮 | 可优化 | 表达不地道，动作可以更直接。 | `Confirm transfer` | P2 | 高 |
| `Money is on the road` | 转账状态 | 错误 | 直译掩盖实际支付状态。 | `Funds in transit` | P1 | 高 |
| `Authorized` | 支付状态 | 需补充上下文 | 只有底层状态确为授权时才能使用，不能代替 captured 或 settled。 | 使用系统确认的支付生命周期状态 | P0（条件式） | 低 |

## 假设 / 需补充上下文

需要确认展示金额是否已包含费用，以及 `Authorized` 对应授权、扣款还是结算状态。
