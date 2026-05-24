<!--
TR / Türkçe: Lütfen aşağıdaki bölümleri doldurun.
EN / English: Please fill in the sections below.
-->

## Özet / Summary

<!-- TR: Bu PR'ın ne yaptığını ve neden gerekli olduğunu kısaca açıklayın. -->
<!-- EN: Briefly describe what this PR does and why it is needed. -->

## Etkilenen paket / Affected package

- [ ] `initorm/query-builder`
- [ ] `initorm/dbal`
- [ ] `initorm/database`
- [ ] `initorm/orm`

## Değişiklik türü / Type of change

- [ ] Hata düzeltmesi / Bug fix
- [ ] Yeni özellik / New feature
- [ ] Geriye dönük uyumsuz değişiklik / Breaking change
- [ ] Dokümantasyon / Documentation
- [ ] Refactor — kullanıcıya görünür değişiklik yok / no user-visible change

## İlgili konu / Related issues

<!-- Fixes #123 / Refs #123 -->

## Bağımlılık zinciri etkisi / Dependency chain impact

<!--
TR: Daha alt katmandaki bir pakette (QueryBuilder veya DBAL) değişiklik yaptıysanız,
bağımlı paketlerde (Database, ORM) sürüm yükseltmesi gerekip gerekmediğini belirtin.
EN: If you changed a lower-layer package (QueryBuilder or DBAL), state whether
dependent packages (Database, ORM) need a version bump and link related PRs.
-->

- [ ] Bu değişiklik yalnızca bu paketi etkiler / This change only affects this package
- [ ] Bağımlı paketlerde takip PR'ı açıldı / Follow-up PR opened in dependent package(s): _link_

## Test / Tests

- [ ] `php vendor/bin/phpunit` yerel olarak çalıştırıldı / ran locally
- [ ] Yeni davranış için test eklendi / Added tests for new behavior
- [ ] Bu paket test suite barındırmıyor — manuel test edildi / This package has no test suite — tested manually

## Kontrol listesi / Checklist

- [ ] PSR-12 kod stiline uygun / Code follows PSR-12
- [ ] Public API PHPDoc güncel / Public API PHPDoc is up to date
- [ ] `Facade\DB` etkilendiyse `@method static` notları güncellendi / `@method static` annotations updated if `Facade\DB` is affected
- [ ] [CONTRIBUTING](https://github.com/InitORM/.github/blob/main/CONTRIBUTING.md) okundu / read

## Notlar / Additional notes

<!-- Ekran görüntüleri, benchmark sonuçları, vb. / Screenshots, benchmarks, etc. -->
