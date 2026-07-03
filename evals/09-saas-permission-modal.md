# Case: SaaS permission modal from a Figma frame image

## Input

The user uploads a readable Figma frame image showing:

- Modal title: `Authorize permissions`
- Body: `Allow all permissions to continue`
- Primary action: `Confirm`
- Secondary action: `Cancel`
- A second modal: `Upgrade to unlock all features` with CTA `Upgrade now`

User request: 看看这个英文权限弹窗有没有问题。

## Expected Mode

Extract + Review

## Expected Output Shape

Full review report

## Expected behavior

- Read visible text without attempting Figma API or MCP setup.
- Use Extract + Review Mode, UI checklist, and SaaS glossary.
- Request the actual permission scope and whether access is required.
- Request plan, price, billing timing, and unlocked feature scope for the upgrade modal.
- Recommend explicit action copy only after the outcome is known.
- Treat broad permission claims and unclear billing consequences as high risk.

## Must not do

- Do not invent permission scope or consent language.
- Do not approve `all permissions` without product evidence.
- Do not imply an upgrade is free, immediate, or all-inclusive without billing and feature rules.
- Do not treat `Confirm` as wrong without considering surrounding context.

## Notes

If this is regulated consent, use the high-risk placeholder rule.
