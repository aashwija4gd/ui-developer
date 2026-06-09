---
name: ui-developer
description: Generate or repair repository-consistent UI code using the ui-generation prompts, rules, manifests, and validation workflow in this folder. 
---

# UI Developer

Use this skill when generating or repairing UI code in this repository. Treat `/references` as the local source of truth for prompts, design rules, token registries, validation rules, and workflow notes.

## Workflow

1. Read the tas request and nearby code context. 
2. Load `references/rules/STYLEGUIDE.md` and `references/rules/ORG-STYLEGUIDE.md` first.
3. Load only the narrowest addition rule file that matches the task:
    - layout and structure: `references/rules/layout.md`
    - components and states: `references/rules/components.md`
    - spacing and sizing: `references/rules/spacing.md`
    - typography: `references/rules/typography.md`
    - color and contrast: `references/rules/color.md`
    - interaction and focus: `references/rules/interaction.md`
    - accessibility: `references/rules/accessibility.md`
    - motion: `references/rules/motion.md`
    - navigation: `references/rules/navigation.md`
    - content writing: `references/rules/content-writing.md`
    - data display: `references/rules/data-display.md`
    - icons: `references/rules/icons.md`
    - locale and formatting: `references/rules/locale-formatting.md`
4. Check the relevant manifests before using token, component, currency, or status value. 
5. Use `references/prompts/generation-prompt.md` to shape new output.
6. Use `references/prompts/repair-prompt.md` when fixing validator or review failures.
7. Follow the workflow docs in `references/workflows/` when the task is CLI-, editor-, or CI-oriented.
8. Run validation against `references/validators/rules.md` and `references/validators/violations.schema.json` before returning the result.

## Required Behavior

- Prefer existing repository primitives over new abstractions.
- Use only approved tokens, components, statuses, and formatting rules. 
- Preserve accessibility, responsive behavior, and existing interaction patterns.
- Keep changes minimal and repository-consistent.
- If required data is missing, state exactly what is missing instead of inventing it.

## Output 

Return only the requested patch, diff, or code block format for the task. Do not add explanation unless the task explicitly asks for it.