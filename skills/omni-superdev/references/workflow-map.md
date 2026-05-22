# Workflow Map

Use this map when a request could trigger more than one skill.

## Task Size

| Situation | Default route |
| --- | --- |
| One obvious localized edit | Small task path: inspect, edit, verify |
| New user-visible behavior | Standard development with product intent, technical approach, `omni-tdd`, and verification |
| Multiple subsystems or cross-session work | `planning-with-files`, or `omni-file-planning` if a lighter persisted plan is enough |
| Bug, failing test, unexpected behavior | `omni-debug`, then TDD regression if code changes |
| Release/merge readiness | Verification, review, then finish/PR workflow |

## Surface Routing

| Surface | Use |
| --- | --- |
| UI, dashboard, app screen, component, design system | `ui-ux-pro-max` |
| Local web app QA, screenshots, browser logs | `webapp-testing` |
| Generic browser automation/data extraction | `playwright` |
| MCP server or external service tool interface | `mcp-builder` |
| Failing GitHub Actions PR checks | `gh-fix-ci` |
| PR review comments to address | `gh-address-comments` |
| Code review or merge-readiness review | `brooks-review` |
| Security review/threat modeling | `security-best-practices` or `security-threat-model` only when explicitly security-focused |
| Code cleanup after implementation | `code-simplifier` |
| Humanizing prose/review/commit text | `unslop`, `unslop-review`, or `unslop-commit` only when explicitly requested |

## Product-To-Test Chain

For standard feature work:

1. Product intent: user, job, current pain, success criteria.
2. Technical design: interface, data flow, dependencies, failure behavior.
3. Implementation: smallest coherent slice, `omni-tdd` for behavior changes.
4. Quality pass: simplify changed code without changing behavior.
5. Verification: run the most relevant tests/checks and report evidence with `omni-verify`.

## Open Design

Open Design is an optional external library for rich visual artifacts, decks, prototypes, and design-heavy templates. Do not install or invoke it by default. Consider it only when the user explicitly asks for Open Design, a polished design artifact, HTML deck, prototype, poster, or visual system beyond normal app UI.

## DarcyGB

No reliable local or public source was available during v1 creation. Do not invent DarcyGB rules. Add a reference only after the user provides a trustworthy source.
