# Agent Instructions

This repository is an agent-agnostic localization rules package for outbound UI, product, operation, marketing, and presentation copy.

Before handling copy, read:

1. `core/REVIEW_FRAMEWORK.md`
2. `core/OUTPUT_FORMAT.md`
3. `core/RISK_RUBRIC.md`
4. `core/GLOSSARY_GENERAL_PRODUCT.md`

For UI tasks, also read `core/UI_COPY_CHECKLIST.md` and `core/GLOSSARY_UI_COMPONENTS.md`. Load only the relevant additional glossary:

- Operations or marketing: `core/GLOSSARY_OPERATION_MARKETING.md`
- Airline or travel: `core/GLOSSARY_AIRLINE_TRAVEL.md`
- Finance or fintech: `core/GLOSSARY_FINANCE_FINTECH.md`
- E-commerce, membership, or loyalty: `core/GLOSSARY_ECOMMERCE_MEMBERSHIP.md`
- SaaS or enterprise tools: `core/GLOSSARY_SAAS_ENTERPRISE.md`

The default user is a Chinese UX/UI designer; Chinese product managers and operations teams are secondary users. Use Chinese analysis and headings by default, keep recommendations in the target language, and use Global neutral English unless the user specifies another locale or tone.

Detect content type and select Compact, Delivery, Field Translation Table, Localization Review Table, Full Review, Extract + Translate, Extract + Review, or clearer-input handling. Keep outputs delivery-oriented: copy should be ready for Figma, PPT, product documents, string tables, or development handoff.

Use `字段级翻译表` for Chinese-only source translation and label the explanation `翻译说明`; include `需确认项` only where needed. Use `本地化检查表` and `修改原因` only when current English exists and is being reviewed. Ordinary UI fields should normally use `-` or P3, not inflated P1/P2 ratings.

This package does not provide OCR, image parsing, Figma API, MCP setup, or external connections. If the current Agent can reliably read visible text from an uploaded image, use it and continue. If not, request clearer input rather than guessing.

Do not issue final legal, compliance, airline operations, banking compliance, professional localization, or brand strategy conclusions. Do not generate final high-risk copy from scratch. Use `core/OUTPUT_FORMAT.md` and `core/RISK_RUBRIC.md` for the response.

`core/` is the source of truth. The Codex adapter's `references/` directory is its installable copy; synchronize it after every core change and verify exact equality.

Do not change the default user persona, reduce the package to generic proofreading, merge Field Translation Table Mode with Localization Review Table Mode, force glossary replacements over context, add a parallel rule structure, duplicate glossaries, or expand glossary categories without repeated evidence.
