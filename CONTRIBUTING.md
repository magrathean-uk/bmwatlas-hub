# Contributing and support

BMW Atlas Hub is at the design stage. There is no collector to install or troubleshoot. Useful contributions include documentation corrections and evidence about authorised provider access, data availability, regional limits, storage, and local API design.

## Propose a change

Use [GitHub issues](https://github.com/magrathean-uk/bmwatlas-hub/issues) for non-sensitive questions and design proposals. Describe the problem, the proposed decision, alternatives, and supporting references. Separate observations from assumptions, and give the date and context of provider evidence.

For a pull request, explain the change and its scope. Link the relevant issue when there is one. Keep changes focused and state which claims and links you checked. There are no build or test commands in the current repository.

The project has no software licence yet. Read [Licensing](docs/licensing.md) before proposing code or third-party material. Licensing and contribution terms need to be settled before external implementation work is accepted; no assignment or inbound licence terms are established by this guide.

## Keep reports safe

Use synthetic examples. Do not attach credentials, tokens, account identifiers, VINs, location history, vehicle exports, or private service details. Public issues are not a place for vulnerability reports; use [Security](SECURITY.md).

Provider research must stay within authorised access. Document uncertainty and regional differences instead of generalising from one vehicle or account.

## Check documentation

Before submitting, check that local links resolve, headings and tables read correctly, and new claims agree with the current repository. Preserve the licence and trademark statements. Keep planned features labelled as plans and record any references you could not verify.

When implementation begins, consider [Clean Development](https://github.com/magrathean-uk/clean-development) for managing supported development caches and build output. It is optional; this documentation-only repository needs no setup.
