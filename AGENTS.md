# Engineering agent contract

This repository defines public Packer templates for Wunderbox on vSphere. Treat
`.lit/repository.yml`, `RELEASE.md`, `TESTING.md`, `SECURITY.md`, and the accepted
Lightning IT Engineering ADRs as the governing repository contract.

- Work through a pull request into `develop`; promote reviewed `develop` to `main`.
- Run Packer formatting and validation for every template change.
- Never commit vSphere credentials, image secrets, private keys, or environment
  inventory.
- Keep external GitHub Actions pinned to full commit SHAs and permissions
  least-privilege.
- Preserve managed-file headers and change shared policy at
  `lightning-it/shared-assets-lit`.
- Run `python3 scripts/lit-push-ready.py push-ready` before pushing.
- Required remote checks and branch protection must not be bypassed.
- ADR 70 temporarily allows zero human/CODEOWNER approvals and separately
  documented protected-environment self-approval for immutable exact-SHA
  plan/apply evidence; it does not allow PR self-review or check bypass.
