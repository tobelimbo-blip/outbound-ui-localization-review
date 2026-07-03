# Case: Empty state with external booking channels

## Input

- Product: Airline website
- Component: My Trips empty state
- Meaning: 部分渠道订单不会自动显示，用户可手动添加
- Current copy: `No trips yet`
- User request: 检查这句英文

## Expected Mode

Compact Mode

## Expected Output Shape

Brief recommendation

## Expected behavior

- Use Compact Mode with Chinese analysis and English recommended copy.
- Say the title is natural but incomplete as a full empty state.
- Recommend a title plus helper text that preserves channel limits and manual recovery.
- Use P2 by default; raise to P1 only when manual add is essential to recovery.

## Must not do

- Do not mark `No trips yet` as semantically wrong in every context.
- Do not assign P0 solely because the product is an airline.
- Do not invent which channels are affected.

## Notes

This case tests semantic completeness without over-correction.
