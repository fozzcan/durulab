# DURU LAB

Duru Özcan'ın 3D baskı koleksiyonu için tek sayfalık mağaza sitesi.
Sunucu gerektirmez — sadece HTML, CSS ve JavaScript. GitHub Pages'te ücretsiz yayınlanır.

## Klasörde ne var

| Dosya | Ne işe yarar |
|---|---|
| `index.html` | Sitenin tamamı: tasarım, ürün listesi, sepet, sipariş formu |
| `img/` | 31 ürün ve atölye görseli (WebP) |
| `favicon.svg` | Tarayıcı sekmesindeki simge |
| `.nojekyll` | GitHub Pages'in dosyaları olduğu gibi yayınlaması için |

## GitHub Pages'te yayınlama (terminal gerekmez)

1. [github.com/new](https://github.com/new) adresinden yeni bir depo aç.
   - **Repository name:** `durulab`
   - **Public** seçili olsun, *Add a README* işaretli **olmasın**.
   - **Create repository**
2. Açılan sayfada **uploading an existing file** bağlantısına tıkla.
3. Bu klasörün **içindekileri** (klasörün kendisini değil) sürükleyip bırak:
   `index.html`, `favicon.svg`, `.nojekyll` ve `img` klasörü.
4. Altta **Commit changes** düğmesine bas.
5. Depoda **Settings → Pages** bölümüne gir.
   - **Source:** `Deploy from a branch`
   - **Branch:** `main` · **Folder:** `/ (root)` → **Save**
6. Bir iki dakika sonra sayfa yenilendiğinde adres görünür:
   `https://KULLANICI-ADIN.github.io/durulab/`

Bu adres herkese açıktır; link verdiğin herkes açabilir.

> `.nojekyll` gizli bir dosyadır; sürükle-bırak sırasında görünmüyorsa Finder'da `Cmd+Shift+.`,
> Windows Gezgini'nde *Görünüm → Gizli öğeler* ile görünür yap. Yüklenmezse de site çalışır.

## Güncellemek

Dosyayı GitHub'da açıp kalem simgesine basarak düzenleyebilir, **Commit changes** dedikten
sonra siteyi bir dakika içinde güncellenmiş görürsün.

### Fiyat veya ürün değiştirme

`index.html` içinde `const PRODUCTS = [` satırını bul. Her ürün şu kalıpta:

```js
{ id:'stadium', name:'Galatasaray Stadyum', price:3000, cat:'Maket',
  tag:'Işıklı tribünleriyle stadyum maketi',
  long:'Uzun açıklama…',
  specs:[['Malzeme','PLA filament'],['Parça','Çok parçalı montaj']],
  imgs:['img/stadium.webp','img/stadium-d.webp'] },
```

- `price` sadece sayı olmalı — `3000` gibi, nokta veya `TL` yazma. Sayfada `3.000 ₺` olarak görünür.
- `cat` şunlardan biri: `Maket`, `Teknoloji`, `Mutfak`, `Dekor`, `Oyuncak`.
- Ürünü kaldırmak için süslü parantezle biten bloğun tamamını sil.

### Görsel değiştirme

Yeni fotoğrafı `img/` klasörüne yükle ve ürünün `imgs` satırındaki dosya adını değiştir.
İlk görsel kapak olarak kullanılır; kare (1:1) olması en iyi sonucu verir.

### İletişim adresi

Sayfanın altındaki `merhaba@durulab.com` bir yer tutucudur. `index.html` içinde iki yerde geçer;
ikisini de kendi adresinle değiştir.

## Siparişler nereye gidiyor?

Şu an hiçbir yere. Sipariş formu müşteriye bir sipariş numarası veriyor ve
"sipariş özetini kopyala" düğmesiyle özeti panoya alıyor — müşteri bunu sana
WhatsApp veya e-posta ile gönderiyor.

Siparişlerin doğrudan e-postana düşmesini istersen [Formspree](https://formspree.io) gibi
ücretsiz bir servis formu birkaç satırla bağlar; istediğinde eklerim.

---

Tasarımlar ve fotoğraflar Duru Özcan'a aittir.
