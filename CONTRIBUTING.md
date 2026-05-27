# Contributing to feature-today

Thanks for your interest in contributing! This document covers what is shared by every feature-today repository. Each repo may add its own `CONTRIBUTING.md` with project-specific details.

## Code of Conduct

This project is governed by the [Code of Conduct](./CODE_OF_CONDUCT.md). By participating, you agree to uphold it.

## Workspace setup

See [`feature-today/.dev`](https://github.com/feature-today/.dev) for the multi-root workspace, the unified DevContainer, and the canonical agent rules.

Quick start:

```bash
mkdir feature-today && cd feature-today
gh repo clone feature-today/.dev
gh repo clone feature-today/.github
gh repo clone feature-today/website
gh repo clone feature-today/my
gh repo clone feature-today/common
gh repo clone feature-today/server
code .dev/feature-today.code-workspace
```

## Pull Requests

1. Fork & branch off `main` — `git switch -c feat/short-description`
2. Make focused commits — see commit format below
3. Run locally: `pnpm typecheck && pnpm lint && pnpm fmt.check && pnpm test && pnpm build`
4. Push and open a PR
5. Wait for CI green + at least one review

PR scope guidelines:
- Keep PRs small and focused (one logical change)
- Update docs when you change behavior
- Add or update tests
- Reference the issue: `Closes #123`

## Commit messages

[Conventional Commits](https://www.conventionalcommits.org/) with a **gitmoji**:

```
<type>(<scope>): <emoji> <description>
```

- Description ≤72 chars, lowercase, imperative mood, no trailing period
- Always include exactly ONE emoji
- Allowed scopes per repo: see `.vscode/settings.json` (`conventionalCommits.scopes`)

Type → emoji table: see [`feature-today/.dev/AGENTS.md`](https://github.com/feature-today/.dev/blob/main/AGENTS.md).

Examples:

- `feat(select): ✨ add project filtering`
- `fix(ci): 🐛 pin pnpm version`
- `docs(readme): 📝 clarify clone order`

## Stack expectations

- Node ≥ 24, pnpm (latest)
- TypeScript strict, no `any`
- oxlint (no ESLint), oxc-formatter (no Prettier)
- Vitest for tests
- AGPL-3.0 header on every source file (`auto-header` devcontainer feature handles this)
- Everything in **English**

## Reporting bugs / suggesting features

Open an issue in the relevant repo. Use the provided templates.

## Security

See [`SECURITY.md`](./SECURITY.md) — please **do not** open public issues for vulnerabilities.

---

Happy contributing! 🎉
