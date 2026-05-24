<h1 align="center">InitORM</h1>

<p align="center">
  Lightweight, PDO-based PHP database stack — Query Builder, DBAL, Database Manager, and ORM as independent Composer packages.
</p>

<p align="center">
  <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="MIT"></a>
  <a href="https://www.php.net/"><img src="https://img.shields.io/badge/PHP-%E2%89%A58.0-777BB4.svg" alt="PHP 8.0+"></a>
  <a href="https://packagist.org/packages/initorm/orm"><img src="https://img.shields.io/packagist/dt/initorm/orm.svg?label=ORM%20downloads" alt="Packagist downloads"></a>
</p>

---

InitORM is an open-source PHP database stack distributed under the MIT license. Each layer is its own Composer package, so you can pull in only the layer you need.

## Packages

| Package | Purpose | Composer |
| --- | --- | --- |
| [QueryBuilder](https://github.com/InitORM/QueryBuilder) | Pure SQL query assembly with parameter binding | `composer require initorm/query-builder` |
| [DBAL](https://github.com/InitORM/DBAL) | PDO connection lifecycle + data mapper | `composer require initorm/dbal` |
| [Database](https://github.com/InitORM/Database) | Query Builder + DBAL with CRUD shortcuts and a static facade | `composer require initorm/database` |
| [ORM](https://github.com/InitORM/ORM) | Models, entities, accessors/mutators, soft deletes | `composer require initorm/orm` |

## How the layers fit together

```
QueryBuilder ─┐
              ├─► Database ─► ORM
DBAL ─────────┘
```

Pick the lowest layer that solves your problem — you do not have to take the full ORM if all you need is a query builder.

## Quick start

```bash
composer require initorm/orm
```

```php
use InitORM\ORM\Model;

class User extends Model
{
    protected array $credentials = [
        'dsn'      => 'mysql:host=localhost;dbname=test',
        'username' => 'root',
        'password' => '',
    ];

    protected string $schema   = 'users';
    protected string $schemaId = 'id';
}
```

## Documentation

Each package ships its own GitHub Wiki:

- [QueryBuilder Wiki](https://github.com/InitORM/QueryBuilder/wiki)
- [DBAL Wiki](https://github.com/InitORM/DBAL/wiki)
- [Database Wiki](https://github.com/InitORM/Database/wiki)
- [ORM Wiki](https://github.com/InitORM/ORM/wiki)

## Community

- **Bug reports** → open an issue in the affected package repository
- **Questions & ideas** → start a [Discussion](https://github.com/orgs/InitORM/discussions)
- **Security disclosures** → see [SECURITY.md](https://github.com/InitORM/.github/blob/main/SECURITY.md)

Contribution guidelines live in [`CONTRIBUTING.md`](https://github.com/InitORM/.github/blob/main/CONTRIBUTING.md) (also available in [Turkish](https://github.com/InitORM/.github/blob/main/CONTRIBUTING.tr.md)).

![initorm-icon](https://github.com/InitORM/.github/assets/104234499/b9be28df-b0d0-4e83-9ab3-eab4ede0a7a2)
