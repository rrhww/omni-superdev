---
name: planning-with-files
description: Use when maintaining, migrating, or auditing the legacy planning-with-files module during omni-superdev consolidation. Ordinary software or product work should use omni-superdev, which now owns persistent planning mode.
allowed-tools: "Read Write Edit Bash Glob Grep"
metadata:
  version: "2.37.0"

---

# Planning with Files (Legacy Compatibility)

This module is deprecated as a primary workflow entrypoint.

Persistent planning is now owned by `omni-superdev` through its internal `persistent-planning` mode.

Canonical resources now live here:

- `templates/planning/`
- `scripts/planning/`
- `references/planning/`
- `references/modes/persistent-planning.md`

Keep this bundled directory only for migration, compatibility, and auditing.
