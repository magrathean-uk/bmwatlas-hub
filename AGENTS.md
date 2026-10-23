# BMW Atlas Hub context

BMW Atlas Hub is a documentation-only design placeholder. The repository has no application code, manifest, build system or test suite. [README.md](README.md) describes its current status and proposed behaviour.

## Design and documentation

The current design describes an owner-controlled, read-only default and authorised providers. The repository does not establish BMW endorsement or implemented feature parity with other products.

Documentation includes relative links, headings, Markdown template front matter, contribution guidance, security information and licensing material. Document consistency is separate from runtime or vehicle behaviour.

## Legal and contribution context

The project uses AGPL-3.0-only with section 7 additional terms and maintainer-only contribution with assignment, following the owner's 2026-09-27 decision. [NOTICE](NOTICE), [Legal overview](docs/legal/overview.md) and [Governance](docs/governance/governance.md) describe the terms. [Security](.github/SECURITY.md) and [Contributing](.github/CONTRIBUTING.md) describe reporting and proposals.

## Development environment

The machine's `~/dev/machine/env.zsh` provides routed storage variables. `$TMPDIR` identifies session scratch, `$CLEAN_DEV_BUILDS` identifies throwaway build output, and cache variables identify dependency caches. `.clean-development.json` records repository build and dependency directories.
