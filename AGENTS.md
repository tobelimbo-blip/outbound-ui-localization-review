# Agent Instructions

This project is an agent-agnostic localization package for UI, product presentation, marketing, and structured copy.

Before reviewing, translating, or rewriting copy, read:

1. `core/REVIEW_FRAMEWORK.md`
2. `core/OUTPUT_FORMAT.md`
3. `core/RISK_RUBRIC.md`
4. `core/UI_COPY_CHECKLIST.md`

For airline-related work, also read `core/AIRLINE_GLOSSARY.md`. For finance or fintech work, also read `core/FINANCE_GLOSSARY.md`.

First detect the content type and Review, Translation, Rewrite, or corresponding Extract mode. By default, respond to Chinese users with Chinese analysis and Chinese section headings while keeping recommended UI, slide, or product copy in the target language. Switch the analysis and structure to English only when the user explicitly requests it.

This project does not provide an OCR engine, image parser, Figma API connector, MCP setup, or external data connection. If the current agent can reliably read visible text from an uploaded screenshot, PPT, web page image, app screen, or Figma frame image, it must use that capability and continue the requested task. Do not refuse solely because the input is visual. If text is unreadable, cropped, too small, or unsupported by the current environment, ask for source text or a clearer image.

State what is missing when the intended meaning, component, business condition, or platform constraint cannot be determined; do not invent it. Do not make final legal, compliance, airline operations, banking compliance, or professional localization conclusions. Do not generate final high-risk legal, privacy, consent, payment, refund, fee, eligibility, banking, or airline-operation copy from scratch; use the core placeholder rule when approved source copy is missing or unreadable.

Use `core/OUTPUT_FORMAT.md` for the response and `core/RISK_RUBRIC.md` for problem types and priorities.
