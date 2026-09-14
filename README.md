# UrunAciklama

Entegra ürün formlarına elle tek tek girilen açıklamaları hızlandırmak için basit, tek dosyalık bir araç.

## Ne işe yarar?

AI'dan aldığınız ham açıklama metnini (Kullanıcı Avantajları, Teknik Özellikler, Paket İçeriği,
Nerelerde Kullanılır, SSS bölümleriyle) yapıştırın; araç bunu Entegra'nın kullandığı HTML biçimine
(mavi başlık kutuları + madde işaretleri) otomatik çevirir. Ürünleri listeye ekleyip toplu Excel
dosyası olarak da indirebilirsiniz.

## Kullanım

`index.html` dosyasını doğrudan tarayıcıda açın (çift tıklamak yeterli, kurulum gerekmez).

1. Ürün kodunu ve AI'dan aldığınız ham metni yapıştırın.
2. Sağdaki önizlemeden kontrol edin.
3. Tek ürün için "Kaynak Kodunu Kopyala" ile Entegra'nın Kaynak Kodu alanına direkt yapıştırın,
   ya da "Listeye Ekle" ile ürünü listeye ekleyip toplu işleme devam edin.
4. Bittiğinde "Excel Olarak İndir" ile tüm listeyi `.xlsx` olarak indirin.

## Bilinen eksik

Excel çıktısındaki sütunlar şu an genel (`Ürün Kodu`, `Açıklama (HTML)`). Entegra'nın gerçek toplu
içe aktarma şablonu (sütun adları/sırası) netleşince buna göre uyarlanacak.

## Format kuralları (ham metin girerken)

- Her bölüm başlığı ("Kullanıcı Avantajları", "Teknik Özellikler", "Paket İçeriği",
  "... Nerelerde Kullanılır?", "Sıkça Sorulan Sorular (SSS)") kendi satırında olmalı.
- Madde satırları `*` veya `-` ile başlamalı.
- Teknik Özellikler'de `Etiket: Değer` biçimindeki satırlarda etiket otomatik kalın yapılır.
- Kalın gösterilmesini istediğiniz ifadeleri `**bu şekilde**` işaretleyin.
- SSS bölümünde soru satırı `?` ile bitmeli, cevap satırı başında boşluk + `*` ile girintili olmalı.
