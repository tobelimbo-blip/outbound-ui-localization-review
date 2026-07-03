# Case: Airline operational states

## Input

Review mappings for:

- 计划起飞
- 预计起飞
- 延误
- 取消
- 已出发
- 已到达

## Expected Mode

Full Review Mode

## Expected Output Shape

Full review report

## Expected behavior

- Keep `Scheduled`, `Estimated`, `Delayed`, `Cancelled` or `Canceled`, `Departed`, and `Arrived` distinct.
- Ask for locale preference for cancelled/canceled when not supplied.
- Ask whether departed means gate departure or takeoff, and arrived means landing or gate arrival, when operational precision matters.
- Treat ambiguous operational definitions as high risk.

## Must not do

- Do not merge scheduled and estimated times.
- Do not infer cancellation from delay.
- Do not present the result as airline operations approval.

## Notes

Use the airline glossary and verified data definitions.
