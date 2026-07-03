# Case: Login versus Log in

## Input

Review both occurrences:

1. Header action button: `Login`
2. Page title: `Login`

## Expected Mode

Compact Mode

## Expected Output Shape

Brief recommendation

## Expected behavior

- Recommend `Log in` for the action button.
- Allow `Login` as the page title or noun label.
- Distinguish component role before judging correctness.
- Treat the button change as an improvement, not a high-risk error.

## Must not do

- Do not replace both occurrences automatically.
- Do not claim `Login` is always grammatically wrong.

## Notes

Confidence should be high because component types are supplied.
