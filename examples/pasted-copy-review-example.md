# 粘贴文案检查示例

## 输入

- 产品背景：航空公司海外网站
- 页面：My Trips
- 组件：空状态
- 中文含义：用户还没有订机票，但部分渠道的订单无法自动回显，可手动添加
- 当前英文：`No trips yet`
- 限制：移动端，短标题 + 辅助说明

## 输出

### 结论

当前文案可以作为短标题使用，但作为完整空状态不够完整。

### 主要问题

`No trips yet` 只表达暂无可展示行程，没有说明部分渠道订单可能不会自动回显，也没有引导用户手动添加。

### 维度检查

| 维度 | 判断 |
|---|---|
| 语义准确性 | 不完整，遗漏渠道限制和手动添加入口。 |
| 海外表达习惯 | `No trips yet` 本身自然，但更适合简单空状态。 |
| UI 可读性 | 适合作为标题，但需要辅助说明。 |
| 误解 / 客诉风险 | 用户可能误以为订单不存在或订票失败。 |

### 推荐文案

Title: **No trips found**
Helper text: **Bookings made through some channels may not appear automatically. You can add a booking manually.**

### 备选方案

移动端更短版本：

Title: **No trips to show**
Helper text: **Can’t see your booking? Add it manually.**

### 优先级

**P2**。当前标题可理解，但完整空状态缺少必要说明。
如果“手动添加订单”是该页面的核心恢复路径，则可提升为 **P1**。

### 假设 / 需补充上下文

需要确认页面是否提供“手动添加订单”按钮，以及用户是否主要通过外部渠道购票。
