# Omni SuperDev Workflow Map

Use this map when a request could need more than one internal Omni SuperDev module. Internal modules live under `references/bundled/` and are part of this skill, not separate installation requirements.

For the full R&D automation matrix, read `references/automation-matrix.md`.

## Task Size

| Situation | Default route |
| --- | --- |
| One obvious localized edit | Small task path: inspect, edit, verify |
| New user-visible behavior | Repo recon → discovery/design → planning → TDD implementation → targeted hardening → fresh verification |
| Multiple subsystems or cross-session work | Repo recon → discovery/design → file-backed planning → phased execution |
| Bug, failing test, unexpected behavior | Root-cause debugging, then TDD regression coverage if code changes |
| Multiple independent failures or task slices | Parallel investigation when there is no shared state or sequencing dependency |
| Review feedback arrived and needs evaluation before implementation | Verify feedback against codebase, then implement one item at a time |
| Release/merge readiness | Fresh verification → code/test/security health checks as needed → changelog → branch finishing |
| Security-sensitive work | Secure-by-default review; add threat modeling or ownership mapping when explicitly requested |
| Migration into Codex | Migration intake → dry run → migrate → validate generated Codex artifacts |

## Surface Routing

| Surface | Use |
| --- | --- |
| Broad or unfamiliar repo | `references/automation-matrix.md` repo recon |
| Codex migration | `references/bundled/migrate-to-codex/SKILL.md` |
| UI, dashboard, app screen, component, design system | `references/bundled/ui-ux-pro-max/SKILL.md` |
| Local web app QA, screenshots, browser logs | `references/bundled/webapp-testing/SKILL.md` |
| Generic browser automation/data extraction | `references/bundled/playwright/SKILL.md` |
| Persistent browser or Electron debugging | `references/bundled/playwright-interactive/SKILL.md` |
| Desktop/system screenshot | `references/bundled/screenshot/SKILL.md` |
| MCP server or external service tool interface | `references/bundled/mcp-builder/SKILL.md` |
| Failing GitHub Actions PR checks | `references/bundled/gh-fix-ci/SKILL.md` |
| PR review comments to address | `references/bundled/gh-address-comments/SKILL.md` |
| Code review or merge-readiness review | `references/bundled/brooks-review/SKILL.md` |
| Codebase health dashboard | `references/bundled/brooks-health/SKILL.md` |
| Test-suite quality review | `references/bundled/brooks-test/SKILL.md` |
| Security best-practice review | `references/bundled/security-best-practices/SKILL.md` |
| Threat modeling | `references/bundled/security-threat-model/SKILL.md` only when explicitly AppSec-focused |
| Security ownership map | `references/bundled/security-ownership-map/SKILL.md` only when explicitly ownership/bus-factor-focused |
| Code cleanup after implementation | `references/automation-matrix.md` native simplification pass |
| Jupyter notebook artifact | `references/bundled/jupyter-notebook/SKILL.md` |
| Changelog or release notes | `references/automation-matrix.md` native changelog pass |
| Creating or editing skills | `references/bundled/writing-skills/SKILL.md` |
| Human-facing engineering prose | Use Omni-native concise writing unless the user provides a specific voice requirement |

## Product-To-Test Chain

For standard feature work:

1. Repo recon and automation staging: `references/automation-matrix.md`
2. Product intent and design: `references/bundled/brainstorming/SKILL.md`
3. Implementation planning: `references/bundled/writing-plans/SKILL.md`
4. Workspace isolation when appropriate: `references/bundled/using-git-worktrees/SKILL.md`
5. Implementation execution: `references/bundled/subagent-driven-development/SKILL.md` or `references/bundled/executing-plans/SKILL.md`
6. Behavior changes: `references/bundled/test-driven-development/SKILL.md`
7. Surface-specific hardening: UI, browser, MCP, security, test-quality, PR/CI, or notebook modules as needed
8. Review and completion: `references/bundled/requesting-code-review/SKILL.md`, `references/bundled/verification-before-completion/SKILL.md`, and `references/bundled/finishing-a-development-branch/SKILL.md`

## Full Bundle Notes

This skill intentionally preserves `using-superpowers` and `writing-skills` alongside the execution-oriented workflow references.

They are not the default path for every task, but they are part of the full bundled Superpowers content and should not be omitted when packaging or installing `omni-superdev/`.

The package also includes expanded R&D automation modules for migration, Playwright automation, interactive UI debugging, screenshots, notebooks, security, codebase health, and test quality. These are internal references, not extra skills to install.

## Artifact Boundary

Do not require external design, PDF, writing, or changelog skills. If a requested artifact does not have a bundled module, use `references/automation-matrix.md` and normal project tooling to produce it as part of Omni SuperDev.
