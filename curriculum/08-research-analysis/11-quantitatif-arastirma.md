# 11. Quantitatif Arastirma (Nicel Arastirma)

## 11.1 Giris

Nicel arastirma, sayisal veri toplama ve istatistiksel analiz yoluyla hipotezleri test etme ve genellenebilir sonuclar cikarma yontemidir. Is dunyasinda en sik kullanilan arastirma turudur: musteri memnuniyeti anketlerinden pazar buyuklugu arastirmalarina kadar.

**Temel Ozellikler:**
- Buyuk orneklemler (n > 100)
- Yapilandirilmis veri toplama araclari
- Istatistiksel analiz
- Genellenebilir sonuclar
- Nesnel olcme

## 11.2 Anket Tasarimi (Survey Design)

### Anket Tasariminin 5 Adimi

1. **Arastirma Hedefini Belirle**: Anketten ne ogrenmek istiyorsunuz?
   - Iyi: "Musterilerimizin fiyat hassasiyetini olcmek"
   - Kotu: "Musteriler hakkinda genel bilgi toplamak"

2. **Sorulari Tasarla**: Her soru bir hedefe hizmet etmeli
   - Kapali uclu: Coktan secmeli, Likert olcegi, siklik sorusu
   - Acik uclu: "Baska ne eklemek istersiniz?" (sinirli sayida)

3. **Anket Akisini Yapilandir**:
   - Basit -> Karmasik -> Kisisel -> Demografik
   - En kolay sorular basta (anketi biraktirma)
   - En onemli sorular erken (yorulma etkisi)
   - Demografik sorular sonda (kisisel, anketi biraktirabilir)

4. **Pilot Test**: 10-20 kisiyle test et
   - Sorular anlasiliyor mu?
   - Tahmini dolum suresi ne kadar?
   - Mantikli yanitlar veriliyor mu?

5. **Dagit ve Topla**: Hedef kitleye uygun kanal
   - Email, in-app, SMS, web pop-up, yuz yuze

### Soru Tipleri

| Soru Tipi | Ornek | Ne Zaman Kullanilir? |
|---|---|---|
| **Likert (5-7 puan)** | "Urunumuzden memnunum: 1-5" | Tutum, memnuniyet olcme |
| **Semantic Differential** | "Urun: Ucuz 1-5 Pahali" | Algı olcme |
| **Siraalama** | "Asagidakileri oneme gore siralayin" | Onceliklendirme |
| **Coktan secmeli (tek)** | "En sik hangi urunu kullaniyorsunuz?" | Kategorizasyon |
| **Coktan secmeli (coklu)** | "Hangi ozellikleri kullaniyorsunuz?" | Davranis profilleme |
| **Acik uclu** | "Nasil iyilestirebiliriz?" | Kesif, nitel veri |
| **Sayisal** | "Kac yasindasiniz?" | Demografi |

### Anket Uzunlugu ve Yorgunluk

- **3-5 dakika**: Ideal anket suresi
- **5-7 dakika**: Kabul edilebilir
- **8+ dakika**: Anketi birakma orani %20+ artar
- **1-3 soru**: Minimum (NPS gibi)

### Anket Tasariminda Yaygin Hatalar

1. **Leading Questions (Yonlendiren Sorular)**
   - Kotu: "Premium urunumuzun ne kadar kaliteli buluyorsunuz?"
   - Iyi: "Premium urunumuzu nasil degerlendiriyorsunuz?"

2. **Double-Barreled (Cift Namlulu)**
   - Kotu: "Urun kalitesinden ve fiyatindan memnun musunuz?"
   - Iyi: Iki ayri soru

3. **Negative Wording (Olumsuz Ifade)**
   - Kotu: "Kullanimi zor bulmuyor musunuz?"
   - Iyi: "Kullanimi nasil buluyorsunuz?"

4. **Ambiguous Terms (Belirsiz Terimler)**
   - Kotu: "Sik kullaniyor musunuz?" (sik ne demek?)
   - Iyi: "Haftada kac kez kullaniyorsunuz? ( ) 0-2 ( ) 3-5 ( ) 6+"

5. **Leading Scale (Yonlendiren Olcek)**
   - Kotu: 1(Kotu) 2 3 4 5(Mukemmel) — sadece pozitif
   - Iyi: Dengeli olcek (cevresel secenekler esit)

## 11.3 Orneklem Secimi (Sampling)

### Orneklem Turleri

| Tur | Aciklama | Avantaj | Dezavantaj |
|---|---|---|---|
| **Basit Rastgele** | Herkesin esit sansi | En tarafsiz | Ulasmasi zor |
| **Tabakali** | Once gruplara ayir, sonra rastgele | Alt grup analizi mumkun | Grup tanimi kritik |
| **Kume** | Kume sec (sehir, sube) | Maliyet dusuk | Hassasiyet dusuk |
| **Kolayda** | Ulasilabilir kisiler | Hizli, ucuz | Genellenemez |
| **Kartopu** | Bir kisi digerini yonlendirir | Niş kitleye ulasir | Yanli |

### Orneklem Buyuklugu Hesaplama

**Formul (basit rastgele icin):**
```
n = (Z^2 * p * (1-p)) / E^2

n = orneklem buyuklugu
Z = guven seviyesi (1.96 = %95 guven)
p = beklenen oran (0.5 maksimum varyans)
E = hata payi (0.05 = %5)
```

**Ornek:** %95 guven, %5 hata payi
n = (1.96^2 * 0.5 * 0.5) / 0.05^2 = **384 kisi**

### Yanit Orani Kalibrasyonu

Anket gonderdiginiz herkes yanitlamaz. Yanit orani tahmin edilip orneklem buyutulmelidir:
- Email anketleri: %10-20 yanit orani
- In-app anketler: %30-60
- SMS: %5-15
- Yuz yuze: %60-90

**Gerekli gonderi = (Hedef orneklem) / (Yanit orani)**

Ornek: 384 hedef, %20 yanit -> 1,920 kisiye anket gonderilmeli

## 11.4 Survey Bias (Anket Yanliliklari)

| Yanlilik | Aciklama | Cozum |
|---|---|---|
| **Social Desirability** | Kisiler kendini iyi gosterme egilimi | Anonimlik, dolayli sorular |
| **Acquiescence Bias** | Evet deme egilimi | Olumlu/olumsuz sorulari karistir |
| **Non-Response Bias** | Yanit vermeyenler farklidir | Yanit oranini artir, non-respondent analizi |
| **Recall Bias** | Kisiler dogru hatirlamaz | Kisa zaman araliklari, "son 1 ay" gibi |
| **Cultural Bias** | Kultur soru algisini etkiler | Lokalize et, pilot test yap |
| **Central Tendency** | Uc noktalardan kacma | Etiketleri degistir, cift sayi kullan |
| **Order Bias** | Sira gosterimi etkiler | Randomize et, dongusel dengesle |

### Likert Olceginde Nokta Sayisinin Etkisi

| Olcek | Avantaj | Dezavantaj |
|---|---|---|
| **5 puan** | Standart, karsilastirilabilir | Merkezi egilim |
| **7 puan** | Daha fazla varyans | Anlamsal belirsizlik |
| **4 puan (cift)** | Zorunlu taraf sectirme | Hayali farklar |
| **6 puan** | Dengeli, 2 ucta 3'er secenek | Standart degil |
| **100 puan** | Cok duyarli | Anlamsiz farklar |

**Tavsiye:** Genel anketler icin 5-7 puan Likert. NPS icin 0-10 (orijinal standart).

## 11.5 NPS (Net Promoter Score)

### Tanim ve Hesaplama

NPS, en yaygin musteri sadakati olcumudur. Tek bir sorudan olusur:

> "Bizi/urunumuzu bir arkadasiniza tavsiye etme olasiliginiz nedir?"
> 0 (Hic mumkun degil) --- 10 (Kesinlikle tavsiye ederim)

**Kategorizasyon:**
- **Promoters (9-10)**: Sadik, tekrar alir, tavsiye eder
- **Passives (7-8)**: Memnun ama hevesli degil, rakibe gecme potansiyeli
- **Detractors (0-6)**: Memnun degil, sirkete zarar verebilir

**Hesaplama:** % Promoters - % Detractors = NPS (-100 ile +100 arasi)

### NPS Best Practices (2025 Guncel)

**Anket Tasarimi:**
- Standart 0-10 olcegini kullan (farkli olcekler benchmark ile karsilastirmayi imkansiz kilar)
- Trafik isigi renklendirmesi (yesil/sari/kirmizi) KULLANMA — 2025 arastirmasi yanlilik yarattigini gosteriyor
- Emoji veya hover efektleri kullanma
- Tum secenekler ayni anda gorunur olmali (kaydirma gerektirmemeli)
- Her zaman acik uclu takip sorusu ekle: "Bu puani neden verdiniz?"

**Zamanlama:**
- Transactional NPS (tNPS): Her musteri etkilesiminden sonra
- Relational NPS (rNPS): 3 ayda bir, genel iliski olcumu

**NPS'nin Sinirlari:**
- Metrik oyunlara aciktir (prompter hunt, detractor suppression)
- Kulturler arasi farkliliklar: Japonya'da 9-10 nadiren verilir, ABD'de daha yaygin
- NPS iyilesmesi her zaman gelir artisi getirmez
- B2B'de tek bir "tavsiye" sorusu yeterli olmayabilir (farkli kullanici rolleri)

### Tamamlayici Metrikler

| Metrik | Ne Olcer? | Kullanimi |
|---|---|---|
| **CSAT** | Anlik memnuniyet | Belirli bir etkilesim sonrasi |
| **CES** | Musteri eforu | "Isimi halletmek ne kadar kolaydı?" |
| **Churn Rate** | Kayip orani | Abonelik modellerinde |
| **LTV/CAC** | Karlilik | Musteri kazanma verimliligi |
| **Retention** | Kalici lik | Kullanici davranisi |

## 11.6 Anket Verisi Analizi

### Veri Temizleme
- **Straight-lining**: Tum sorulara ayni cevabi verenleri cikar
- **Speeders**: Anketi cok hizli tamamlayanlari cikar (ornek: 3 dakikalik anket > 30 saniye)
- **Incomplete**: Eksik yanitlari belirle (cikar veya impute)
- **Outliers**: Mantik disi degerleri temizle

### Istatistiksel Testler

| Soru | Test |
|---|---|
| Iki grup arasinda fark var mi? | t-test |
| Ikiden fazla grup arasinda fark var mi? | ANOVA |
| Kategorik degiskenler iliskili mi? | Chi-square |
| Degiskenler korele mi? | Pearson/Spearman |
| Anket guvenilir mi? | Cronbach's Alpha |

### Cronbach's Alpha (Guvenilirlik)
Ayni kavrami olcen birden fazla sorunun tutarliligini olcer:
- 0.9+ = Mukemmel
- 0.8-0.9 = Iyi
- 0.7-0.8 = Kabul edilebilir
- 0.7- = Zayif

## 11.7 En Iyi Kaynaklar

### Kitaplar
1. **"The Survey Kit"** - Arlene Fink (Sage, 2003) — Anket tasariminin kapsamli 10 ciltlik serisi
2. **"Survey Research Methods"** - Floyd Fowler (Sage, 2014) — Anket metodolojisinin akademik standardi
3. **"The Ultimate Question 2.0"** - Fred Reichheld & Rob Markey (Harvard Business Review Press, 2011) — NPS'nin kurucu kitabi
4. **"Testing Statistical Hypotheses"** - Lehmann & Romano (Springer, 2005) — Hipotez testinin teorik temeli
5. **"Naked Statistics"** - Charles Wheelan (W.W. Norton, 2013) — Istatistigi anlasilir hale getiren basucu kitabi

### Online Kaynaklar
- **Qualtrics Blog** (qualtrics.com): Anket tasarimi ve deneyim
- **SurveyMonkey Blog**: Anket yanliliklarini azaltma
- **NPS Benchmarks**: Sektor bazinda NPS karsilastirmalari
- **Netflix Tech Blog - Experimentation Platform**: Buyuk olcekli deney ve anket sistemleri

## 11.8 Vaka Calismalari

### Vaka 1: Apple ve Musteri Memnuniyeti
Apple, musteri memnuniyetini olcmek icin kendi anket sistemini (Apple Customer Pulse) kullanir. 2025 itibariyla, Apple Store'lar icin NPS puani 72 ile perakende sektorunde en yukseklerden biridir.

**Yontem:**
- Her Apple Store ziyaretinden sonra anket gonderilir
- Relational NPS 6 ayda bir olculur
- Acik uclu sorular NLP ile analiz edilir
- Sonuclar sube yoneticilerinin performans degerlendirmesine dogrudan baglanir

**Elestiri**: Calisanlarin NPS puanlarina gore degerlendirilmesi, "prompter hunt" davranisina yol acabilir.

### Vaka 2: Turkcell Musteri Deneyimi
Turkcell, Turkiye'de musteri memnuniyeti anketlerini en sistematik kullanan sirketlerdendir. 2025'te:
- Her musteri hizmetleri gorusmesi sonrasi tNPS
- 3 ayda bir rNPS anketi
- 600.000+ aylik anket yaniti
- NLP ile acik uclu analiz

**Yontem standardizasyonu**: Tum kanallarda (arama, online, sube) ayni sorulari kullanarak kanallar arasi karsilastirma yaparlar.

## 11.9 Pratik Alistirmalar

### Alistirma 1: Anket Tasarimi
Bir online kahve satis sirketi icin bir musteri memnuniyet anketi tasarlayin:
- 5-7 soru
- En az 3 farkli soru tipi
- Olası yanliliklari belirleyin ve duzeltmeler yazin
- Anket akisini cizin
- Bir kisiye test edin ve geri bildirim alin

### Alistirma 2: Orneklem Hesabi
Bir sirketin calisan memnuniyet anketi yapacaksiniz:
- Sirkette 1,500 kisi calisiyor
- %95 guven, %3 hata payi istiyorsunuz
- Beklenen yanit orani: %30
- Kac kisiye anket gondermelisiniz?
- Tabakali ornekleme kullanmak isterseniz (departmanlara gore) nasil yaparsiniz?

### Alistirma 3: NPS Analizi
Bir sirketin NPS sonuclari:
- 1000 yanit: 350 Promoter, 300 Passive, 350 Detractor
- NPS = ?
- Prompter'lar nasil kullanilabilir? (referral program)
- Detractor'lar icin aksiyon plani ne olmali?
- Gecen yil NPS = -10 iken bu yil bu sonuc: iyilesme var mi?

### Alistirma 4: Anket Yorgunlugu Tespiti
Bir veri setinde:
- Anket gonderilen kisi: 10,000
- Tamamlayan: 2,500 (%25)
- Ortalama tamamlama suresi: 4:32 dk
- 58 kisi 45 saniyenin altinda tamamladi
- 134 kisi tum sorulara "3" verdi (5'li Likert)
- 500 kisi ilk 2 sorudan sonra birakti

Ne yapardiniz? Hangi yanitlari temizlerdiniz? Hangi gelismeleri onerirdiniz?

## 11.10 Turkiye'de Bu

### Anket Arastirmasinin Durumu
- Turkiye'de pazar arastirmasi sektoru (IPSOS, NielsenIQ, Kantar, Areda Survey) profesyonel standartlarda calisir
- Anket araci olarak SurveyMonkey ve Google Forms en yaygin
- Yerli alternatifler: Anket.com.tr, SurveyLab
- Mobil internet penetrasyonu yuksek oldugu icin mobil anket giderek yayginiyor
- Kentsel/kirsal, Genc/yasli gibi gruplar arasindaki dijital ucurum anket katilimini etkiler

### Kulturel Duyarlilik
- "Kesinlikle katiliyorum" kullanimi Turkiye'de daha az yaygın (sosyal begeni yanliligi)
- Yasli nufus icin anket dilinin basitlestirilmesi gerekebilir
- Kadin ve genclere ulasmak icin farkli kanallar kullanmak gerekir
- 2025 enflasyon ortaminda fiyat hassasiyeti sorulari daha hassas ele alinmalidir

---

**Baglantili Moduller:** [Pazar Arastirmasi](02-pazar-arastirmasi.md), [Arastirma Metodolojisi](01-arastirma-metodolojisi.md), [Veri Analizi](04-veri-analizi.md)
