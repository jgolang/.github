# Contributing

Each module is its own repository and Go module. Before opening a pull request:

- Open an issue first for anything larger than a small fix, so the change can be agreed on.
- Branch from `master` as `<type>/<short-description>`; one focused change per pull request.
- Write tests first; use the standard `testing` package.
- Run, in the module directory: `gofmt -l .` (no output), `go vet ./...`,
  `go test -race ./...`, and `govulncheck ./...`. CI runs the same checks.
- Use [Conventional Commits](https://www.conventionalcommits.org/):
  `type(scope): description`, with `!` for breaking changes.
- Public API changes follow semantic versioning: deprecate before removing.

Supported Go versions are the two latest Go releases.
