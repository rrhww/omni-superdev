---
name: omni-verify
description: Use when wrapping up work in the Omni SuperDev suite and you need to verify outcomes before claiming completion.
---

# Omni Verify

Do not claim success without evidence.

## Before Completion

Verify the most relevant checks for the work that changed.

Examples:

- targeted tests
- build or type checks
- lint for touched surfaces
- manual acceptance checks for narrow local behavior

## Report

Always state:

- what changed
- what you verified
- the result of those checks
- what was not verified
- remaining risks, if any

## Rules

- Evidence beats confidence
- Narrow verification is fine when the change is narrow
- If you skip a check, say so explicitly
