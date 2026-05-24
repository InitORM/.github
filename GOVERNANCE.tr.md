# Yönetişim

English version: [GOVERNANCE.md](GOVERNANCE.md)

InitORM, tek bakımcılı küçük bir açık kaynak projedir. Bu belge, katkıda bulunanlara karşı şeffaf olmak amacıyla kararların nasıl alındığını açıklar.

## Roller

### Bakımcı

[Muhammet ŞAFAK](https://github.com/muhammetsafak), tüm InitORM paketlerinin proje lideri ve tek bakımcısıdır. Bakımcı şu konularda son söz sahibidir:

- API tasarımı ve geriye dönük uyumsuz değişiklikler
- Sürüm kapsamı, versiyonlama ve etiketleme
- Pull request'lerin kabul/red kararı ve kapsamı
- Code of Conduct uygulaması

### Katkıda bulunanlar

Issue açan, discussion başlatan, pull request gönderen veya dokümantasyonu iyileştiren herkes katkıda bulunandır. Katılım için yazma erişimi gerekmez.

## Kararlar nasıl alınır

- **Küçük değişiklikler** (hata düzeltmeleri, dokümantasyon, iç refactor): bakımcı pull request'i doğrudan inceleyip merge eder.
- **Public API değişiklikleri**: önce bir issue veya discussion'da tartışılır, sonra uygulanır. Geriye dönük uyumsuz değişiklikler, etkilenen pakette major sürüm artışı ve bağımlı paketlerde takip eden artışlar gerektirir.
- **Paketler arası değişiklikler**: [CONTRIBUTING.tr.md](CONTRIBUTING.tr.md) içindeki bağımlılık zinciri kurallarına göre işlenir.

Bir konu tartışmalıysa ve tartışmada uzlaşıya varılamazsa, bakımcının kararı kesindir.

## Versiyonlama

Tüm paketler [Semantic Versioning](https://semver.org/) izler. Tag'ler paket reposundan push edilir; release'ler, Packagist GitHub webhook'u aracılığıyla otomatik olarak [Packagist](https://packagist.org/packages/initorm/) üzerinde yayımlanır.

## Bu belgenin değiştirilmesi

Bu dosyaya karşı bir pull request açın. Yönetişim değişiklikleri bakımcı onayı gerektirir.
