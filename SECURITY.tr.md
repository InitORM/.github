# Güvenlik Politikası

English version: [SECURITY.md](SECURITY.md)

## Desteklenen sürümler

Güvenlik güncellemeleri, her InitORM paketinin en güncel minor sürümü için sağlanır. Eski minor sürümler, bakımcının takdirine bağlı olarak düzeltme alabilir.

| Paket | Desteklenen |
| --- | --- |
| `initorm/orm` | en güncel `1.x` |
| `initorm/database` | en güncel `1.x` |
| `initorm/dbal` | en güncel `1.x` |
| `initorm/query-builder` | en güncel `1.x` |

## Güvenlik açığı bildirimi

Güvenlik açıkları için **public** issue veya discussion **açmayın**.

Aşağıdaki kanallardan birini kullanın:

1. **GitHub Private Vulnerability Reporting** (tercih edilir): Etkilenen paket reposunun **Security** sekmesinden rapor açın — örneğin <https://github.com/InitORM/ORM/security/advisories/new>.
2. **E-posta**: <info@muhammetsafak.com.tr> adresine `[InitORM Security] <paket>` konu satırıyla.

Lütfen şu bilgileri ekleyin:

- Etkilenen paket ve sürüm(ler)
- PHP ve veritabanı sürücü sürümleri
- Sorunun açıklaması ve etkisi
- Adım adım reprodüksiyon (PoC memnuniyetle karşılanır)
- Önerilen çözüm (varsa)

## Ne beklemeli

- **5 iş günü** içinde alındı onayı.
- **14 iş günü** içinde değerlendirme ve ilk yanıt.
- Koordineli açıklama: düzeltme hazır olduğunda, anonim kalınmak istenmediği sürece raporlayana atıfta bulunan bir advisory yayımlanır.

InitORM'u ve kullanıcılarını güvende tuttuğunuz için teşekkürler.
