# Case: E-commerce campaign card in a web screenshot

## Input

The user uploads a readable campaign-card screenshot containing:

- 新人限时优惠
- 输入优惠码
- 全网最低价
- 立即领取
- 使用失败，请稍后重试

User request: 检查并优化英文活动文案。

## Expected Mode

Extract + Review

## Expected Output Shape

Full review report

## Expected behavior

- Use Extract + Review Mode and Marketing / Landing Page Copy.
- Prefer `New user offer`, `Enter promo code`, and context-appropriate `Claim now`.
- Flag the lowest-price claim for evidence and approved terms.
- State the definition of new user and campaign end time as required context.
- Ask whether the failure is an invalid coupon, an eligibility problem, or a temporary system error before finalizing the error message.

## Must not do

- Do not add urgency, savings, or exclusivity not present in approved source copy.
- Do not generate campaign terms from scratch.
- Do not use a generic retry message when retrying could repeat a failed checkout action.
- Do not treat every marketing improvement as an error.

## Notes

The lowest-price claim may be P0 or P1 depending on exposure and substantiation.
