# GitHub Copilot review instructions

- Review every change for correctness, security, least privilege, and failure behavior.
- When present, apply all repository-specific guidance in `AGENTS.md` and path-scoped instruction files.
- Treat malformed external input as an error rather than silently coercing it.
- Check that credentials are scoped to the smallest required job.
- Require new or modified third-party GitHub Actions dependencies to use immutable commit SHAs.
- Explain each finding's impact and propose a concrete fix.
- Prefer a regression test for bugs and security issues.
- Treat `AGENTS.md` as the canonical repository contract. A managed
  `AGENTS_SHA256` marker below binds these instructions to the reviewed
  `AGENTS.md`; instruction drift is a blocking finding.

<!-- Managed contract: Codex and Copilot must apply AGENTS.md. -->
<!-- AGENTS_SHA256: a574603ae0305ca772345a243dc5d149b52b55ac7b1601ca6e5ecd84f7b9ec74 -->
