# Case: Product proposal slide screenshot

## Input

The user uploads a readable PPT screenshot and asks: 把这一页 PPT 翻译成英文。

Visible hierarchy:

- Step label
- Main positioning title
- Before / After sections
- Supporting sentences
- Three bullets per side
- Footer navigation hints

## Expected Mode

Extract + Translate

## Expected Output Shape

Delivery copy block

## Expected behavior

- Use Extract + Translate Mode and identify Product Presentation / Slide.
- Output `可直接替换为`, `翻译说明`, and `需确认内容`.
- Preserve hierarchy, contrast, and approximate text length.
- Use professional proposal language rather than literal UI labels.

## Must not do

- Do not refuse because the input is a screenshot.
- Do not force the slide into a UI review table.
- Do not invent a brand strategy or approved product positioning.

## Notes

If a key term is ambiguous, provide one working translation and mark it for confirmation.
