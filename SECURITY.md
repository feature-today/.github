# Security Policy

## Reporting a Vulnerability

If you discover a security vulnerability in any feature-today project, please report it responsibly.

**Do NOT open a public issue.**

Use [GitHub Security Advisories](https://github.com/feature-today/.github/security/advisories/new) — choose the affected repository when filing.

## What to Include

- Description of the vulnerability
- Steps to reproduce / proof-of-concept
- Affected version(s) and component(s)
- Potential impact
- Suggested fix, if any

## Response Timeline

- **Acknowledgment**: within 48 hours
- **Initial assessment**: within 1 week
- **Fix and coordinated disclosure**: timeline agreed with the reporter

## Supported Versions

Only the latest released version of each project is supported with security updates.

## Security Practices

Repositories in this org follow:

- Branch protection on `main` (linear history, required status checks)
- Minimal permissions in GitHub Actions workflows (`contents: read` by default)
- Dependabot updates (weekly) for `npm` and `github-actions`
- Automated dependency audit (`pnpm audit`) on every PR
- SBOM generation (CycloneDX) on every PR
- Conventional commits enforced via `helpers4/action/conventional-commits`
