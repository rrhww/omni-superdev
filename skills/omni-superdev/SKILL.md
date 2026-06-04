---
name: omni-superdev
description: Use when the user wants an independent all-in-one software/product development automation skill, 全能超人, Omni SuperDev, end-to-end R&D delivery, product-to-technical-plan-to-implementation-to-test, 产品开发链路, 产品-技术方案-实现-测试, or asks Codex to build, fix, ship, review, test, design, debug, secure, release, or coordinate a mixed software task.
---

# Omni SuperDev

Act as a self-contained end-to-end product and software development automation workflow.

Omni SuperDev is based on and adapted from the Superpowers workflow model, but it is packaged as one independent skill. Its full workflow content and companion references live inside this skill directory under `references/bundled/`, so a user who installs only `omni-superdev/` still gets the complete development process.

## Core Principle

Omni SuperDev owns the full workflow.

Preserve the full discipline of the bundled Superpowers-derived modules:

- Product discovery before creative implementation
- Written design before non-trivial code
- Test-first behavior changes
- Root-cause-first debugging
- Evidence before completion claims
- Review before merge or release
- Durable planning for long or multi-phase work
- Codebase reconnaissance, migration, UI, browser automation, web QA, MCP, PR/CI, security, quality, and release support from the bundled companion references and Omni-native automation playbooks

Do not weaken these into quick summaries. When a task needs a detailed procedure, read the matching internal reference in `references/bundled/<module>/SKILL.md` and follow it as part of Omni SuperDev.

Resolve every `references/bundled/...` path relative to the installed `omni-superdev/` skill directory, not relative to the user's project root. When running bundled scripts, use the actual installed path to this skill directory.

Read `references/automation-matrix.md` for the full R&D automation matrix. Use it to decide which stages run automatically, which stages need user confirmation, and which bundled reference or Omni-native playbook owns the work.

## Internal Modules

Use these bundled references as Omni SuperDev's internal playbooks, not as external install requirements:

| Need | Internal reference |
| --- | --- |
| Codebase intake, git history signals, hotspots, ownership hints | `references/automation-matrix.md` |
| Product discovery, requirements, design approval | `references/bundled/brainstorming/SKILL.md` |
| Worktree isolation | `references/bundled/using-git-worktrees/SKILL.md` |
| Implementation planning | `references/bundled/writing-plans/SKILL.md` |
| Task-by-task execution | `references/bundled/subagent-driven-development/SKILL.md` or `references/bundled/executing-plans/SKILL.md` |
| Feature or bugfix implementation | `references/bundled/test-driven-development/SKILL.md` |
| Debugging and failing tests | `references/bundled/systematic-debugging/SKILL.md` |
| Parallel independent investigations | `references/bundled/dispatching-parallel-agents/SKILL.md` |
| Post-implementation simplification | `references/automation-matrix.md` |
| Code review feedback | `references/bundled/receiving-code-review/SKILL.md` |
| Pre-merge review | `references/bundled/requesting-code-review/SKILL.md` |
| Completion and release readiness | `references/bundled/verification-before-completion/SKILL.md` and `references/bundled/finishing-a-development-branch/SKILL.md` |
| Long-running file-backed planning | `references/bundled/planning-with-files/SKILL.md` |
| UI/UX implementation or review | `references/bundled/ui-ux-pro-max/SKILL.md` |
| Local web app QA | `references/bundled/webapp-testing/SKILL.md` |
| Generic browser automation | `references/bundled/playwright/SKILL.md` |
| Interactive browser or Electron debugging | `references/bundled/playwright-interactive/SKILL.md` |
| System screenshots when browser capture is insufficient | `references/bundled/screenshot/SKILL.md` |
| MCP server work | `references/bundled/mcp-builder/SKILL.md` |
| Codex migration work | `references/bundled/migrate-to-codex/SKILL.md` |
| GitHub CI or PR comments | `references/bundled/gh-fix-ci/SKILL.md` or `references/bundled/gh-address-comments/SKILL.md` |
| Code review heuristics | `references/bundled/brooks-review/SKILL.md` |
| Codebase health dashboard | `references/bundled/brooks-health/SKILL.md` |
| Test suite quality review | `references/bundled/brooks-test/SKILL.md` |
| Security best practices | `references/bundled/security-best-practices/SKILL.md` |
| Repository threat modeling | `references/bundled/security-threat-model/SKILL.md` |
| Security ownership and bus-factor map | `references/bundled/security-ownership-map/SKILL.md` |
| Jupyter notebooks for experiments or tutorials | `references/bundled/jupyter-notebook/SKILL.md` |
| Release notes and changelog drafting | `references/automation-matrix.md` |
| Skill authoring | `references/bundled/writing-skills/SKILL.md` |

## Intake

Before changing files, ground in the repo and identify:

- Goal and user-visible success criteria
- Task size: small, standard, complex, or incident/debug
- Surface: backend, frontend/UI, MCP, PR/CI, docs/artifact, or mixed
- Risk: public API, data/security, migration, release, or low-risk local change
- Verification command or acceptance check

Ask the user only when intent or tradeoffs cannot be discovered from local context.

## Workflow

Read `references/workflow-map.md` when the task type is unclear or mixed. Treat that map as Omni SuperDev's own workflow map.

1. Recon: understand repo shape, git signals, risks, toolchain, and migration needs.
2. Discover: understand user goal, constraints, audience, and success criteria.
3. Design: for creative or non-trivial work, shape requirements and present an approvable design before implementation.
4. Plan: write an implementation plan for multi-step work, including tests, files, risks, automation stages, and verification.
5. Implement: use test-first development for features, bug fixes, refactors, and behavior changes.
6. Debug: when behavior is broken or surprising, complete root-cause investigation before changing code.
7. Harden: run targeted quality, test-quality, security, UI, browser, MCP, PR/CI, and ownership checks as needed by risk and surface.
8. Verify: run fresh relevant checks before claiming completion.
9. Finish: summarize changes, evidence, skipped checks, release notes, and remaining risks; use branch finishing guidance when preparing merge or release.

## Discipline Gates

- Creative implementation requires a design first. For detailed pressure-tested rules, read `references/bundled/brainstorming/SKILL.md`.
- Behavior-changing implementation requires TDD. For the full RED-GREEN-REFACTOR discipline, read `references/bundled/test-driven-development/SKILL.md`.
- Bugs and failing tests require root-cause-first debugging. For the full process, read `references/bundled/systematic-debugging/SKILL.md`.
- Completion claims require fresh verification evidence. For the full gate, read `references/bundled/verification-before-completion/SKILL.md`.
- Review comments require technical evaluation before implementation. For the full pattern, read `references/bundled/receiving-code-review/SKILL.md`.
- Large or resumable tasks require durable planning. For file-backed planning, read `references/bundled/planning-with-files/SKILL.md`.
- Security-sensitive work requires secure-by-default review and, when the user asks for AppSec modeling, threat modeling. Read `references/bundled/security-best-practices/SKILL.md` or `references/bundled/security-threat-model/SKILL.md`.
- Release readiness requires more than tests when risk is high: add health, test-quality, security, PR/CI, and changelog checks from `references/automation-matrix.md`.

## Role Lens

For non-trivial tasks, check the plan from five views:

- PM: problem, audience, scope, success criteria
- Architect: boundaries, interfaces, data flow, failure modes
- Engineer: implementation path, reuse, maintainability
- QA: test cases, regression risk, acceptance checks
- Designer: interaction, clarity, accessibility, visual fit when UI/artifacts are involved

These are thinking lenses, not automatic subagents. Use real subagents only when the work naturally splits into independent domains and the environment supports it.

## Conflict Policy

Read `references/conflict-policy.md` before combining multiple broad workflow modules.

- User instructions win.
- Repo/project instructions win over global habits.
- Omni SuperDev owns the flow; bundled references deepen the flow.
- Prefer one primary path plus targeted internal modules.
- If an internal reference uses legacy phrases such as "invoke skill", interpret that as "read and follow this bundled reference as part of Omni SuperDev."

## Completion Gate

Before claiming completion, apply the evidence gate from `references/bundled/verification-before-completion/SKILL.md`.

Report:

- What changed
- What was verified, with command/result
- Any skipped checks or remaining risks
