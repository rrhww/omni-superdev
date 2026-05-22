# Install Omni SuperDev

## Quick Install

Copy this repository's `skills/` directory contents into a Codex-visible skills location.

Resulting structure:

```text
skills/
  omni-superdev/
  omni-tdd/
  omni-debug/
  omni-verify/
  omni-file-planning/
  planning-with-files/
  ui-ux-pro-max/
  webapp-testing/
  mcp-builder/
  gh-fix-ci/
  gh-address-comments/
  brooks-review/
  _shared/
```

`_shared/` is required by `brooks-review`, so keep it alongside the other skill folders.

## Common Install Locations

Depending on the host environment, common locations include:

- `~/.agents/skills/`
- a project-local skills directory if your environment supports one

## Important

Do not copy only `omni-superdev/`.

Copy the full contents of this repository's `skills/` directory and preserve the folder layout, otherwise bundled specialty routes such as `brooks-review` or `planning-with-files` will be incomplete.

## What Is Already Included

This suite already ships with:

- the Omni router and lightweight discipline skills
- persistent planning
- UI/UX guidance
- local web testing
- MCP server workflow guidance
- GitHub PR/CI helper skills
- code review guidance

So users do not need to install those skills separately.

## Runtime Prerequisites

Some bundled skills still expect normal local tools when invoked:

- Python for script-backed skills
- `gh` for GitHub PR/CI workflows
- Playwright and local servers for browser-based QA

These are workflow prerequisites, not extra skill package installs.
