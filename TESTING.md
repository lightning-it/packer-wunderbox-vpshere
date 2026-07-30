# Testing

This repository uses the Lightning IT shared test model.

## Test Profiles

- `packer-fmt`
- `packer-validate`

## Supported Matrix

Operating systems and runners:

- `ubuntu-latest`

Products and runtimes:

- `wunderbox`
- `vsphere`

## When Tests Run

- Normal pull requests run the declared test profiles relevant to changed files.
- Renovate and verified shared-assets or repository-quality synchronization pull requests target `develop` and may auto-merge only after required checks pass.
- `develop` to `main` promotion pull requests run the strongest validation profile for this repository.
- Trusted `main` release workflows build and publish artifacts only after validation succeeds.

## Local Commands

Run the managed repository-policy checks:

```bash
python3 -m venv .venv
.venv/bin/python -m pip install PyYAML==6.0.3
.venv/bin/python scripts/lit-repository-quality.py
```

Run the repository-specific commands declared in
`.lit/push-ready.json` and the required CI workflow named in
`.lit/repository.yml`. Do not substitute unrelated toolchains.

Heavy Incus execution is not required for this repository. Do not report an Incus run as part of its acceptance evidence.

## Interpreting GitHub Actions

The GitHub Actions matrix is the primary dashboard. Job names should expose the repository class, OS/runtime where applicable, and profile, for example `repository / quality`.

Release evidence is generated during trusted release workflows and attached to or linked from GitHub Releases where the repository publishes release artifacts.

## OpenSSF Enrollment Promotion Evidence

The protected ancestry backmerge joins:

- reviewed `develop` source `4e57d8841bbf16e19415662ef85ba82a7177cff7`, which records OpenSSF Best Practices project `13890`;
- protected `main` source `d2beddb7f6f16095e2b176deae7ca617cb144985`.

The resulting two-parent commit preserves the `develop` tree while making the
current protected `main` history an ancestor. This evidence does not claim that
the repository already contains executable Packer templates or that the OpenSSF
questionnaire has reached the passing level.
