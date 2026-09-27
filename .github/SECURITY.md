# Security

## Current scope

BMW Atlas Hub is a design-stage repository with no runnable collector, deployment code, or supported software release. Its documentation describes intended controls; those controls have not been implemented or validated here. This document does not constitute a security audit.

This repository adopts the [Magrathean security policy](https://github.com/magrathean-uk/.github/blob/main/SECURITY.md) for reporting, research conduct, safe harbour, and disclosure. The project context below does not narrow those terms.

## Report a concern privately

Use the contact listed in the shared policy: [contact@magrathean.uk](mailto:contact@magrathean.uk), with the subject `SECURITY: bmwatlas-hub`. Include the affected file or commit, the concern and likely impact, and enough redacted evidence to assess it. Do not post sensitive reports in public issues or pull requests.

GitHub private reporting is an option only if **Report a vulnerability** is available for this repository. No response deadline is promised here.

## Design requirements

The intended service would handle vehicle credentials, access tokens, and sensitive telemetry, including location history. Future implementation must:

- keep credentials and tokens out of commits, logs, diagnostics, and plaintext storage;
- use least privilege and redact sensitive payloads;
- bind local services safely by default and authenticate local API access;
- document token revocation and data deletion;
- preserve the distinction between authorised provider access, local storage, and local API consumers.

These requirements come from the proposed design. The authentication method, credential lifecycle, threat model, and deployment exposure remain open decisions. Assess new code against its actual inputs and trust boundaries; this placeholder does not establish security exclusions or accepted risks for future code.

The shared policy does not authorise testing BMW systems or other people's vehicles, accounts, or infrastructure. Such testing requires authority from the relevant owner.
