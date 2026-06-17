# Persistent Planning Mode

Use this internal mode for long-running, cross-session, or multi-phase work that needs durable planning files.

## Core Pattern

Treat the filesystem as durable working memory:

- `task_plan.md` tracks phases, decisions, and status
- `findings.md` stores discoveries worth preserving
- `progress.md` logs execution state, checks, and errors

## Canonical Assets

- Templates: `templates/planning/`
- Scripts: `scripts/planning/`
- Deep references: `references/planning/`

## Operating Rules

- Create or refresh planning files before sustained execution.
- Re-read planning files before major decisions or after long context gaps.
- Update progress after each meaningful phase.
- Log failures and mutate the approach instead of repeating a failed action.
- Use this mode only when persistence meaningfully reduces risk or coordination cost.
