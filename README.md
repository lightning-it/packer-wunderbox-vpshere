# packer-wunderbox-vpshere

<!-- BEGIN LIT_QUALITY_BADGES -->

[![CI](https://github.com/lightning-it/packer-wunderbox-vpshere/actions/workflows/repository-quality.yml/badge.svg?branch=develop)](https://github.com/lightning-it/packer-wunderbox-vpshere/actions/workflows/repository-quality.yml)
[![OpenSSF Scorecard](https://api.scorecard.dev/projects/github.com/lightning-it/packer-wunderbox-vpshere/badge)](https://scorecard.dev/viewer/?uri=github.com/lightning-it/packer-wunderbox-vpshere)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)

<!-- END LIT_QUALITY_BADGES -->

<!-- BEGIN LIT_SHARED_RELEASE_MODEL -->

## Release and Quality Model

This repository follows the Lightning IT shared release and quality model.

See [RELEASE.md](./RELEASE.md) for:

- branch and release flow
- required quality checks
- test matrix
- release evidence
- artifact publishing
- supported repository-specific release behavior

Repository classification: **Packer Template Repository**.
Required test profiles: `packer-fmt, packer-validate`.
Publishing targets: `none`.

## Supported and Tested Platforms

| Platform / Product | Status | Validation |
|---|---:|---|
| ubuntu-latest | Supported | Packer validate |
| wunderbox | Tested where applicable | Packer validate |
| vsphere | Tested where applicable | Packer validate |

<!-- END LIT_SHARED_RELEASE_MODEL -->
Packer templates to build Wunderbox VM images on VMware vSphere.
