# Contributing to the XChain Platform

This is the organization-wide default contributing guide. Most repositories ship
their own `CONTRIBUTING.md` with the exact build, test, and release steps for
that service; that file takes precedence where it exists. This default covers
the conventions shared across the platform.

If you're reporting a security issue, **stop here** and read `SECURITY.md`
instead. Security reports go through a private channel.

## Before you start

- Find the repository that owns the code you want to change (see the
  [organization profile](https://github.com/XChain-Platform) for the repo map).
- Read that repository's `README.md` and `CONTRIBUTING.md` for its specific
  setup and test commands. For who owns each area, see `MAINTAINERS.md` in the
  [`xchain-documentation`](https://github.com/XChain-Platform/xchain-documentation)
  repository.
- For anything larger than a bug fix or a single self-contained change, open an
  issue first to align on direction before opening a PR.

## Shared conventions

- **Node.js 22** exactly. The platform pins Node 22 fleet-wide; other major
  versions are not validated and some fail in non-obvious ways.
- **Plain JavaScript**, no TypeScript. Match the style of the surrounding file:
  naming, structure, and comment density. Comment the *why* that isn't obvious,
  not what the code already says.
- **Never use the em-dash character** in code, comments, or docs. Rewrite the
  sentence instead.
- **Branch off the default branch** (`master` for most repos, `main` for some)
  and keep history linear (rebase, don't merge).
- **No `Co-Authored-By` trailers.** This is a project policy.
- **Never `--no-verify`.** If a hook fails, fix the cause; don't bypass it.
- **Never commit a `.env` or any real credential.** Secrets live only in a local
  `.env`, loaded at runtime.

## Pull requests

1. Run the repository's test suite and confirm it passes.
2. Update that repository's `CHANGELOG.md` where one exists.
3. Make sure `git status` is clean apart from intended changes.
4. Open the PR with a clear title and a description of what changed and why.

For non-security bugs, open an issue on the relevant repository. For security
bugs, see `SECURITY.md`.

## Code of Conduct

We follow our [Code of Conduct](./CODE_OF_CONDUCT.md), adapted from the
Contributor Covenant 2.1. Be kind, assume good faith, and disagree without being
a jerk.
