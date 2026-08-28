# BMW Atlas Hub

> **Status: design-stage / pre-alpha. There is no runnable collector in this repository yet.**

BMW Atlas Hub is a planned self-hosted, local-first service for collecting, normalising, storing, and exposing telemetry from BMW vehicles. The intended implementation language is Rust.

The project is being explored as a BMW-focused counterpart to [Teslatlas Hub](https://github.com/magrathean-uk/teslatlas-hub), but it will not claim feature parity until authentication, data availability, rate limits, regional behaviour, and long-running reliability are proven against supported BMW interfaces.

## Intended principles

- **Owner-controlled data** — telemetry should remain on infrastructure controlled by the vehicle owner.
- **Read-only by default** — collection and analytics take priority over remote vehicle commands.
- **Authorised interfaces only** — no credential theft, paywall bypass, or circumvention of BMW access controls.
- **Explicit provenance** — retain source timestamps, collection timestamps, units, and quality flags.
- **Operationally boring** — bounded retries, durable state, observable failures, documented recovery, and safe upgrades.
- **Stable local contract** — consumers should depend on a versioned local API and schema rather than provider-specific payloads.

## Proposed scope

The design target is a small service with four clear boundaries:

1. **Provider adapter** — authorised BMW authentication and retrieval, isolated from the rest of the codebase.
2. **Normalisation** — stable vehicle, location, charging, range, odometer, state, and capability models.
3. **Storage** — durable local history with migrations, retention controls, and export/backup support.
4. **Local API** — authenticated read access for first-party apps, dashboards, and automation.

Exact provider support, deployment targets, database choice, polling model, and compatibility matrix are still open decisions. They should be documented before implementation is presented as usable.

## Non-goals

- Presenting undocumented or reverse-engineered behaviour as an official BMW API.
- Shipping default remote-control features with a large blast radius.
- Relaying vehicle data through a Magrathean-operated cloud service.
- Hiding degraded, stale, partial, or regionally unavailable source data.
- Claiming production readiness without long-running evidence and recovery testing.

## Security baseline

Vehicle credentials and tokens must never be committed, logged, included in diagnostics, or stored in plaintext. Any future implementation must use least privilege, redact sensitive payloads, bind local services safely by default, and document token revocation and data deletion.

Security reports should follow the shared [Magrathean security policy](https://github.com/magrathean-uk/.github/blob/main/SECURITY.md).

## Project status

The repository currently reserves the project name and documents the intended boundary. Before the first implementation release it still needs:

- a documented authentication and provider-support decision;
- an architecture decision record for storage and local API contracts;
- a threat model and credential lifecycle;
- fixtures that contain no personal or vehicle-identifying data;
- CI, tests, migrations, packaging, upgrade, backup, and rollback paths;
- an explicit software licence.

Until those exist, treat BMW Atlas Hub as a public design placeholder rather than deployable software.

## Trademarks and independence

BMW, BMW ConnectedDrive, and related names and marks are trademarks of Bayerische Motoren Werke AG. BMW Atlas Hub is an independent project and is not affiliated with, endorsed by, sponsored by, or supported by BMW AG.

No software licence is granted by this repository until a `LICENSE` file is published. Copyright © 2026 Magrathean UK Ltd. All rights reserved.
