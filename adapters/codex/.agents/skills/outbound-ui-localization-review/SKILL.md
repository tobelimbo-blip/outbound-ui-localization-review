---
name: outbound-ui-localization-review
description: Review, translate, and rewrite Chinese-to-English outbound UI and product copy for overseas products. Use for UI localization, product copy reviews, screenshots, PPT slides, Figma frame images, website screenshots, app UI, string tables, operation copy, marketing copy, empty states, buttons, forms, modals, toasts, status labels, error messages, product proposals, and design reviews across travel, airline, finance, fintech, e-commerce, membership, loyalty, SaaS, enterprise tools, logistics, education, healthcare, creator tools, AI products, and consumer apps. Do not use as OCR, Figma API, MCP setup, legal approval, compliance approval, airline operations approval, banking compliance review, or final brand strategy approval.
---

# Outbound UI Localization Review

Review, translate, or rewrite copy already supplied as text or reliably readable in the current Agent's visual input.

## Load references

Always read:

1. `references/REVIEW_FRAMEWORK.md`
2. `references/OUTPUT_FORMAT.md`
3. `references/RISK_RUBRIC.md`
4. `references/GLOSSARY_GENERAL_PRODUCT.md`

For UI screens or components, also read `references/UI_COPY_CHECKLIST.md` and `references/GLOSSARY_UI_COMPONENTS.md`.

Load only the relevant additional glossary:

- Operations, marketing, campaigns, or landing pages: `references/GLOSSARY_OPERATION_MARKETING.md`
- Airline or travel: `references/GLOSSARY_AIRLINE_TRAVEL.md`
- Finance or fintech: `references/GLOSSARY_FINANCE_FINTECH.md`
- E-commerce, membership, or loyalty: `references/GLOSSARY_ECOMMERCE_MEMBERSHIP.md`
- SaaS or enterprise tools: `references/GLOSSARY_SAAS_ENTERPRISE.md`

## Apply the framework

- Detect content type and select Compact, Delivery, Field Translation Table, Localization Review Table, Full Review, Extract + Translate, Extract + Review, or clearer-input handling before answering.
- For Chinese users, default to Chinese analysis while keeping recommended copy in the target product language.
- Use clear, concise Global neutral English unless the user specifies another locale or tone.
- If visible screenshot text is readable, use it and continue; if it is not reliable, request clearer input rather than guessing.
- Preserve usable copy and distinguish errors, risks, improvements, optional polish, and missing context.
- Never generate final high-risk legal, privacy, consent, payment, refund, eligibility, banking, or airline-operation copy from scratch.
