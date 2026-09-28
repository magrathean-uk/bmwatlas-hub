<h1 align="center">BMW Atlas Hub</h1>

<p align="center">A planned self-hosted service for collecting, normalising, storing and exposing BMW vehicle telemetry.</p>

<p align="center">
  <a href="docs/legal/overview.md">Licence</a>
</p>

**Design-stage / pre-alpha. There is no runnable collector in this repository.**

BMW Atlas Hub is a planned self-hosted service for collecting, normalising, storing, and exposing BMW vehicle telemetry on infrastructure controlled by the vehicle owner. Rust is the intended implementation language; no application code or build manifest is present yet.

The project takes inspiration from [Teslatlas Hub](https://github.com/magrathean-uk/teslatlas-hub). BMW authentication, data availability, rate limits, regional behaviour, and long-running reliability still need to be established. Feature parity is not claimed.

## Planned scope

The design has four proposed parts:

| Part | Intended responsibility |
| --- | --- |
| Provider adapter | Authorised BMW authentication and data retrieval, isolated from local storage and consumers. |
| Normalisation | Consistent vehicle, location, charging, range, odometer, state, and capability records. |
| Storage | Local history with migrations, retention controls, exports, and backups. |
| Local API | Authenticated read access for apps, dashboards, and automation. |

These are design goals, not available features. Provider support, deployment targets, database choice, polling behaviour, and the compatibility matrix remain undecided.

## Design boundaries

- Keep telemetry under the vehicle owner's control. A Magrathean-operated telemetry relay is outside the proposed scope.
- Prioritise collection and analysis, with read-only access by default. Remote vehicle commands are not a default feature.
- Use authorised interfaces. Do not bypass BMW access controls or describe undocumented behaviour as an official API.
- Preserve source and collection timestamps, units, and quality flags. Make stale, partial, and unavailable data visible.
- Design bounded retries, durable state, observable failures, recovery, and safe upgrades.
- Give consumers a versioned local API and schema, separate from provider-specific payloads.

## What is available now

This repository contains project documentation. There are no installation, build, test, or run commands, and no software release to deploy.

Before an implementation can be presented as usable, the project needs decisions and evidence for authentication and provider support, storage and API contracts, credential handling, synthetic fixtures, tests, migrations, packaging, upgrades, backups, and rollback. CI configuration is a separate maintainer decision.

For design proposals, documentation corrections, and questions, see [Contributing](.github/CONTRIBUTING.md). For sensitive reports, see [Security](.github/SECURITY.md).

## Licence and independence

BMW Atlas Hub is free software under the GNU Affero General Public License, version 3 only. See [LICENSE](LICENSE) and [NOTICE](NOTICE). Our [additional terms](docs/legal/additional-terms.md) and [legal notice](docs/legal/overview.md) apply alongside the licence; [governance](docs/governance/governance.md) explains how the project is maintained and how contributions are assigned. Copyright © 2026 MAGRATHEAN UK LTD.

Teslatlas Hub is a related Magrathean project, named here only as a design reference; its licence and contributor terms are separate from this project's.

BMW, BMW ConnectedDrive, and related names and marks are trademarks of Bayerische Motoren Werke AG. BMW Atlas Hub is independent. It is not affiliated with, endorsed by, sponsored by, or supported by BMW AG.

<sub>© 2026 MAGRATHEAN UK LTD · [Legal](https://github.com/magrathean-uk/.github/blob/main/LEGAL.md)</sub>
