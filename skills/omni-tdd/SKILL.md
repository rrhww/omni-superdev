---
name: omni-tdd
description: Use when implementing a feature, bugfix, or behavior change inside the Omni SuperDev suite and you need a lightweight test-first workflow before writing implementation code.
---

# Omni TDD

Write the check first. Confirm it fails for the right reason. Then write the smallest implementation that makes it pass.

## Use When

- Adding user-visible behavior
- Fixing a bug that should stay fixed
- Changing logic that can regress

## Core Loop

1. Write one small test or verification step for the behavior.
2. Run it and confirm it fails for the expected reason.
3. Implement the smallest change to make it pass.
4. Re-run the relevant checks.
5. Clean up only after green.

## Rules

- No behavior-changing implementation before a failing check exists
- Keep the test scope narrow
- Prefer the smallest coherent slice
- If a test is hard to write, simplify the design first

## Exceptions

You can skip this only for:

- docs-only changes
- pure configuration edits
- work where the user explicitly does not want a test-first flow
