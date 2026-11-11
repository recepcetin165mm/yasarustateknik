# Yaşar Usta Teknik | PHP Site ve Yönetim Paneli

## Teknik kurulum
- PHP 8.1 veya üstü, GD + WebP uzantısı, Apache + mod_rewrite gereklidir. GitHub Pages/Cloudflare Pages PHP çalıştırmaz.
- ZIP içeriğini PHP hostingin web kök klasörüne yükleyin. `admin/` ve `data/` klasörleri sunucu tarafından yazılabilir olmalıdır.
- `/admin/` adresinden ilk kurulum kodunu (sunucudaki `admin/kurulum-kodu.php` içinde) girin ve yeni şifre belirleyin.
- Panelde firma/iletişim, saatler ve hizmet bölgeleri bilgilerini onaylayıp **Kaydet ve siteyi güncelle** deyin.
- Fotoğraflar iki servis alanına bağlıdır; panelden değiştirilebilir.

## Yayın öncesi kritik doğrulamalar
1. Yeni işletmenin gerçek telefon numarasını admin panelinden girin.
2. `yeni iletişim e-postası` e-posta adresi doğrulanmamış örnek adrestir; panelden gerçek e-postaya değiştirin.
3. İşletmenin hukuki unvanı, adresi, çalışma saatleri, sunduğu hizmetler ve verdiği taahhütleri doğrulayın. Adreste müşteri kabulü yoksa açıkça belirtin.
4. KVKK / gizlilik / çerez metinleri taslaktır. Gerçek veri akışlarına göre güncellenmeli ve hukuki gözden geçirme yapılmalıdır.
5. `robots.txt`, `sitemap.xml`, canonical ve JSON-LD metinleri panelle yeniden üretilir. Canlı yayında son URL'leri test edin.
6. Google Ads için **Sistemleri Atlatma** veya **Güvenliği İhlal Edilen Site** sorunları yalnızca tasarım değişikliğiyle çözülmez. Site güvenliği, yönlendirmeler, DNS, işletme şeffaflığı ve hesap geçmişi ayrıca incelenmelidir.

## Yapı
- `templates/`: İçerik şablonları (PHP panelindeki kaydetme işlemi bunlardan HTML çıktısı oluşturur).
- `admin/`: Şifreli yönetim paneli.
- `data/`: Sitenin JSON ayarları ve panel kimlik doğrulaması (web erişiminden engellenir).
- `css/`, `js/`, `img/`: Tasarım, işlevler, siteye eklenmiş iki fotoğraf.
- `index.html`: PHP paneli tarafından oluşturulmuş, hızlı açılan statik ana sayfa.

**Not:** Bu sistem, PHP ile yönetilen ve HTML çıktısı üreten bir sitedir. Sitenin görüntülenmesi hızlıdır; güncellemeler PHP panelinden yapılır.
