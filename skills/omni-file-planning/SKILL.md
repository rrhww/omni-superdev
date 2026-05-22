---
name: omni-file-planning
description: Use when work in the Omni SuperDev suite is long-running, multi-phase, cross-session, or needs persistent planning files on disk.
---

# Omni File Planning

Use simple markdown files as persistent task memory when a task is too large to trust to conversation context alone.

## Use When

- Work spans multiple phases
- The task is likely to continue in later sessions
- Multiple subsystems are involved
- You need durable progress tracking

## Minimal File Set

Create these files in the working project:

- `task_plan.md`
- `findings.md`
- `progress.md`

## Process

1. Write the goal and phases in `task_plan.md`.
2. Record discoveries in `findings.md`.
3. Log progress and verification in `progress.md`.
4. Re-read the plan before major decisions.
5. Update the files after each phase.

## Rules

- Do not use this for tiny local tasks
- Keep notes concise and current
- Store decisions on disk, not only in chat context
