# Governance

Türkçe sürüm: [GOVERNANCE.tr.md](GOVERNANCE.tr.md)

InitORM is a small, single-maintainer open-source project. This document describes how decisions are made, in the interest of being transparent with contributors.

## Roles

### Maintainer

[Muhammet ŞAFAK](https://github.com/muhammetsafak) is the project lead and sole maintainer across all InitORM packages. The maintainer has final say on:

- API design and breaking changes
- Release scope, versioning, and tagging
- Acceptance, rejection, and scope of pull requests
- Code of Conduct enforcement

### Contributors

Anyone who opens an issue, starts a discussion, submits a pull request, or improves documentation is a contributor. Contributors do not need write access to participate.

## How decisions are made

- **Small changes** (bug fixes, documentation, internal refactors): the maintainer reviews and merges the pull request directly.
- **Public API changes**: discussed first in an issue or discussion, then implemented. Breaking changes require a major-version bump in the affected package and a follow-up bump in dependent packages.
- **Cross-package changes**: handled per the dependency-chain rules in [CONTRIBUTING.md](CONTRIBUTING.md).

If an issue is contentious and consensus is not reached in discussion, the maintainer's decision is final.

## Versioning

All packages follow [Semantic Versioning](https://semver.org/). Tags are pushed from the package repository, and releases are published to [Packagist](https://packagist.org/packages/initorm/) automatically via the Packagist GitHub webhook.

## Changing this document

Open a pull request against this file. Changes to governance require maintainer approval.
