# Repository guide

## Current boundary

BMW Atlas Hub is a documentation-only design placeholder. There is no application code, manifest, build system, or test suite. Keep proposed behaviour distinct from implemented features and retain the status in [README.md](README.md).

## Changes and checks

- Inspect the current files and Git status before editing; preserve unrelated work.
- Complete authorised changes through the relevant checks, including necessary safe local steps. Use bounded delegation for independent work when useful; ask only when a missing decision changes scope or authority.
- Check README claims against the current tree. Do not invent installation, build, test, provider, platform, or release support.
- For documentation changes, check relative links, headings, Markdown template front matter, and consistency between README, contribution, security, and licensing guidance. Report the checks and any remaining gaps.
- If implementation is added, document commands from its actual manifests and scripts and run the relevant checks before claiming completion. Documentation checks are not runtime or vehicle acceptance.

## Project constraints

- Preserve the owner-controlled, read-only-by-default design and authorised-provider boundary. Do not imply BMW endorsement or parity with Teslatlas Hub.
- Keep credentials, VINs, locations, account details, and private telemetry out of examples, fixtures, reports, and logs. Use synthetic examples.
- This project's licence and contributor terms follow Teslatlas Hub's structure (owner decision, 2026-09-27): AGPL-3.0-only with section 7 additional terms, and closed, maintainer-only contribution with assignment. See [NOTICE](NOTICE), [docs/legal/overview.md](docs/legal/overview.md) and [docs/governance/governance.md](docs/governance/governance.md).
- Legal files (`LICENSE`, `NOTICE`, `docs/legal/`, contributor terms, copyright and attribution strings) are owner-controlled: change them only on the owner's explicit instruction.
- Follow [Security](.github/SECURITY.md) for sensitive reports and [Contributing](.github/CONTRIBUTING.md) for public proposals.

Keep instructions here; [CLAUDE.md](CLAUDE.md) imports this file. Use short, direct prose and avoid em dashes in new documentation.
