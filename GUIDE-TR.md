# Live Assistant (saat) + Gateway Assistant (telefon) — hızlı rehber

Amazfit (Zepp OS), Huawei Watch 3 / Watch 4, **Wear OS** saatinizle (Galaxy Watch, Pixel Watch, TicWatch…) ya da **HarmonyOS**'lu Huawei saatinizle (Watch 5, Watch 6, Watch Ultimate 2…) Gemini ile konuşursunuz ve Android telefonunuzdaki **Gateway Assistant** uygulaması sayesinde şunları yapabilirsiniz:
Google evinizi kontrol etmek, arama yapmak, WhatsApp mesajları göndermek/okumak/yanıtlamak ve telefonun sesini kullanmak.
Herkes kendi telefonunu, Google hesabını ve Gemini anahtarını kullanır: paylaşılacak bir şey yok.

🌐 Uygulamalar **Türkçe, İngilizce, İtalyanca, İspanyolca, Fransızca, Portekizce (Portekiz ve Brezilya) ve Bulgarca** konuşur: saatin ve telefonun dilini otomatik olarak izlerler. · *English: [GUIDE.md](GUIDE.md)* · *Italiano: [GUIDA.md](GUIDA.md)* · *Español: [GUIA.md](GUIA.md)* · *Français : [GUIDE-FR.md](GUIDE-FR.md)* · *Português: [GUIA-PT.md](GUIA-PT.md)* · *Português do Brasil: [GUIA-BR.md](GUIA-BR.md)* · *Български: [GUIDE-BG.md](GUIDE-BG.md)*

## Neye ihtiyacınız var
- **Zepp** uygulaması yüklü ve saati zaten eşlenmiş bir Android telefon
- Bir **Gemini API anahtarı** (ücretsiz veya daha hızlı yanıtlar için krediyle): https://aistudio.google.com/apikey
- Telefonda Google Home'unuza bağlı **Google** uygulaması (Asistan) (yalnızca ev komutları için)

<a id="api-keys"></a>
## API anahtarları
Anahtarlar Gateway Assistant → **🔑 API anahtarları** bölümüne **yalnızca bir kez** girilir ve tüm saatler için geçerlidir; her saatin sayfasından *Anahtarları saate gönder* ile (veya yüklerken) Live'a verirsiniz.
- **Gemini** (gerekli, ücretsiz): Google hesabınızla https://aistudio.google.com/apikey adresini açın → **Create API key** → bir proje seçin veya oluşturun → anahtarı kopyalayın (`AIza` veya `AQ.` ile başlar) ve Gateway'e yapıştırın → *Gemini anahtarını kaydet*. Ücretsiz planın günlük sınırları vardır; biraz krediyle yanıtlar daha hızlı gelir.
- **Groq** (isteğe bağlı, ücretsiz): https://console.groq.com/keys adresini açın, giriş yapın (Google ile olur) → **Create API Key** → bir ad verin → anahtarı kopyalayın (`gsk_` ile başlar, yalnızca bir kez gösterilir) ve Gateway'e yapıştırın → *Groq anahtarını kaydet*. Yazılı yanıtları yaklaşık 1 saniyede verir.
- Bir anahtarı kaldırmak için *Kaydet* düğmesine basılı tutun.

## 1 · Gateway Assistant'ı yükleyin (telefon)
1. APK'yı telefona indirin: **https://github.com/Kkaoss969/gateway-assistant-download/raw/main/GatewayAssistant.apk**
2. Açın ve Android sorarsa bu kaynaktan yüklemeye izin verin.
3. **Gateway Assistant**'ı açın ve **Gateway'i başlat**'a dokunun.
4. **İzinler** listesinde ⚪ olan her satıra, hepsi ✅ olana kadar dokunun:
   kişiler ve aramalar · diğer uygulamaların üzerinde göster · WhatsApp gönderimi (erişilebilirlik) · WhatsApp okuma (bildirimler) · pil kısıtlaması yok.
   ⚠ **Erişilebilirlik**: Android'in "Gateway Assistant (WhatsApp sending)" sayfasında **yalnızca üstteki ilk anahtarı** ("Açık") açın. İkincisini, "Gateway Assistant (WhatsApp sending) kısayolu"nu **açmayın**: yalnızca bir Android kısayoludur ve açıksa otomatik dokunmalar (WhatsApp Gönder, alarm Kapat/Ertele, Gemini'ye gönderme) çalışmaz.
   Bir ayar "kısıtlı" ise: Ayarlar → Uygulamalar → Gateway Assistant → ⋮ menü → *Kısıtlı ayarlara izin ver*.
5. **Kodu kopyala**'ya dokunun (kanal kodu).

## 2 · Live Assistant'ı saate yükleyin
1. Zepp uygulamasında geliştirici modunu açın: Profil → Ayarlar → Hakkında → Zepp logosuna birkaç kez dokunun.
2. **https://kkaoss969.github.io/gateway-assistant-download/** adresini açın, saatinizi seçin ve **QR kodunu** Zepp uygulamasıyla tarayın (Profil → tarama simgesi).
3. Zepp uygulamasında **Live Assistant** uygulamasının ayarlarını açın ve doldurun:
   - **Gemini API anahtarı**
   - **Şehrim** (hava durumu ve yerel haberler)
   - **Gateway Assistant → Kod**: 1. adımda kopyalanan kodu yapıştırın
   - **Groq API anahtarı** (isteğe bağlı, https://console.groq.com → *API Keys* adresinden ücretsiz): haberler ve yazılı sorular yaklaşık 1 saniyede yanıtlanır; sesli sorular Gemini'de kalır
   - **Sık kullandığınız adlar** (isteğe bağlı): kişiler, şehirler, takımlar… doğru adların anlaşılmasına yardımcı olur
   - **Uygulama dili**: genellikle saatin dili; saat Türkçe ise kendiliğinden Türkçe olur, aksi halde **Türkçe**'yi burada seçin

## 3 · Önerilenler
- **Saatte aramalar**: Zepp uygulaması → Profil → saat → Uygulama ayarları → Telefon → *Aramaları saatte yanıtla* (ve Bluetooth'u eşleyin).
- **Telefon kilitliyken WhatsApp**: Ayarlar → Güvenlik → Smart Lock / Extend Unlock → *Güvenilir cihazlar* → saati ekleyin.
- **Çift WhatsApp (klon)**: telefonda ikinci, klonlanmış bir WhatsApp varsa (Samsung Dual Messenger, diğer telefonlarda "Çift uygulamalar"), metin mesajları gönderilir ama **saatten sesli mesajlar gönderilmez** (WhatsApp sohbeti ses olmadan açar). Sesli mesaj göndermek için klon WhatsApp'ı kaldırın; aynı WhatsApp'ta iki hesap sorun değildir. Gateway bunu WhatsApp gönderimi düğmesinde ⚠️ ile belirtir.
- **Beeper (deneysel)**: WhatsApp ve Telegram bağlı [Beeper](https://play.google.com/store/apps/details?id=com.beeper.android) kullanıyorsanız Gateway'de *🧪 Beeper*'a dokunun ve erişime izin verin: metin mesajları WhatsApp açılmadan ve erişilebilirlik olmadan, telefon kilitliyken bile gönderilir; Telegram'da herhangi bir sohbete yazabilirsiniz. Sesli mesajlar yine WhatsApp üzerinden gider.
  Beeper olmadan telefon uyanır ve mesaj kilidi açtığınızda gönderilir.
- **Telefon kilitliyken ev komutları**: Google uygulaması → Ayarlar → Google Asistan → Kilit ekranı → kişisel sonuçlar açık.
- **Not**: Google Asistan bazı işlemleri Türkçe desteklemediği için Gateway ev komutlarını Asistana İngilizce iletir; siz saate Türkçe konuşmaya devam edersiniz.

**Telefon alarmı**: çaldığında saat titrer ve **Kapat** ve **Ertele** düğmelerini kendiliğinden açar. Saat, Live Assistant'ı her açtığınızda (ve her alarmdan sonra) sonraki alarmın saatini öğrenir: telefonda yeni bir alarm oluşturursanız uygulamayı saatte bir kez açın. ⚠ **Uyku modunda** veya **rahatsız etmeyin** modunda saat üçüncü taraf uygulamaları engeller: uyku modunu / rahatsız etmeyin'i alarmdan birkaç dakika önce bitecek şekilde planlayın (saat Ayarlar → Rahatsız etmeyin → Planlanmış).

**Gemini Live (deneme)**: Zepp uygulaması → Live Assistant → Ayarlar'da **Gemini Live kullan**'ı açın (aynı telefonda Gateway Assistant 1.65 veya üstü gerekir). Yanıt, ses sentezini beklemeden doğrudan ses olarak gelir; Live başarısız olursa normal yöntem kullanılır.

## Huawei saat (Watch 3, Watch 4)
**Huawei Watch 3 ve Watch 4** (Android tabanlı olanlar) için **Gemini Live**'lı **Live Assistant** var: siz konuşurken soru zaten Gemini'ye gider ve yanıt doğrudan ses olarak, genellikle 1-3 saniyede geri gelir. Saatin Wi-Fi'si veya LTE'siyle, ayrıca Gateway üzerinden yalnızca Bluetooth ile de çalışır. **Gateway Assistant**'tan yüklenir, bilgisayar gerekmez.
1. Saatte: Ayarlar → Hakkında → **yapı numarasına** birkaç kez dokunun. Sonra **Geliştirici seçenekleri**'nde **HDC hata ayıklama** ve **Wi-Fi üzerinden hata ayıklama**'yı açın.
2. Saat ve telefon **aynı Wi-Fi'de** (telefonun erişim noktası da olur).
3. Gateway Assistant'ta **⌚ Huawei saat: yükleme ve tanılama**'ya dokunun, *Wi-Fi üzerinden hata ayıklama* altında gösterilen IP'yi girin ve **Live Assistant'ı indir ve yükle**'ye dokunun. İlk seferde saat bağlantıya izin vermenizi ister: **Her zaman izin ver**'e dokunun.
   Gateway saate kanal kodunu ve kutu işaretliyse Gemini anahtarınızı verir; ayrıca uygulamayı pil tasarrufundan hariç tutar.
4. Gateway Assistant'ta **✅ Huawei Bluetooth: açık** görünene kadar **⚪ Huawei Bluetooth'a izin ver**'e dokunun: saat böylece telefonun Bluetooth'u üzerinden **Wi-Fi veya LTE olmadan** çalışır.
5. **Alt düğme**: aynı sayfada **Alt düğme: Live Assistant'ı aç**'a dokunun. Saatin alt düğmesine basınca Celia yerine Live Assistant dinlemeye hazır açılır (*Celia'yı geri yükle* bunu geri alır).

Saatte *Yeni sohbet* altındaki **dişli** ayarları açar (şehir, Otomatik/Bluetooth/İnternet bağlantısı, ses, güncellemeler, tanılama); **taç** sayfaları kaydırır. Sorular, ses, hava durumu ve haberler, Google ev, Kişiler ve WhatsApp, aramalar, hızlı komutlar, hatırlatıcılar, el feneri, ses düzeyi ve parlaklık, adımlar ve nabız hepsi çalışır. Sesle **ekran DPI**'ını da değiştirebilirsiniz ("dpi'yi 280 yap", "dpi'yi sıfırla"; 90 ile 400 arası, standart 320); saat ayarlarında **DPI'yı sıfırla**, Gateway'de (Huawei saat sayfası, *Ekran DPI* bölümü) **Ayarla** ve **Sıfırla (320)** var.
**Telefon alarmı**: çaldığında saat titrer ve **Durdur** ile **Ertele**'yi gösterir (gece modunda bile; gece modu bir dakika önce kapatılır, Ertele yeniden açar). Son dakika alarmlarıyla da çalışır: Sağlık uygulaması → Cihazlar → saat → Bildirimler'de **Gateway Assistant**'ı açın.
**Güncellemeler**: Gateway Assistant yüklü ve yeni sürümü gösterir; aynı sayfadan veya saatten (Ayarlar → *Denetle ve yükle*, Wi-Fi üzerinden hata ayıklama açıkken) güncelleyin.
**Groq (isteğe bağlı)**: Live genel soruları kendisi yanıtlar; komutları (ev, aramalar, WhatsApp, alarmlar, hava durumu, haberler) uygulama yürütür ve Groq anahtarıyla metin kısmı yaklaşık 1 saniyede hazır olur. Ücretsiz anahtar: https://console.groq.com → *API Keys* → *Create API Key* (`gsk_` ile başlar) ve Gateway'e yapıştırın → *🔑 API anahtarları* → *Groq anahtarını kaydet*.
**Tanılama**: Gateway'e kendiliğinden ulaşır (Huawei saat sayfası; saatten de Ayarlar → *Gateway Assistant'a gönder*). **Paylaş** ile size yardım eden kişiye metin dosyası olarak (WhatsApp, Telegram, e-posta) gönderirsiniz.
**İki sallamayla aç (deneme)**: saat ayarlarında *Deneme: iki güçlü sallama uygulamayı açar*'ı açın. Ekran açıkken art arda iki sert sallama Live Assistant'ı dinlemeye hazır açar; her zaman açık ekranda pil tasarrufu için sensör kapalıdır: ekranı yeniden açmak için bileğinizi kaldırın. Alt düğme de çalışır.
**Huawei güç tasarrufu**: saat Live Assistant'ı arka planda kapatabilir (uygulamayı yeniden açana kadar alt düğme ve sallamalar çalışmaz). Gateway'de, Huawei saat sayfasında **PowerGenie: kaldır**'a dokunun (saat izin vermezse devre dışı bırakır; **PowerGenie: geri yükle** geri alır). Wi-Fi üzerinden hata ayıklama açık kalır ve aynı ağdaysanız, saat Live Assistant'ı kapattığında Gateway onu kendiliğinden yeniden etkinleştirir.

### Kendi uygulamalarınızı saate yükleyin
Aynı Gateway sayfasında, **Kendi uygulamalarınızı saate yükleyin** bölümünde: **📲 Yüklenecek uygulamayı seçin**'e dokunun ve indirilen dosyayı seçin. Tek **APK**'lar ve bölünmüş paketler **APKS**, **XAPK** (OBB dosyaları dahil) ve **APKM** çalışır. Live Assistant'taki gibi Wi-Fi üzerinden hata ayıklama gerekir. Aşağıdaki kutuya bir **adb komutu** yazabilir (ör. yüklü uygulamaları listelemek için `pm list packages -3`) (**Saatte çalıştır** bölümü) ve **Çalıştır**'a dokunabilirsiniz: sonuç aşağıda görünür, **Sonucu kopyala** kopyalar.

## Wear OS saat (beta)
Live Assistant, **Android 9 ve üstü Wear OS saatlerde** de çalışır; yuvarlak ve dikdörtgen (Galaxy Watch, Pixel Watch, Oppo Watch, Mi Watch, TicWatch, Fossil…), Google Asistan'ın ve WhatsApp'ın artık çalışmadığı eski **Wear OS 2 ve 3** saatler dahil. Huawei'dekiyle aynı uygulamadır: Gemini Live ile sesli sorular, grafik hava durumu, Gateway üzerinden Ev, Kişiler, WhatsApp ve Telegram.
**Telefonla bağlantı**: önce resmi Wear OS kanalı (Bluetooth, Wi-Fi veya ağ, Wear OS seçer), sonra doğrudan Bluetooth. Gateway saate anahtarları ve kanal kodunu verir: saatin ağı varsa telefondan uzakta da çalışır.

**Yükleme** — Gateway Assistant'ta **⌚ Wear OS saat: yükleme ve tanılama**'ya dokunun. Önce saatte **Geliştirici seçenekleri**'ni açın: Ayarlar → Hakkında (Galaxy'de *Saat hakkında → Yazılım bilgileri*) → **Yazılım sürümü** veya **Yapı numarası**'na birkaç kez dokunun. Saat ve telefon **aynı Wi-Fi'de** (telefonun erişim noktası da olur). Sonra bağlantıyı seçin:
- **Kablosuz hata ayıklama (Wear OS 4 ve üstü)**: Geliştirici seçenekleri → **Kablosuz hata ayıklama** açık (*Bu ağda her zaman izin ver*).
  1. Saatte **Yeni cihaz eşle**'yi açın (6 haneli bir kod görünür).
  2. Gateway'de **yalnızca kodu** yazın ve **🔗 Eşle**'ye dokunun: IP, bağlantı noktası ve eşleme bağlantı noktası ağda otomatik bulunur (**🔍 Saati bul** düğmesi; alanlarına elle de yazılabilir). Eşlemeden sonra düğme yeşil olur, **Eşlendi ✓**: yinelemeye gerek yok.
  3. **⬇ Live Assistant'ı indir ve yükle**'ye dokunun. Bağlantı noktası, Kablosuz hata ayıklamayı her yeniden açtığınızda değişir: bir komut bağlanamazsa bağlantı noktası alanını boşaltın, Gateway onu yeniden bulur.
- **Wi-Fi üzerinden hata ayıklama (Wear OS 2 ve 3)**: Geliştirici seçenekleri → **ADB hata ayıklama** ve **Wi-Fi üzerinden hata ayıklama** açık. Saatin IP'sini girin (bağlantı noktası zaten **5555**) ve **⬇ Live Assistant'ı indir ve yükle**'ye dokunun; saatte hata ayıklamayı kabul edin (**Her zaman izin ver**).

Gateway uygulamayı yükler, izinleri (mikrofon, sensörler, güncellemeler) verir, pil tasarrufundan hariç tutar, anahtarları verir ve açar. Her düğme adımları bir pencerede gösterir (size yardım edene göndermek için **Kopyala**).
**Pixel Watch**'ta yüklemeden sonra simge uygulama listesinde görünmezse saati yeniden başlatın.
**Live'ı açan düğme** — saatte Live'ın ayarlarında (dişli): *Ana sayfaya uzun basma: Google asistanı yerine Live*; **Galaxy Watch Ultra**'da **orta (turuncu) düğme**: Samsung'un düğme ayarlarında **Uygulama yok**'u seçin, sonra Live'da **Düğme uygulamasını öğren**'e dokunun ve düğmeye bir kez basın. Düğme koruyucu etkin değilse Gateway'de **🔑 Live'a izinleri ver**'e dokunun.
**Telefon bildirimleri (yalnızca Huawei)**: Gateway → Huawei saat sayfası → **🔔 Saatte telefon bildirimleri**: uygulamaları seçin (değiştirmek için dokunun: kapalı → *yakında*, Bluetooth ile → *uzakta da*, internet üzerinden de, günde en fazla 40). Saatte kapatılan veya dokunulan bildirim telefondan da kaybolur. Wear OS ve Amazfit'te bildirimler zaten kendi uygulamalarından gelir.
**Saatte Telegram** (Wear OS ve Huawei): telefon Bluetooth ile bağlı değilken, LTE veya Wi-Fi üzerinden Telegram'ı (metinler, sesli mesajlar, fotoğraflar) doğrudan saatten okur ve gönderirsiniz. Bir kez, telefonun yanında ve Gateway'de *Doğrudan Telegram* açıkken bağlayın: saatte Live ayarları → **Telegram'ı bağla (telefondan)**. Gateway girişi kendiliğinden kabul eder; iki adımlı doğrulamada saat şifreyi sorar. Saat, Telegram → Cihazlar'da *Live Assistant (orologio)* olarak görünür. Bağlantı yalnızca gerektiğinde açılır ve 2 dakika sonra kapanır.
**Güncellemeler**: saatte dişli → *Denetle ve yükle*. Wear OS 4 ve üstünde uygulama kendini günceller (ilk seferde *Bilinmeyen uygulamaları yükle*'ye izin verin, sonra onaylayın); Wear OS 2 ve 3'te açık kalması gereken Wi-Fi üzerinden hata ayıklama ile olur.
**Aynı sayfada**: *Anahtarları saate gönder*; **Ekran DPI** (*Sıfırla* modelin fabrika DPI'ına döner, ör. Samsung'da 340); **Kendi uygulamalarınızı yükleyin** (APK, APKS, XAPK, APKM); **Saatte çalıştır** (adb komutları); saat **Tanılaması** (model ve Android sürümüyle).
**Düğme**: Galaxy Watch'ta Ayarlar → Gelişmiş özellikler → Tuşları özelleştir → *Çift basma* → **Live Assistant**. Galaxy Watch Ultra'nın orta düğmesi için düğme koruyucuyu hazırlıyoruz: Gateway'de **🔎 Düğmeleri incele**'ye dokunun, 15 saniye boyunca saatin düğmelerine basın ve sonucu gönderin.

## HarmonyOS saat (Watch 5, Watch 6, Watch Ultimate 2…) (beta)
APK yükleyemeyen **HarmonyOS NEXT**'li Huawei saatler (ör. Watch 5, Watch 6, Watch Ultimate 2) için **HarmonyOS için Live Assistant** var. Diğer sürümlerle aynı özelliklere sahiptir: Gemini Live ile sesli sorular, hava durumu, Ev, Kişiler, WhatsApp ve Telegram, telefon alarmları, geçmiş. Bilgisayar gerekmeden **Gateway Assistant** üzerinden yüklenir.
**Neden Huawei geliştirici hesabı gerekir**: HarmonyOS yalnızca saatinizin tanımlayıcısını (UDID) içeren bir profille imzalanmış uygulamaları yükler. Gateway anahtarı, sertifikayı ve profili DevEco Studio gibi **sizin** hesabınızla oluşturur. Bunlar yalnızca telefonunuzda kalır ve paylaşılmaz.

**1 · Huawei geliştirici hesabı (bir kez)**
1. https://developer.huawei.com adresini açın, **Huawei Kimliğinizle** giriş yapın (Sağlık uygulamasındaki olur) ve **geliştirici kaydını** tamamlayın (ücretsiz, bireysel hesap). Kimlik doğrulaması için geçerli bir belge (kimlik kartı veya pasaport) ve bir kredi kartı gerekir: onaylandı görünene kadar bekleyin.
2. Gateway Assistant'ta **⌚ HarmonyOS saat: bağlantı ve tanılama** → **🔏 HAP imza dosyaları** → **🔐 Otomatik profiller: Huawei hesabıyla giriş (DevEco gibi)** öğesine dokunun.
3. Tarayıcı açılır: geliştirici hesabıyla giriş yapın ve onaylayın. Tarayıcı kendiliğinden Gateway'e döner ve **✅ Giriş yapıldı** gösterir; düğme adınızla birlikte **🔐 Huawei hesabı:** olur (dokunarak çıkış yaparsınız).
Başka bir şey gerekmez: hata ayıklama anahtarı ve sertifikası ilk yüklemede kendiliğinden oluşturulur (ya da hemen, **🪄 Huawei hesabıyla anahtar ve sertifika oluştur** ile). Her hesapta en fazla 3 hata ayıklama sertifikası olabilir (Gateway'inki kendiliğinden değiştirilir): DevEco Studio ile yapılmış 3 sertifikanız varsa ve Gateway bunu bildirirse, AppGallery Connect'te eskilerden birini silin (*Sertifikalar, uygulama kimlikleri ve profiller → Sertifikalar*).

**2 · Saati hazırlayın**
1. Saatte: Ayarlar → Hakkında → **Geliştirici seçenekleri** görünene kadar **sürüme** birkaç kez dokunun.
2. Geliştirici seçeneklerinde **hata ayıklamayı (HDC)** ve **Wi-Fi hata ayıklamayı** açın: saat **IP ve bağlantı noktasını** gösterir (ör. 192.168.0.191:44911). Hata ayıklamayı her yeniden açtığınızda bağlantı noktası değişir.
3. Saat ve telefon **aynı Wi-Fi ağında** (telefonun erişim noktası da olur).

**3 · Live Assistant'ı yükleyin**
1. Gateway'de: **⌚ HarmonyOS saat** → **📲 Live'ı saate yükle veya güncelle**.
2. Saatin **IP**'sini ve **bağlantı noktasını** yazın ya da **🔎 Saati Wi-Fi'de bul** öğesine dokunun (IP zaten yazılıysa bağlantı noktasını birkaç saniyede bulur).
3. **⬇ Siteden** öğesine dokunun. Gateway Live Assistant'ı indirir, saati hesabınıza kaydeder, profili oluşturur, uygulamayı imzalar, yükler ve Gateway'e bağlı olarak açar (kanal kodu ve anahtarlar). Pencerede **✅ Tamam** görünene kadar her adımı görürsünüz.
4. İlk seferde saat hata ayıklama **bağlantısına izin vermenizi** ister: kabul edin.
Saatte başkası tarafından imzalanmış bir Live Assistant zaten varsa, Gateway önce onu kaldırıp kaldırmayacağını sorar (saatteki uygulama verileri kaybolur).

**Güncellemeler**: Gateway Assistant yeni bir sürüm olduğunda gösterir. Aynı şekilde güncellenir (📲 Yükle veya güncelle → ⬇ Siteden), Wi-Fi hata ayıklama açıkken; ayarlar ve veriler korunur.
**Telefonla bağlantı**: Live kendiliğinden doğrudan Wi-Fi'yi (aynı ağ), Bluetooth'u ve son olarak kanal koduyla interneti (saatin Wi-Fi'si veya LTE'si) dener. Bluetooth kullanmak için: saatte ⚙ → **🔵 Gateway ile Bluetooth testi** (Bluetooth iznini verin).
**Arka planda Live (beta)**: ⚙ → **🌙 Arka planda Live** ile saat, uygulama kapalıyken de Bluetooth ile mesaj uyarıları alır ve her 30 dakikada bir alarmları ve mesajları kontrol eder. Biraz daha fazla pil kullanır ve önce başarılı bir Bluetooth testi gerekir.
**Tanılama**: saatte ⚙ → Tanılama → 📤 Gateway; Gateway'de ⌚ HarmonyOS saat → **Tanılama** içinde bulunur.
**Kendi imza dosyalarınız var mı?** (DevEco Studio kullananlar için): **🔏 HAP imza dosyaları** içine parolasıyla **.p12** anahtarını, **.cer** hata ayıklama sertifikasını ve **.p7b** profillerini yüklersiniz (uygulama başına bir tane, saatin UDID'si ile; UDID'yi **🛠 hdc araçları** → **📋 Saat tanımlayıcısı (UDID)** içinden kopyalarsınız). **🤖 Otomatik profiller (AppGallery Connect)** düğmesi Avrupa hesaplarıyla çalışmayan resmi API'leri kullanır: bu durumda Huawei hesabıyla girişi kullanın.
**Diğer araçlar** (🛠 hdc araçları): **🔑 Gemini anahtarını ve kanalı Live'a gönder**, saatte komutlar. **HAP seç** ile başka HarmonyOS uygulamaları da yüklersiniz: Huawei hesabı bağlıysa Gateway bunları kendisi imzalar.

## iPhone ile
Gateway Assistant yalnızca Android içindir: iOS bir uygulamanın sürekli açık kalmasına, WhatsApp'ta "Gönder"e basmasına, bildirimleri okumasına veya Google Asistan'a ifade iletmesine izin vermez.
**Live Assistant iPhone ile de çalışır**: Gemini'ye sorular, ses, hava durumu, haberler, hatırlatıcılar, ses düzeyi, parlaklık ve el feneri.
Kullanılamayanlar: Google ev komutları, kişilerinizden adla arama, WhatsApp gönderme ve okuma, yedek telefon sesi.
- 1. adımı atlayın ve **Gateway Assistant → Kod**'u boş bırakın.
- **Zepp uygulamasını arka planda açık tutun** (kaydırarak kapatmayın): iOS onu askıya alırsa saat "telefona ulaşılamıyor" der.
- Saatte normal aramalar Zepp uygulamasındaki Bluetooth aramalarıyla çalışır.

## Bilek hareketleri (sallamalar)
Gürültülü ortamda veya eller doluyken kullanışlıdır. Saatteki uygulama ayarlarından (Huawei) açılıp kapatılır ve uygulama açıkken çalışır:
- **Dinlerken bir sallama**: sessizliği beklemeden soruyu hemen gönderir.
- **Düşünürken bir sallama** (renkler dönerken): soruyu iptal eder.
- **Konuşurken bir sallama**: sesi durdurur.
- **Boştayken bir sallama**: yeni soru (yeniden dinler).
- **İki sallama**: uygulamayı kapatır. İkincisini kısa bir aradan sonra ve birinciden **daha sert** yapın, böylece normal bir ikinci deneme onu yanlışlıkla kapatmaz.
- **Durdur düğmesi (Huawei ve Amazfit)**: dinlemeye başladığından yanıt gelene kadar *Yeni sohbet* yerine kırmızı bir **■ Durdur** düğmesi çıkar: soruyu göndermeden iptal eder (veya gelen yanıtı bırakır) ve o sorunun komutları yürütülmez. Dinlerken orta düğmeye dokunmak hemen gönderir. Bir WhatsApp/Telegram mesajı veya sesli mesaj gönderildiğinde titreşim ve kısa bir sesle büyük bir **yeşil ✓** görünür (gizlilik modunda ses yok); başarısız olursa **kırmızı ✗**.
Açıldıktan sonraki ilk 2 saniyede sallamalar sayılmaz. **30 saniye** hareketsizlikten sonra uygulama kendiliğinden kadrana döner.

## Neler söyleyebilirsiniz
- "Yarın hava nasıl?", "Galatasaray nasıl oynadı?", herhangi bir soru (hava durumu sorularında saat bir **grafik kart** da gösterir: şimdi, sonraki saatler ve sonraki günler)
- "Mutfak ışığını aç", "iyi geceler"
- "Mario'yu ara" (birden fazla Mario varsa saatte birine dokunursunuz)
- "Mario'ya WhatsApp gönder: on dakikaya oradayım" (onaylamak için **… kişisine gönder**'e dokunun)
- "WhatsApp mesajlarımı oku", "Anna'ya yanıt ver: olur"
- "Telegram'da Luca'ya yanıt ver: yoldayım" (yalnızca yakın zamanda bildirimi olan Telegram sohbetlerine; "mesajlarımı oku" Telegram'dakileri de gösterir)
- "Mario'ya sesli mesaj gönder": 🎤 kişisine dokunun, konuşun ve göndermek için yeniden dokunun. WhatsApp sesli notu olarak gelir; Huawei'de telefona Bluetooth gerekir (veya Kişiler sayfasında bir favoride **WhatsApp'a basılı tutun**: kayıt hemen başlar)
- "Yarının alarmını kapat", "alarmı durdur", "alarmı ertele" (**telefon** alarmları)
- "Perşembe saat 10'da dişçiyi takvimime ekle, bir saat önce hatırlat", "yarın ne var?" (**telefon** takvimi: Gateway Assistant'ta **Takvime izin ver**'e dokunun)
- "Alışveriş listeme süt ekle", "not al: ampul al", "yarın saat 9'da Luca'yı aramamı Google Görevler'de hatırlat" (**Keep** ve **Görevler**: Gateway ifadeyi telefondaki Gemini'ye yazar; Gateway Assistant erişilebilirliği ve Gemini'de Keep ve Görevler uzantıları açık olmalı)
- "Saat 7'ye kadar rahatsız etmeyin'i aç", "rahatsız etmeyin'i kapat" (**telefonun** Rahatsız etmeyin modu: Gateway Assistant'ta **Rahatsız etmeyin'e izin ver**'e dokunun; telefonda ayarlı istisnalar geçerlidir)
- "Akşam 6'da dişçiyi aramamı hatırlat", "saat 7'de alarm", "sesi aç"

**Hızlı komutlar ve favoriler**: Gateway Assistant'ta, "Saatte: hızlı komutlar ve favoriler" bölümünde Asistan için bir ifadeyle düğmeler (ör. "Shield" → "Shield'ı aç") ve rehberinizden favori kişiler ekleyin. Saatte, orta düğmenin yanında: **ev** simgesi (veya **‹** oku) düğmelerinizle (Gemini olmadan doğrudan telefonun Asistanına giderler) ve açıp kapatmak için **Rahatsız etmeyin** ile **Ev**'i açar; **mesajlar** simgesi (veya **›** oku) favorileriniz ve **WhatsApp** (mesajı söyleyin ve Gönder ile onaylayın) ile **Ara** düğmeleriyle **Kişiler**'i açar.

**Favoriler ve gruplar**: kişiler ve gruplar arasında en fazla **16 favori**. **+ WhatsApp grubu ekle** ve **+ Telegram grubu ekle** ile bir grup seçersiniz: saatte son mesaj (ve kimin yazdığı), baloncuklar ve yanıtlarla kendi kartını alır. **Uyarılar**: bir favori size yazdığında (veya favori bir grupta) saat adı ve önizlemeyi gösterir, dokunmak o uygulamanın sohbetini açar. Doğrudan WhatsApp ve Telegram ile uyarılar telefon bildirim göstermese bile gelir.

**Gizlilik modu**: orta düğmenin sağ altındaki **mikrofon** düğmesine dokunun: yeşil bir **klavye** olur: mikrofon kapalı kalır ve orta düğme klavyeyi açar; sorunuzu yazın, yanıt yalnızca metin olarak, ses olmadan gelir. Sese dönmek için yeniden dokunun. Tek bir yazılı soru için orta düğmeye **basılı da tutabilirsiniz**. Zepp OS 4 veya üstü bir saat gerekir.

## Bir şeyler ters giderse
- Zepp uygulaması → Live Assistant → **Tanılama**: her soruda ne olduğunu gösterir. Gateway Assistant'a da ulaşır (**⌚ Amazfit saat: tanılama**): oradan kopyalar veya **Dosyayı paylaş** ile dosya olarak gönderirsiniz.
- Gateway Assistant'ta **Günlük** aramaları, mesajları ve komutları gösterir.
- Gateway çalışıyor olmalı ("Gateway çalışıyor ✓") ve pil kısıtlaması olmamalı.
- Gateway'de **🐞 Sorun bildir** veya saatten sesle ("bir sorun bildir: WhatsApp düğmesi çalışmıyor"): rapor, mesaj metinleri ve numaralar gizlenmiş olarak günlük ve saatlerin tanılamasıyla geliştiriciye ulaşır. İlk seferde onay ister. Gateway tekrarlanan sorunları da kendiliğinden bildirir (her tür için günde en fazla bir kez).
- Gateway düğmesi çalışırken **yeşil**, durduğunda **kırmızıdır**.
- **Anonim kullanım sayımı**: Gateway günde bir kez yalnızca rastgele bir kimlik ve uygulama sürümlerini gönderir, kişisel veri yok. **📊 Anonim kullanım sayımı** ile kapatın.
