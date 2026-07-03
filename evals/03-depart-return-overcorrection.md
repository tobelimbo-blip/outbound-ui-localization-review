# Case: Common airline labels without over-correction

## Input

An airline booking card contains:

- 出发 / 返程 → current English: `Depart / Return`
- 优惠码 → current English: `Promotion Code`
- 查询 → current English: `Search`

User request: 按字段检查这些英文是不是都需要改。

## Expected Mode

Localization Review Table Mode

## Expected Output Shape

Localization review table

## Expected behavior

- Keep `Depart / Return` as a common compact travel pattern.
- Explain that `Promo code` is shorter, but `Promotion Code` is acceptable.
- Keep `Search` when the surrounding flight-search context is explicit; mention `Search flights` only as a clearer standalone CTA.
- Use Optional polish or Improvement, with P2 or P3 as supported by context.
- Use `修改原因` only because current English is provided for each field.

## Must not do

- Do not label all three strings as errors.
- Do not replace `Depart` with `Departure` without a component reason.
- Do not offer a synonym list.

## Notes

This case tests commonness, brevity, and contextual judgment.
