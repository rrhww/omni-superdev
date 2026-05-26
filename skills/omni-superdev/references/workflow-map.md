# Omni SuperDev Workflow Map

Use this map when a request could need more than one internal Omni SuperDev module. Internal modules live under `references/bundled/` and are part of this skill, not separate installation requirements.

## Task Size

| Situation | Default route |
| --- | --- |
| One obvious localized edit | Small task path: inspect, edit, verify |
| New user-visible behavior | Discovery/design → planning → TDD implementation → fresh verification |
| Multiple subsystems or cross-session work | Discovery/design → file-backed planning → phased execution |
| Bug, failing test, unexpected behavior | Root-cause debugging, then TDD regression coverage if code changes |
| Multiple independent failures or task slices | Parallel investigation when there is no shared state or sequencing dependency |
| Review feedback arrived and needs evaluation before implementation | Verify feedback against codebase, then implement one item at a time |
| Release/merge readiness | Fresh verification → review → branch finishing |

## Surface Routing

| Surface | Use |
| --- | --- |
| UI, dashboard, app screen, component, design system | `references/bundled/ui-ux-pro-max/SKILL.md` |
| Local web app QA, screenshots, browser logs | `references/bundled/webapp-testing/SKILL.md` |
| Generic browser automation/data extraction | `playwright` |
| MCP server or external service tool interface | `references/bundled/mcp-builder/SKILL.md` |
| Failing GitHub Actions PR checks | `references/bundled/gh-fix-ci/SKILL.md` |
| PR review comments to address | `references/bundled/gh-address-comments/SKILL.md` |
| Code review or merge-readiness review | `references/bundled/brooks-review/SKILL.md` |
| Security review/threat modeling | `security-best-practices` or `security-threat-model` only when explicitly security-focused |
| Code cleanup after implementation | `code-simplifier` |
| Creating or editing skills | `references/bundled/writing-skills/SKILL.md` |
| Humanizing prose/review/commit text | `unslop`, `unslop-review`, or `unslop-commit` only when explicitly requested |

## Product-To-Test Chain

For standard feature work:

1. Product intent and design: `references/bundled/brainstorming/SKILL.md`
2. Implementation planning: `references/bundled/writing-plans/SKILL.md`
3. Workspace isolation when appropriate: `references/bundled/using-git-worktrees/SKILL.md`
4. Implementation execution: `references/bundled/subagent-driven-development/SKILL.md` or `references/bundled/executing-plans/SKILL.md`
5. Behavior changes: `references/bundled/test-driven-development/SKILL.md`
6. Review and completion: `references/bundled/requesting-code-review/SKILL.md`, `references/bundled/verification-before-completion/SKILL.md`, and `references/bundled/finishing-a-development-branch/SKILL.md`

## Full Bundle Notes

This skill intentionally preserves `using-superpowers` and `writing-skills` alongside the execution-oriented workflow references.

They are not the default path for every task, but they are part of the full bundled Superpowers content and should not be omitted when packaging or installing `omni-superdev/`.

## Open Design

Open Design is an optional external library for rich visual artifacts, decks, prototypes, and design-heavy templates. Do not install or invoke it by default. Consider it only when the user explicitly asks for Open Design, a polished design artifact, HTML deck, prototype, poster, or visual system beyond normal app UI.

## DarcyGB

No reliable local or public source was available during v1 creation. Do not invent DarcyGB rules. Add a reference only after the user provides a trustworthy source.
