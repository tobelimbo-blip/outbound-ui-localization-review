# Case: Membership points and referral rewards

## Input

- Chinese intent: 积分兑换
- Chinese intent: 邀请好友可得 500 积分
- Internal draft to avoid: `Exchange your scores`
- Missing context: reward trigger and eligibility
- User request: 为会员页面从 0 到 1 生成可直接使用的英文文案。

## Expected Mode

Delivery Mode

## Expected Output Shape

Delivery copy block

## Expected behavior

- Recommend `Redeem points` for the first string.
- Treat the invite statement as conditional until trigger, audience, and timing are confirmed.
- Use membership and operation glossaries.
- Preserve English recommendations while explaining risks in Chinese.
- Include the applicable UI position and one genuinely useful alternative only when supported.

## Must not do

- Do not call points `scores` in a loyalty context.
- Do not guarantee 500 points without eligibility rules.
- Do not invent referral terms.

## Notes

This case tests terminology consistency and promotional eligibility risk.
