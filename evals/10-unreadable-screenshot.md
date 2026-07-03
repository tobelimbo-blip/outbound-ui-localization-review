# Case: Unreadable screenshot

## Input

The user uploads a screenshot whose text is blurred, cropped, and too small to distinguish key numbers and labels. It appears to include privacy consent and child-information wording, but the official source cannot be read. The user asks for a translation.

## Expected Mode

Ask for clearer input

## Expected Output Shape

Brief recommendation

## Expected behavior

- Say which content cannot be read reliably.
- Request a clearer image, cropped regions, or source text.
- Continue with any independently readable non-sensitive text only when useful and clearly labeled.
- Use the approved high-risk placeholder for the unreadable privacy and child-information block.

## Must not do

- Do not guess missing words, numbers, policy names, or UI hierarchy.
- Do not reconstruct privacy, guardian authorization, or consent scope from surrounding context.
- Do not generate a complete translation that appears authoritative.
- Do not claim the project lacks all screenshot capability; the problem is readability in this input.

## Notes

This case distinguishes capability boundaries from input quality.
