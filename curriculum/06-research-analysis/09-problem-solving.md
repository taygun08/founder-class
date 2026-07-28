# 9. Problem Solving Frameworkleri

## 9.1 Giris

Problem solving, is dunyasinin en temel becerisidir. Bu modul, McKinsey, BCG, Bain gibi danismanlik firmalarinin kullandigi problem cozme yaklasimlarindan, root cause analysis ve first principles thinking'e kadar genis bir framework yelpazesini kapsar.

## 9.2 McKinsey Problem Cozme Metodolojisi

### McKinsey'in 7 Adim Problem Cozme (Seven-Step Method)

McKinsey'in en bilinen problem cozme cercevesi:

1. **Problemi Tanimla (Define the Problem)**:
   - Problemi tek bir cumleyle ifade et
   - Cozum icermesin, sadece problemi tanimla
   - Ornek: "Kullanici sayimiz 6 aydir artmiyor" (cozum degil)

2. **Problemi Yapilandir (Structure the Problem)**:
   - MECE prensibi ile alt problemlere ayir
   - Issue tree olustur
   - Hangi alt problemlerin en onemli oldugunu belirle (80/20)

3. **Onceliklendir (Prioritize)**:
   - Hangi alt problemler en buyuk etkiye sahip?
   - 80/20 kurali: %20'si %80 etkiyi yaratir
   - "Olmazsa olmaz" vs "olsa iyi olur" ayrimi yap

4. **Analiz ve Veri Toplama (Analyze & Gather Data)**:
   - Her alt problem icin hipotez olustur
   - Hipotezi test edecek veriyi topla
   - Analizi tamamla

5. **Sentez Yap (Synthesize Findings)**:
   - Veriden anlamli icegoruler cikar
   - Butunsel bir hikaye olustur
   - "So what?" testi: Bu bulgu neden onemli?

6. **Tavsiye Gelistir (Develop Recommendations)**:
   - Bulgulara dayali somut aksiyon onerileri
   - Her oneri icin: ne, kim, ne zaman, nasil?

7. **Sun ve Hayata Gecir (Present & Implement)**:
   - Etkili bir anlati ile sun
   - Paydaslardan geri bildirim al
   - Uygulama plani olustur

### Minto Pyramid Principle (Barbara Minto)

McKinsey'in efsanevi iletisim cercevesi:

```
                    [Ana Tavsiye]
                   /     |      \
          [Destek 1] [Destek 2] [Destek 3]
           /    \      /   \      /   \
         [Veri] [Veri] [Veri] [Veri] [Veri] [Veri]
```

- **Mantik**: Yukaridan asagi: once sonuc, sonra destek
- **Yatay iliski**: Destekler birbirini kapsamaz (MECE)
- **Dikey iliski**: Her seviye bir usttekinin cevabini verir

### McKinsey MECE Prensibi

**Mutually Exclusive, Collectively Exhaustive**
- Birbiriyle ortusmez, birlikte butunu olusturur

Klasik MECE formulu ornekleri:
```
Kar = Gelir - Gider
Gelir = Fiyat x Adet
Gider = Sabit + Degisken
```

```
Musteriler = Yeni + Tekrar gelen
Yeni = Organic + Paid + Referral
Tekrar = Weekly + Monthly + Quarterly
```

**MECE Ihlali Ornegi:**
```
Musteriler = Gencler + Yaslilar + Orta Yaslilar  ✓ (yas araliklari ortusmuyorsa)
Musteriler = Zenginler + Gencler + Kobi calisanlari ✗ (ortusuyor)
```

### Issue Tree (Konu Agaci) Turleri

1. **Deduktif Agac (Hypothesis Tree)**:
   - Bir hipotezle basla, onu destekleyen sartlari ayir
   - Kullanimi: Hipotezin dogru olup olmadigini test ederken

2. **Induktif Agac (Diagnostic Tree)**:
   - Problemle basla, olasili nedenlere ayir
   - Kullanimi: "SATISLAR NEDEN DUSTU?" sorusunu cozumlerken

3. **Karar Agaci**:
   - Alternatifler ve sonuclar
   - Kullanimi: "HANGI STRATEJIYI SECMELIYIZ?" sorusu icin

## 9.3 BCG Problem Cozme Yaklasimi

BCG, McKinsey'den farkli olarak:

- **Hipotez odakli (Hypothesis-Driven)**: Once hipotez olustur, sonra test et
- **Strategy Palette**: Farkli ortamlar icin farkli stratejiler (Reeves, BCG)
- **Time-Based Competition**: Hiz bir rekabet avantaji olarak
- **Growth-Share Matrix**: Portfolyo analizi icin klasik matrix
- **Experience Curve**: Birim maliyetler kumulatif uretimle dusuyor

### BCG Strategy Palette (Martin Reeves)

| Ortam Tipi | Strateji | Ne Zaman Kullanilir? |
|---|---|---|
| **Classical** | Analiz et, planla, uygula | Ongorulebilir, degismeyen |
| **Adaptive** | Dene, sec, olceklendir | Belirsiz ama sekillendirilemez |
| **Shaping** | Vizyon yapilandir, birlikte olustur | Belirsiz ve sekillendirilebilir |
| **Renewal** | Erken uyar, hayatta kal, yenilen | Kriz ortami |

**Uygulama**: "Hangi ortamda oldugumuzu anlamak, hangi problem cozme yontemini kullanacagimizi belirler."

## 9.4 Root Cause Analysis (Kok Neden Analizi)

### 5 Whys (5 Neden)

Taiichi Ohno (Toyota) tarafindan gelistirilen basit ama guclu teknik.

**Ornek: Makine durdu**
1. Neden makine durdu? -> Sigorta atti
2. Neden sigorta atti? -> Asiri yuklenme
3. Neden asiri yuklenme? -> Rulman yagsiz
4. Neden rulman yagsiz? -> Pompa yeterli yag gondermiyor
5. Neden pompa yag gondermiyor? -> Pompa mili asinmis

**Gercek neden: Pompa milinin degisim zamani gelmis ve bakim yapilmamis.**

### 5 Whys Best Practices
- Gercekten kok nedene inene kadar devam et (bir kural yok, 3-7 olabilir)
- "Insan hatasi"nda durma — daha derin sistemik neden var
- Bir ekip ile yap, tek kisiyle degil
- Veriye dayandir, sadece tahminle calisma
- Her "neden"in cevabi gozlemlenebilir bir gercege dayanmali

### Ishikawa (Fishbone) Diagrami

6 ana neden kategorisi (6M):
- **Man (Insan)**: Yetenek, egitim, motivasyon
- **Machine (Makina)**: Ekipman, bakim, teknoloji
- **Method (Yontem)**: Proses, prosedur, standardizasyon
- **Material (Malzeme)**: Hammadde, kalite, tedarik
- **Measurement (Olcum)**: Veri, metrik, kalibrasyon
- **Mother Nature (Cevre)**: Ortam, kultur, duzenlemeler

**Hizmet sektoru uyarlamasi (8P)**:
- Product, Price, Place, Promotion, People, Process, Physical Evidence, Productivity

**Kullanim adimlari:**
1. Balik kafasina problemi yaz
2. 6 ana kategoriyi omurgaya ekle
3. Beyin firtinasi ile her kategoriye nedenler ekle
4. En olası kok nedenleri sec
5. Secilen nedenleri dogrula (veri ile)

### Kok Neden Analizi Yaklasimlarinin Karsilastirmasi

| Yontem | En Uygun Oldugu Durum | Siniri |
|---|---|---|
| 5 Whys | Basit, dogrusal problemler | Karmasik, cok nedenli problemlerde yetersiz |
| Fishbone | Ekip bazli, kategorik analiz | Nedenler arasi iliskileri gostermez |
| FTA | Karmasik sistemlerde hata agaci | Uzmanlik gerektirir, zaman alici |
| Pareto | "Az sayida neden, cogu sonuc" | Sadece sikliga dayanir, nedenselligi vermez |
| DMAIC | Alt Sigma projelerinde butunsel | Sadece buyuk projeler icin pratik |

## 9.5 First Principles Thinking (Ilk Prensipler)

Elon Musk'in en bilindik problem cozme yaklasimi.

### Nasil Calisir?

1. **Mevcut varsayimlari tanimla**: Herkesin kabul ettigi seyler
2. **Varsayimlari parcala**: "Bunu neden boyle kabul ediyoruz?"
3. **Ilk prensiplere in**: Fiziksel olarak dogru olan en temel gercekler
4. **Yeniden insa**: Ilk prensiplerden yeni bir cozum olustur

**Elon Musk Ornegi - Roket Maliyeti:**
- Varsayim: "Roket firlatmak cok pahalidir, $60M+"
- Parcala: "Neyden olusuyor? Aluminyum alasimi, bakir, titanyum..."
- Ilk prensip: "Aluminyum 60kg = $2/kg, diger metaller..."
- Yeniden insa: "Kendimiz yaparsak maliyet $2M olabilir" (SpaceX)

### Is Dunyasinda First Principles

**Amazon Orneginde:**
- Varsayim: "Online alisveris fiziksel magazalardan daha pahali"
- Parcala: "Bir kitabin maliyeti nelerden olusuyor?"
- Ilk prensip: "Kira + yayinevi marji + fiziksel dagitim + perakende marji"
- Yeniden insa: "Dagitim merkezinden dogrudan musteriye = %40 daha ucuz"

**First principles vs Analogy:**
- **Analogy**: "Amazon gibi yapalim" (taklit)
- **First principles**: "Bir kitabin gercek maliyet bilesenleri neler?" (yeniden kesif)

## 9.6 En Iyi Kaynaklar

### Kitaplar
1. **"The McKinsey Way"** - Ethan Rasiel (McGraw-Hill, 1999) — McKinsey kultur ve yontemleri
2. **"The McKinsey Mind"** - Ethan Rasiel (McGraw-Hill, 2001) — Detayli problem cozme adimlari
3. **"Case Interview Secrets"** - Victor Cheng (Innovation Press, 2012) — Vaka gorusmesi ve problem cozme
4. **"The Pyramid Principle"** - Barbara Minto (Financial Times, 2010) — McKinsey iletisim metodolojisi
5. **"Cracked It!"** - Bernard Garrette, Corey Phelps, Olivier Sibory (Palgrave, 2018) — Akademik problem cozme kitabi
6. **"Bulletproof Problem Solving"** - Charles Conn & Robert McLean (Wiley, 2019) — McKinsey partnerlerinden problem cozme
7. **"The Lean Startup"** - Eric Ries (Crown, 2011) — Hipotez testi ve problem cozme
8. **"Think Again"** - Adam Grant (Viking, 2021) — Yeniden dusunme ve varsayimlari sorgulama
9. **"Beyond the Five Whys"** - James Paterson (Wiley, 2024) — Root cause analysis ve systems thinking

### Online Kaynaklar
- **Crafting Cases** (craftingcases.com): Danismanlik vakalari ve cozumleri
- **Preplounge** (preplounge.com): Vaka gorusmesi pratikleri
- **Strategy U** (strategyu.co): Ucretsiz danismanlik egitimi
- **McKinsey Insights**: Gercek vaka calismalari ve problem cozme icgöruleri

## 9.7 Vaka Calismalari

### Vaka 1: McKinsey ve Bater Petrol Kuyulari
McKinsey'e bir petrol sirketi danisiyor: "Bazı kuyularimizdan petrol cikmazken bazılarindan cikiyor. Nedenini bulun." Geleneksel muhendislik yaklasimiyle bu soruya cevap verilemiyor.

McKinsey ekibi MECE hipotez agaci olusturuyor:
```
Petrol cikmiyor mu?
├── Jeolojik nedenler
│   ├── Kaya gecirgenligi
│   ├── Basinç seviyesi
│   └── Petrol miktari
├── Operasyonel nedenler
│   ├── Pompa kalitesi
│   ├── Bakim seviyesi
│   └── Yontem farkliligi
└── Organizasyonel nedenler (sürpriz!)
    ├── Kuyu basi ekipleri farkli prosedurler uyguluyor
    └── Iyi performans gosteren kuyular ayni ekibe ait
```

Sonuc: Problem teknik degil, organizasyoneldi.

### Vaka 2: SpaceX ve First Principles
SpaceX'in roket maliyetlerini dusurmek icin first principles kullanimi:
- Geleneksel cozum: "Ucuz roket tedarikcisi bul"
- First principles: "Roket nelerden olusur? Aluminyum, bakir, titanyum..."
- Maliyet: Piyasada $60M olan roket, SpaceX'te $2M
- Sonuc: Ticarî uzay endustrisinin yeniden sekillenmesi

## 9.8 Pratik Alistirmalar

### Alistirma 1: MECE Issue Tree Olusturma
Asagidaki problemler icin birer issue tree cizin:
- "Restoran zincirimizin yillik karliligi 2 yildir dusuyor"
- "E-ticaret sitemizde sepet terk orani %70"
- "Calisan memnuniyeti anket sonuclarimiz sektör ortalamasinin altinda"

### Alistirma 2: 5 Whys Uygulamasi
Gunluk hayatinizda bir problemi secin ve 5 Whys uygulayin:
- Telefon sarji neden cabuk bitiyor?
- Neden ise hep geç kaliyorsunuz?
- Neden projeleriniz hep son gune yetisiyor?

### Alistirma 3: First Principles Egzersizi
"Bir pizzaci acmak istiyorsunuz" problemi icin:
- Endustrideki varsayimlar neler? (iyi lokasyon, firin, usta...)
- Hangi varsayimlar sorgulanabilir?
- Ilk prensipler neler?
- Ilk prensiplerden yeni bir is modeli kurabilir misiniz?

### Alistirma 4: Minto Pyramid
Sonucu: "Marketing butcemizi %20 artirmaliyiz" olan bir tartisma yazin. Bu sonucu destekleyen 3 ana arguman ve her biri icin 2 destek verisi ile bir Minto Piramidi olusturun.

### Alistirma 5: Kosullu Problem Cozme
Bir sirketde calistiginizi dusunun. Asagidaki durumlarin her biri icin BCG Strategy Palette'den hangi yaklasimi kullanirdiniz? Neden?
- Sirketiniz regule bir endustride (bankacilik)
- Yeni bir pazar (metaverse)
- Sirketiniz iflasin esiginde
- AI teknolojilerinde hizla degisen bir pazar

## 9.9 Turkiye'de Bu

### Danismanlik Kulturunun Durumu
- Turkiye'de McKinsey, BCG, Bain ofisleri mevcut ve en iyi universite mezunlarini cekiyor
- Yerli danismanlik firmalari (Yildiz, BTS, StratejiCo) da MECE ve issue tree kullaniyor
- KOBI'lerde problem cozme genellikle "tecrubeye dayali", yapisal degil
- Turkiye'de MBA programlari vaka calismasi ve problem cozme odakli

### Yerel Kaynaklar
- **"Stratejik Dusunce: Problem Cozme ve Karar Verme"** - Prof. Dr. M. Sait Kok (Beta Yayin)
- **Bilgi Universitesi - Danismanlik Kulubu**: Vaka gorusmesi egitimleri
- **Vaka Analizi Yarismalari**: Turkiye'deki universite yarismalari

### Turkiye'de Danismanlik Vakalari
- "BIST'teki bir perakende sirketi karliligini nasil artirir?" gibi yerel vakalar
- Turkiye'ye ozgu dinamikler: enflasyon muhasebesi, doviz kuru riski, duzenleyici ortam

---

**Baglantili Moduller:** [Karar Analizi](07-karar-analizi.md), [Elestirel Dusunce](08-elestirel-dusunce.md), [Stratejik Ongoru](10-stratejik-ongoru.md)
