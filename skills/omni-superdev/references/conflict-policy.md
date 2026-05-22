# Conflict Policy

Use this when multiple skills or workflows appear relevant.

## Priority

1. Explicit user instruction in the current turn
2. Repository/project instructions
3. Safety, data protection, and verification requirements
4. Omni SuperDev routing decision
5. Narrow specialty skills
6. General style preferences

## Routing Rules

- Use one broad workflow at a time.
- Use narrow skills for domain execution, not for competing process control.
- Do not let `planning-with-files` trigger merely because a task has several tool calls; use it for long, complex, or resumable work.
- Do not let UI/design skills trigger for backend-only or non-visual changes.
- Do not let writing-polish skills affect normal engineering conversation unless explicitly requested.
- Do not use real subagents unless the user asks for agents/parallel work or independent task slices make them clearly useful and allowed.

## Superpowers Relationship

Superpowers inspired the engineering discipline model behind this suite, and Omni SuperDev is explicitly based on that model. But this package now ships as its own self-contained suite, so users do not need to install Superpowers separately just to get the normal Omni flow.

This package ships with its own lightweight core discipline skills:

- `omni-tdd` for behavior-changing implementation
- `omni-debug` for bugs and failures
- `omni-verify` for completion checks
- `omni-file-planning` for persisted multi-phase work

It also bundles specialty companions such as `planning-with-files`, `ui-ux-pro-max`, `webapp-testing`, `mcp-builder`, `gh-fix-ci`, `gh-address-comments`, and `brooks-review`.

Omni SuperDev decides when those disciplines apply and keeps them from becoming separate competing entry points.

## Tie Breakers

- If the user says "quick", use the small-task path unless risk is high.
- If the user says "完整链路", "全流程", or "端到端", use standard or complex flow.
- If the task touches security, auth, payments, data loss, migrations, or public APIs, choose the more rigorous path.
- If the task is purely docs or text, skip TDD and use appropriate document/text skills.
- If a skill's frontmatter is broad but the current task is narrow, prefer the narrower match.
