# Omni SuperDev Workflow Map

Use this map when a request could need more than one Omni SuperDev capability or operating mode. Treat it as guidance for balanced execution inside `omni-superdev`, not as a replacement for senior judgment.

For the full R&D automation matrix, read `references/automation-matrix.md`.

## Task Size

| Situation | Default approach |
| --- | --- |
| One obvious localized edit | Small task path: inspect, edit, verify |
| New user-visible behavior | Direct delivery: product intent → design if needed → TDD implementation → targeted hardening → fresh verification |
| Multiple subsystems or cross-session work | Enter `persistent-planning` mode and phase the work using `omni-superdev` planning assets |
| User wants a written implementation plan | Enter `plan-authoring` mode |
| User already has a written plan to carry out | Enter `plan-execution` mode |
| Written plan with mostly independent tasks in this session | Escalate from `plan-execution` to `same-session delegated execution` mode |
| Bug, failing test, unexpected behavior | Root-cause debugging, then TDD regression coverage if code changes |
| Multiple independent failures or task slices | Parallel investigation when there is no shared state or sequencing dependency |
| Review feedback arrived and needs evaluation before implementation | Verify feedback against codebase, then implement one item at a time |
| Release/merge readiness | Fresh verification → code/test/security health checks as needed → changelog → branch finishing |
| Security-sensitive work | Secure-by-default review; add threat modeling or ownership mapping when explicitly requested |
| Migration into Codex | Migration intake → dry run → migrate → validate generated Codex artifacts |

## Surface Guidance

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

1. Product intent and design when needed.
2. Technical approach and file boundaries.
3. Direct delivery or a plan mode depending on task shape.
4. TDD for behavior changes.
5. Surface-specific hardening only where risk warrants it.
6. Fresh verification before any completion claim.

## Process Hierarchy

Use this hierarchy consistently:

- `omni-superdev` owns end-to-end process control and mode selection.
- Discipline modules under `references/bundled/` enforce rigor gates.
- Domain modules under `references/bundled/` provide specialty execution tools.
- Legacy process modules under `references/bundled/` exist only as deprecated compatibility shims.
