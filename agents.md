# agents.md — theme-example

## Repository Overview

A reference implementation for creating custom themes for ownCloud Server (OC10). Demonstrates how to override branding elements including logos, colors, background images, copyright text and CSS styles.

- **Classification:** Infrastructure / Tooling
- **Activity Status:** Archived/Legacy
- **License:** AGPL-3.0
- **Language:** CSS, PHP

## Architecture & Key Paths

- `appinfo/` — ownCloud app metadata (`info.xml`)
- `core/` — Theme overrides (CSS, images)
- `defaults.php` — Text/branding overrides (copyright, slogans)
- `LICENSE` — AGPL-3.0 license file

## Development Conventions

- Standard ownCloud OC10 theme app structure
- The folder name must match the `<id>` in `appinfo/info.xml`
- No build system; files are edited directly
- Unsigned app (integrity check must be bypassed in config)

## Build & Test Commands

No build or test commands. This is a template/reference repository.

## Important Constraints

- **AGPL-3.0 copyleft license:** The OSPO Apache 2.0 migration requires auditing this copyleft license.
- **Archived/legacy:** Not actively maintained. For oCIS theming, use the web frontend configuration instead.
- **Unsigned app:** Requires `integrity.ignore.missing.app.signature` config entry.
- **OC10 only:** This theming approach applies only to ownCloud Server, not oCIS.


## OSPO Policy Constraints

### GitHub Actions
- **Only** use actions owned by `owncloud`, created by GitHub (`actions/*`), verified on the GitHub Marketplace, or verified by the ownCloud Maintainers.
- Pin all actions to their full commit SHA (not tags): `uses: actions/checkout@<SHA> # vX.Y.Z`
- Never introduce actions from unverified third parties.

### Dependency Management
- Dependabot is configured for automated dependency updates.
- Review and merge Dependabot PRs as part of regular maintenance.
- Do not introduce new dependencies without discussion in an issue first.

### Git Workflow
- **Rebase policy**: Always rebase; never create merge commits. Use `git pull --rebase` and `git rebase` before pushing.
- **Signed commits**: All commits **must** be PGP/GPG signed (`git commit -S -s`).
- **DCO sign-off**: Every commit needs a `Signed-off-by` line (`git commit -s`).
- **Conventional Commits & Squash Merge**: Use the [Conventional Commits](https://www.conventionalcommits.org/) format where the repository enforces it. Many repos use squash merge, where the PR title becomes the commit message on the default branch — apply Conventional Commits format to PR titles as well. A reusable GitHub Actions workflow enforces this.

## Context for AI Agents

- This is a template repository -- meant to be cloned and customized.
- No build system, CI or tests.
- Customization happens by editing `defaults.php` (texts), `core/css/styles.css` (visual) and replacing image files.
- For oCIS, theming is handled entirely differently through the web frontend.
