# Plan Authoring Mode

Use this internal mode when the user wants a written implementation plan as the main deliverable.

## Goal

Produce a decision-complete implementation plan that another engineer or agent can execute without making product or technical decisions on their own.

## Operating Rules

- Map file boundaries before defining tasks.
- Prefer small, testable, coherent task slices.
- Include concrete verification commands and expected outcomes.
- Keep code examples and interface details specific enough to remove ambiguity.
- Avoid placeholders such as `TODO`, `TBD`, or vague “handle edge cases” language.

## Supporting Asset

- Review prompt: `prompts/plan-document-reviewer-prompt.md`
