---
name: omni-superdev
description: Use when the user wants an all-in-one product development flow, 全能超人, omni-superdev, end-to-end delivery, product-to-technical-plan-to-implementation-to-test, 产品开发链路, 产品-技术方案-实现-测试, or asks Codex to build, fix, ship, review, test, design, or coordinate a software/product task where workflow routing matters.
---

# Omni SuperDev

Act as the routing layer for end-to-end product development. Use one clear entry point, then delegate to narrower skills only when their specialty is needed.

This suite is based on and adapted from the Superpowers discipline model, but it is packaged as a self-contained suite.

This suite includes its own lightweight core execution companions:

- `omni-tdd`
- `omni-debug`
- `omni-verify`
- `omni-file-planning`

This suite also bundles the main specialty companions that used to require separate installs:

- `planning-with-files`
- `ui-ux-pro-max`
- `webapp-testing`
- `mcp-builder`
- `gh-fix-ci`
- `gh-address-comments`
- `brooks-review`

Prefer the built-in Omni discipline skills for default control flow, and use the bundled specialty skills when their domain is needed.

## Core Rule

Classify first, then choose the lightest sufficient workflow. Do not stack multiple process skills by default.

## Intake

Before changing files, ground in the repo and identify:

- Goal and user-visible success criteria
- Task size: small, standard, complex, or incident/debug
- Surface: backend, frontend/UI, MCP, PR/CI, docs/artifact, or mixed
- Risk: public API, data/security, migration, release, or low-risk local change
- Verification command or acceptance check

Ask the user only when intent or tradeoffs cannot be discovered from local context.

## Workflow Router

Read `references/workflow-map.md` when the task type is unclear or mixed.

- **Small task:** inspect, patch, run narrow verification, summarize.
- **Standard development:** clarify product intent, sketch technical approach, use `omni-tdd` for behavior changes, implement, simplify, verify with `omni-verify`.
- **Complex or multi-session:** use `planning-with-files` for full persisted task state, or `omni-file-planning` for a lighter in-suite version, then follow the standard flow in phases.
- **Debug/failing tests:** use `omni-debug` before proposing fixes.
- **New feature or bugfix:** use `omni-tdd` unless the task is config/docs-only or the user explicitly waives TDD.
- **UI/UX:** use `ui-ux-pro-max` for visual, layout, interaction, accessibility, or product-surface design.
- **Local web QA:** use `webapp-testing`; use `playwright` only for generic browser automation.
- **MCP server:** use `mcp-builder`.
- **PR/CI:** use `gh-fix-ci`, `gh-address-comments`, or `brooks-review` based on whether the task is failed checks, review comments, or code review.
- **Artifact/deck/design asset:** prefer built-in document/presentation skills; consider Open Design only as an optional external design library, not a default dependency.

If a routed specialty skill is unavailable, treat that as an incomplete suite install or packaging issue before treating it as a missing external dependency.

## Role Lens

For non-trivial tasks, check the plan from five views:

- PM: problem, audience, scope, success criteria
- Architect: boundaries, interfaces, data flow, failure modes
- Engineer: implementation path, reuse, maintainability
- QA: test cases, regression risk, acceptance checks
- Designer: interaction, clarity, accessibility, visual fit when UI/artifacts are involved

These are thinking lenses, not automatic subagents. Use real subagents only when the user asks for parallel agent work or the task naturally splits into independent workstreams.

## Conflict Policy

Read `references/conflict-policy.md` before combining multiple broad workflow skills.

- User instructions win.
- Repo/project instructions win over global habits.
- Omni SuperDev routes; narrow skills execute.
- Built-in Omni suite skills provide the default discipline layer for this suite, while bundled specialty skills provide deeper domain coverage.
- Prefer one primary workflow plus targeted specialty skills.

## Completion Gate

Before claiming completion, use `omni-verify`.

Report:

- What changed
- What was verified, with command/result
- Any skipped checks or remaining risks
