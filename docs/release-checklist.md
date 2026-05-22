# Release Checklist

Use this checklist before publishing the Omni SuperDev suite to GitHub.

## Required

- [ ] Confirm the root [LICENSE](../LICENSE) matches how you want to publish your Omni SuperDev wrapper content
- [ ] Keep bundled third-party license files inside each bundled skill directory
- [ ] Keep [third-party.md](./third-party.md) with the upstream attribution list
- [ ] Copy the full `skills/` directory contents when documenting installation
- [ ] Keep `skills/_shared/` next to `skills/brooks-review/`
- [ ] Make sure no local/private paths or private project notes remain in README/docs

## Nice To Check

- [ ] Open [README.md](../README.md) and confirm the installation story is clear
- [ ] Open [install.md](./install.md) and confirm the final folder structure matches the repo
- [ ] Spot-check `skills/omni-superdev/SKILL.md` after any routing edits
- [ ] Run a quick script smoke test for `ui-ux-pro-max`, `webapp-testing`, and `gh-fix-ci`

## Suggested First GitHub Release Notes

- Self-contained Omni SuperDev suite
- Based on and adapted from the Superpowers workflow model
- Bundles common specialty skills so users do not need extra skill installs
- Includes third-party attribution and per-skill bundled license files
