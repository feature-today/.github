# .github

Org-wide GitHub configuration for **feature-today** — reusable workflows, issue / PR templates, community files, dependabot, and the org profile.

This repository ships no runtime code. Each product repo references the reusable workflows here as:

```yaml
uses: feature-today/.github/.github/workflows/<workflow>.yml@main
```

See [`AGENTS.md`](./AGENTS.md) for canonical rules (the source of truth is [`feature-today/.dev/AGENTS.md`](https://github.com/feature-today/.dev/blob/main/AGENTS.md)).

## License

[AGPL-3.0-or-later](./LICENSE)
