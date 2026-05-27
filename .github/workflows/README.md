# Reusable workflows

Org-wide reusable workflows for feature-today. Consumed from any repo with:

```yaml
uses: feature-today/.github/.github/workflows/<file>.yml@main
```

## Workflows

| File                          | Purpose                                                       |
| ----------------------------- | ------------------------------------------------------------- |
| `ci-node.yml`                 | Install (pnpm), typecheck, lint (oxlint), fmt.check, test, build |
| `conventional-commits.yml`    | Validate commits + PR title via `helpers4/action`             |
| `security-audit.yml`          | `pnpm audit` + OSV scanner                                    |
| `sbom.yml`                    | Generate CycloneDX SBOM artifact                              |
| `coverage.yml`                | Download coverage artifact + upload to Codecov                |
| `pr-checks.yml`               | Aggregator — calls all of the above with sensible defaults    |

## Minimal product-repo workflow

```yaml
# .github/workflows/pr-checks.yml
name: PR checks
on:
  pull_request:
  push:
    branches: [main]

jobs:
  pr-checks:
    uses: feature-today/.github/.github/workflows/pr-checks.yml@main
    secrets: inherit
```

Every product repo MUST expose these pnpm scripts: `typecheck`, `lint`, `fmt.check`, `test`, `test.coverage`, `build`.
