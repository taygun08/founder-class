# 06 — Finansal Analiz

> **Modul:** Research & Analysis
> **Seviye:** Temel / Orta
> **On Kosul:** Temel Muhasebe Bilgisi, Excel Kullanimi

---

## 1. Giris

Finansal analiz, bir sirketin mali sagligini, performansini ve potansiyel risklerini anlamak icin finansal verilerin sistematik olarak incelenmesidir. Bu beceri yalnizca muhasebeciler veya finans director'lari icin degil, is dunyasinda karar alan **herkes** icin kritiktir.

### Neden Herkes Finansal Analiz Bilmeli?

- **Girisimci / Startup Kurucusu:** Yatirimci sunumu hazirlarken unit economics, churn ve burn rate hesaplamalari yapmaniz gerekir.
- **Orta Kademe Yonetici:** Departman butcenizi savunmak ve kaynak tahsisi kararlarina katilmak icin temel P&L okuryazarligi sarttir.
- **Urun Yoneticisi:** Yeni bir ozelligin ROI'sini hesaplamak, A/B testlerinin mali sonuclarini yorumlamak finansal analiz gerektirir.
- **Pazarlamaci:** Musteri edinme maliyeti (CAC), marketing spend ROT, kampanya karliligi olcumunden sorumlusunuzdur.
- **Yatirimci:** Bir sirkete sermaye koymadan once finansal tablolari okuyup yorumlayabilmelisiniz.

Finansal analiz, "sayilarin hikayesini anlatmak"tir. Bu modul, sizi mali tablolari sadece okuyan degil, onlardan anlam cikaran, egilimleri goren ve stratejik kararlar alan bir is insani yapacak.

---

## 2. Finansal Tablolarin Okunmasi

Finansal analizin temeli, uc temel finansal tabloyu dogru okumak ve bunlar arasindaki iliskiyi anlamaktir.

### 2.1 Bilanco (Balance Sheet)

Bilanco, sirketin **belirli bir andaki** finansal durumunu gosterir. Temel denklem:

```
VARLIKLAR (Assets) = KAYNAKLAR (Liabilities) + OZ SERMAYE (Equity)
```

| Bilesen | Alt Kalemler | Nelere Dikkat Edilmeli |
|---|---|---|
| **Donen Varliklar** | Nakit, Ticari Alacaklar, Stoklar, Kisa Vadeli Yatirimlar | Nakit seviyesi trendi; alacak yaslandirma; stok devir hizi |
| **Duran Varliklar** | Maddi Duran Varliklar (tesis, makine), Maddi Olmayan Duran Varliklar (serefiye, patent), Kullanim Hakki | Sermaye yogunlugu; varlik yas i; serefiye / toplam varlik orani |
| **Kisa Vadeli Yukumlulukler** | Ticari Borclar, Banka Kredileri (kisa), Kisa Vadeli Karsiliklar | Likidite riski; kisa vadeli borclarin donen varliklarla karsilanmasi |
| **Uzun Vadeli Yukumlulukler** | Banka Kredileri (uzun), Tahvil, Kira Yukumlulukleri, Ertelenmis Vergi | Borc vadesi; sabit odeme yukumlulugu; faiz yuku |
| **Ozkaynaklar** | Odenmis Sermaye, Kar Yedekleri, Gecmis Yillar Karlari, Donem Net Kar | Bilesik buyume orani (CAGR) uzerinden ozkaynak trendi; dagitilmamis karlar |

**Bilanco okurken dikkat edilmesi gereken esik sorular:**

- Sirket kisa vadeli yukumluluklerini karsilayabiliyor mu? (Likidite)
- Varliklarin ne kadari borcla finanse ediliyor? (Kaldirac / Leverage)
- "Serefiye" (goodwill) gibi maddi olmayan varliklar bilanconun ne kadarini olusturuyor?
- Bilanco disi yukumlulukler var mi? (Operasyonel kiralamalar, kontenjan yukumlulukleri)

### 2.2 Gelir Tablosu (Income Statement / P&L)

Gelir tablosu, sirketin **belirli bir donemdeki** performansini gosterir.

```
Net Satis Geliri (Revenue)
- Satislarin Maliyeti (COGS)
= Bruk Kar (Gross Profit)
- Faaliyet Giderleri (Ar-Ge, Pazarlama, Genel Yonetim)
= Faaliyet Kari (EBIT / Operating Profit)
+/- Diger Gelir/Giderler
- Faiz Gideri
= Vergi Oncesi Kar (EBT)
- Vergi
= Net Donem Kari (Net Income)
```

| Kalem | Anlami | Yorum |
|---|---|---|
| **Revenue** | Sirketin temel faaliyetlerinden elde ettigi hasiat | Gelirin surdurulebilir mi? Tek seferlik mi? Ne kadar organik? |
| **COGS** | Satisi yapilan urunun/hizmetin dogrudan maliyeti | Bruttan nasil etkileniyor? Hammaddede fiyat riski var mi? |
| **Brut Margin** | (Revenue - COGS) / Revenue | Sirketin fiyatlama gucunu gosterir. Trend yukseliyor mu? |
| **EBITDA** | Faiz, Vergi, Amortisman ve Itfa oncesi kar | Nakit yaratma gucunu yaklasik olarak olcer. "Operasyonel nakit akisi proxy'si" |
| **Net Income** | Hissedarlara kalan nihai tutar | Tum gider, faiz ve vergiler dusuldukten sonraki donem kari |

**Uyarilar:**

- **Revenue recognition (hasiat kaydi):** Hasiat ne zaman kayda aliniyor? Teslimatta mi, sozlesme imzasinda mi, uzun vadeli projelerde tamamlanma yuzdesine gore mi?
- **One-off items:** EBITDA'ya eklenen "duzeltilmis" (adjusted) kalemler — bazen sirketler surekli giderleri "one-off" gibi gosterme egiliminde olabilir.
- **EBITDA vs Operating Cash Flow:** EBITDA, calisma sermayesi degisimini ve yenileme yatirimlarini hesaba katmaz. Her zaman **Free Cash Flow** ile birlikte degerlendirin.

### 2.3 Nakit Akis Tablosu (Cash Flow Statement)

"Cash is king." Gelir tablosunda kar gosteren bir sirket, nakit akis tablosunda battigini gosterebilir.

| Bolum | Icerik | Onemli Nokta |
|---|---|---|
| **Isletme Faaliyetlerinden Nakit Akisi** | Net kar + amortisman + calisma sermayesi degisimi | Sirketin asil isinden nakit uretip uretmedigini gosterir |
| **Yatirim Faaliyetlerinden Nakit Akisi** | Sabit varlik alimi (CapEx), sirket alimi, finansal yatirimlar | Buyume harcamalari. CapEx / EBITDA orani kritik |
| **Finansman Faaliyetlerinden Nakit Akisi** | Borc alimi/odemesi, temettu, hisse senedi ihraci/geri alimi | Sermaye yapisindaki degisimler |

**Uc kritik metrik:**

1. **Free Cash Flow (FCF)** = Isletme Nakit Akisi - CapEx
   - Sirketin temettu odeyebilme, borc odeme, yatirim yapma kabiliyeti
2. **Cash Conversion Rate** = FCF / EBITDA
   - EBITDA'nin ne kadarina nakit olarak ulasiliyor? (Saglikli: %60+)
3. **FCF Yield** = FCF / Piyasa Degeri
   - Bir hisse icin "nakit verimliligi" — tahvil faizine benzer

### 2.4 Uc Tablonun Birbiriyle Iliskisi

Uc tablo birbirine baglidir ve birini anlamadan digerini anlamak zordur:

```
                                 ┌─────────────────────────────┐
                                 │      GELIR TABLOSU          │
                                 │  Revenue - Tum Giderler      │
                                 │  = Net Kar (+/-)             │
                                 └──────────┬──────────────────┘
                                            │ Net Kar (en temel baglanti)
                                            ▼
                                 ┌─────────────────────────────┐
                                 │    NAKIT AKIS TABLOSU        │
                                 │  + Net Kar                   │
                                 │  +/- Amortisman              │
                                 │  +/- Calisma Sermayesi       │
                                 │  = Isletme Nakit Akisi       │
                                 │  - CapEx (yatirim)           │
                                 │  +/- Borc / Sermaye Degisimi │
                                 │  = NAKIT DEGISIMI            │
                                 └──────────┬──────────────────┘
                                            │ Nakit degisimi
                                            ▼
                                 ┌─────────────────────────────┐
                                 │       BILANCO               │
                                 │  Nakit artisi/azalisi        │
                                 │  Net Kar > Ozkaynak artisi   │
                                 │  Nakit = onceki + degisim    │
                                 └─────────────────────────────┘
```

Ornegin: Bir sirket buysa kar ettigini gosteriyorsa (gelir tablosu) ama nakit seviyesi dusuyorsa (nakit akis / bilanco), bu genellikle su anlamlara gelir:
- Alacaklar hizla artiyordur (tahsilat sorunu)
- Stoklar sisiyordur (satin alma takimi fazla alim yapmistir)
- Buyuk bir CapEx harcamasi yapiliyordur (yatirim donemi)

---

## 3. Oran Analizi (Ratio Analysis)

Oran analizi, finansal tablolardaki mutlak rakamlari anlamli kiyaslamalara donusturur. Bir sirketi tek basina analiz etmek degil, **sektor ortalamalari, rakipler ve sirketin kendi gecmisi** ile karsilastirmak esastir.

### 3.1 Likidite Oranlari

Sirketin kisa vadeli borclarini odeyebilme gucunu olcer.

| Oran | Formul | Sektorik Deger | Yorum |
|---|---|---|---|
| **Cari Oran** | Donen Varliklar / KV Yukumlulukler | 1.5x - 2.5x | <1.0 ise acil likidite riski; >3.0 ise verimsiz nakit yonetimi |
| **Asit-Test Orani (Quick Ratio)** | (Donen Varliklar - Stoklar) / KV Yukum | 0.8x - 1.5x | Stoklara bagimli degil. Imalatatta kritik |
| **Nakit Orani** | (Hazir Degerler + Menkul Kiymet) / KV Yukum | 0.2x - 0.5x | En muhafazakar olcum. Kriz donemlerinde onemli |

**Pratik Uygulama:** Bir sirketin cari orani 0.7 ise, bu sirket KV yukumluluklerinin yalnizca %70'ini kisa vadeli varliklariyla karsilayabiliyor demektir. Bankalar bu sirkete ek kredi acmada tereddut eder.

### 3.2 Karlilik Oranlari

Sirketin faaliyetlerinden ne kadar kar elde ettigini olcer.

| Oran | Formul | Ideal (sektore gore degisir) |
|---|---|---|
| **Brut Kar Marj** | (Net Satis - COGS) / Net Satis | Yuksek (%40+ = fiyatlama gucu var) |
| **Faaliyet Kar Marj (EBIT Margin)** | EBIT / Net Satis | Operasyonel verimlilik gostergesi |
| **Net Kar Marj** | Net Kar / Net Satis | Vergi & faiz sonrasi ne kaliyor? |
| **ROE (Ozkaynak Karliligi)** | Net Kar / Ortalama Ozkaynak | %15+ genellikle iyi kabul edilir |
| **ROA (Aktif Karliligi)** | Net Kar / Ortalama Toplam Varlik | Varlik kullanim verimliligi |
| **ROCE (Kullanilan Sermaye Karliligi)** | EBIT / (Ozkaynak + Finansal Borc) | Sirketin toplam sermayeyi ne kadar verimli kullandigini gosterir |

**Not:** ROE, sermaye yapisindan (leverage) etkilenir. ROE yuksek olan bir sirket cok borclu olabilir. Bu nedenle ROE'yi Dupont analiziyle parcalamak gerekir (Bkz. Bolum 7).

### 3.3 Kaldirac / Borcluluk Oranlari

Sirketin ne kadar borcla calistigini ve borc odeme kabiliyetini olcer.

| Oran | Formul | Esik Deger | Yorum |
|---|---|---|---|
| **Borc / Ozkaynak (D/E)** | Toplam Borc / Ozkaynak | <1.0 muhafazakar; >2.0 riskli | Sektore gore degisir (altyapi sirketleri 3-4x olabilir) |
| **Toplam Borc / Toplam Varlik** | Toplam Borc / Toplam Varlik | <0.50 genelde kabul edilebilir | Varliklarin ne kadari yabanci kaynakla finanse ediliyor |
| **Faizin Karsilanma Sayisi (ICR)** | EBIT / Faiz Giderleri | >3.0 guvenli; <1.5 riskli | Faiz odemeleri kac kez karsilaniyor? |
| **Debt / EBITDA** | Net Finansal Borc / EBITDA | <3.0x saglikli; >5.0x riskli | Kredi derecelendirmede en kritik metrik |

**Borcluluk Değerlendirme Tablosu:**

```python
D/E < 0.5: Dusuk kaldirac, konservatif
D/E 0.5 - 1.5: Orta kaldirac, tipik sirket
D/E 1.5 - 3.0: Yuksek kaldirac, buyume odakli / sermaye yogun sektorler
D/E > 3.0: Yuksek finansal risk (sektor toleransina bagli)
```

### 3.4 Verimlilik / Faaliyet Oranlari

Sirketin varliklarini ne kadar etkin kullandigini olcer.

| Oran | Formul | Yorum |
|---|---|---|
| **Aktif Devir Hizi** | Net Satis / Ortalama Toplam Varlik | 1.0x alti sermaye yogun; >2.0x hafif varlik modeli |
| **Stok Devir Hizi** | COGS / Ortalama Stok | Yuksek = hizli satis; cok yuksekse stoksuz kalma riski |
| **Stok Gun Sayisi (DOS / DIO)** | (Ort. Stok / COGS) x 365 | Kac gunde stok tukeniyor? Sektore gore hedef degisir |
| **Alacak Tahsil Gun Sayisi (DSO)** | (Ort. Ticari Alacak / Net Satis) x 365 | Ortalama kac gunde tahsilat? >60 gun riskli |
| **Borc Odeme Gun Sayisi (DPO)** | (Ort. Ticari Borc / COGS) x 365 | Tedarikciye kac gunde odeme yapiyor? |

**Cash Conversion Cycle (CCC) = DIO + DSO - DPO**

Sirketin nakdini ne kadar sureyle faaliyetlerinde bagli tuttugunu gosterir. Negatif CCC (ornegin perakende devleri) = sirket tedarikciden once musteriden tahsilat yapiyor demektir.

```
Amazon (2023): CCC ~ -30 gun
                 Stok 45 gun + Alacak 15 gun - Borc 90 gun = -30 gun
                 → Tedarikcilerine 90 gunde oduyor, musteriden aninda aliyor.
```

### 3.5 Degerleme Oranlari

Sirketin piyasadaki degerlemesini olcmek icin kullanilir (genellikle halka acik sirketlerde).

| Oran | Formul | Yorum |
|---|---|---|
| **F/K (P/E)** | Hisse Fiyati / Hisse Basina Kar | "Geri odeme suresi (yil)". Yuksek = buyume beklentisi |
| **EV/EBITDA** | (Piyasa Degeri + Net Borc) / EBITDA | Bircok analistin tercih ettigi degerleme carpani |
| **FD/Satis (P/S)** | Piyasa Degeri / Yillik Satis | Henuz kar etmeyen sirketler icin kullanisli |
| **PD/DD (P/B)** | Piyasa Degeri / Defter Degeri | Bankalar, sigorta sirketleri icin standart |
| **PEG Ratio** | F/K / EPS Buyume Orani (yillik) | <1.0 "ucuz"; >2.0 "pahali" (buyume fiyata dahil) |
| **Temettu Verimi** | Hisse Basina Temettu / Hisse Fiyati | Gelir odakli yatirimcilar icin |

**Uygulama Notu:** Tek bir carpanla sirket degerlemek tehlikelidir. Genellikle 3-5 carpan bir arada kullanilir ve sektor ortalamalariyla karsilastirilir.

### 3.6 Sektore Ozel Oranlar: SaaS / Abonelik Sirketleri

Geleneksel oranlar abonelik bazli sirketlerde yetersiz kalir. Asagidaki metrikler SaaS (Software as a Service) sirketleri icin standarttir:

| Metrik | Formul / Tanim | Saglikli Deger |
|---|---|---|
| **MRR (Monthly Recurring Revenue)** | Aylik Yinelenen Gelir | Buyume trendi pozitif |
| **ARR (Annual Recurring Revenue)** | MRR x 12 | Yillik bazda yinelenen gelir |
| **Net Revenue Retention (NRR)** | (Baslangic ARR + Upsum + Expansion - Churn) / Baslangic ARR | >120% "cok iyi"; >100% "iyi" |
| **Gross Churn (Musteri Kaybi)** | Ayrilan Musteri / Toplam Musteri | <%5 aylik |
| **Net Churn** | Kaybedilen ARR / Toplam ARR | Negatif de olabilir (upsell > churn) |
| **LTV (Musteri Yasam Boyu Degeri)** | ARPU / Churn Orani (aylik) | Rehber: CAC'in 3-5 kati |
| **CAC (Musteri Edinme Maliyeti)** | Satis&Pazarlama Gideri / Yeni Musteri | Sektore gore $500-$50,000 |
| **LTV / CAC** | LTV / CAC | >3x ideal; 1-3x iyilestirilmeli; <1x sorunlu |
| **Burn Multiple** | Net Nakit Tuketimi / Net Yeni ARR | <1.0x verimli; >2.0x asiri harcama |
| **Rule of 40** | Buyume Orani (%) + Kar Marj (%) | >40 "basarili"; <20 "gozden gecirilmeli" |
| **Magic Number** | (Yeni C. ARR x 4) / Bir onceki donem S&P harcamasi | >1.0x yuksek verimli satis |

**Ornek:** Bir SaaS sirketinin MRR'si $100K, aylik churn %3, ARPU (Musteri Basina Ortalama Gelir) $500 olsun:

```
LTV = $500 / 0.03 = $16,667
CAC = $5,000 ise LTV/CAC = 3.33x → ideal
Aylik kaybedilen ARR = $100K x 0.03 = $3,000
```

---

## 4. Trend Analizi

Bir donemlik finansal veri yeterli degildir. Trend analizi, sirketin **zaman icinde** nasil degistigini gosterir ve eger karar verme icin kritiktir.

### 4.1 Zaman Serisi Analizi (3-5 Yil Trend)

En az 3 yil, tercihen 5 yillik veri uzerinde:

- **Revenue CAGR**: Son 5 yildaki yillik bilesik buyume orani
- **Gross Margin Trend**: Yukari mi, asagi mi? (Fiyatlama gucu veya maliyet yapisi)
- **Operating Margin Trend**: Olceklendikce marjlar aciliyor mu?
- **FCF Trend**: Buyume ile birlikte nakit akisi mi artiyor, yoksa hep yatirim mi gerekiyor?

**CAGR Formulu:**

```
CAGR = (Son Deger / Ilk Deger)^(1/n) - 1
```

| Yil | Revenue | CAGR (Base) | EBITDA |
|---|---|---|---|
| 2020 | 100M TL | - | 20M TL |
| 2021 | 130M TL | %30 | 28M TL |
| 2022 | 180M TL | %34 | 35M TL |
| 2023 | 220M TL | %35 | 40M TL |
| 2024 | 300M TL | %32 | 55M TL |

> 2020-2024 Revenue CAGR = (300/100)^(1/4) - 1 = %31.6

### 4.2 Common-Size Analizi (Dikey Analiz)

Tum kalemleri **gelir yuzdesi** olarak ifade etmek, sirketleri ve donemleri boyut farkindan bagimsiz karsilastirmayi saglar.

| Kalem | 2022 | 2023 | 2024 | Trend |
|---|---|---|---|---|
| Revenue | %100.0 | %100.0 | %100.0 | Sabit (referans) |
| COGS | %55.0 | %53.2 | %50.1 | Iyilesiyor! |
| AR-GE | %12.0 | %13.5 | %15.0 | Artiyor (yatirim) |
| Pazarlama | %10.5 | %9.8 | %9.0 | Verimli |
| GYG (SG&A) | %8.0 | %7.5 | %7.2 | Olceklendikce dusuyor |
| EBIT | %14.5 | %16.0 | %18.7 | Pozitif trend |
| Net Kar | %10.2 | %11.3 | %13.0 | Pozitif |

Bu tablo, sirketin olceklendikce marjlarini iyilestirdigini (operating leverage) acikca gosterir.

### 4.3 Buyume Orani Analizi

- **YoY (Year over Year)**: Bir onceki yilin ayni donemine gore
- **QoQ (Quarter over Quarter)**: Bir onceki ceyrege gore (mevsimsel sirketlerde dikkatli kullanilmali)
- **Mom (Month over Month)**: Startup ve yuksek buyumeli sirketler icin

```
Yillik Buyume Orani (YOY) = (Cari Donem - Onceki Donem) / Onceki Donem
```

**Uyari:** Bir sirket %100 buyume bildiriyorsa ama onceki yil base etkisi cok dusukse ("base effect"), bu kadar heyecanlanmayin. Base effect ornegi:

- 2023 Revenue: 1M TL → 2024 Revenue: 5M TL = %400 buyume (base cok kucuk)
- 2024 Revenue: 5M TL → 2025 Revenue: 10M TL = %100 buyume (daha etkileyici mutlak artis)

### 4.4 Mevsimsel Duzeltme ve Trend Ayrisma

Bircok sirket mevsimseldir (perakende 4. ceyrek; turizm 2.-3. ceyrek). Mevsimselligi arindirmak icin:

- **Trailing Twelve Months (TTM)**: Son 12 aylik veriyi toplayarak mevsimsellikten arindirmak
- **Weighted Moving Average**: Mevsimsel indeks hesaplayarak trendi cikarmak
- **X-13ARIMA-SEATS**: Ileri duzey mevsimsel duzeltme (ABD Census Bureau metodu)

Basit bir yaklasim: Her ceyregin yillik gelirin yuzdesini hesaplayin:

```
Q1 = %20, Q2 = %25, Q3 = %30, Q4 = %25 → 3. ceyrek en guclu
```

---

## 5. Benchmarking

Bir sirketin finansal sagligini anlamak icin, onu **karsilastirilabilir bir gruba** gore konumlandirmak gerekir.

### 5.1 Dogru Referans Grubunu Bulmak

Benchmarking icin en kritik adim, dogru peer group secimidir:

1. **Sektor (Endustri)**: Ayni NACE / ISIC kodunda mi?
2. **Olcek**: Benzer gelir buyuklugunde mi? (Milyar dolarlik sirketle startup karsilastirilmaz)
3. **Cografi Bolge**: Ayni enflasyon, faiz, duzenleme ortaminda mi?
4. **Is Modeli**: Asset-heavy mi asset-light mi? Abonelik mi proje bazli mi?

**Kaynaklar:**
- **Sektor ortalamalari:** KAP.gov.tr sektor raporlari, TCMB sektor bilanco verileri
- **Kuresel:** Damodaran Online (Aswath Damodaran'in sektorel verileri)
- **Ozel:** McKinsey, Deloitte sektor raporlari, S&P Capital IQ
- **Turkiye:** Finnet, Matriks, Is Yatirim, Garanti BBVA sektor raporlari

### 5.2 Endustri Ortalamalari vs Aspirasyonel Benchmark

Iki tur benchmarking vardir:

| Tur | Tanim | Kullanim |
|---|---|---|
| **Sektor Ortalamasi** | Ayni sektordeki tum sirketlerin medyani | "Ortalamanin altinda miyiz?" |
| **Best-in-Class** | Sektorun en iyi %25 (ust cuval) | "Hedefimiz bu olmali" |
| **Aspirasyonel** | Farkli sektor ama en iyi operasyonel sirketler | "Amazon gibi nakit cevrimine sahip olabilir miyiz?" |

```
Sizin Pazar Marjı: %18  |  Sektor Ortalamasi: %15 | Best-in-Class: %25
→ Sektorde iyisiniz ama en iyi olmaya daha yol var.
```

### 5.3 Sinir Otesi Benchmarking Zorluklari

Sirketleri farkli ulkelerde karsilastirirken dikkat edilmesi gerekenler:

| Sorun | Etkisi | Cozum |
|---|---|---|
| **UFRS vs Yerel GAAP** | Finansal tablo farkli kalemler icerebilir | UFRS bazli set kullanin |
| **Enflasyon** | Turkiye, Arjantin gibi ulkelerde tarihsel maliyet sisebilir | Endeksleme / enflasyon muhasebesi |
| **Kur Volatilitesi** | Doviz bazli borclar karistirir | Ayni para birimine cevirin; fonksiyonel para birimini sorgulayin |
| **Vergi Yapilari** | Net kar marjlarini dogrudan etkiler | Vergi oncesi carpanlar kullanin (EBITDA, EBIT) |
| **Isletme Modeli** | Ayni sektorde farkli modeller olabilir (marketplace vs stok tutan perakende) | Ornek bazli inceleme |

### 5.4 Best-in-Class vs Medyan Karsilastirmasi

Bir ornek benchmarking tablosu:

| Metrik | Sirket X | Sektor Medyan | Best-in-class | Durum |
|---|---|---|---|---|
| Brut Margin | %45 | %38 | %52 | Iyi |
| EBITDA Margin | %22 | %18 | %30 | Orta |
| D/E | 2.1x | 1.5x | 0.8x | Zayif (cok borclu) |
| ROE | %18 | %14 | %28 | Iyi |
| Stok Gun (DOS) | 45 gun | 55 gun | 32 gun | Ortalama |
| Revenue CAGR (5y) | %12 | %8 | %18 | Iyi |

---

## 6. Due Diligence

Due diligence, bir sirkete yatirim yapmadan veya sirketi satin almadan once yapilan detayli arastirma surecidir.

### 6.1 Finansal DD Kontrol Listesi

**1. Gelir Kalitesi (Revenue Quality)**

- [ ] Gelir surdurulebilir mi? Yinelenen (recurring) gelir yuzdesi nedir?
- [ ] Musteri konsantrasyonu: En buyuk 5 musteri gelirin yuzde kacini olusturuyor?
- [ ] Backlog / siparis mevcut mu? Gerceklesmemis satislarin tutari?
- [ ] Revenue recognition politikasi sektor standardina uygun mu?
- [ ] Sozlesme yenileme orani (renewal rate) nedir?

**2. Gider Normalizasyonu (Expense Normalization)**

- [ ] Bir defaya mahsus giderler nelerdir? (Operasyon DD icin normalise edilmeli)
- [ ] Sirket sahibinin kisisel harcamalari sirket uzerinden mi geciriliyor? (owner's compensation)
- [ ] Yuklenici/outsourcing maliyetleri normal piyasa kosullarinda mi?
- [ ] KDV/vergi uyumu ne durumda? Gecmis donem vergi borcu var mi?
- [ ] Kira sozlesmeleri ve diger baglayici harcamalar rayicta mi?

**3. Borc Yapisi**

- [ ] Borc vade dagilimi (kisa / uzun vade)
- [ ] Faiz orani ve sabit/degisken faiz dagilimi
- [ ] Borc sozlesmelerindeki kosullar (covenants): D/E < 2.5x gibi
- [ ] Covariant riski: Bir sart ihlalinde borcun tamami muaccel mi oluyor?
- [ ] Bagli sirketler arasi borclar ve guvence mektuplari

**4. Calisma Sermayesi (Working Capital)**

- [ ] DSO trendi artiyor mu? (Kotu sinyal)
- [ ] Stok yaslandirma: Eski stok var mi? Stok karsiligi yeterli mi?
- [ ] Tedarikci kosullari: DPO degisiyor mu? Tedarikciler daha erken odeme mi istiyor?
- [ ] Mevsimsel calisma sermayesi ihtiyaci: Hangi aylarda nakde daha fazla ihtiyac var?

### 6.2 Kirmizi Bayraklar (Red Flags)

| Kirmizi Bayrak | Ne Anlama Gelebilir | Arastirma Sorusu |
|---|---|---|
| **Revenue artarken nakit akmasi dusuyor** | Tahsilat sorunu, "channel stuffing" | "Alacak gun sayiniz neden 35'ten 60'a cikti?" |
| **Sik sik muhasebe politika degisikligi** | Kar manipulasyonu (earnings management) | "Amortisman yonteminizi neden degistirdiniz?" |
| **Iliskili taraf islemleri (RPT)** | Kar transferi, gizli borc | "Yonetim kurulu uyenize ait sirkete odemeler nedir?" |
| **Surekli "one-time" giderler** | Adjusted EBITDA sisebilir | "Son 5 yilda her sene 'one-time' gider var — bu bir kez degil mi?" |
| **Big bath charges (toplu zarar yazma)** | Yeni CEO eski donemi temizliyor | "Bu serefiye dususu neden simdi?" |
| **Bilanco disi yukumlulukler** | Riskler gizleniyor olabilir | "Operasyonel kiralamalar toplam borca eklenirse ne olur?" |
| **Denetci gorusu (Audit Opinion)** | "Going concern" uyarisi veya olumlu gorus disi | En buyuk kirmizi bayrak |

**Unutulmamali:** Warren Buffett'in kurali: "Bir yoneticinin size karinizin nerede oldugunu anlatamadigini soyledigi bir sirkete yatirim yapmayin. Eger karinin kaynagini anlayamiyorsaniz, sirketi de anlamiyorsunuz demektir."

### 6.3 Operasyonel DD

| Kontrol Alani | Incelenecek Konular |
|---|---|
| **Musteri Konsantrasyonu** | Ilk 1/3/5/10 musteri gelirin %'si, sozlesme bitis tarihleri |
| **Calisan Metrikleri** | Calisan devir hizi, org. semasi, yetenek yogunlugu, ucret seviyesi |
| **Tedarikci Bagimliligi** | Ilk 3 tedarikci yuzdesi; alternatif kaynak mevcut mu? |
| **IT / Veri Altyapisi** | Finansal verilerin sistem entegrasyonu, raporlama otomasyonu |
| **Regulasyon / Lisans** | Faaliyet izinleri, patentler, dava riski |

---

## 7. Dupont Analizi

Dupont analizi, **ROE'yi** bilesenlerine ayirarak sirketin nerede avantajli (veya zayif) oldugunu gosterir.

### 7.1 ROE Ayrismasi (3 Bilesenli Model)

```
             Net Kar      Net Satis      Toplam Varlik
ROE = ───────────── × ───────────── × ────────────────
           Net Satis     Toplam Varlik    Ort. Ozkaynak

ROE = Net Kar Marjı × Varlik Devir Hizi × Finansal Kaldirac
```

**Her bilesenin anlami:**

| Bilesen | Ne Olcer? | Yuksek Olmasi Iyi Mi? |
|---|---|---|
| **Net Kar Marj** | Karlilik = fiyatlama gucu, maliyet kontrolu | Genelde evet, ama cok yuksek rekabet cekebilir |
| **Varlik Devir Hizi** | Verimlilik = varliklari ne kadar iyi kullaniyor | Evet, dusukse sermaye yogun sektor sinyali |
| **Finansal Kaldirac** | Risk = ne kadar borcla calisiyor | ROE'yi artirir ama riski de artirir |

### 7.2 Nasil Yorumlanir?

**Ornek A: Luks Marka (Hermes gibi)**
- Net Kar Marj: %25 (cok yuksek)
- Varlik Devir: 0.6x (dusuk — stoklu, magazali)
- Finansal Kaldirac: 1.3x (dusuk borc)
- **ROE = %25 x 0.6 x 1.3 = %19.5**

**Ornek B: Perakende Devi (Walmart gibi)**
- Net Kar Marj: %2.8 (cok dusuk)
- Varlik Devir: 2.3x (yuksek — hizli donus)
- Finansal Kaldirac: 2.5x (orta-yuksek kaldirac)
- **ROE = %2.8 x 2.3 x 2.5 = %16.1**

> A sirketi fiyatlama gucuyle, B sirketi verimlilik ve kaldiracla ayni ROE'ye ulasiyor. Hangisi daha "kaliteli"? A'nin ROE'si surdurulebilir, B'ninki dovunsel ekonomiye duyarli.

### 7.3 5 Bilesenli Genisletilmis Model

Daha detayli analiz icin ROE 5 bilesene ayrilabilir:

```
ROE = (Net Kar / EBT) × (EBT / EBIT) × (EBIT / Satis) × (Satis / Varlik) × (Varlik / Ozkaynak)

ROE = Vergi Yuk × Faiz Yuk × Faaliyet Karliligi × Varlik Verimliligi × Kaldirac
```

Bu ayrisma, faiz ve vergi yukunun ROE'ye etkisini de gormemizi saglar.

---

## 8. Sirket Degerleme Temelleri

### 8.1 DCF (Indirgenmis Nakit Akisi)

DCF, bir sirketin degerinin, gelecekte yaratacagi tum serbest nakit akislarinin **bugune indirgenmis** toplami oldugu fikrine dayanir.

```
∑                            FCF_t
Firma Degeri =     ───────────────────
                  t=1     (1 + WACC)^t

Terminal Degeri =  FCF_{n+1}  /  (WACC - g)

Nihai Deger = Firma Degeri + Terminal Degeri - Net Borc + Nakit
```

| Degisken | Anlami |
|---|---|
| **FCF** | Free Cash Flow (Isletme Nakdi - CapEx) |
| **WACC** | Agirlikli Ortalama Sermaye Maliyeti (Weighted Average Cost of Capital) |
| **g** | Terminal donem buyume orani (genelde GDP + enflasyon = %2-4) |
| **Net Borc** | Toplam Borc - Nakit |

**DCF'nin Avantajlari:**
- Sirketin nakit yaratma gucune odaklanir
- Varsayimlari acikca belirtmek zorundasiniz (buyume, WACC, terminal buyume)

**DCF'nin Dezavantajlari:**
- WACC ve terminal buyume varsayimlarina cok duyarli (20 yillik bir ongoru)
- "Garbage in, garbage out" — varsayimlar degisince deger de degisir
- Kisa gecmisi olan sirketler icin guvenilmez

### 8.2 Carpan Yontemi (Trading Comparables)

Benzer sirketlerin piyasa carpanlarini kullanarak degerleme:

| Yuklem | Carpan | Nasil? |
|---|---|---|
| Tum sirket (borclu) | EV/EBITDA, EV/Sales | En yaygin |
| Tum sirket (borcsuz) | EV/EBIT, EV/FCF | Capital structure'dan arindirilmis |
| Sadece hisse senedi | F/K (P/E), PD/DD (P/B) | Hissedarlar icin |

```
Peer Sirket Median EV/EBITDA = 12.0x
Hedef Sirket EBITDA = 50M TL
→ Implied Enterprise Value = 50M x 12.0 = 600M TL
→ Implied Equity Value = 600M - 150M (net borc) = 450M TL
```

Orta olcekteki bir sirket icin 5-10 peer secilir ve carpanlarin medyani alinir.

### 8.3 Benzer Islemler (Precedent Transactions)

Gecmiste benzer sirketlerin hangi carpanlarla satildigina bakilir:

| Islem | Yil | Target | EV/EBITDA |
|---|---|---|---|
| A Sirketi satin aldi B'yi | 2022 | 14.0x |
| C Sirketi satin aldi D'yi | 2023 | 12.5x |
| E Sirketi satin aldi F'yi | 2024 | 11.0x |

**Uyari:** Precedent transaction'lar genelde trading comparables'dan daha yuksek carpan icerir, cunku kontrol primi (control premium) eklenir.

### 8.4 Hangi Yontem Ne Zaman Kullanilir?

| Durum | En Uygun Metod | Neden? |
|---|---|---|
| **Halka acik, istikrarli nakit akisi** | DCF | Nakit akisi ongorulebilir |
| **Halka acik, bol peer var** | Trading Comparables | Carpanlar guvenilir |
| **Satin alma / devralma** | DCF + Precedent | Iki yontemle havuza yatirim yapilir |
| **Startup / zarar eden sirket** | P/S, EV/S, karsilastirilabilir | Kar yok, FCF yok |
| **Bankalar, finansallar** | P/B, P/E, DDM | Varlik-agirlikli, DCF uygun degil |
| **Emlak sirketleri** | NAV (Net Asset Value) | Varlik bazli degerleme |

**Altin Kural:** Hicbir zaman tek bir degerleme yontemi kullanmayin. 2-3 metodun sonuclarini karsilastirin ve bir "deger araligi" (valuation range) olusturun.

> "It is better to be approximately right than precisely wrong." — John Maynard Keynes (degerleme icin gecerli)

---

## 9. Modern Araclar

### 9.1 Kurumsal Araclar

| Arac | Kullanim Alani | Maliyet |
|---|---|---|
| **Bloomberg Terminal** | Gercek zamanli veri, tahvil, opsiyon, global veri | ~$20,000/yil |
| **S&P Capital IQ** | Finansal veri, carpanlar, islemler | ~$15,000/yil |
| **Refinitiv Eikon** | Bloomberg alternatifi | ~$18,000/yil |
| **FactSet** | Portfoy yonetimi, arastirma | ~$12,000/yil |
| **Moody's / Fitch / S&P** | Kredi derecelendirme raporlari | Ucretsiz (rapor bazli) |

**Not:** Bu araclar Turkiye'de genellikle sadece buyuk kurumsal yatirimcilar, bankalar ve portfoy yonetim sirketlerinde bulunur.

### 8.2 (9.2) Gizli Sirket Veri Kaynaklari

| Arac | Odak |
|---|---|
| **PitchBook** | Private equity, venture capital verisi (girisimler) |
| **CB Insights** | Startup degerleme, yatirim trendleri |
| **Crunchbase** | Startup fon toplama, temel metrikler |
| **Tracxn** | Hindistan/Asya odakli startup ekosistemi |
| **Preqin** | Alternatif yatirimlar (PE, VC, Hedge Fund) |

### 9.3 Ucretsiz / Dusuk Maliyetli Araclar

| Arac | URL | Kullanim |
|---|---|---|
| **Yahoo Finance** | finance.yahoo.com | Hisse verisi, temel oranlar, haber |
| **Google Finance** | finance.google.com | Gercek zamanli fiyat, portfoy takibi |
| **Ycharts** | ycharts.com | Detayli chart ve oran analizi (ucretli plan da var) |
| **Simply Wall St** | simplywallst.com | Gorsel finansal analiz |
| **KAP** | kap.gov.tr | BIST sirketlerinin resmi bildirimleri |
| **Finnet** | finnet.com.tr | BIST detayli finansal veri |
| **Matriks** | matriksbilgi.com | Canli BIST verisi |
| **Is Yatirim** | isyatirim.com.tr | Aracilik raporlari, analiz |

### 9.4 Excel'de XIRR / XNPV

| Fonksiyon | Kullanim | Formul |
|---|---|---|
| **XIRR** | Duzenli olmayan nakit akislari icin ic verim orani | =XIRR(degerler, tarihler, tahmin) |
| **XNPV** | Duzenli olmayan tarihlerdeki nakit akislarinin bugunku degeri | =XNPV(indirim_orani, degerler, tarihler) |

**Ornek XIRR:** Bir startup'a 2020'de 1M TL yatirdiniz, 2022'de 0.5M TL temettu aldiniz, 2024'te sirketinizi 5M TL'ye sattiniz:

```
= XIRR({-1000000, 500000, 5000000}, {"2020-01-01", "2022-06-15", "2024-12-01"})
```

### 9.5 Python ile Finansal Analiz

Python, buyuk veri setlerinde finansal analizi hizlandirir.

| Kutuphane | Kullanim |
|---|---|
| **yfinance** | Yahoo Finance'dan hisse verisi cekme |
| **pandas-datareader** | Coklu kaynaktan finansal veri |
| **quantlib** | Opsiyon fiyatlama, faiz turevleri |
| **numpy-financial** | NPV, IRR, PMT hesaplamalari |
| **matplotlib / plotly** | Finansal gorsellestirme |
| **openpyxl** | Excel raporlamasi |

**Basit Bir Kod (ornek):**

```python
import yfinance as yf
import pandas as pd

# THYAO (Turk Hava Yollari) verisini cek
ticker = yf.Ticker("THYAO.IS")

# Finansal tablolar
balance_sheet = ticker.balance_sheet
income_stmt = ticker.financials
cash_flow = ticker.cashflow

# Cari Oran
current_assets = balance_sheet.loc["Total Current Assets"].iloc[0]
current_liab = balance_sheet.loc["Total Current Liabilities"].iloc[0]
current_ratio = current_assets / current_liab

print(f"Cari Oran: {current_ratio:.2f}")
```

---

## 10. En Iyi Kaynaklar

### Temel Basilmasi Gereken Kitaplar

| Kitap | Yazar | Nereden Baslamali? |
|---|---|---|
| **Financial Statement Analysis** | K.R. Subramanyam (Cengage) | Akademik standart. En kapsamli. |
| **The Interpretation of Financial Statements** | Benjamin Graham (HarperBusiness) | Klasik. Temel bilgiler, yatirim odakli. |
| **Financial Intelligence** | Berman & Knight (HBR Press) | Finans bilmeyen yoneticiler icin en iyi baslangic. |
| **Valuation** | McKinsey: Tim Koller (Wiley) | Degerlemenin "Incil"i. Profesyoneller icin. |
| **The Little Book of Valuation** | Aswath Damodaran (Wiley) | Degerlemenin en pratik, anlasilir anlatimi. |
| **Security Analysis** | Graham & Dodd (McGraw-Hill) | Deger yatirimciligi klasigi, 800 sayfa. |
| **Financial Modeling** | Simon Benninga (MIT Press) | Excel modelleme icin en kapsamli. |

### Yeni / Guncel Kaynaklar (2024-2025)

| Kitap | Yazar | Odak |
|---|---|---|
| **Advanced Financial Analysis** | Azhar ul Haque Sario (2025) | En guncel kapsamli finansal analiz kitabi. |
| **Pocketbook of Financial Statement Analysis** | B.D. Chatterjee (2025) | Pratik referans, DD check-listleri icerir. |
| **Warren Buffett and the Interpretation of Financial Statements** | M. Buffett & D. Clark | Buffett'in gozunden finansal tablo okuma. |

### Online Kaynaklar

| Platform | URL | Icindekiler |
|---|---|---|
| **Damodaran Online** | pages.stern.nyu.edu/~adamodar/ | Sektor verileri, ders notlari, spreadsheet'ler |
| **Aswath Damodaran YouTube** | youtube.com | DCF ve degerleme uzerine kapsamli dersler |
| **Corporate Finance Institute (CFI)** | corporatefinanceinstitute.com | Ucretsiz ve ucretli sertifika programlari |
| **Investopedia** | investopedia.com | Tanimlar, ornekler, rehberler |
| **McKinsey's Strategy & Corporate Finance** | mckinsey.com | Stratejik finans yazilari |
| **Harvard Business Review (HBR)** | hbr.org | Finansal yonetim makaleleri |
| **Mergers & Inquisitions** | mergersandinquisitions.com | Investment banking ve finansal modelleme |
| **Wall Street Prep** | wallstreetprep.com | Pratik finans egitimi (ucretli) |
| **Breaking Into Wall Street (BIWS)** | breakingintowallstreet.com | Kariyer odakli finans egitimi |

---

## 11. Vaka Calismalari

### 11.1 Enron Skandali (2001)

**Ozet:** Enron, 2001'de iflas eden ABD enerji devi. Piyasa degeri $60B'den sifira dustu.

**Kullanilan Manipulasyonlar:**
- **Mark-to-Market Muhasebesi:** Uzun vadeli sozlesmelerin bugunku degerini hemen gelir olarak kaydetti.
- **Bilanco Disi Araclar (SPE):** Borclari ozel amacli sirketlerde (Special Purpose Entities) sakladi, bilanco disi birakti.
- **Iliskili Taraf Islemleri:** CFO Andrew Fastow, sirket adina kendine ait sirketlerle islem yapti.

**Oran Analizinde Gorulebilecek Kirmizi Bayraklar (Retrospektif):**

| Metrik | Enron (2000) | Sektor Ortalamasi | Dikkat Cekici? |
|---|---|---|---|
| F/K (P/E) | ~60x | ~15x | Asiri pahali |
| Revenue growth | >%150 | <%20 | Base effect var mi? |
| Operating Cash Flow / Net Income | 0.3x | ~1.0x | Kar nakit yaratmiyor! |
| Debt/Equity (bilanco ici) | 1.2x | 1.0x | Normal gorunuyor — ama asil borc bilanco disi |

**Ders:** Operasyonel nakit akisi / net kar oranina dikkat edin. Bilanco disi riskleri sorgulayin. Yoneticilerin iliskili taraf islemlerini inceleyin.

### 11.2 Amazon'un Bilincli Kar Bastirmasi

**Ozet:** Amazon 1994-2003 arasi neredeyse sifir (veya negatif) net kar gosterdi. Ama sirketin degeri katlanarak artti.

**Strateji:**
- Amazon her kazandigi fazla dolar nakit i tekrar buyume yatirimina yonlendirdi (CapEx, Ar-Ge, lojistik)
- EBITDA ve FCF surekli pozitifti
- Amazon'un net kari degil, **Free Cash Flow / Hisse** metrigi onemliydi

| Yil | Net Kar | FCF | CapEx | FCF/Hisse (yillik degisim) |
|---|---|---|---|---|
| 2015 | $596M | $5.3B | $4.6B | - |
| 2018 | $10.1B | $19.4B | $12.4B | >2 kat artis |
| 2020 | $21.3B | $26.2B | $35.7B | Buyuk yatirim yili |
| 2023 | $30.4B | $36.2B | $48.5B | Yuksek CapEx'e ragmen FCF guclu |

**Dersler:**
- Buyume sirketlerinde net kara degil, FCF'ye ve yatirim harcamalarina bakmak gerekir
- "Amazon gibi olmak" istiyorsaniz, once yatirimlarinizin karsiligini ne zaman alacaginizi hesaplamalisiniz
- Amazon'un yatirim dongusu: altyapi harcamasi → olceklenme → marj iyilesmesi → FCF patlamasi

### 11.3 Turkcell Finansal Analizi (Turkiye Ornegi)

Turkcell, BIST'te islem goren en buyuk telekom sirketidir.

| Metrik | 2021 | 2022 (YK Enflasyon) | 2023 (YK Enflasyon) |
|---|---|---|---|
| Revenue (mTL) | 28.1B | 35.7B | 47.8B |
| EBITDA Margin | %44 | %42 | %41 |
| Net Kar (mTL) | 3.9B | 6.2B | 8.4B |
| FCF (mTL) | 2.1B | 3.8B | 5.5B |
| D/E | 0.6x | 0.5x | 0.4x |
| ROE | %28 | %25 | %22 |

**Turkcell Ozelinde Dikkat Edilmesi Gerekenler:**

1. **Enflasyon muhasebesi:** 2022'den itibaren uygulanan enflasyon muhasebesi nedeniyle finansallar onemli olcude degisti. Eski verilerle karsilastirma yaparken dikkatli olun.
2. **Kur riski:** Turkcell'in geliri TL, ancak ekipman yatirimlari ve borcunun bir kismi doviz cinsinden.
3. **Rezilyans:** Telekom sektoru, kriz donemlerinde nispeten istikrarlidir (insanlar iletisimden vazgeemez).
4. **Regulasyon riski:** BTK duzenlemeleri, lisans yenileme ucretleri, fiyat tavanlari.

**Analiz:** EBITDA marjlarinin %40+ seviyesi telekomda sektor standardina uygun. Azalan ROE, artan sermaye tabanindan kaynaklaniyor (base effect). D/E'nin 0.4x olmasi Finansal acidan guclu oldugunu gosteriyor.

### 11.4 Tesla Degerleme Tartismasi

**Ozet:** Tesla, 2020-2024 arasi piyasa degeri $50B ile $1.2T arasinda dalgalandi. Ayni sirket icin farkli analistler $100 ile $500 arasi hisse fiyati hedefi verdi.

**Varsayim Farkliliklarinin Degerlemeye Etkisi:**

| Varsayim | Iyimser Senaryo | Kotumser Senaryo |
|---|---|---|
| **2028 ARB (Arac Satisi)** | 20M arac/yil | 5M arac/yil |
| **Otonom Surus / Robotaxi** | $500B deger (basarili) | $0 (gerceklesmiyor) |
| **Otomotiv Brut Marj** | %30 (olceklenme) | %18 (rekabet baski) |
| **Terminal Buyume (g)** | %5 | %2 |
| **WACC** | %9 | %13 |
| **Implied Hisse Degeri** | **$500+** | **<$100** |

**Dersler:**
- DCF varsayimlari degistikce sirket degeri katlanarak degisir
- Tesla gibi "hikaye sirketleri" (story stocks) icin degerlemede DCF'den cok sektorel carpanlar ve nispi karsilastirma kullanilir
- Cok sayida analistin farkli deger bulmasi normaldir — onemli olan varsayimlari sorgulamak

**Pratik Kural:** Degerleme raporu okurken, once varsayimlara bakin (buyume orani, WACC, terminal buyume). Varsayimlar mantikli degilse, sonuc da mantikli degildir.

---

## 12. Pratik Alistirmalar

Bu bolum, ogrenilen konseptlerin pekistirilmesi icin 5 alistirma icerir.

### Alistirma 1: Gercek Bir Sirketin Oranlarini Hesaplama

1. KAP.gov.tr'den bir BIST sirketi secin (ornegin: THYAO, EREGL, FROTO)
2. Son yillik finansal tablolarini bulun
3. Asagidaki oranlari hesaplayin:
   - Cari Oran, Asit-Test Orani
   - Brut Marj, Faaliyet Marj, Net Marj
   - ROE, ROA, ROCE
   - Borc/Ozkaynak, ICR, Debt/EBITDA
   - DSO, DIO, DPO, CCC
   - FCF, FCF/EBITDA
4. Her bir oran icin "iyi / kotu / neter" diye yorum yazin

### Alistirma 2: BIST Sirketi 5 Yillik Trend Analizi

| Yil | Revenue | Brut Marj | EBITDA | Net Kar | FCF | D/E |
|---|---|---|---|---|---|---|
| 2020 | ? | ? | ? | ? | ? | ? |
| 2021 | ? | ? | ? | ? | ? | ? |
| 2022 | ? | ? | ? | ? | ? | ? |
| 2023 | ? | ? | ? | ? | ? | ? |
| 2024 | ? | ? | ? | ? | ? | ? |

- Revenue CAGR hesaplayin (5 yil)
- Her metrik icin en iyi ve en kotu yili belirleyin
- Hangi metriklerde duzgun bir trend var? Hangileri daginik?
- Sirketin stratejik donemlerini (buyume, karlilik, borc azaltma) trende yansitin

### Alistirma 3: Excel'de Basit DCF Modeli

1. Bir sirket icin 5 yillik projeksiyon yapin:
   - Revenue buyumesi (varsayim)
   - EBITDA marji (varsayim)
   - CapEx / Gelir orani (varsayim)
   - Calisma sermayesi degisimi (varsayim)
   - WACC (son 3 yillik getirilere gore)
2. Terminal Degeri = EBITDA_5 x Terminal Carpan
3. Firma Degerini ve hisse degerini hesaplayin
4. Duyarlilik analizi yapin: WACC, buyume, marj degisince ne oluyor?

**Ipuclari:**
- WACC hesaplamasi: ozkaynak maliyeti (CAPM) + borc maliyeti agirlikli
- Terminal buyume oranini fazla kullanmayin (TL bazli %2-4 makul)
- Modeli carpraz kontrol edin: cikan deger carpanlarla uyumlu mu?

### Alistirma 4: Benchmarking Tablosu

3 sirket belirleyin (sektor icinde rakip) ve 10 oran uzerinden karsilastirin:

| Oran | Sirket A | Sirket B | Sirket C | Sektor Medyan |
|---|---|---|---|---|
| Brut Marj | | | | |
| EBITDA Marj | | | | |
| Net Marj | | | | |
| ROE | | | | |
| Cari Oran | | | | |
| D/E | | | | |
| DSO | | | | |
| Revenue Buyume (YoY) | | | | |
| FCF/Revenue | | | | |
| EV/EBITDA | | | | |

**Cikarim:** Hangi sirket en iyi gorunuyor? Hangi oranlarda lider? Sirket B'nin nerede duzeltme yapmasi gerekir?

### Alistirma 5: Kirmizi Bayrak Tespiti

Asagidaki senaryoda kirmizi bayraklari bulun:

> ABC Tekstil A.S. (BIST kodu: ABCT) 5 yillik finansal verileri:
> - Revenue 2020: 100M TL → 2024: 300M TL (CAGR %31)
> - Net Kar 2020: 8M TL → 2024: 45M TL (CAGR %54)
> - Isletme Nakit Akisi 2020: 5M TL → 2024: -10M TL
> - DSO 2020: 45 gun → 2024: 85 gun
> - 2023'te Amortisman yontemi degisti (dogrusaldan azalan bakiyeye)
> - 2024'te YK son karariyla serefiye dususu yapildi (5M TL)
> - En buyuk musteri: ABC Tekstil gelirinin %62'sini tek bir musteri olusturuyor
> - Yonetim kurulu baskaninin esine ait bir sirkete 2024'te 12M TL danismanlik odenmis

**Aranan:** En az 5 kirmizi bayrak tespit edin ve her biri icin "neden sorunlu" aciklamasi yazin.

---

## 13. Turkiye'de Finansal Analiz

### 13.1 Veri Kaynaklari

**Resmi Kaynaklar:**

| Kaynak | URL | Icerik |
|---|---|---|
| **Kamuyu Aydinlatma Platformu (KAP)** | kap.gov.tr | Tum BIST sirketlerinin finansal tablolari, ozet dokumlari, bagimsiz denetim raporlari |
| **Merkezi Kayit Kurulusu (MKK)** | mkk.com.tr | Yatirimci bilgileri, portfoy verisi |
| **TCMB Elektronik Veri Dagitim Sistemi** | evds.tcmb.gov.tr | Makroekonomik veri, sektor istatistikleri |
| **SPK (Sermaye Piyasasi Kurulu)** | spk.gov.tr | Duzenlemeler, haftalik bultenler |
| **BIST (Borsa Istanbul)** | borsaistanbul.com | Pay piyasasi, borclanma araclari verisi |

**Ticari / Ucretli Kaynaklar:**

| Kaynak | Kullanim | Fiyat |
|---|---|---|
| **Finnet** | Sirket finansallari, oran analizi, karsilastirma | Ucretli (kurumsal/ bireysel) |
| **Matriks** | Canli BIST verisi, teknik analiz, derinlik | Ucretli |
| **Is Yatirim** | Arastirma raporlari, sektor analizleri | Musterilere ucretsiz |
| **Garanti BBVA Yatirim** | Aracilik arastirma raporlari | Musterilere ucretsiz |
| **Yatirim Finansman** | Finansal model, sektor raporlari | Musterilere ucretsiz |
| **Rasyonet** | Temel analiz platformu | Ucretli |
| **Foreks** | Gercek zamanli veri | Ucretli |

### 13.2 Turkiye Muhasebe Standartlari (TMS / TFRS)

Turkiye'deki sirketler icin iki temel standart seti vardir:

- **TFRS (Turkiye Finansal Raporlama Standartlari)**: UFRS (IFRS) ile neredeyse birebir uyumlu, BIST sirketleri icin zorunlu
- **TMS (Turkiye Muhasebe Standartlari)**: TFRS'nin temelini olusturan muhasebe standartlari
- **BOBI (Buyuk ve Orta Buyuklukte Isletmeler)**: Kucuk ve orta olcekli isletmeler icin alternative, daha sade standart

**UFRS ve TFRS Arasindaki Farklar:**

| Fark | UFRS | TFRS (Turkiye) |
|---|---|---|
| **Ertelenmis Vergi** | Genelde fark yok | Enflasyon muhasebesinden kaynaklanan farklilik |
| **Serefiye** | Impairment only | Ayni |
| **Enflasyon Muhasebesi** | IAS 29 — hiperenflasyon | YoY %100+ enflasyon nedeniyle zorunlu (2022 sonrası) |
| **Kira Muhasebesi (TFRS 16)** | Tum kiralamalar bilanco ici | Birebir ayni |
| **Hasiat Kaydi (TFRS 15)** | 5 adimli model | Birebir ayni |

### 13.3 Enflasyon Muhasebesi ve Finansal Analize Etkisi

**Turkiye'de Enflasyon Muhasebesi (IAS 29 Uygulamasi):**

Turkiye'de 2022'den itibaren enflasyon muhasebesi uygulamasi zorunlu hale gelmistir. Bunun finansal analize etkileri buyuktur:

| Etki Alanı | Enflasyon Muh. Once | Enflasyon Muh. Sonra |
|---|---|---|
| **Satis Geliri** | Nominal TL | Enflasyonla duzeltilmis |
| **Maddi Duran Varlik** | Tarihi maliyet | Yeniden degerleme |
| **Amortisman** | Tarihi maliyet uzerinden | Duzeltilmis varlik degeri uzerinden |
| **Ozkaynak** | Kucumsenmis (historical) | Enflasyon duzeltmesiyle daha gercekci |
| **Net Kar** | Enflasyon nedeniyle sisirilmis | Daha gercekci (bazen dusuk) |
| **ROE** | Yapay olarak yuksek | Daha gercekci |

**Onemli Uyarilar:**

1. **Eski vs Yeni Veri Karsilastirmasi:** 2022 oncesi ve sonrasi verileri karsilastirirken yontem farkini dikkate alin.
2. **Parasal Olmayan Varliklar:** Enflasyon duzeltmesinde parasal olmayan varliklara (stok, duran varlik) enflasyon endeksi uygulanir.
3. **Parasal Varliklar (Nakit, Alacak, Borc):** Enflasyon duzeltmesi uygulanmaz — bunlar zaten nominal deger uzerindendir.
4. **Duzeltilmis Finansallara Gecis:** BIST sirketlerinin 2022 ve 2023 finansallari 2024'te yeniden duzenlenmisti. Gecmise donuk metrikleri hesaplarken **duzeltilmis verileri** kullanin.

### 13.4 Turk Lirasi Volatilitesi ve Kur Analizi

Turkiye'de finansal analiz yaparken doviz dinamiklerini anlamak kritiktir:

**Kur Riskini Anlama Adimlari:**

1. **Fonksiyonel Para Birimi:** Sirket hangi para biriminde raporluyor? Cogu BIST sirketi TL raporluyor.
2. **Doviz Pozisyonu:** Sirketin doviz cinsinden varliklari eksi doviz cinsinden borclari = Net Doviz Pozisyonu
   - Negatifse (borclar > varliklar): TL deger kaybederse borc yukleri artar (zarar)
   - Pozitifse: TL deger kaybinden kar ederler (ihracatcilar gibi)
3. **Kur Hassasiyeti:** %10 TL deger kaybinda net kar ne kadar degisir? (Duyarlilik analizi)
4. **Doviz Cinsinden Borc / Toplam Borc:** Oran ne kadar yuksekse, kur riski o kadar fazla

**Ornek Hesaplama:**

```
Sirket'in Net Doviz Pozisyonu = $50M (borc fazlasi, negatif)
$1 = 20 TL → $50M = 1.000M TL
$1 = 30 TL (+%50) → $50M = 1.500M TL → Kur Zarari = 500M TL
```

**Turkiye'ye Ozel Doviz Stratejileri:**

- **Dogal Hedge:** Gelirleri doviz olan sirketler (ihracatcilar) kur riskine dogal olarak korunur
- **Financial Hedge:** Forward, swap, opsiyon ile korunma
- **Operasyonel Hedge:** Yurtdisi gelirleri ve yurtdisi maliyetleri eslestirmek

### 13.5 Turkiye'de Sektor Analizi Ipuclari

| Sektor | Odak Metrikler | Risk Faktorleri |
|---|---|---|
| **Banka** | Takipteki krediler (NPL), sermaye yeterlilik (CAR), net faiz marji (NIM) | Faiz politikasi, regulasyon, kredi riski |
| **Perakende** | Stok devir, brut marj, metrekare basina satis | Tuketici guveni, online rekabet |
| **Insaat / GYO** | DSO, net borc / ozkaynak, doviz pozisyonu | Faiz oranlari, konut fiyat endeksi |
| **Teknoloji** | F/K, revenue buyumesi, FCF marji, AR-GE / Satis | Yetenek kaybi, rekabet, yatirim dongusu |
| **Enerji** | EBITDA marji, borcluluk, CapEx planlari | Kur, emtia fiyatlari, regulasyon |
| **Gida / Icecek** | Brut marj, stok devir, marka degistirme maliyeti | Enflasyon, hammadde maliyeti, mevsimsellik |
| **Uretim / Sanayi** | Kapasite kullanimi, stok/satis orani, doviz pozisyonu | Emtia fiyatlari, dis talep, kuresel arz zinciri |

---

## Ek: Hatirlatma Tablosu — Temel Finansal Oranlar

| Oran Kategorisi | Oran Adi | Formul | Saglikli Aralik |
|---|---|---|---|
| **Likidite** | Cari Oran | DV / KVY | 1.5x - 2.5x |
| **Likidite** | Asit-Test | (DV - Stok) / KVY | 0.8x - 1.5x |
| **Karlilik** | Brut Marj | (Rev - COGS) / Rev | Sektore gore |
| **Karlilik** | EBITDA Marj | EBITDA / Rev | Sektore gore |
| **Karlilik** | Net Marj | Net Kar / Rev | Sektore gore |
| **Karlilik** | ROE | Net Kar / Ozkaynak | >%15 |
| **Kaldirac** | D/E | Toplam Borc / Ozkaynak | <2.0x |
| **Kaldirac** | ICR | EBIT / Faiz | >3.0x |
| **Kaldirac** | Debt/EBITDA | Net Borc / EBITDA | <3.0x |
| **Verimlilik** | Varlik Devir | Satis / Varlik | Sektore gore |
| **Verimlilik** | DSO | (Tic.Alacak / Satis) x 365 | Sektore gore |
| **Verimlilik** | CCC | DIO + DSO - DPO | Mumkunse dusuk |
| **Degerleme** | F/K (P/E) | Fiyat / EPS | Sektore gore |
| **Degerleme** | EV/EBITDA | Firma Degeri / EBITDA | Sektore gore |
| **Degerleme** | FD/Satis | Piyasa Degeri / Satis | Sektore gore |

---

*Bu dokuman, "Research & Analysis" modulunun Finansal Analiz bolumudur. Excel uygulamalari ve Python ornekleri ayri calisma dosyalarinda verilecektir. Ornek alistirmalar icin KAP.gov.tr uzerinde bir BIST sirketi secilerek calisma yapilmasi onerilir.*
