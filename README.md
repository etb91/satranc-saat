# Satranç Saati

Tarayıcıda çalışan, kurulum gerektirmeyen sade bir satranç saati. Telefonu ya da tableti iki oyuncunun arasına koyup kullanmak için tasarlandı.

## Özellikler

- **Kurulum ekranı:** Site her açıldığında önce süre ve renkler seçilir. Son seçimler hatırlanır.
- **İki oyunculu ekran:** Ekran ikiye bölünür, üstteki oyuncunun alanı ters döner ve karşıdaki oyuncu kendi süresini düz okur.
- **Sırası gelenin alanı büyür:** Sıra kimdeyse onun alanı genişler, rakibinki küçülüp söner.
- **Bekleme ve duraklatma görünümü:** Saat başlamadan önce ve oyun duraklatıldığında iki oyuncunun alanı da küçük ve soluk görünür.
- **Gerçek saat gibi başlangıç:** İlk hamleyi yapacak oyuncunun saatini rakibi başlatır (satrançta siyah, beyazın saatini başlatır).
- **Renk seçenekleri:**
  - **Siyah / Beyaz:** Klasik görünüm. Sadece hangi oyuncunun beyaz olduğu seçilir, ilk hamleyi her zaman beyaz yapar.
  - **Renkli:** Her oyuncu 12 renkten birini seçer, ardından kimin başlayacağı seçilir. Rakibin seçtiği renk seçilemez.
- **Artış seçenekleri:**
  - **Artış yok:** Hamleden sonra süre eklenmez.
  - **Fischer:** Her hamleden sonra belirlenen saniye kadar süre eklenir.
- **Hazır süreler:** 1+0, 3+0, 3+2, 5+0, 5+3, 10+0, 15+10, 30+0
- **Özel süre:** Dakika, saniye ve artış miktarını kendin belirleyebilirsin.
- **Farklı süreler:** İki oyuncuya ayrı süre verebilirsin (handikap).
- **Az süre uyarısı:** 10 saniyenin altında süre ondalıklı gösterilir ve oyuncunun alanı yanıp söner.
- **Hamle sayacı:** Her oyuncunun kaç hamle yaptığı gösterilir.
- **Ses:** Her hamlede tok bir vuruş sesi, süre bitince alçak bir uyarı çalar. Kurulum ekranından kapatılabilir.
- **Ekranı açık tutma:** Oyun sırasında ekran kendiliğinden kapanmaz (destekleyen tarayıcılarda).

## Kullanım

1. Siteyi açınca kurulum ekranı gelir:
   1. **Süre:** Hazır sürelerden birini seç ya da kendin gir.
   2. **Renk:**
      - "Siyah / Beyaz" seçersen, beyazla üstteki mi alttaki mi oyuncunun oynayacağını seç.
      - "Renkli" seçersen, her oyuncu kendi rengini seçer, sonra kimin başlayacağını seç.
2. **Tamam**'a bas. İki oyuncunun alanı da küçük ve soluk görünür, saat beklemededir.
3. **Siyah** (renkli modda başlamayan oyuncu) kendi alanına dokunur, beyazın saati başlar.
4. Her oyuncu hamlesini yaptıktan sonra **kendi alanına dokunur**, böylece rakibin saati başlar.
5. Ortadaki ⏸ düğmesiyle oyunu duraklatabilirsin. Duraklatınca iki taraf da soluklaşır, ▶ ile devam edilir.
6. Süresi biten oyuncunun alanında **"Süre doldu"** yazar.

### Düğmeler

| Düğme | İşlev |
|---|---|
| ▶ / ⏸ | Başlat, duraklat, devam et |
| ↺ | Aynı ayarlarla yeniden başlat |
| ☰ | Yeni oyun (kurulum ekranı) |

### Klavye kısayolları (bilgisayarda)

| Tuş | İşlev |
|---|---|
| `Boşluk` | Sırayı değiştir |
| `P` | Duraklat / devam et |
| `R` | Sıfırla |
| `Esc` | Kurulum ekranını kapat (oyun sırasında açıldıysa) |

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
