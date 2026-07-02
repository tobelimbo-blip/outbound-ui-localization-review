# Outbound UI Localization Review

A portable, agent-agnostic instruction package for reviewing, translating, and rewriting outbound UI, product presentation, and marketing copy supplied as text or readable visual input.

This repository is a cross-agent rules package, not a Codex-only skill. It provides shared review criteria plus thin adapters for Codex, Claude, Cursor, Trae, and other agents that can read Markdown instructions.

## Scope

The package works when copy is supplied as text or is visibly readable in an uploaded screenshot. It supports Review, Translation, Rewrite, and visual Extract combinations and checks whether target-language copy:

- preserves the original Chinese business meaning;
- follows common overseas product conventions;
- fits the target UI component and screen size;
- may cause misunderstanding, complaints, or incorrect user action; and
- can be replaced with clearer final copy.

It is not an OCR product or a Figma plugin. It does not provide an OCR engine, image parser, Figma API connector, MCP setup, or external data connection. However, if the current agent can read visible text from an uploaded screenshot, slide, web page image, app screen, or Figma frame image, it should use that existing capability and continue the requested task. It must not refuse solely because the input is visual. If text is unreadable, cropped, or too small, ask for source text or a clearer image.

The package does not generate final high-risk legal, privacy, consent, payment, refund, eligibility, banking, or airline-operation copy from scratch.

```text
Screenshot / slide / web image / Figma frame image / pasted copy / CSV / JSON
  -> current agent reads visible text when capable, or user supplies source text
  -> framework detects content type and task mode
  -> Chinese analysis by default for Chinese users
  -> target-language UI, slide, or product-copy recommendations
```

## Suitable tasks

Use this package for outbound product UI, including:

- airline, travel, finance, fintech, SaaS, and enterprise products;
- overseas web and mobile interfaces; and
- buttons, tabs, empty states, status tags, forms, error messages, modals, toasts, table columns, and tooltips.
- product presentations, PPT or slide pages, proposals, landing pages, banners, slogans, and copy tables.

A useful input normally includes the component type, page context, Chinese meaning, current English copy, industry context, and mobile or web constraints. When key context is missing, the reviewer should identify the uncertainty instead of inventing a business rule.

For Chinese users, analysis and section headings are Chinese by default. Recommended UI copy remains in the target product language; an English UI therefore still receives English recommendations. English analysis is used when explicitly requested.

## Review dimensions

1. **Semantic accuracy** — preservation of business meaning, conditions, status, and required user action.
2. **Overseas convention** — natural wording consistent with established product patterns.
3. **UI readability** — clarity, length, scanability, and fit for the component.
4. **Risk of misunderstanding or complaint** — ambiguity around eligibility, fees, refunds, payment, flight or account status, rights, restrictions, and next actions.
5. **Recommended copy** — the strongest final wording, with alternatives only for a real constraint or tone difference.

## Repository layout

- `core/` contains the platform-independent framework, output contract, risk rubric, component checklist, and domain glossaries.
- `adapters/` tells each supported agent how to load and apply the core files without duplicating them.
- `examples/` shows single-item, batch, screenshot, slide translation, and before/after tasks.
- `AGENTS.md` is the generic entry point for agents that support repository instructions.

## Use with an agent

- **Codex:** keep `core/` at the project root, then copy `adapters/codex/.agents/skills/outbound-ui-localization-review/` into the target repository's `.agents/skills/`, or point Codex to that `SKILL.md`.
- **Claude:** keep `core/` at the project root, then copy `adapters/claude/outbound-ui-localization-review/` into the location used for project skills.
- **Cursor:** copy `adapters/cursor/AGENTS.md` to the project root if needed and place the `.mdc` file under the project's rule directory.
- **Trae:** add the contents of `adapters/trae/rules.md` to the relevant project rules.
- **Other agents:** read the root `AGENTS.md`, then load the required files from `core/`.

Paths in the adapters assume the core files remain available in the same repository or are copied with the adapter.

## Test the package

1. Ask in Chinese for a single review and confirm the analysis and headings are Chinese while recommended English UI copy remains English.
2. Ask for page translation and confirm Translation Mode returns a source-to-target table rather than a review report.
3. Ask for a concise rewrite and confirm Rewrite Mode explains the change without unnecessary alternatives.
4. Test `Login`, `Depart / Return`, `Promotion Code`, and `Search` in different components and confirm acceptable copy is not automatically marked wrong.
5. Remove a material fact, such as payment state or booking source, and confirm the output uses “需补充上下文” instead of guessing.
6. Request privacy or child-consent copy without approved source text and confirm the output uses the Chinese high-risk placeholder rather than generating final copy.
7. Ask “把这一页 PPT 翻译成英文” with a clear slide screenshot and confirm the output preserves the slide hierarchy.
8. Ask “把这张网页截图翻译成英文” and confirm visible sections are grouped and translated.
9. Ask “检查这张 App 页面里的英文” and confirm Extract + Review Mode uses the UI review format.
10. Ask “看看这个 Figma 截图里的英文有没有问题” and confirm the agent reads the frame image without trying to configure Figma or MCP.
11. Ask “把这个产品方案页改成更自然的英文” and confirm Extract + Rewrite Mode preserves meaning and hierarchy.
12. Upload an unreadable or cropped image and confirm the agent requests source text or a clearer image without guessing.
13. Explicitly request an English report and confirm both analysis and section headings switch to English.

## Disclaimer

This project provides localization and UI writing suggestions. It does not replace legal, compliance, airline operations, banking compliance, or professional localization review.
