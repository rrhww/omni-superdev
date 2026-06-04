# Conflict Policy

Use this when multiple Omni SuperDev internal modules appear relevant.

## Priority

1. Explicit user instruction in the current turn
2. Repository/project instructions
3. Safety, data protection, and verification requirements
4. Omni SuperDev workflow decision
5. Internal specialty references
6. General style preferences

## Workflow Rules

- Use one broad workflow path at a time.
- Use internal references for domain execution, not for competing process control.
- Do not use file-backed planning merely because a task has several tool calls; use it for long, complex, or resumable work.
- Do not use UI/design guidance for backend-only or non-visual changes.
- Do not let writing-polish guidance affect normal engineering conversation unless explicitly requested.
- Do not use real subagents unless the user asks for agents/parallel work or independent task slices make them clearly useful and allowed.
- Do not treat bundled references as separate installed skills; they are internal playbooks inside Omni SuperDev.
- Do not require external artifact skills when an Omni-native automation pass can do the job.

## Superpowers Relationship

Superpowers inspired the engineering discipline model behind this skill, and Omni SuperDev is explicitly based on that model.

The intent of this package is to preserve that discipline inside one independent skill so users do not need a separate Superpowers install to get the normal Omni flow.

This skill bundles the full-strength workflow backbone directly under `references/bundled/`, including:

- `brainstorming`
- `dispatching-parallel-agents`
- `executing-plans`
- `finishing-a-development-branch`
- `receiving-code-review`
- `requesting-code-review`
- `subagent-driven-development`
- `systematic-debugging`
- `test-driven-development`
- `using-git-worktrees`
- `using-superpowers`
- `verification-before-completion`
- `writing-plans`
- `writing-skills`

It also bundles specialty companion references such as `planning-with-files`, `ui-ux-pro-max`, `webapp-testing`, `mcp-builder`, `gh-fix-ci`, `gh-address-comments`, `brooks-review`, `brooks-health`, `brooks-test`, `migrate-to-codex`, `playwright`, `playwright-interactive`, `screenshot`, `jupyter-notebook`, `security-best-practices`, `security-threat-model`, and `security-ownership-map`.

Omni SuperDev decides when those disciplines apply and keeps them as one coherent workflow.

`using-superpowers` is preserved as upstream content inside the bundle. For this package, `omni-superdev` is the installed first entry point.

If an upstream reference says "invoke skill" or names an upstream module, interpret it as "read and follow the corresponding file under `references/bundled/<name>/`."

## Automation Relationship

`references/automation-matrix.md` is Omni SuperDev's native R&D automation map. Use it for repo recon, post-implementation simplification, changelog/release-note drafting, and artifact boundaries that are not safe to bundle as third-party skills.

When a bundled module and the automation matrix both apply, use the bundled module for detailed execution and the matrix for sequencing.

## Tie Breakers

- If the user says "quick", use the small-task path unless risk is high.
- If the user says "完整链路", "全流程", or "端到端", use standard or complex flow.
- If the task touches security, auth, payments, data loss, migrations, or public APIs, choose the more rigorous path.
- If the task is purely docs or text, skip TDD and use appropriate document/text skills.
- If an internal reference is broad but the current task is narrow, use only the relevant section.
- If release readiness is requested, add health, test-quality, security, PR/CI, changelog, and verification gates according to risk.
