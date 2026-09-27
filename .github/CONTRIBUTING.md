# Contributing

Bug reports, documentation fixes and focused changes are welcome. Before you
start substantial work, discuss any change to the design, data model,
authentication approach, licensing or branding.

## How changes are made

Only the maintainer changes the official repository. To propose a change,
open a pull request. The maintainer reviews it and may accept, amend or
decline it. See [Governance](../docs/governance/governance.md).

## Prepare a change

Use synthetic data. Never submit credentials, VINs, precise journeys, private
logs or production databases. Describe the problem you are solving, keep the
change small, and leave unrelated content alone.

## Check the result

This repository is documentation-only; there is no build or test suite yet.
Check that local links resolve, headings and tables read correctly, and new
claims agree with the current repository. Report the checks you ran.

## File headers

Once source code exists, every file will begin with
`SPDX-License-Identifier: AGPL-3.0-only`. In third-party or adapted files,
keep the original notices and add a dated note of your changes.

## Contributor terms

By opening a pull request, you agree to these terms for the material in it
(your **contribution**):

1. **Sign-off.** Sign off every commit under the
   [Developer Certificate of Origin 1.1](../docs/governance/developer-certificate-of-origin-1.1.md)
   (`git commit -s`), using your real name.
2. **Licence.** You license your contribution under AGPL-3.0-only, this
   project's licence. You also give MAGRATHEAN UK LTD (**Magrathean**) the
   right to license it on other terms.
3. **Assignment.** Before a substantial contribution is merged, Magrathean
   will ask you to sign an assignment agreement for
   [individuals](../docs/governance/individual-contributor-assignment-agreement.md)
   or [organisations](../docs/governance/corporate-contributor-assignment-agreement.md).
   Signed agreements are kept private.
4. **Your rights.** You may go on using your own contribution for any
   purpose. You are credited as its author in the Git history and the
   release notes.
5. **Issues and comments.** Only pull requests are contributions. Magrathean
   claims no rights in issues, comments or discussions. If the maintainer
   wants to use material posted there, you will be asked to submit it as a
   pull request.
6. **Disclosure.** In the pull request, identify anything you did not write
   yourself, with its source and licence, and any employer or client
   restriction.
7. **No obligation.** Magrathean need not accept or keep any contribution.

## Submit

GitHub holds the source only. Do not add CI, security automation, releases or
binary publication unless the owner asks.

Report vulnerabilities privately through [SECURITY.md](SECURITY.md). Follow
the [Magrathean code of conduct](https://github.com/magrathean-uk/.github/blob/main/CODE_OF_CONDUCT.md).
