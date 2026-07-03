# Case: Chinese-only homepage UI translation

## Input

用户上传一张只有中文的首页 UI 截图，并说：“翻译一下首页的内容”。页面包含问候语、企业名称、余额卡片、快捷入口和普通操作标签，但没有当前英文稿。

## Expected Mode

Field Translation Table Mode

## Expected Output Shape

Field translation table

## Must use columns

- 原中文
- 推荐英文
- 使用位置 / 语境
- 翻译说明
- 需确认项
- 风险等级

## Expected behavior

- Preserve homepage module hierarchy.
- Use concise English that can be pasted into UI.
- Use `-` for ordinary fields with no confirmation need or material risk.
- Use a placeholder for the official registered company name and request the approved English name.

## Must not do

- Do not use `修改原因` as a table header.
- Do not assume an existing English draft.
- Do not assign P1 or P2 to every ordinary field.
- Do not invent a legal company name, account type, amount basis, or financial state.

## Notes

This case separates source-only translation from localization review.
