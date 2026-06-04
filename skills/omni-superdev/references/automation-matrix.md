# Omni SuperDev Automation Matrix

Use this matrix to turn Omni SuperDev from a linear workflow into an end-to-end R&D automation system. The user still installs only `omni-superdev/`; all bundled module paths resolve relative to this skill directory.

## Automation Modes

| Mode | When to use | Behavior |
| --- | --- | --- |
| Small task | Localized, low-risk change | Inspect the touched area, edit, run narrow verification, summarize. |
| Standard delivery | Feature, bugfix, UI change, MCP/tooling work | Run recon, discovery/design, plan, TDD or root-cause flow, implementation, verification, and finish. |
| Release readiness | Merge, publish, release notes, "can we ship?" | Add health, test-quality, security, CI/PR, changelog, and branch finishing checks. |
| Incident/debug | Broken behavior, failing test, production-like issue | Use root-cause debugging before fixes; add regression coverage before claiming completion. |
| Migration/onboarding | Existing project moving into Codex or unfamiliar repo | Run repo recon and migration guidance before implementation. |

## Full Lifecycle Stages

| Stage | Trigger | Automation owner |
| --- | --- | --- |
| 0. Repo recon | New repo, unclear scope, large task, onboarding | Omni-native git recon: inspect commit count, recent churn, hotspots, test/build files, ownership hints, and risky surfaces before deep code reading. |
| 1. Migration intake | User asks to migrate instructions, skills, agents, or MCP config | `references/bundled/migrate-to-codex/SKILL.md` |
| 2. Product discovery | New feature, ambiguous product intent, creative work | `references/bundled/brainstorming/SKILL.md` |
| 3. Technical planning | Multi-file, non-trivial, risky, or phased implementation | `references/bundled/writing-plans/SKILL.md`; use `references/bundled/planning-with-files/SKILL.md` for resumable work. |
| 4. Workspace isolation | Large or risky code changes | `references/bundled/using-git-worktrees/SKILL.md` when isolation is useful and safe. |
| 5. Implementation | Feature, bugfix, refactor, behavior change | `references/bundled/test-driven-development/SKILL.md` for behavior changes; `references/bundled/subagent-driven-development/SKILL.md` or `references/bundled/executing-plans/SKILL.md` for planned task execution. |
| 6. Debugging | Failing tests, unexpected behavior, flaky symptoms | `references/bundled/systematic-debugging/SKILL.md` |
| 7. Cleanup | User asks to simplify, or implementation left avoidable complexity | Omni-native simplification pass: limit to changed/requested files, preserve behavior and public APIs, remove duplication/nesting/unclear names only when verification can prove safety. |
| 8. UI/UX | Screens, components, dashboards, design systems, visual QA | `references/bundled/ui-ux-pro-max/SKILL.md` |
| 9. Browser QA | Local web app testing, browser logs, screenshots, flows | Prefer `references/bundled/webapp-testing/SKILL.md`; use `references/bundled/playwright/SKILL.md` for generic browser automation and `references/bundled/playwright-interactive/SKILL.md` for persistent UI debugging. |
| 10. System capture | Need desktop/system screenshot or browser capture is insufficient | `references/bundled/screenshot/SKILL.md` |
| 11. MCP/tooling | MCP server, tool interface, external API integration | `references/bundled/mcp-builder/SKILL.md` |
| 12. Notebook artifacts | Experiments, tutorials, reproducible analysis notebooks | `references/bundled/jupyter-notebook/SKILL.md` |
| 13. Security hardening | Auth, payments, data, public APIs, secrets, user asks for security | `references/bundled/security-best-practices/SKILL.md` |
| 14. Threat modeling | User asks for threat model, abuse paths, AppSec model | `references/bundled/security-threat-model/SKILL.md` |
| 15. Security ownership | User asks for bus factor, sensitive ownership, CODEOWNERS reality | `references/bundled/security-ownership-map/SKILL.md` |
| 16. Code review | Review request, merge readiness, PR quality risk | `references/bundled/brooks-review/SKILL.md` |
| 17. Health dashboard | "How healthy is this codebase?", release risk, broad quality check | `references/bundled/brooks-health/SKILL.md` |
| 18. Test quality | Brittle tests, slow tests, mock abuse, test-suite quality review | `references/bundled/brooks-test/SKILL.md` |
| 19. GitHub PR/CI | Failing checks, review comments | `references/bundled/gh-fix-ci/SKILL.md` or `references/bundled/gh-address-comments/SKILL.md` |
| 20. Release notes | Release, changelog, user-facing update summary | Omni-native changelog pass: read git history, group user-visible changes, filter internal noise, call out breaking changes/security fixes, and keep language user-facing. |
| 21. Completion | Before success claims, merge, PR, or publish | `references/bundled/verification-before-completion/SKILL.md` and `references/bundled/finishing-a-development-branch/SKILL.md` |

## Native Repo Recon

Use this lightweight recon before reading deeply when scope is broad:

1. Identify project type from files such as package manifests, lockfiles, test config, CI config, Docker files, and framework conventions.
2. Inspect git recency, churn, and hotspots with non-destructive git history commands.
3. Find test/build/lint commands from package scripts, CI config, Makefiles, task files, or docs.
4. Identify sensitive surfaces: auth, payments, permissions, migrations, secrets, networking, parsers, uploads, and public APIs.
5. Use findings to choose the strictness of planning, TDD, security, and verification.

## Native Simplification Pass

Use after implementation only when it improves maintainability without changing behavior:

- Stay inside changed files or user-specified scope.
- Preserve public APIs, data formats, error behavior, migrations, and tests.
- Prefer naming duplicated logic, reducing nesting, deleting stale comments, and clarifying conditionals.
- Do not perform broad rewrites, architecture changes, or unrelated formatting churn.
- Run the same narrow verification used for the implementation.

## Native Changelog Pass

Use for release notes when no bundled release-note module is present:

1. Determine range: since last tag, since last release branch, or user-specified commits.
2. Group commits into features, fixes, improvements, security, breaking changes, docs, and internal-only.
3. Rewrite technical commits into user-facing language.
4. Exclude noise unless it affects users or operators.
5. Include verification status and known limitations when the release depends on them.

## Artifact Boundary

Some local skills may exist in an author's environment but are not bundled here because their local license does not allow public redistribution or no clear license file was available. Do not require users to install those skills. Instead, use Omni-native workflow guidance and normal project tooling to create release notes, Markdown docs, screenshots, notebooks, or other artifacts when requested.
