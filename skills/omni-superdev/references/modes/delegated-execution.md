# Same-Session Delegated Execution Mode

Use this internal mode when a written plan exists, task slices are mostly independent, and delegated work in the current session improves throughput.

## Goal

Keep overall control in `omni-superdev` while using fresh worker/reviewer contexts for task execution and review loops.

## Canonical Prompts

- `prompts/implementer-prompt.md`
- `prompts/spec-reviewer-prompt.md`
- `prompts/code-quality-reviewer-prompt.md`

## Operating Rules

- Dispatch one implementer per task slice, not many conflicting implementers at once.
- Preserve review order: spec compliance first, code quality second.
- Re-run the relevant review after fixes; do not wave issues through.
- Keep final responsibility for quality, scope, and verification in `omni-superdev`.
