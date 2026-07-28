# 05 — Veri Gorsellestirme (Data Visualization)

---

## 1. Giris

Veri gorsellestirme, sayisal bilgiyi grafiksel temsiller araciligiyla anlamli, sezgisel ve eyleme gecirilebilir ice donusturme sanati ve bilimidir. 2025 yilina geldigimizde, her gun 328 milyar terabayt veri uretilirken, bir insanin bu veri yiginini ham haliyle anlamlandirmasi imkansiz hale gelmistir. Bu noktada gorsellestirme, bilgiyi kesfetmek (exploratory analysis), iletmek (explanatory analysis) ve karar almayi hizlandirmak (operational dashboards) icin vazgecilmez bir aractir.

**2025 ve Otesinde Neden Daha da Onemli?**

- **AI tarafindan uretilen icerik cagi:** Yapay zeka modelleri metin, grafik ve hatta video uretebiliyor. Ancak AI'nin urettigi gorsellestirmeler genelde yaniltici olabilir, cunku orneklem secimi (sampling bias), olcek manipulasyonu ve baglamsiz gosterim yaygindir. Bu nedenle insan gozunun gorsel elestirel dusunme (visual literacy) becerisi her zamankinden degerli.
- **Self-service analytics:** Tableau, Power BI, Looker Studio gibi araclar sayesinde teknik olmayan kullanicilar bile kendi grafiklerini olusturabiliyor. Ancak bu "gorsellestirme demokratiklesmesi" beraberinde kalite sorunlarini getiriyor — yanlis grafik turu, carpik eksenler, gereksiz suslemeler.
- **Mobile-first is dunyasi:** Yoneticiler kararlarinin %80'ini mobil cihazlardan aldigi dashboard'lar uzerinden veriyor. Mobilde calisan bir gorsellestirme tasarimi, masaustunden farkli kurallar gerektiriyor.
- **Data storytelling kulturel bir gereklilik:** Sirket icinde "veriyle konusmak" bir iletisim bicimi haline geldi. Kimin veriyi daha iyi gorsellestirip anlatabildigi, kimin karar surecinde daha etkili oldugunu belirliyor.

---

## 2. Edward Tufte Prensipleri

Edward Tufte, Yale Universitesi'nden istatistik profesorudur ve "The Visual Display of Quantitative Information" (1983) kitabiyla veri gorsellestirmenin temellerini atmis, bugun hala gecerli olan prensipleri sistematize etmistir.

### 2.1 Data-Ink Ratio (Murekkep-VeriOrani)

Data-Ink, grafigin veriyi temsil eden her bir noktasidir. Non-data-ink ise eksen cizgileri, arkaplan renkleri, gereksiz etiketler gibi veriyi dogrudan iletmeyen ogelerdir.

**Formul:**

```
Data-Ink Ratio = Data-Ink / Total-Ink
```

**Hedef:** 1.0'a yaklasmak. Grafiginizdeki her bir murekkep damlasi (piksel) bir veriyi iletmelidir.

**Modern dijital yorum:** Dijitalde "murekkep" yerine "piksel" veya "ekran alani" olarak dusunulur. Bir web dashboard'unda her bir pixel karar aliciya bir bilgi vermelidir. Bos arkaplan renkleri, 3D efektler, gradient dolgular cogu zaman data-ink oranini dusurur.

**Uygulama ornegi:** Bir bar chart'ta:
- **Kotu:** 3D efektli, gradient mavi dolgulu, grid cizgili, kalin eksen cizgili, gereksiz data label'li bir grafik (data-ink ratio ~0.3)
- **Iyi:** Minimal gri grid, sade bir renk, sadece gerekli eksen etiketleri, veri dogrudan bar boyundan okunabilir (data-ink ratio ~0.8)

### 2.2 Lie Factor (Yalan Faktoru)

Lie Factor, bir grafikte gosterilen etkinin, gercek verideki etkiye oranidir. Tufte bunu "grafikte yalan soyleme olcumu" olarak tanimlar.

**Formul:**

```
Lie Factor = (Grafikte algilanan etki boyutu) / (Verideki gercek etki boyutu)
```

- **Lie Factor = 1.0:** Grafik dogruyu soyluyor (dogrusal, tarafsiz)
- **Lie Factor > 1.0:** Grafik abartiyor
- **Lie Factor < 1.0:** Grafik kucumsuyor

**Gercek hayattan ihlal ornegi:** Bir ekonomi haber sitesinde, petrol fiyatlarindaki %5'lik artis, 3 kat buyuklukte bir daireyle gosterilmistir. Dairenin alani %15'lik bir artisi (3^2) temsil ettigi icin Lie Factor = 3'tur. Yani okuyucu gercekte %5'lik bir artisi uc kati buyuklukte algilar.

**Cozum:** Her zaman olcekleri 1:1 orantili kullanin. Gorsel boyut degisimi, verideki degisimle birebir eslesmelidir. Bar chart kullaniyorsaniz Y-eksenini sifirdan baslatin.

### 2.3 Chartjunk ve Eliminasyonu

Chartjunk, veri iletimine katkisi olmayan her turlu gorsel suslemedir:

- **Grid haritasi (chartjunk cross-hatching):** Gereksiz desen ve taramalar
- **3D perspektif:** Duz bir bar chart'in 3D gosterimi derinlik algisini bozar
- **Gereksiz ikonlar:** Her bir bar'in ustunde minik ikonlar kullanmak
- **Moire efektleri:** Cakisan desenlerin gozde yanilma yaratmasi
- **Gradient ve golgeler:** Estetik ama bilgi tasimayan ogeler
- **Duck:** Tufte'nin "grafik olmayan bir nesneye donusmus grafik" olarak tanimladigi sey (ornegin, bir gazete grafiginin araba sekline sokulmasi)

**Cozum stratejisi:** "Graphical Excellence" konseptiyle, her bir gorsel ogeyi "Bu ogeyi cikarsam veri kaybi olur mu?" testine tabi tutun. Cevap "hayir" ise o ogeyi silin.

### 2.4 Small Multiples (Kucuk Katlilar)

Ayni grafik yapisinin (same chart type, same scale, same axes) farkli bir kategorik degisken boyunca tekrarlandigi gorsellestirme turudur. Bu yaklasim, karsilastirmali analiz icin son derece gucludur.

**Temel prensip:** Goz, ayni yapidaki grafikleri yan yana gordugunde, aralarindaki tek fark olan veri degisimini hizla algilar. Bu, Gestalt'in "farki algilama" prensibine dayanir.

**Ornek:** Her bir ulke icin ayri bir GDP line chart. 30 ulke, ayni X ve Y eksenleriyle yan yana kucuk karelerde. Goz, bir ulkedeki ani cokusu (2008 krizi, COVID) hemen fark eder. Buyuk tek bir grafikte bu kaybolur.

**Uygulama alanlari:**
- Zaman serilerinde karsilastirma
- Bolgesel analiz (Turkiye icin 81 il, ayni olcekte)
- Kategori bazinda trend karsilastirmalari

### 2.5 Micro/Macro Readings (Mikro/Makro Okumalar)

Iyi bir gorsellestirme, ayni anda hem genel resmi (macro) hem de detaylari (mikro) okuyucuya sunabilmelidir. Kullanici once agac gorur, sonra yapraklara odaklanir.

**Ornek:** New York Times'in yayinladigi "How Trump and Biden's Social Media Feeds Compare" gorsellestirmesi — uzaktan bakildiginda iki renkli bir yapi gorulur (hangi kullanicinin daha fazla paylasim yaptigi), yaklasildiginda her bir paylasimin metni, tarihi, platformu okunur.

**Pratik uygulama:** Bir satis dashboard'u:
- **Macro:** Yillik toplam gelir trendi (cizgi grafigi)
- **Mikro:** Belirli bir haftaya tiklayinca o haftanin gunluk detaylari
- **Mikro-mikro:** Bir gune tiklayinca o gunun kategori bazinda dokumu

### 2.6 Smallest Effective Difference

Bir veri gorsellestirmesinde iki elementi ayirt etmek icin gereken minimum farki kullanin. Gozun ayirt edebileceginden cok daha fazla renk, boyut veya sekil farki kullanmayin.

**Ornek:** Bir scatter plot'ta iki kategoriyi ayirmak icin:
- **Asiri:** Kirmizi-mavi-siyah-beyaz 4 farkli nokta tipi ve 3 farkli boyut
- **Minimum etkin fark:** Iki zitton rengi (mavi ve kirmizi) ve sekil degisikligi (daire ve ucgen) yeterlidir

**Prensip:** "Less is more." Goz, farki minimum duzeyde algilayabiliyorsa, ek fark eklemek sadece gurultudur.

### 2.7 Word-Data Integration (Sozcuk-Veri Butunlesmesi)

Veriyi metinle butunlestirmek, ayri bir grafik ve ayri bir metin blogu olusturmaktan daha etkilidir. Tufte buna "escaping flatland" — verinin duzlemden kurtulup hikayeye karismasi der.

**Sparklines:** Tufte'nin bulusu olan sparkline, boyut olarak bir metin satiri kadar (genelde 20x100 piksel) olan, eksensiz, basit bir cizgi grafigidir.

```
Ornek: Ay sonu nakit akisi:  ────╱╲──╱╲──╱╲───╱╲──  +%2.3
```

**Inline bar chart:** Tablo icinde, bir hucrenin icinde kucuk bir bar gosterimi. Ornegin, Excel'deki "data bars" ozelligi.

**Uygulama:** Tum finansal yatirim raporlari, Bloomberg terminal ekranlari, kar-zarar tablolari sparkline kullanir. Bir yonetici ayri bir grafik acmak zorunda kalmadan, tablodaki bir satirda trendi gorur.

---

## 3. Grafik Turleri ve Ne Zaman Kullanilacagi

Dogru grafik turunu secmek, veri gorsellestirmenin en kritik adimlarindan biridir. Yanlis grafik turu, dogru veriyi bile yanlis anlatir.

### 3.1 Dogru Kullanimlar

| Grafik Turu | Kullanim Amaci | Ornek |
|---|---|---|
| **Bar Chart** | Kategorik karsilastirmalar (yatay veya dusey) | 2024'te en cok satan 5 urun kategorisi |
| **Line Chart** | Zaman icindeki trendler ve sureklilik | Aylik enflasyon orani, 2019-2024 |
| **Scatter Plot** | Iki surekli degisken arasindaki iliski (korelasyon) | Reklam harcamasi vs satis geliri |
| **Heatmap** | Iki kategorik degiskenin kesistigi noktadaki yogunluk | Website ziyaret saati vs gun (hangi saatlerde trafik yogun) |
| **Histogram** | Bir surekli degiskenin dagilimi | Musteri yas dagilimi, 20-30-40-50+ yas bantlari |
| **Box Plot** | Dagilimin dortte birliklerle gosterimi | Departman bazinda maas dagilimi (medyan, Q1, Q3, aykiri degerler) |
| **Area Chart** | Zaman icinde birikimli hacim gostermek | Toplam musteri sayisi birikimi |
| **Violin Plot** | Box plot'un yogunluk versiyonu | Gelir dagiliminin sekli (cok modlu dagilimlari gosterir) |
| **Bump Chart** | Kategorilerin zaman icinde siralama degisimi | Marka siralamasinin yil icinde degisimi |
| **Waterfall** | Bir baslangic degerinden bitis degerine adim adim gecis | Gelir tablosu (gelir - maliyet - brut kar - vergi - net kar) |
| **Sankey Diagram** | Akis ve gecis miktarlari | Web sitesi sayfa gecis akisi, enerji kaynak akisi |
| **Treemap** | Hiyerarsik verilerin alan bazli gosterimi | Isletim sistemi disk kullanim analizi |

### 3.2 Kacinilmasi Gereken Grafik Turleri

| Grafik Turu | Sorun | Alternatif |
|---|---|---|
| **Pie Chart (Pasta Grafigi)** | Insan beyni acilari dogru karsilastiramaz; 3'ten fazla kategori kullanilamaz; Lie Factor yuksek | Bar chart (tercihen sorted bar) |
| **3D Chart** | Perspektif carpikligi, derinlik algisi veriyi bozar, data-ink ratio dusuk | Duz 2D versiyonu |
| **Radar Chart** | Eksenler arasi karsilastirma imkansiza yakin, kalabalik goruntu | Parallel coordinates veya bar chart tablosu |
| **Donut Chart** | Pie ile ayni sorunlar, ustelik ortadaki bosluk faydasiz | Ayni sekilde bar chart |
| **Bi-polar Chart** | Iki farkli renkli eksen, kafa karistirici | Iki ayri bar chart |

**Pie chart icin Tufte'nin meshur sozu:** "A pie chart is the worst way to communicate information, except when the question is 'What percentage of the audience likes pie charts?'"

**Ozel durum:** Pie chart, bir butunun sadece iki parcasi oldugu durumda kullanilabilir (%60 vs %40). Ancak yine de bar chart daha dogru algilanir.

### 3.3 Per Customer

**Waterfall Grafik:** Finansal analizde cok degerlidir. Ornegin:

| Adim | TL | Birikimli |
|---|---|---|
| Brut Gelir | +100.000 | 100.000 |
| Iade ve Indirimler | -5.000 | 95.000 |
| Net Satis | +0 | 95.000 |
| Satis Maliyeti | -40.000 | 55.000 |
| Brut Kar | 0 | 55.000 |
| Isletme Giderleri | -30.000 | 25.000 |
| Vergi | -5.000 | 20.000 |
| **Net Kar** | | **20.000** |

Her satir bir bar olarak, onceki barin bitiminden baslayarak gosterilir. Bu, kar-zarar akisini tek bakista anlamayi saglar.

**Sankey Diagram:** Turkiye'de pek yaygin olmasa da, dijital pazarlama akislarinda (hangi channel'dan gelen kullanici hangi sayfaya gidiyor) ve enerji sektorunde (hangi kaynak hangi tuketime gidiyor) kullanilir.

---

## 4. Dashboard Tasarimi

Dashboard, bir isletmenin saglik durumunu tek bir ekranda ozetleyen gorsel bir yonetim panelidir. Stephen Few'a gore: "A dashboard is a visual display of the most important information needed to achieve one or more objectives."

### 4.1 KPI Hiyerarsisi: Leading vs Lagging Indicators

**Lagging Indicators (Gecikmeli Gosterge):** Gecmisi olcer, sonuclari gosterir. Degistirmek icin artik gec kalmis olabilirsiniz.
- Ornek: Aylik gelir, musteri memnuniyet skoru, calisma kazasi sayisi
- Dashboard'da: En ustte, en belirgin yerde

**Leading Indicators (Oncu Gosterge):** Gelecegi tahmin ettiren, erken uyari veren metrikler.
- Ornek: Haftalik yeni musteri adayi sayisi, calisma izni basvuru sayisi, stok devir hizi
- Dashboard'da: Lagging'in yaninda veya altinda, karsilastirmali

**KPI Pramid organizasyonu (yukaridan asagiya):**

```
Seviye 1 (Executive): 3-5 en kritik metrik — gelir, kar, musteri memnuniyeti
Seviye 2 (Managerial): 8-12 metrik — departman performansi
Seviye 3 (Operational): 20+ metrik — gunluk is akisi, detay tablolari
```

### 4.2 Gestalt Ilkeleri Dashboard Layout'unda

Gestalt psikolojisi, insan beyninin gorsel ogeleri nasil grupladigini aciklar. Dashboard tasariminda bu ilkeler kritiktir:

| Ilke | Aciklama | Dashboard Uygulamasi |
|---|---|---|
| **Proximity (Yakinlik)** | Birbirine yakin ogeler iliskili algilanir | Ayni konudaki KPI'lari yan yana koyun, iliskisiz KPI'lari ayirin |
| **Similarity (Benzerlik)** | Benzer renk/sekil ayni tur veri olarak algilanir | Tum gelir metrikleri yesil, maliyetler kirmizi |
| **Closure (Butunleme)** | Eksik goruntuyu beyin tamamlar | Kartlar arasinda bosluk birakmak gerekmez; beyin her karti ayri bir obje olarak algilar |
| **Figure-Ground** | Bir ogenin on planda mi arka planda mi algilandigi | KPI kartlari icin kucuk bir golge (drop shadow) on plana cikmayi saglar |
| **Common Fate (Ortak Yazgi)** | Ayni yonde hareket eden ogeler iliskili algilanir | Scroll bar ile asagi inen tum ogelerin ayni dashboard'a ait oldugu anlasilir |

### 4.3 Information Density: Ne Kadar Cok?

Stephen Few ve Tufte'nin ortak gorusu: dashboard'lar bilgi yogun olmalidir. Ancak bunu karisikliktan (clutter) ayirmak gerekir.

**Denge tablosu:**

| Dusuk Yogunluk | Ideal Yogunluk | Yuksek Yogunluk (Clutter) |
|---|---|---|
| 1 grafik, devasa bosluk | 4-6 KPI, 2-3 grafik, dengeli bosluk | 10+ grafik, uyusuk renkler, cakisan eksenler |
| Kullanici "daha fazla veri lazim" der | Kullanici 5 saniyede durumu anlar | Kullanici "ne nerede" diye kaybolur |
| Scroll gerektirmez | Single-screen (FHD veya 4K) | Cok fazla scroll gerektirir |

**Kural:** Bir dashboard'da maksimum 5-7 ana metrik, 2-3 ana grafik. Detaylar drill-down ile erisilebilir olmali, ayni ekranda gosterilmemeli.

### 4.4 Mobile-First Dashboard Tasarimi

2025'te kararlarin %80'i mobil cihazlardan aliniyor. Bu nedenle dashboard tasarimina mobile-first yaklasmak zorunludur.

**Mobile-first kurallar:**
- **Tek iletisim hedefi:** Her mobil ekran sadece bir soruyu cevaplamali (ornegin: "Bugunku satis hedefini yakaladik mi?")
- **Dokunmatik dostu hedefler:** En kucuk dokunulabilir oge 44x44 piksel (Apple HIG standardi)
- **Yatay scroll'dan kacin:** Veriyi dikey olarak duzenle
- **Kucuk KPI'lar:** KPI kartlari 2x2 grid'de, her biri tek sayi + etiket + mini sparkline
- **Gesture-based navigation:** Kaydirma (swipe), dokunma (tap), basinli tutma (long press) ile drill-down
- **Responsive degil, adaptive:** Ayni dashboard masaustu ve mobilde farkli bir layout'a sahip olmali

**Responsive vs Adaptive:** Responsive tasarim elementleri daraltir/kucultur; adaptive tasarim ise mobil icin tamamen farkli bir bilgi hiyerarsisi sunar. Dashboard icin adaptive daha dogrudur.

### 4.5 Drill-Down vs Drill-Through

| | Drill-Down | Drill-Through |
|---|---|---|
| **Ne yapar?** | Ayni ekranda daha detayli seviyeye gecer | Farkli bir dashboard'a/rapora gecis yapar |
| **Ornek** | "2024 Yillik Satis" -> "2024-Q4 Satis" -> "Aralik 2024 Gunluk" | "Sirket Dashboard" -> "Satis Departmani Dashboard" |
| **Kullanim** | Hiyerarsik veri yapilarinda | Ilgili ama farkli veri kumelerinde |
| **Avantaj** | Baglam kaybolmaz | Farkli bir perspektif sunar |

**En iyi uygulama:** Kullaniciya her drill-down seviyesinde bir "geri don" (breadcrumb) yolu gosterin. Ornek: `Anasayfa > Satis > 2024 > Q4 > Aralik`

---

## 5. Veri Hikayelestirme (Data Storytelling)

Veri gorsellestirme sadece grafik cizmek degildir; bir hikaye anlatma aracidir. Cole Nussbaumer Knaflic'in "Storytelling with Data" kitabina gore, en iyi veri sunumlari bir hikaye yapisina sahiptir.

### 5.1 The Three-Act Structure in Data Narratives

**1. Perde — Context (Baglam):**
- "Durum nedir?" sorusunu cevapla
- Mevcut durumu gosteren bir "before" grafigi sun
- Problemi veya firsati tanit

**2. Perde — Conflict (Catisma):**
- "Ne degisti?" veya "Sorun ne?" sorusunu cevapla
- Verideki kirilma noktasini, trend degisimini goster
- "Aha" anini yakala — izleyicinin "iste bu!" diyecegi grafik

**3. Perde — Resolution (Cozum):**
- "Ne yapmaliyiz?" sorusunu cevapla
- Onerilen aksiyonun veriyle desteklenmis hali
- "After" grafigi (tahmini veya gerceklesen)
- Cagri (call to action)

**Ornek: Bir perakende sirketinde stok yonetimi sunumu:**
- **1. Perde:** "Gecen yil stok maliyetlerimiz %15 artti. Iste 12 aylik trend." (Line chart)
- **2. Perde:** "Fakat satislar sadece %3 artti. Yani stok-satis orani bozuldu. Ozellikle X kategorisinde stok fazlasi var." (Scatter plot: kategori bazinda stok vs satis)
- **3. Perde:** "X kategorisinde stogu %30 azaltirsak, 2 milyon TL tasarruf ederiz. Iste onerilen hedef stok seviyeleri." (Waterfall chart: tasarruf hesaplamasi)

### 5.2 The "So What?" Test for Every Chart

Her grafiginiz icin su soruyu sorun: **"So what? Bu grafigi gorunce ne yapacagim?"**

| Grafik | "So what?" cevabi yoksa | "So what?" cevabi varsa |
|---|---|---|
| Aylik satis trendi | "Satislar su sekilde..." | "Nisan'da satislar dustu, cunku rakip kampanya baslatti. Mayis'ta karsilasma stratejisi devreye alinmali." |
| Musteri memnuniyeti skoru | "Memnuniyet %72." | "Memnuniyet %72, sektor ortalamasi %78. Ozellikle iade surecinde sikayet var, bu sureci iyilestirmeliyiz." |

**Pratik test:** Grafigi bir arkadasiniza gosterin ve "ne anladin?" diye sorun. Cevabi sadece veriyi tanimlamaksa (descriptive), grafiginiz eksik. Eger "su neden boyle?" (diagnostic) veya "sunu yapmaliyiz" (prescriptive) diyorsa, basarili.

### 5.3 How to Structure a Data-Driven Presentation

1. **Baslik (Headline):** "Turkiye E-Ticaretinde Mobil Odemeler Yuzde 40'a Ulasti" — bir iddia, bir rakam, bir yon
2. **Baglam (Context):** 1-2 slide ile sektor genel durumu (neden bu konu simdi?)
3. **Veri (Evidence):** 3-5 grafik, her biri bir oncekinden sonraki soruyu cevaplasin
4. **Icgoru (Insight):** "Bu veri bize ne soyluyor?" — her grafikten sonra bir cumle
5. **Aksiyon (Action):** "Simdi ne yapmaliyiz?" — net bir oneri
6. **Kapanis (Close):** "Hatirlatma" slide'i — en onemli 3 rakam

**Slayt basina kural:** Bir slayt = bir mesaj. Bir slaytta birden fazla grafik varsa, hepsi ayni mesaji desteklemeli.

### 5.4 Minto Pyramid Principle for Data Argumentation

Barbara Minto'nun McKinsey icin gelistirdigi bu prensip, veri argumanlarini piramit seklinde yapilandirir:

```
                    [Ana Mesaj]
                   /     |      \
            [Destek 1] [Destek 2] [Destek 3]
              /   \       /   \      /   \
           [V1] [V2]   [V3] [V4]  [V5] [V6]
```

**Is akisi:**
1. **En tepede ana sonuc:** "Stok maliyetlerimizi %20 azaltabiliriz"
2. **Orta seviyede 3 ana neden:**
   - Talebi dogru tahmin edemiyoruz
   - Tedarik zincirinde gecikme var
   - Stok tutma maliyeti artti
3. **En altta veri:** Her bir neden icin 2-3 grafik

**Neden ise yarar:** Yoneticiler once sonucu gorur, sonra "neden?" sorusunu sorarak detaya iner. Piramit yapisi, bu dogal sorgulama akisini destekler.

---

## 6. Renk ve Erisilebilirlik

Renk, veri gorsellestirmenin en guclu ama en tehlikeli aracidir. Yanlis renk secimi, veriyi anlasilmaz kilabilir veya yanlis mesaj verebilir.

### 6.1 Color Theory for Data Viz

**Uc temel renk paleti turu:**

| Tur | Kullanim | Ornek | Palette Sayisi |
|---|---|---|---|
| **Categorical** | Kategorik veri ayrimi (ulkeler, urunler) | Mavi, Kirmizi, Yesil, Turuncu, Mor | 5-8 renk |
| **Sequential** | Sfrdan yuksege dogru giden veri (nufus yogunlugu) | Acik maviden koyu maviye | 5-9 ton |
| **Divergent** | Iki ucun da anlamli oldugu veri (+/- fark, memnuniyet) | Kirmizi -> Beyaz -> Yesil | 5-11 ton |

**Categorical palette dikkat:** Renkler birbirinden ayirt edilebilir olmali ve ayni kulturel agirliga sahip olmamali.

**Sequential palette dikkat:** Acik tondan koyu tona dogru giden tek bir renk ailesi kullanilir. Data ink'ta tonal fark, verideki farki yansitir.

**Divergent palette dikkat:** Ortadaki nor nokta (genelde beyaz, acik gri) kritiktir. Ortalamanin alti bir renk (mavi), ustu baska bir renk (kirmizi) ile gosterilir.

### 6.2 Colorblind-Safe Design

Dunya nufusunun yaklasik %8'i (erkeklerde %10, kadinlarda %0.5) renk korudur. En yaygin turler:
- **Deuteranopia:** Yesil zayifligi (en yaygin, %6)
- **Protanopia:** Kirmizi zayifligi (%2)
- **Tritanopia:** Mavi zayifligi (cok nadir, %0.01)

**Colorblind-safe tasarim ilkeleri:**

1. **Renge ek olarak baska bir kanal daha kullan:** Sekil (daire vs ucgen), desen (taranmis vs duz), etiket
2. **Color Brewer paletleri kullan:** ColorBrewer 2.0 (colorbrewer2.org), colorblind-safe paletler sunar
3. **Kirmizi-yesil birlikteliginden kacin:** En yaygin renk koru turu bunlari ayirt edemez. Bunun yerine mavi-turuncu kullanin
4. **Simulasyon testi:** Cobb (chroma.js) veya Color Oracle ile grafiginizi renk koru filtrelerinden gecirin
5. **Zitlik (contrast) kontrolu:** Arkaplan-yazi kontrasti WCAG AA (4.5:1) standardini karsilamali

**Ornek palet (colorblind-safe):**

| Kategori | Renk |
|---|---|
| Kategori 1 | #0077BB (Mavi) |
| Kategori 2 | #EE7733 (Turuncu) |
| Kategori 3 | #33BBEE (Acik Mavi) |
| Kategori 4 | #EE3377 (Pembe) |
| Kategori 5 | #009988 (Yesil) |
| Kategori 6 | #CCBB44 (Sari) |

### 6.3 Cultural Color Meanings

Veri gorsellestirme kuresel bir sirkette, ozellikle de Turkiye gibi dogu-bati arasindaki bir ulkede dikkatli olmayi gerektirir.

| Renk | Bati Anlami | Cin/Japonya | Hindistan | Orta Dogu |
|---|---|---|---|---|
| **Kirmizi** | Tehlike, kayip, uyari | Bereket, sans | Evlilik, temizlik | Dikkat |
| **Yesil** | Basari, para (ABD finans) | Sadakat | Bereket | Islam'da kutsal renk |
| **Mavi** | Guven, kurumsal | Olumsuzluk | Krishna'nin rengi | Koruyucu |
| **Sari** | Uyari, dikkat | Imparatorluk, kutsal | Ticaret | Mutluluk |
| **Siyah** | Matem, guc, zarafet | Su, guven | Kotuluk | Matem |
| **Beyaz** | Temizlik, masumiyet | Matem, yas | Saflik (fakat dul kadinlar giyer) | Temizlik |

**Turkiye ozelinde:**
- Kirmizi genelde "kayip" veya "kadin" (is hayatinda) olarak algilanir
- Yesil dogrudan Islam ile iliskilendirilir, bu nedenle politik icerikli veride dikkatli olunmali
- Mavi en "guvenli" renktir; Turk sirket dashboard'larinda yaygindir
- Sari uyari icin evrenseldir, Turkiye'de de "dikkat" anlamiyla uyusur

---

## 7. Arac Karsilastirmasi

Veri gorsellestirme araclari uc ana kategoride incelenebilir: enterprise BI araclari, kod tabanli araclar, ve web tabanli ge e da

### 7.1 Tableau

| Ozellik | Degerlendirme |
|---|---|
| **Artilar** | Drag-drop arayuz, cok guclu kesif (discovery), canli veri baglantisi, LOD (Level of Detail) hesaplamalari, genis topluluk ve egitim kaynaklari |
| **Eksiler** | Lisans maliyeti yuksek (Creator ~$70/ay), buyuk veri setlerinde yavaslayabilir, ince ayarli tasarim icin sinirli, Tableau Server kurulumu karmasik |
| **Ne zaman kullanilmali** | Veri kesfi (exploratory), self-service analytics, yonetici dashboard'lari, sirket ici raporlama |
| **Turkiye kullanimi** | Turkiye'de finans ve perakende sektorunde yaygin. Turk Telekom, Garanti BBVA, Trendyol gibi buyuk firmalar Tableau kullaniyor. Tableau Public ucretsiz ancak veriniz halka acik olur. |

**Tableau'nun guclu yonu — LOD Expressions:**
```tableau
{FIXED [Kategori] : SUM([Satis])}  // Her kategori icin toplam satis, filtrelerden bagimsiz
```

### 7.2 Power BI

| Ozellik | Degerlendirme |
|---|---|
| **Artilar** | Microsoft ekosistemi ile tam uyum (Excel, Azure, Teams), ucretsiz masaustu surumu, DAX dili cok guclu, copilot entegrasyonu (2025'te gelisti), kurumsal guvenlik |
| **Eksiler** | Mac'te masaustu surumu yok (web surumu sinirli), karmasik veri modellerinde DAX ogrenme egrisi dik, buyuk dataset'lerde Power BI Premium gerekiyor, gorsellestirme ozellestirme sinirli (custom visual'lar kalite sorunlu) |
| **Ne zaman kullanilmali** | Microsoft sirketlerinde standart, finans ve IT ekipleri icin ideal, self-service reporting |
| **Turkiye kullanimi** | Turkiye'de KOBiler arasinda Power BI daha yaygin (Excel'den gecis kolay). Ko Holding, Dogus Grubu, Turkcell Power BI kullaniyor. Ucretsiz surumu nedeniyle girisimciler arasinda populer. |

**Power BI DAX ornegi:**
```dax
Yillik Buyume = 
VAR OncekiYil = CALCULATE([ToplamSatis], SAMEPERIODLASTYEAR(Takvim[Tarih]))
RETURN
DIVIDE([ToplamSatis] - OncekiYil, OncekiYil, 0)
```

### 7.3 Looker / Looker Studio

| Ozellik | Degerlendirme |
|---|---|
| **Artilar** | Google Cloud entegrasyonu, LookML ile veri modeli tanimlama (tek kaynak), olceklenebilir, ucretsiz Looker Studio (eski Data Studio), web tabanli kurulum gerektirmez |
| **Eksiler** | Looker (Studio degil) pahali (~$3,000+/yil), ogrenme egrisi var, Google Cloud disinda sinirli entegrasyon, canli veri sorgulari yavas olabilir |
| **Ne zaman kullanilmali** | Pazaralamada Google Ads/Analytics entegrasyonu icin ideal, dijital urun sirketleri icin uygun, startup'lar ve KOBiler Looker Studio'yu ucretsiz kullanabilir |
| **Turkiye kullanimi** | Turk dijital ajanslar Looker Studio'yu musteri raporlamasi icin yaygin kullanir. Dijital pazarlama sektorunde standart haline gelmiştir. |

### 7.4 Python (matplotlib, seaborn, plotly)

| Ozellik | Degerlendirme |
|---|---|
| **Artilar** | Tam esneklik, tekrar uretilebilirlik (reproducibility), buyuk veri ile calisma (pandas+matplotlib), ozellestirilebilir her sey, ucretsiz, Jupyter notebook'larla entegre |
| **Eksiler** | Kod bilgisi gerektirir, interaktif grafik icin plotly/dash veya streamlit gerekli, kurulum ve ortam yonetimi sorunlari, dogrudan is kullanicisi kullanamaz |
| **Ne zaman kullanilmali** | Veri bilimi ekipleri, akademik calismalar, otomatik raporlama, ozel istatistiksel gorsellestirmeler |
| **Turkiye kullanimi** | Turk veri bilimi toplulugunda en populer arac. Kaggle Turkiye toplulugu, Turk veri bilimi bootcamp'leri genelde Python ogretiyor. |

**Python ornegi:**
```python
import matplotlib.pyplot as plt
import seaborn as sns

sns.set_theme(style="whitegrid")
fig, ax = plt.subplots(figsize=(10, 6))

# Tufte prensipleriyle uyumlu bir bar chart
sns.barplot(data=df, x='sehir', y='gelir', palette='Blues_d', ax=ax)
ax.set_xlabel('')  # Gereksiz etiket yok
ax.set_ylabel('Ortalama Gelir (TL)')
ax.spines[['top', 'right', 'left']].set_visible(False)  # Sadece alt eksen
ax.tick_params(left=False)  # Tick isaretleri yok
plt.show()
```

### 7.5 D3.js

**Ne zaman kullanilmali:** Ozel, interaktif web gorsellestirmeleri icin. Borsa grafikleri, ag goruntuleme, ozel haritalar, haber sitesi gorsellestirmeleri.

**Ornek kullanim:** The New York Times haber grafiklerinin neredeyse tamami D3.js ile yapilir. Turkiye'de Teyit.org'un yalan haber dogrulama gorsellestirmeleri.

**Avantaj:** DOM uzerinde tam kontrol, SVG/Canvas destegi, CSS ile tam uyum, her tarayicida calisir.
**Dezavantaj:** Javascript bilgisi sart, ogrenme egrisi cok dik, buyuk veri setlerinde performans sorunu olabilir.

---

## 8. Yaygin Hatalar (ve Cozumleri)

### 8.1 Truncated Y-Axis Manipulation

**Hata:** Y-eksenini sifirdan baslatmayarak kucuk farklari abartmak.

**Ornek:** Bir partinin oy orani %30'dan %33'e cikti. Grafik 30-33 arasini gosteriyor. Goruntu: oy orani "firlamis" gibi algilaniyor. Oysa degisim sadece %10 nispi (3/30).

**Cozum:** Bar chart'larda Y-ekseni her zaman 0'dan baslamalidir. Line chart'larda ise fark gostermek icin 0'dan baslatmak zorunda degilsiniz, ancak bunu belirtmelisiniz (ornegin, eksen uzerinde "||" isareti ile kirilma gostermek). Tufte buna "broken axis" der ve ancak cok hakli bir neden varsa kullanilmasini onerir.

### 8.2 Cherry-Picked Time Periods

**Hata:** Kullaniciya dogru hikayeyi anlatmak icin baslangic ve bitis zamanini manipule etmek.

**Ornek:** "Enflasyon 2024'te% 10 azaldi" — ama 2024 baslangici enflasyonun zirve yaptigi ay secilmis. Eger dogru baslangic secilseydi (bir onceki yil ayni ay), enflasyon %5 artmis olarak gorulecekti.

**Cozum:** Zaman serilerinde mumkun oldugunca uzun bir pencere kullanin. Kisa bir zaman araligi secmek zorundaysaniz, bu secimi gerekcelendirin. "Bir onceki yilin ayni donemi" (year-over-year) karsilastirmasi, cherry-picking'i engeller.

### 8.3 Dual-Axis Chart Misuse

**Hata:** Iki farkli olcekteki veriyi ayni grafikte iki farkli Y-ekseni ile gostermek.

**Sorun:** Iki eksenin olcegi farkli oldugunda, korelasyon algisi tamamen yaniltici olabilir. Ornegin, bir ekseni 0-100, digerini 0-1,000,000 yaparak herhangi iki seriyi "birbiriyle hareket ediyor" gibi gosterebilirsiniz.

**Cozum:** Dual-axis kullanmak yerine:
1. Iki ayri grafik kullanin (small multiples)
2. Her iki seriyi de normalize edin (index = 100)
3. Veya farkli renklerle tek eksende gosterilebilecek sekilde olceklendirin

### 8.4 Overplotting

**Hata:** Bir scatter plot'ta yuzlerce binlerce noktanin uste binmesiyle verinin dagiliminin kaybolmasi.

**Ornek:** 10,000 musterinin gelir vs harcama scatter plot'i. Tum noktalar birbirine binmis, sadece siyah bir kume gorunuyor, dagilim okunamaz.

**Cozum stratejileri:**
- **Opacity (saydamlik):** Noktalari yari saydam yaparak biriken bolgelerin daha koyu olmasini saglama
- **Binning (kutulama):** 2D histogram veya hexbin plot kullanma
- **Sampling (ornekleme):** Rasgele orneklem alarak grafigi seyreltme
- **Jittering:** Kategorik eksende noktalari hafifce kaydirarak ust uste binmeyi azaltma

### 8.5 Using Wrong Chart Type

| Veri | Yanlis Grafik | Dogru Grafik |
|---|---|---|
| Zaman serisi (surekli) | Bar chart (aralarda bosluk var) | Line chart |
| Kategori karsilastirmasi | Line chart (kategoriler arasinda gecis yok) | Bar chart |
| Parca-butun iliskisi | Bar chart (butunu gostermez) | Stacked bar chart veya treemap |
| Korelasyon | Iki ayri bar chart | Scatter plot |
| Dagilim | Bar chart (histogram yapay) | Histogram veya box plot |
| Hiyerarsi | Pie chart (duz gosterir) | Treemap veya dendrogram |

---

## 9. En Iyi Kaynaklar

| Kitap | Yazar | Yayinevi | Odak |
|---|---|---|---|
| **The Visual Display of Quantitative Information** | Edward Tufte | Graphics Press | Tufte prensipleri, klasik ornekler |
| **Envisioning Information** | Edward Tufte | Graphics Press | Renk, harita, uzamsal veri |
| **Beautiful Evidence** | Edward Tufte | Graphics Press | Sparklines, sunum teknikleri |
| **Storytelling with Data** | Cole Nussbaumer Knaflic | Wiley | Is dunyasi icin pratik rehber |
| **Information Dashboard Design** | Stephen Few | Analytics Press | Dashboard tasarim prensipleri |
| **Show Me the Numbers** | Stephen Few | Analytics Press | Tablo ve grafik tasarimi |
| **The Functional Art** | Alberto Cairo | Peachpit | Gazetecilik ve veri gorsellestirme |
| **The Truthful Art** | Alberto Cairo | New Riders | Istatistiksel okuryazarlik |
| **Data Points** | Nathan Yau | Wiley | FlowingData perspektifi |
| **Dear Data** | Giorgia Lupi & Stefanie Posavec | Particular Books | El cizimi, veriyi sanata donusturme |
| **Fundamentals of Data Visualization** | Claus O. Wilke | O'Reilly | Renk, eksen, olcek hakkinda detayli teknik rehber |

**Cevrimici Kaynaklar:**

| Kaynak | URL / Platform | Aciklama |
|---|---|---|
| **Makeover Monday** | makeovermonday.co.uk | Her hafta bir grafigi yeniden tasarlama |
| **The Pudding** | pudding.cool | Dijital dergi, deneysel gorsellestirme |
| **FlowingData** | flowingdata.com | Nathan Yau'nun blogu |
| **Observable D3 Notebooks** | observablehq.com | Interaktif D3.js ornekleri |
| **DataWrapper** | datawrapper.de | Hizli, temiz gorsellestirme araci |
| **ColorBrewer 2.0** | colorbrewer2.org | Renk paleti secici (colorblind-safe) |
| **Our World in Data** | ourworldindata.org | Kuresel veri, guzel gorsellestirme ornekleri |
| **R Graph Gallery** | r-graph-gallery.com | Her grafik turu icin R kodu |
| **Python Graph Gallery** | python-graph-gallery.com | Python ile ayni |
| **Tableau Public Gallery** | public.tableau.com | Topluluk dashboard'lari |

**Turkiye'de Takip Edilecek Kisisel Bloglar / Hesaplar:**

- **Veri Bilimi Okulu** (veribilimiokulu.com) — Turkce veri gorsellestirme egitimleri
- **Miuul** (miuul.com) — Veri bilimi ve gorsellestirme bootcamp'leri
- **Ali Ercan Ozgur** — Tableau ve data viz uzmani, Turkce icerikler
- **Turkce Tableau Toplulugu** — Facebook/LinkedIn grubu

---

## 10. Vaka Calismalari

### 10.1 Napoleon's March (Minard) — The Greatest Viz Ever Made

**Kim:** Charles Joseph Minard, 1869
**Ne gosteriyor:** Napoleon'un 1812'de Rusya seferine cikan 422,000 askerinin, Moskova'ya varis ve donus yolculugundaki kaybi.

**Gorsellestirmede 6 boyut tek haritada:**
1. Asker sayisi (cizgi kalinligi) — en temel veri
2. Konum (harita uzerinde x-y koordinati)
3. Yon (kahverengi gidis, siyah donus)
4. Sicaklik (alt tarafta Reaumur olceginde)
5. Zaman (tarihler)
6. Nehir gecisleri (fiziksel engeller)

**Neden bu kadar iyi?**
- Bir bakista 422,000 askerin sadece 10,000'inin geri donebildigi anlasiliyor
- Lie Factor = 1.0 (olcekler dogru)
- Micro/macro: Uzaktan bakinca kalin bir cizginin inceldigini, yaklastikca her bir noktanin tarihi ve sicakligi goruluyor
- Chartjunk yok: her cizgi, her renk bir veri tasiyor

### 10.2 1854 Cholera Map (John Snow) — Visualization Saving Lives

**Kim:** Dr. John Snow, 1854
**Ne gosteriyor:** Londra Soho'da kolera salgininin kaynagini.

**Yontem:** Haritada her kolera olumunu bir nokta (dot) olarak isaretledi. Noktalarin Broad Street'teki bir su pompasinda kumelendigini gordu. Pompayi kaldirtinca salgin durdu.

**Veri gorsellestirme acisindan onemi:**
- **Kesifsel veri analizinin (EDA) ilk orneklerinden**
- **Bir hipotezi gorsellestirme ile dogrulama** (o donem "kotu hava" teorisi varken Snow veriyle su teorisini kanitladi)
- **Konumsal veri gorsellestirmenin (GIS) oncusu**

### 10.3 Hans Rosling's Gapminder — Data Storytelling Mastery

**Kim:** Hans Rosling, Gapminder Foundation
**Ne gosteriyor:** Ulkelerin gelir (GDP per capita) ve yasam beklentisi (life expectancy) iliskisini zaman icinde.

**Neden etkileyici?**
- **Hareketli bubble chart:** Her ulke bir balon, balon buyuklugu nufus, x-ekseni gelir, y-ekseni yasam beklentisi. Yil gectikce balonlar hareket ediyor.
- **Anlatim bicimi:** Rosling, veriyi bir hikaye gibi anlatiyor: "1962'de dunya ikiye ayrilmisti: zengin Batı, fakir Dogu. Simdi 2020'ye bakin, aradaki fark kapandi."
- **Gerçek zamanli sunum tekniĞi:** TED konusmasinda, izleyicilere "tahmin edin hangi ulke nerede?" diye sorup balonlari gosteriyor. Bu, veri hikayelestirmenin en iyi orneklerinden.

### 10.4 Turkiye Enflasyon Verisi Gorsellestirmeleri

**Iyi ornek:** Turkiye Istatistik Kurumu (TUIK) tarafindan yayinlanan TÜFE yillik degisim grafigi. Sade, clean, 2015-2024 arasi trend net goruluyor. Tek bir line chart, indeks bazli.

**Kotu ornek:** Bazi haber sitelerinde enflasyon grafigi. Y-ekseni sifirdan baslamiyor, sadece iki ay secilmis (cherry-pick), 3D efektli bar chart.

**Tartisma konusu:** Turkiye'de enflasyon verisi politik olarak hassas oldugu icin, farkli kaynaklar (ENAG, TUIK, bagimsiz ekonomistler) farkli gorsellestirme tercihleri yapiyor. Bu, Tufte'nin "lie factor" prensibinin politik ekonomide nasil kullanildigina dair iyi bir ornek.

### 10.5 Apple Health Dashboard Design Analysis

**Dashboard elemanlari:**
1. **Ustte (En kritik):** Gunluk aktivite halkalari — Move, Exercise, Stand (3 renkli halka, hedefe gore doluluk)
2. **Ikinci sirada:** Adim sayisi ve mesafe (KPI kart + small multiples haftalik trend)
3. **Ucuncu sirada:** Kalp atis hizi, uyku, kan oksijeni (detay grafikler)
4. **En altta:** Trendler (sparkline ile haftalik degisim)

**Gestalt prensipleriyle uyumu:**
- **Proximity:** Aktivite halkalari bir arada, kalp sagligi ayri bir grupta
- **Similarity:** Tum KPI kartlar ayni form faktorunde
- **Closure:** Halkalar eksik olsa da beyin butunleri tamamliyor

**Tufte acisindan degerlendirme:**
- **Data-ink ratio:** Yuksek. Az renk, cok veri
- **Chartjunk:** Yok. Minimal tasarim
- **Micro/macro:** Activity rings (macro: genel aktivite) ve detay rapor (micro: saatlik detay)
- **Kritik:** Halkalarin 3D efekti Tufte'nin hosuna gitmezdi, ancak kullanici testlerinde etkili oldugu kanitlanmis

---

## 11. Pratik Alistirmalar

Her alistirma ogrencinin portfolyosuna eklenebilecek bir cikti uretmelidir.

### 11.1 Bad Chart Redesign (Before/After)

**Alistirma:** Internette buldugunuz kotu bir veri gorsellestirmesini secin (ornegin, 3D pie chart ile gosterilmis bir pazar payi verisi). Tufte prensiplerini kullanarak yeniden tasarlayin.

**Yapilacaklar:**
1. Orijinal grafigin neden kotu oldugunu analiz edin (Lie Factor, chartjunk, yanlis grafik turu)
2. Dogru grafik turunu secin
3. Data-ink ratio'yu artirin
4. Renk paletini duzeltin
5. "So what?" testini gecen bir versiyon olusturun
6. Before/after karsilastirmasi ile birlikte teslim edin

**Teslimat:** Tableau Public, Power BI, Python veya el cizimi ile yapilabilir.

### 11.2 Build a Business Dashboard

**Alistirma:** Kucuk bir isletmenin (ornegin, bir kahve dukkani zinciri) performansini izleyen bir dashboard olusturun.

**KPI'lar (minimum):**
- Gunluk toplam satis (bugun, gecen hafta bugun, aylik hedefe gore)
- En cok satan 5 urun
- Musteri basina ortalama harcama
- Yogun saatler (heatmap: gun vs saat)
- Stok durumu (kritik seviyede olan urunler)
- Musteri memnuniyeti (anket skoru)

**Araclar:** Tableau Public (ucretsiz) veya Power BI Desktop (ucretsiz)

**Not alma:** Tasarim kararlarinizi Tufte ve Few prensipleri ile gerekcelendirin. Neden bu rengi sectiniz? Neden bu grafik turunu sectiniz? Kac KPI koydunuz ve neden?

### 11.3 Sparkline-Infused Report

**Alistirma:** Bir Excel tablosunda aylik finansal verileri sparkline ile zenginlestirin.

**Adimlar:**
1. 12 aylik gelir, gider ve kar verisi iceren bir tablo olusturun
2. Her bir satirin yanina Excel sparkline (cizgi veya kazanc/kayip) ekleyin
3. Hucresel data bars ile her hucredeki rakamin gorselini ekleyin
4. Kosullu bicimlendirme (conditional formatting) ile en yuksek/degerleri vurgulayin

**Cikti:** Tek bir Excel sayfasinda, hic grafik eklemeden, 12 aylik trendi gosteren bir rapor.

### 11.4 Data Story from a Raw Dataset (3-Act Structure)

**Alistirma:** Kaggle.com'dan bir veri seti secin (ornegin: "World Happiness Report 2024" veya "Turkish Economic Indicators"). Veriyi uc perdelik bir hikaye olarak sunun.

**Yapi:**
1. **Perde 1:** "Dunya nasil bir yer?" (3-4 grafikle genel durum)
2. **Perde 2:** "Türkiye nerede duruyor?" (Turkiye'nin diger ulkelerle karsilastirmasi)
3. **Perde 3:** "Ne degismeli?" (Veriye dayali oneri)

**Ipuclari:**
- Her perdede maksimum 2 grafik
- Her grafikten sonra "so what?" cumlesi
- Minto Pyramid: once sonuc, sonra neden

### 11.5 Lie-Finder Exercise

**Alistirma:** 5 adet yaniltici veri gorsellestirmesi bulun. Medyada (TV haberleri, gazeteler, sosyal medya), sirket sunumlarinda veya reklamlarda bulabilirsiniz.

**Her bir yaniltici grafik icin analiz:**
1. Orijinal gorseli kaydedin
2. Hangi prensip ihlal ediliyor? (Lie Factor, truncated y-axis, cherry-picking, chartjunk, yanlis grafik turu)
3. Neden yaniltici oldugunu aciklayin
4. Duzeltilmis versiyonunu olusturun

**Bonus:** Twitter'da dillere düsen "veri gorsellestirme hatalari" paylasimlarini takip edin. Reddit r/dataisugly toplulugu iyi bir kaynaktir.

---

## 12. Turkiye'de Bu: Data Viz Culture in Turkey

### 12.1 TUIK Veri Gorsellestirme Kalitesi

Turkiye Istatistik Kurumu (TUIK), ozellikle son yillarda veri gorsellestirme kalitesini artirmis olsa da, Tufte standartlarina gore hala eksikleri var:

**Artilar:**
- TUIK'in aylik enflasyon bultenleri sade ve tutarli bir formata sahip
- "Istatistiklerle Turkiye" yayini renkli ve anlasilir haritalar iceriyor
- TUIK veri portali (data.tuik.gov.tr) interaktif tablolar sunuyor

**Eksiler:**
- Bazi grafiklerde hala 3D efekt kullaniliyor
- Renk paletleri colorblind-safe degil (kirmizi-yesil ayrimina dayali)
- Ozellikle bolgesel haritalarda sinir uyusmazliklari ve renk skalasi hatalari gorulebiliyor
- Veri indirme ve ham veriye erisim sinirli

### 12.2 Turkiye'de Dashboard Kulturu

**Kamu sektoru:**
- Belediyeler (Istanbul, Ankara, Izmir) GOZLEM veya turevi platformlarla acik veri dashboard'lari yayinliyor
- Saglik Bakanligi COVID-19 doneminde gunluk veri dashboard'i ile iyi bir ornek sergiledi
- Ancak genel olarak kamu kurumlarinda veri gorsellestirme bilinci dusuk

**Ozel sektor:**
- Bankacilik ve finans sektoru Tableau/Power BI kullaniminda onde
- Perakende (Trendyol, Hepsiburada) data-driven dashboard kulture sahip
- Startup'lar Looker Studio'yu agirlikli kullaniyor
- KOBi'lerde veri gorsellestirme bilinci hala emekleme asamasinda

**Akademi ve sivil toplum:**
- TUBITAK ve TUSIAD yayinlarinda veri gorsellestirme kalitesi degisken
- Teyit.org, dogrulama calismalarinda veri gorsellestirmeyi etkin kullaniyor
- IPA (Istanbul Planning Agency) ozellikle sehir verileriyle iyi gorsellestirme ornekleri sunuyor

### 12.3 Turkiye'de En Iyi Dashboard Uygulamalari

| Kurum | Dashboard | Guclu Yonleri |
|---|---|---|
| **IBB (Istanbul Buyuksehir Belediyesi)** | IBB Acik Veri Portal | Arayuz, kategorizasyon, renk kullanimi |
| **Saglik Bakanligi** | COVID-19 Turkiye | Gunlik guncelleme, temiz KPI gosterimi |
| **TurkEximbank** | Ihracat Dashboard | Finansal KPI hiyerarsisi, trend gostergeleri |
| **Trendyol** | Satis Dashboard | Micro/macro dengesi, mobil uyum |
| **Turkcell** | Operasyon Dashboard | Gercel zamanli veri, leading indicator kullanimi |

### 12.4 Turkiye'de Veri Gorsellestirme Egitimi ve Is Piyasasi

**Egitim:**
- Bilgi Universitesi, Ozyegin Universitesi, Koc Universitesi veri gorsellestirme dersleri veriyor
- Bootcamp'ler (Miuul, Veri Bilimi Okulu, Istanbul Data Science Academy) yogun talep goruyor
- Ancak universitelerde veri gorsellestirme ayri bir ders olmaktan cok, istatistik veya veri bilimi derslerinin bir modulu olarak ele aliniyor
- Tufte ve Few gibi temel kaynaklarin Turkce cevirileri sinirli

**Is piyasasi:**
- "Data Visualization Specialist" ilanlari artiyor, ancak cogu "Business Intelligence Analyst" veya "Data Analyst" rolu icinde bir alt beceri
- Tableau + SQL + Python uclu yetenek seti en cok aranan profil
- Turkiye'de ortalama veri gorsellestirme uzmani maasi (2025): deneyime gore 25,000-60,000 TL arasi

---

## Ozet Tablo: Pre-Knowledge Check

| Soru | Evet | Hayir | Cozum |
|---|---|---|---|
| Pie chart kullaniyor muyum? | Kullanmayi birak | Baska grafik turune gec | Bar chart veya treemap |
| Y-ekseni 0'dan basliyor mu? | Devam | Duzelt | Bar chart icin 0 sart, line chart icin belirt |
| Grafigim tek bakista anlasiliyor mu? | Devam | Basitlestir | Bir mesaj, bir grafik |
| Renk koru dostu mu? | Devam | Palet degistir | ColorBrewer kullan |
| "So what?" testini gectim mi? | Sunuma hazir | Yeniden yapilandir | Her grafik icin bir aksiyon |

---

> **"Above all else show the data."** — Edward Tufte
