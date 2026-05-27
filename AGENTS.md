# AGENTS.md — feature-today `.github`

This repository inherits the [canonical organization rules](https://github.com/feature-today/.dev/blob/main/AGENTS.md). Only project-specific details are documented here.

## Scope

- Org-wide GitHub configuration (templates, community files, profile)
- Reusable GitHub Actions workflows consumed by every product repo via `uses: feature-today/.github/.github/workflows/<file>.yml@main`
- Dependabot configuration

## Scopes (Conventional Commits)

Defined in `.vscode/settings.json` — `workflow`, `templates`, `profile`, `deps`, `ci`, `docs`, `security`.

## Rules

- No runtime code.
- Reusable workflows must accept `workflow_call` with documented inputs and minimal default permissions (`contents: read`).
- Pin third-party actions to a SHA when possible; otherwise pin to a major version tag.
- Every workflow declares its required Node version (default `24`) and uses pnpm via `pnpm/action-setup`.
