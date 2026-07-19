# kur-test

Bu repo, **GitHub Actions ile otomasyon öğrenmek amacıyla** hazırlanmış küçük,
eğitim/deneme amaçlı bir projedir. Her gün otomatik çalışan bir iş (workflow),
güncel döviz kurlarını çekip bu dosyaya ve `rates.json` dosyasına yazıyor.

## Nasıl çalışır?

`.github/workflows/test.yml` içindeki iş, her gün TR saatiyle sabah otomatik
tetikleniyor (istenirse Actions sekmesinden elle de çalıştırılabilir):

1. [Frankfurter API](https://frankfurter.dev)'den güncel kuru çeker,
2. `rates.json` dosyasına ham veriyi yazar,
3. Aşağıdaki tabloyu günceller,
4. Değişikliği otomatik olarak commit'ler.

## Kaynak ve önemli not

Kur verisi, Frankfurter API üzerinden **Avrupa Merkez Bankası (ECB)**
referans kurlarına dayanır. ECB'nin kendi belirttiği gibi bu kurlar
**yalnızca bilgi amaçlıdır**, gerçek işlem/ödeme amacıyla kullanılmamalıdır.
EUR→TRY satırı ECB tarafından doğrudan yayınlanmaz; USD bazlı iki kurdan
(`USD→TRY ÷ USD→EUR`) bu repo içinde hesaplanır, yani türetilmiş bir
değerdir.

Bu proje herhangi bir finansal tavsiye, ürün veya hizmet değildir —
tamamen öğrenme ve kişisel kullanım amaçlıdır.

## Başka bir projeden nasıl kullanılır?

Ham veriye şu adresten ulaşılabilir: https://raw.githubusercontent.com/omerrmanav/kur-test/main/rates.json

