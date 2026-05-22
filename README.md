# Omni SuperDev

Omni SuperDev is a self-contained skill suite for full-cycle software and product development.

It is based on and adapted from the Superpowers discipline model, but it is packaged here as one installable suite so users do not need to separately install the common companion skills.

## Positioning

You can think of the suite like this:

- `omni-superdev` is the main router
- `omni-tdd`, `omni-debug`, `omni-verify`, and `omni-file-planning` provide the suite's lightweight built-in discipline layer
- bundled specialty skills provide deeper coverage for UI/UX, local web QA, MCP work, PR/CI work, code review, and persistent planning

That makes Omni SuperDev a good default entry point for software and product work that may span backend, frontend, UI, testing, PR/CI, or MCP.

## Bundled Skills

Core Omni skills:

- `omni-superdev`
- `omni-tdd`
- `omni-debug`
- `omni-verify`
- `omni-file-planning`

Bundled specialty skills:

- `planning-with-files`
- `ui-ux-pro-max`
- `webapp-testing`
- `mcp-builder`
- `gh-fix-ci`
- `gh-address-comments`
- `brooks-review`
- `_shared` support files required by `brooks-review`

## Typical Routing

- Small task: inspect, patch, verify, summarize
- Standard development: clarify product intent, sketch the technical approach, use TDD for behavior changes, implement, simplify, verify
- Complex or multi-session work: use persisted planning, then execute in phases
- Debug or failing tests: start with root-cause-first debugging before proposing fixes
- UI/UX: route to `ui-ux-pro-max`
- Local web QA: route to `webapp-testing`
- MCP work: route to `mcp-builder`
- PR or CI work: route to `gh-fix-ci`, `gh-address-comments`, or `brooks-review`

## Installation

See [docs/install.md](./docs/install.md).

In short, copy this repository's [`skills/`](./skills) directory contents into a Codex-visible skills location and preserve the directory structure.

Common target locations:

- `~/.agents/skills/`
- another project or personal skills directory used by your environment

## What "No Extra Install" Means

Users no longer need separate skill installs for:

- `planning-with-files`
- `ui-ux-pro-max`
- `webapp-testing`
- `mcp-builder`
- `gh-fix-ci`
- `gh-address-comments`
- `brooks-review`

Some routes still rely on normal runtime tools when they are actually used, for example:

- Python for script-backed skills
- `gh` authentication for GitHub workflows
- Playwright or local dev servers for browser testing flows

Those are workflow/runtime prerequisites, not additional skill package installs.

## Licensing

This repository now bundles third-party skill content under their included license files.

- Third-party attribution: [docs/third-party.md](./docs/third-party.md)
- Root repository license: [LICENSE](./LICENSE)
- License notes: [LICENSE-NOTICE.md](./LICENSE-NOTICE.md)
