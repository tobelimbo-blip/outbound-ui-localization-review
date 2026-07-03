# Case: Finance lifecycle status

## Input

- Product: Business banking approval flow
- Meaning: 转账已通过内部审批，但尚未提交银行
- Current copy: `Transfer completed`

## Expected Mode

Full Review Mode

## Expected Output Shape

Full review report

## Expected behavior

- Mark the current copy as materially misleading.
- Recommend `Approved` only if that is the verified workflow state.
- Explain that approval, submission, processing, and settlement are different states.
- Assign P0 because users may believe funds have moved.

## Must not do

- Do not recommend `Authorized`, `Paid`, or `Settled` without state evidence.
- Do not make a banking compliance conclusion.

## Notes

This case tests high-risk state accuracy.
