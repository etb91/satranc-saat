# Satranç Saati

Tarayıcıda çalışan, kurulum gerektirmeyen sade bir satranç saati. Telefonu ya da tableti iki oyuncunun arasına koyup kullanmak için tasarlandı.

## Özellikler

- **İki oyunculu ekran:** Ekran ikiye bölünür, üstteki oyuncunun alanı ters döner ve karşıdaki oyuncu kendi süresini düz okur.
- **Artış seçenekleri:**
  - **Artış yok:** Hamleden sonra süre eklenmez.
  - **Fischer:** Her hamleden sonra belirlenen saniye kadar süre eklenir.
- **Hazır süreler:** 1+0, 3+0, 3+2, 5+0, 5+3, 10+0, 15+10, 30+0
- **Özel süre:** Dakika, saniye ve artış miktarını kendin belirleyebilirsin.
- **Farklı süreler:** İki oyuncuya ayrı süre verebilirsin (handikap).
- **Az süre uyarısı:** 10 saniyenin altında süre ondalıklı gösterilir ve oyuncunun alanı yanıp söner.
- **Hamle sayacı:** Her oyuncunun kaç hamle yaptığı gösterilir.
- **Ses:** Hamle tıkı ve süre bitiş uyarısı çalar, ayarlardan kapatılabilir.
- **Ekranı açık tutma:** Oyun sırasında ekran kendiliğinden kapanmaz (destekleyen tarayıcılarda).
- **Ayarları hatırlama:** Son seçilen ayarlar tarayıcıda saklanır.
- **Siyah, beyaz ve gri** sade tasarım.

## Kullanım

1. Ortadaki **ayarlar** düğmesinden süreyi seç ve **Uygula**'ya bas.
2. Siyahları oynayan oyuncu kendi alanına dokunur, beyazın saati başlar.
3. Her oyuncu hamlesini yaptıktan sonra **kendi alanına dokunur**, böylece rakibin saati başlar.
4. Süresi biten oyuncunun alanında **"Süre doldu"** yazar.

### Düğmeler

| Düğme | İşlev |
|---|---|
| ▶ / ⏸ | Başlat, duraklat, devam et |
| ↺ | Saati sıfırla |
| ☰ | Ayarlar |

### Klavye kısayolları (bilgisayarda)

| Tuş | İşlev |
|---|---|
| `Boşluk` | Sırayı değiştir |
| `P` | Duraklat / devam et |
| `R` | Sıfırla |
| `Esc` | Ayarları kapat |

## Telefona kurma

Sayfayı telefonun tarayıcısında aç, ardından:

- **iPhone (Safari):** Paylaş → **Ana Ekrana Ekle**
- **Android (Chrome):** ⋮ menüsü → **Ana ekrana ekle**

Böylece saat ana ekranda bir uygulama gibi durur.

## Teknik bilgiler

- Tek bir `index.html` dosyasından oluşur: HTML, CSS ve JavaScript içinde. Dış kütüphane kullanmaz.
- Süre ölçümü `performance.now()` ile yapılır, bu yüzden zamanla kayma olmaz.
- Sesler Web Audio API ile üretilir, ses dosyası gerekmez.
- Ekranı açık tutmak için Screen Wake Lock API kullanılır. Bu özellik yalnızca `https` üzerinden açılan sayfalarda çalışır (GitHub Pages bu koşulu sağlar).
