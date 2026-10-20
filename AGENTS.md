# Repository guide

## Current boundary

BMW Atlas Hub is a documentation-only design placeholder. There is no application code, manifest, build system, or test suite. Keep proposed behaviour distinct from implemented features and retain the status in [README.md](README.md).

## Changes and checks

- Inspect the current files and Git status before editing; preserve unrelated work.
- Complete authorised changes through the relevant checks, including necessary safe local steps. Use bounded delegation for independent work when useful; ask only when a missing decision changes scope or authority.
- Check README claims against the current tree. Do not invent installation, build, test, provider, platform, or release support.
- For documentation changes, check relative links, headings, Markdown template front matter, and consistency between README, contribution, security, and licensing guidance. Report the checks and any remaining gaps.
- If implementation is added, document commands from its actual manifests and scripts and run the relevant checks before claiming completion. Documentation checks are not runtime or vehicle acceptance.

<!-- clean-development-policy:v2 (canonical text: ~/dev/source/dev-bootstrap/snippets/clean-development-policy.md) -->
## Clean development (mandatory)

This project follows [Clean Development](https://github.com/magrathean-uk/clean-development) and the machine rule that nothing creates tool state under `~` (only the allow-listed agent homes).

- Load `~/dev/machine/env.zsh`; `~/.zshenv` does this for every zsh. Machine storage preferences live in `~/dev/machine/storage.conf`; workspace navigation is in `~/dev/START-HERE.md`.
- New sessions select `/Volumes/4TB/machine/cache` when the configured volume is actually mounted and writable, otherwise `~/dev/machine/cache` for ordinary smaller work. Use routed `DEVCACHE`, `CLEAN_DEVELOPMENT_{ROOT,CACHE_ROOT,BUILD_ROOT,SCRATCH_ROOT}`, `BOLYKI_DEV_LIBS` and `TMPDIR`; builds and scratch are beneath the selected cache. Keep active-session destinations fixed; stop if required storage disappears. Other users configure their own volume and fallback.
- SpecieX, large video/model jobs and VMs require external storage; never use internal fallback. Persistent labs, credentials, installed toolchains, source and final deliverables are not disposable caches.
- All active Git entry points belong under `~/dev/source/`, third-party repositories in `source/third-party/`, websites in `source/magrathean/`, and Teslatlas products/docs in `source/teslatlas-service/`. Do not read, scan, move or edit `~/dev/porn`.
- Preserve routed tool homes/caches, caller overrides and SDK/toolchain choices. Never unset or bypass routing. Scrubbed environments must restore the reviewed routing before cache-writing tools run; preserve intentional hermetic Git/Cargo isolation.
- Run builds, tests, installs and anything else that writes caches or build output through Clean Development: `clean-development run --session session-only -- <command>`. Follow its docs and keep its receipts.
- Do not add installers or scripts that default into `~` (`~/.cargo`, `~/.rustup`, `~/.cache`, `~/.npm`, `~/.swiftpm`, `~/.gradle`, ...) and do not hardcode `$HOME` paths for caches; use the routed variables.
- Before finishing, run `dev-env-check`, `dev-projects-check` and `dev-audit`; require passing environment/project checks and no new home-audit entries compared with the task baseline. Fix violations your work caused.

## Project constraints

- Preserve the owner-controlled, read-only-by-default design and authorised-provider boundary. Do not imply BMW endorsement or parity with Teslatlas Hub.
- Keep credentials, VINs, locations, account details, and private telemetry out of examples, fixtures, reports, and logs. Use synthetic examples.
- This project's licence and contributor terms follow Teslatlas Hub's structure (owner decision, 2026-09-27): AGPL-3.0-only with section 7 additional terms, and closed, maintainer-only contribution with assignment. See [NOTICE](NOTICE), [docs/legal/overview.md](docs/legal/overview.md) and [docs/governance/governance.md](docs/governance/governance.md).
- Legal files (`LICENSE`, `NOTICE`, `docs/legal/`, contributor terms, copyright and attribution strings) are owner-controlled: change them only on the owner's explicit instruction.
- Follow [Security](.github/SECURITY.md) for sensitive reports and [Contributing](.github/CONTRIBUTING.md) for public proposals.

Keep instructions here; [CLAUDE.md](CLAUDE.md) imports this file. Use short, direct prose and avoid em dashes in new documentation.
