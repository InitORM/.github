# InitORM'a katkı

English version: [CONTRIBUTING.md](CONTRIBUTING.md)

InitORM'u geliştirmeye gösterdiğiniz ilgi için teşekkürler. Bu belge, [InitORM](https://github.com/InitORM) organizasyonu altındaki her pakete uygulanan çalışma akışını kapsar.

## Code of Conduct

Tüm katkıda bulunanların [Code of Conduct](CODE_OF_CONDUCT.tr.md) belgesine uyması beklenir.

## Repo yapısı

InitORM bir monorepo **değildir**. Yığın, her biri kendi GitHub reposu, sürümleri ve etiketleri olan dört bağımsız Composer paketi olarak yayımlanır:

```
QueryBuilder ─┐
              ├─► Database ─► ORM
DBAL ─────────┘
```

Alt katmandaki bir paketteki geriye dönük uyumsuz değişiklik, üstündeki tüm paketlere yansır. Çalışmanız paket sınırlarını aşıyorsa:

1. Önce en alt katmanı merge edip tag'leyin.
2. Bağımlı paket(ler)deki `require` kısıtını merge öncesi güncelleyin.
3. Etkilenen her repoda ayrı pull request açın ve açıklamalarda birbirine link verin.

## Ön koşullar

- `pdo` eklentisiyle birlikte **PHP ≥ 8.0**
- **Composer ≥ 2.0**
- İlgili paket reposunun yerel klonu (fork edilecek olan budur, `.github` reposu değil)

```bash
git clone https://github.com/InitORM/<Paket>.git
cd <Paket>
composer install
```

## Testler

Şu an PHPUnit test suite içeren tek paket [QueryBuilder](https://github.com/InitORM/QueryBuilder). Çalıştırmak için:

```bash
php vendor/bin/phpunit
```

Test suite barındırmayan bir pakete yeni işlevsellik eklerseniz, lütfen en az yeni davranışı kapsayan minimal bir PHPUnit kurulumu ekleyin.

## Kod stili

- [PSR-12](https://www.php-fig.org/psr/psr-12/) uyumlu yazın.
- Çevredeki kodla tutarlı kalın; dokunmadığınız satırları yeniden biçimlendirmeyin.
- Public API'lerin PHPDoc bloklarını güncel tutun — Database paketindeki `Facade\DB` sınıfı, builder yüzeyini açığa çıkarmak için `@method static` notlarına dayanır.

## Commit ve pull-request akışı

1. `master`'dan (geriye port ediyorsanız ilgili `v1.x` hattından) dallanın.
2. Commit'leri odaklı tutun; sadece *ne* yapıldığını değil, *neden* yapıldığını yazın.
3. İlgili konuları `Fixes #123` veya `Refs #123` ile referans verin.
4. Pull request'i `master`'a karşı açın; PR şablonunu doldurun.
5. İncelemeyi bekleyin. Bakımcı ([@muhammetsafak](https://github.com/muhammetsafak)) PR'ları kişisel olarak inceler; lütfen sabırlı olun.

## Hata bildirme

Etkilenen paketteki **Bug report** issue formunu kullanın. Daima şunları ekleyin:

- Paket ve sürüm (`composer show initorm/<paket>`)
- PHP sürümü (`php -v`)
- Mümkünse çalıştırılabilir, minimal bir reprodüksiyon

## Güvenlik sorunları

Güvenlik açıkları için public issue **açmayın**. [SECURITY.tr.md](SECURITY.tr.md) içindeki açıklama sürecini izleyin.

## Lisans

Katkıda bulunarak, katkılarınızın projenin geri kalanıyla aynı lisans olan [MIT Lisansı](https://opensource.org/licenses/MIT) altında lisanslanacağını kabul etmiş olursunuz.
