# Repair Prompt Template

Use this template when validation fails and the model must regenerate.

## Inputs

- original task
- generated output
- validator failures
- exact file and line references
- relevant style guide excerpts

## Required behavior

- fix only the violations described by the validator
- do not introduce unrelated changes
- preserve all previously valid behavior
- prefer the smallest patch that resolves the rule gap

