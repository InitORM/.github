# Contributing to InitORM

Türkçe sürüm: [CONTRIBUTING.tr.md](CONTRIBUTING.tr.md)

Thank you for your interest in improving InitORM. This document covers the workflow that applies to every package under the [InitORM](https://github.com/InitORM) organization.

## Code of Conduct

All contributors are expected to follow the [Code of Conduct](CODE_OF_CONDUCT.md).

## Repository structure

InitORM is **not** a monorepo. The stack is published as four independent Composer packages, each with its own GitHub repository, releases, and tags:

```
QueryBuilder ─┐
              ├─► Database ─► ORM
DBAL ─────────┘
```

A breaking change in a lower-layer package ripples through every package above it. When your work crosses package boundaries:

1. Land and tag the lowest layer first.
2. Bump the `require` constraint in the dependent package(s) before merging.
3. Open separate pull requests in each affected repository, and link them to one another in the description.

## Prerequisites

- **PHP ≥ 8.0** with the `pdo` extension
- **Composer ≥ 2.0**
- A local clone of the relevant package repository (this is what you fork — not the `.github` repo)

```bash
git clone https://github.com/InitORM/<Package>.git
cd <Package>
composer install
```

## Tests

Only [QueryBuilder](https://github.com/InitORM/QueryBuilder) currently ships a PHPUnit suite. Run it with:

```bash
php vendor/bin/phpunit
```

If you add functionality to a package that has no tests yet, please include a minimal PHPUnit setup that covers at least the new behavior.

## Code style

- Follow [PSR-12](https://www.php-fig.org/psr/psr-12/).
- Stay consistent with surrounding code; do not reformat untouched lines.
- Keep PHPDoc blocks on public APIs up to date — the `Facade\DB` class in Database relies on `@method static` annotations to expose the builder surface.

## Commit and pull-request workflow

1. Branch from `master` (or the relevant `v1.x` line if you are back-porting).
2. Keep commits focused; describe the *why*, not just the *what*.
3. Reference issues with `Fixes #123` or `Refs #123` when applicable.
4. Open the pull request against `master`; fill in the PR template.
5. Wait for review. The maintainer ([@muhammetsafak](https://github.com/muhammetsafak)) reviews PRs personally; please be patient.

## Reporting bugs

Use the **Bug report** issue form in the affected package. Always include:

- Package and version (`composer show initorm/<package>`)
- PHP version (`php -v`)
- A minimal reproduction (preferably runnable)

## Security issues

**Do not** open public issues for security vulnerabilities. Follow the disclosure process in [SECURITY.md](SECURITY.md).

## License

By contributing, you agree that your contributions will be licensed under the [MIT License](https://opensource.org/licenses/MIT) — the same license as the rest of the project.
