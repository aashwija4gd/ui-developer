# Generation Prompt Template

Use this template when generating UI code.

## Inputs

- task description
- target files
- relevant codebase context
- `STYLEGUIDE.md`
- `ORG-STYLEGUIDE.md`
- machine-readable manifests

## Required behavior

- use only approved tokens, components, and statuses
- prefer existing repo primitives over new abstractions
- preserve accessibility and responsive constraints
- output only the requested patch, diff, or code block format

