# UrunAciklama

Entegra ürün formlarına elle tek tek girilen açıklamaları hızlandırmak için basit, tek dosyalık bir araç.

## Ne işe yarar?

AI'dan aldığınız ham açıklama metnini ("Neden ... Tercih Etmelisiniz?", "Seriye Ait Ürün Kodları",
"Profesyonel Kullanım Alanları", "Teknik Genel Bakış", "...com Avantajı:" gibi bölümlerle) yapıştırın;
araç bunu Entegra'nın kullandığı HTML biçimine (mavi başlık kutuları + madde işaretleri) otomatik
çevirir. Ürünleri tek tek listeye ekleyebilir, ya da bir Excel dosyasından **binlerce satırı tek
seferde toplu** dönüştürüp yine Excel olarak indirebilirsiniz.

## Kullanım

`index.html` dosyasını doğrudan tarayıcıda açın (çift tıklamak yeterli, kurulum gerekmez).

### Tek ürün

1. Ürün kodunu ve AI'dan aldığınız ham metni yapıştırın.
2. Sağdaki önizlemeden kontrol edin.
3. Tek ürün için "Kaynak Kodunu Kopyala" ile Entegra'nın Kaynak Kodu alanına direkt yapıştırın,
   ya da "Listeye Ekle" ile ürünü listeye ekleyip toplu işleme devam edin.
4. Bittiğinde "Excel Olarak İndir" ile tüm listeyi `.xlsx` olarak indirin.

### Toplu (Excel'den)

"Excel'den Toplu İçe Aktar" ile bir `.xlsx` dosyası yükleyin. Dosyadaki **her sayfa** taranır;
başlık satırında "STOK KODU"/"ÜRÜN KODU" ile başlayan bir sütun VE "AÇIKLAMA" ile başlayan bir
sütun bulunan sayfalardaki tüm satırlar otomatik dönüştürülüp listeye eklenir (diğer sayfalar
olduğu gibi atlanır). Sonrasında "Excel Olarak İndir" ile tamamını tek dosya halinde alabilirsiniz.

## Bilinen eksik

Excel çıktısındaki sütunlar şu an genel (`Ürün Kodu`, `Açıklama (HTML)`). Entegra'nın gerçek toplu
içe aktarma şablonu (sütun adları/sırası) netleşince buna göre uyarlanacak.

## Format kuralları (ham metin girerken)

- Her bölüm başlığı ("Neden ... Tercih Etmelisiniz?", "Seriye Ait Ürün Kodları",
  "Profesyonel Kullanım Alanları", "Teknik Genel Bakış", "...com Avantajı:"; eski format için de
  "Kullanıcı Avantajları", "Teknik Özellikler", "Paket İçeriği", "... Nerelerde Kullanılır?",
  "Sıkça Sorulan Sorular (SSS)") kendi satırında olmalı.
- Madde satırları `*`/`-` ile başlayabilir; başlamıyorsa her madde bir **boş satırla** ayrılmalı
  (gerçek AI çıktısında genelde böyledir, madde işareti şart değil).
- `Etiket: Açıklama` biçimindeki maddelerde etiket otomatik kalın yapılır.
- Kalın gösterilmesini istediğiniz ifadeleri `**bu şekilde**` işaretleyin.
- SSS bölümünde soru satırı `?` ile bitmeli, cevap satırı başında boşluk + `*` ile girintili olmalı.
- Tam olarak yukarıdaki başlıklardan biri olmasa bile, kısa ve tek satırlık (cümle sonu noktası
  olmayan, `Etiket: değer` biçiminde olmayan) satırlar otomatik olarak yeni bir bölüm başlığı
  sayılır — böylece AI'ın ürettiği farklı ifadeli başlıklar da (ör. "Teknik Genel Bakış ve
  Uyumluluk") doğru tanınır.
