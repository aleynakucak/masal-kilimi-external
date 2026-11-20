# Masal Kilimi | Anadolu Halk Masalları

Anadolu'nun köylerinden derlenmiş halk masallarını okumak için hazırladığım tek sayfalık bir web sitesidir. Kilim motifleri sadece kodla (CSS ve SVG) çizilmiştir. Bu depo, vize projemin harici CSS ve JavaScript dosyalarıyla yeniden yapılandırılmış halidir.

## Bu Ödevde Ne Değişti?

Vize projem başta tek bir `index.html` dosyasıydı. CSS, `<style>` etiketinin içinde; JavaScript ise `<script>` etiketinin içinde yer alıyordu. Bunları harici dosyalara taşıdım:

| Önce | Sonra |
| :--- | :--- |
| `<style> ... </style>` (HTML'in içinde) | `css/style.css` dosyası, `<link rel="stylesheet" href="css/style.css">` ile bağlandı |
| `<script> ... </script>` (HTML'in içinde) | `js/script.js` dosyası, `<script src="js/script.js"></script>` ile bağlandı |

Kodun kendisinde hiçbir değişiklik yapmadım; yalnızca dosya yapısı ayrıştırıldığı için site vizedeki haliyle aynı görünmekte ve çalışmaktadır.

## Proje Yapısı

```text
masal-kilimi-external/
├── index.html      # Sayfanın iskeleti (HTML)
├── css/
│   └── style.css   # Tüm görünüm kuralları, renkler, kilim desenleri, koyu tema
├── js/
│   └── script.js   # Masal verisi ve tüm etkileşimler
└── README.md       # Proje dokümantasyonu
```

`<script>` etiketi, sayfa yüklenirken `body` içindeki öğelerin hazır olması için `</body>` kapanış etiketinden hemen önce konumlandırılmıştır.

## Özellikler

* **Masal listesi:** 8 masal, kartlar halinde görünür. Her kartta tür, yöre ve okuma süresi yazar.
* **Bugünün masalı:** Öne çıkan masal sayfanın en üstünde gösterilir.
* **Arama ve süzme:** Masal adı, yöre ya da konuya göre arama yapılır; türe ve okuma süresine göre filtrelenir.
* **Okuma ekranı:** Seçilen masal ayrı bir ekranda açılır ve üst kısımda okuma ilerleme çubuğu bulunur.
* **Okuma ayarları:** Yazı boyutu, yazı tipi (serif/sans), satır aralığı, önemli cümle vurgusu ve süslü baş harf açılıp kapatılabilir.
* **Açık ve koyu tema:** Tarayıcının temasına göre başlar, istenirse elle değiştirilir.
* **Ayarların hatırlanması:** Tema, okuma ayarları ve okuma konumu `localStorage` ile saklanır.
* **Klavye gezinmesi:** Okurken sağ ok sonraki, sol ok önceki masala geçer; `Esc` tuşu listeye döndürür.
* **Masal önerisi formu:** Sunucu olmadığı için öneri, e-posta uygulamasında hazır mesaj olarak açılır ya da panoya kopyalanır.
* **Erişilebilirlik:** Odak çerçeveleri, `aria` etiketleri ve en az 44 px dokunma alanları kullanıldı.
* **Duyarlı tasarım:** Telefondan masaüstüne kadar tüm ekran boyutlarına uyum sağlar.

## Kullanılan Teknolojiler

HTML5, CSS3 (CSS değişkenleri, Grid, Flexbox, `prefers-color-scheme`), SVG (kodla çizilmiş motifler) ve kütüphanesiz (Vanilla) JavaScript.

## Nasıl Çalıştırılır?

1. Depoyu indirin ya da klonlayın.
2. `index.html` dosyasını herhangi bir tarayıcıda açın (kurulum veya internet bağlantısı gerekmez).

> **Not:** `css/` ve `js/` klasörleri `index.html` ile aynı dizinde bulunmalıdır; aksi halde sayfa stilsiz ve işlevsiz görünür.


## Notlar

* Masal görselleri `data:` (Base64) adresleriyle koda gömülü olduğu için `index.html` ve `js/script.js` dosyaları yaklaşık 1 MB boyutundadır; bu durum sayfanın çalışmasını etkilemez.
* Masal metinleri Anadolu halk anlatılarından derlenmiştir.

## Hazırlayan

* **Ad Soyad:** Aleyna Kucak
* **Öğrenci No:** 86240037
* **Ders:** Programlamaya Giriş
