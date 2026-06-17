# Conflict Policy

Use this when multiple Omni SuperDev internal modules appear relevant.

## Priority

1. Explicit user instruction in the current turn
2. Repository/project instructions
3. Safety, data protection, and verification requirements
4. Omni SuperDev integrated judgment
5. Discipline modules
6. Internal specialty references
7. General style preferences

## Coordination Rules

- Use one broad workflow path at a time.
- Keep `omni-superdev` as the only primary process entrypoint for software/product work.
- Treat legacy process modules as deprecated compatibility shims, not competing workflow controllers.
- Use internal references for domain execution, not for competing process control.
- Do not let persistent planning, plan authoring, or plan execution appear as separate skill identities when `omni-superdev` can own the mode directly.
- Do not use UI/design guidance for backend-only or non-visual changes.
- Do not let writing-polish guidance affect normal engineering conversation unless explicitly requested.
- Do not use real subagents unless the user asks for agents/parallel work or independent task slices make them clearly useful and allowed.
- Do not require external artifact skills when an Omni-native automation pass can do the job.

## Superpowers Relationship

Bundled references remain the rigor and specialty layer inside `omni-superdev`.

Use discipline modules such as:

- `references/bundled/systematic-debugging/SKILL.md`
- `references/bundled/test-driven-development/SKILL.md`
- `references/bundled/verification-before-completion/SKILL.md`

Use domain modules only for specialty execution. Keep overall responsibility for sequencing and quality in `omni-superdev`.

## Legacy Process Modules

These bundled modules are no longer first-class process entrypoints:

- `references/bundled/planning-with-files/SKILL.md`
- `references/bundled/writing-plans/SKILL.md`
- `references/bundled/executing-plans/SKILL.md`
- `references/bundled/subagent-driven-development/SKILL.md`

Keep them on disk for compatibility and migration, but treat `omni-superdev` as the canonical owner of those capabilities.

## Automation Relationship

`references/automation-matrix.md` is Omni SuperDev's native automation map. Use it for sequencing and native passes that are not better expressed as a bundled specialty module.

## Tie Breakers

- If the user says "quick", use the small-task path unless risk is high.
- If the user says "完整链路", "全流程", or "端到端", use standard or complex flow.
- If the task touches security, auth, payments, data loss, migrations, or public APIs, choose the more rigorous path.
- If the task is purely docs or text, skip TDD and use appropriate document/text skills.
- If an internal reference is broad but the current task is narrow, use only the relevant section.
- If release readiness is requested, add health, test-quality, security, PR/CI, changelog, and verification gates according to risk.
