---
name: omni-debug
description: Use when a bug, failing test, broken behavior, or unexpected result needs root-cause-first debugging inside the Omni SuperDev suite.
---

# Omni Debug

Debug by proving the cause before proposing the fix.

## Use When

- A test is failing
- A bug is reproducible
- Output is surprising or inconsistent
- A system behavior changed unexpectedly

## Process

1. Reproduce the problem clearly.
2. Narrow the scope to the smallest failing path.
3. Gather evidence from logs, inputs, outputs, and surrounding code.
4. Form one concrete hypothesis at a time.
5. Test the hypothesis before changing implementation.
6. Once the cause is confirmed, apply the smallest fix.
7. Add or run a regression check.

## Rules

- Do not guess-fix first
- Do not stack multiple speculative changes
- Prefer evidence over intuition
- Record what proved the cause
