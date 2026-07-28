# 1. Arastirma Metodolojisi

## 1.1 Giris

Arastirma metodolojisi, bilgiye sistematik ve guvenilir yollardan ulasma sanatidir. Is dunyasinda bu, "veriye dayali karar alma"nin bilimsel temelidir. Herhangi bir iddiayi test etmekten, bir pazarlama kampanyasinin etkisini olcmeye kadar her sey bu prensiplere dayanir.

## 1.2 Bilimsel Yontemin Is Dunyasindaki Karsiligi

| Bilimsel Yontem Asamasi | Is Dunyasi Karsiligi |
|---|---|
| Gozlem | Pazar trendini veya musteri sikayetini fark etme |
| Soru sorma | "Bu kampanya neden ise yaramadi?" sorusu |
| Hipotez olusturma | "Fiyat artisi talebi %10 dusurdu" onermesi |
| Tahmin yapma | "Eger fiyati %5 artirirsak, marj %8 artar" |
| Test etme | A/B testi ile yeni fiyatin eskiye karsilastirilmasi |
| Analiz ve sonuc | Istatistiksel anlamlilik testi ile karar verme |

## 1.3 Hipotez Testi

### Temel Kavramlar
- **Null hipotez (H0)**: Varsayilan durum, degisiklik yok (ornegin: "yeni tasarim eski tasarimdan farkli degil")
- **Alternatif hipotez (H1)**: Bizim kanitlamak istedigimiz (ornegin: "yeni tasarim donusumu artirir")
- **p-value**: Null hipotezin dogru olmasi durumunda, bu veriyi (veya daha asiri bir sonucu) gorme olasiligi. p < 0.05 ise genelde "istatistiksel olarak anlamli" kabul edilir.
- **Tip I Hata**: Yanlis pozitif (gercekte fark yokken varmis gibi gorme)
- **Tip II Hata**: Yanlis negatif (gercekte fark varken kacirma)

### Pratik Is Dunyasi Uygulamasi
**Ornek:** Bir e-ticaret sirketi, yeni odeme sayfasi tasariminin donusumu artirip artirmadigini test etmek istiyor.

```
H0: Yeni tasarim donusumu degistirmemistir (donusum_eski = donusum_yeni)
H1: Yeni tasarim donusumu artirmistir (donusum_yeni > donusum_eski)

Orneklem: 10,000 kullanici rastgele 2 gruba ayrilir
Sonuc: Yeni tasarimda donusum %5.2 vs eski %4.8, p = 0.03
Karar: p < 0.05 oldugu icin H0 reddedilir, yeni tasarima gecilir
```

## 1.4 Deneysel Tasarim (Experimental Design)

### Randomize Kontrollu Deneyler (RCT)

Is dunyasinda RCT'lerin en yaygin formu **A/B testi**dir. Temel prensipler:

1. **Randomizasyon**: Denekler rastgele kontrol ve tedavi gruplarina atanir
2. **Kontrol grubu**: Degisiklik yapilmayan grup (base-line)
3. **Tedavi grubu**: Degisikligin uygulandigi grup
4. **Koruma**: Cift-kor calismalarda ne denek ne de arastirmaci hangi grupta oldugunu bilir

### A/B Testing Best Practices

- **Yeterli orneklem buyuklugu**: Power analysis ile onceden hesaplanmali
- **Coklu test duzeltmesi**: Birden fazla metrik test ediliyorsa Bonferroni veya FDR duzeltmesi yapilmali
- **Peeking problemi**: Test devam ederken surekli sonuc kontrol etmek Tip I hatayi inflate eder. Onceden bitis suresi belirlenmeli
- **Novelty effect**: Kullanicilar yeni seyi sever (veya sevmez) — test yeterli sure calistirilmali
- **Segmentasyon**: Genel sonuc anlamli degilken belirli segmentlerde anlamli olabilir

### A/B Testing Otesi: Modern Yaklasimlar

**Interleaving Deneyler** (Airbnb, 2025): Ayni kullaniciya iki farkli algoritmanin sonucunu ayni anda gosterip karsilastirma. Geleneksel A/B testine gore 50-100 kat hizlanma saglar.

**Multi-Armed Bandit (MAB)**: A/B testinde kaybeden kola %50 trafik gondermek yerine, algoritma kazanan kola daha fazla trafik vererek kaybi minimize eder. 2025'te gelistirilen doubly robust tahmin yontemleriyle kucuk orneklemlerde bile yuksek istatistiksel guc saglar.

## 1.5 Causal Inference (Nedensel Cikarim)

### Korelasyon != Nedensellik

Bu, veri analizinin en kritik aksiyomudur. Iki degisken arasinda korelasyon olmasi, birinin digerine neden oldugu anlamina gelmez. Ornek:
- Dondurma satisi ile bogulma vakalari arasinda korelasyon vardir. Sebep: ikisi de sicak hava ile iliskilidir.
- Yangin sayisi ile itfaiye araci sayisi arasinda korelasyon vardir. Sebep: ters nedensellik.

### Nedensel Cikarim Yontemleri

1. **Difference-in-Differences (DiD)**: Tedavi grubunun oncesi/sonrasi farki ile kontrol grubunun oncesi/sonrasi farkini karsilastirir. Ornek: Bir sehirde asgari ucret arttiginda istihdam degisimi — komsu sehir kontrol grubu olarak kullanilir.

2. **Regression Discontinuity (RDD)**: Bir esik degerin iki tarafindaki birimleri karsilastirir. Ornek: Sinavi 70 ile gecenlerle 69 ile kalanlar — puandaki kucuk fark nedeniyle birbirine cok benzerdirler, ama farkli muamele gorurler.

3. **Instrumental Variables (IV)**: Disaridan bir degisken (instrument) kullanarak nedensel etkiyi olcer. Ornek: Askerlik hizmetinin gelecekteki kazanc uzerindeki etkisi olculeceginde, dogum gununun random faktoru (Vietnam Savasi'nda lot to sistemi) instrument olarak kullanilir.

4. **Propensity Score Matching (PSM)**: Tedavi grubundaki her birime, kontrol grubunda en cok benzeyen birimi eslestirir. Ornek: Bir egitim programina katilanlarla katilmayanlar, demografik ozelliklerine gore birebir eslestirilir.

5. **Directed Acyclic Graphs (DAGs)**: Nedensel iliskileri gorsel bir grafik olarak modelleme. "Causal Inference for Data Science" (Manning, 2025) kitabinin temel yaklasimi.

## 1.6 En Iyi Kaynaklar

### Kitaplar
1. **"Causal Inference: The Mixtape"** - Scott Cunningham (Yale University Press, 2021) — Nedensel cikarima en pratik giris
2. **"Naked Statistics"** - Charles Wheelan (W.W. Norton, 2013) — Istatistigi anlasilir kilan en iyi populer kitap
3. **"The Book of Why"** - Judea Pearl & Dana Mackenzie (Basic Books, 2018) — Nedenselligin bilimsel temeli
4. **"Trustworthy Online Controlled Experiments"** - Kohavi, Tang, Xu (Cambridge, 2020) — A/B testinin kapsamli rehberi (Ron Kohavi, Microsoft'un A/B testing onculu)
5. **"Impact Evaluation in Firms and Organizations"** (MIT Press, 2025) — R ve Python ile uygulamali, sirket ici etki degerlendirme

### Online Kaynaklar
- **Khan Academy - Probability & Statistics**: Temel istatistik bilgisi
- **Coursera - Causal Inference** (Columbia University): Prof. Peng Ding'in dersi
- **Good Judgment Project**: Forecasting metodolojisi egitimi
- **Evan Miller's Blog** (evanmiller.org): A/B testi istatistikleri uzerine en iyi kaynak
- **Netflix Tech Blog - Experimentation**: Gercek dunya A/B testi vaka calismalari

## 1.7 Vaka Calismalari

### Vaka 1: Microsoft'un A/B Testing Altyapisi
Ron Kohavi onderliginde Microsoft, her yil binlerce A/B testi calistiran bir altyapi kurdu. Bing'de yapilan bir testte, reklam sayisi azaltildiginda gelirin dustugu goruldu (sezgilere aykiri). Yapilan analiz, reklam sayisindaki azalmanin kullanici deneyimini degil, azalan reklam envanterinin dogrudan etkisini yansittigini gosterdi.

### Vaka 2: Airbnb Ranking Algoritmalari
Airbnb (2025), geleneksel A/B testlerinin ranking degisikliklerinde yavas kaldigini gorunce interleaving deneyler gelistirdi. Bu yontemle degisikliklerin etkisi 50-100 kat daha hizli olculebilir hale geldi, ayni anda daha fazla deney calistirilmasina imkan taniyarak inovasyon hizini artirdi.

### Vaka 3: Amazon'un Pricing Testleri
Amazon surekli olarak fiyatlandirma A/B testleri yapar. Ancak musteri segmentasyonu yapmadan ortalama etkiye bakmak yerine, belirli segmentlerdeki (ornegin Prime uyeleri vs uye olmayanlar) etkiyi ayri ayri olcer. Bu sayede fiyat hassasiyeti yuksek ve dusuk gruplar icin farkli stratejiler gelistirir.

## 1.8 Pratik Alistirmalar

### Alistirma 1: A/B Testi Tasarimi
Bir e-ticaret sitesinde "sepete ekle" butonunun rengini degistirmek istiyorsunuz. Su parametreleri belirleyin:
- Null ve alternatif hipotez nedir?
- Hangi metrik(ler)i takip edeceksiniz?
- Kac kullaniciya ihtiyaciniz var? (Power = 0.80, alpha = 0.05, minimum detectable effect = %1)
- Test kac gun surmelidir? (novelty etkisini dusunun)
- Test bitmeden once ne zaman sonuc kontrol edeceksiniz?

### Alistirma 2: Korelasyon vs Nedensellik
Asagidaki iliskilerin her biri icin:
1) Korelasyonun nedeni neler olabilir?
2) Gizli ucuncu degisken ne olabilir?
3) Nedenselligi kesin olarak test etmek icin hangi yontemi kullanirdiniz?

- Sigara icmek ile akciger kanseri
- Egzersiz yapmak ile yasam suresi
- Reklam harcamalari ile satis geliri
- Calisan memnuniyeti ile sirket karliligi
- Egitim seviyesi ile gelir

### Alistirma 3: DAG Olusturma
Bir arkadaslik uygulamasi, premium uyeligi olan kullanicilarin daha fazla eslestirme aldigini fark ediyor. Ancak bu iliski dogrudan nedensel olmayabilir. Olasili nedenleri gosteren bir DAG (Directed Acyclic Graph) cizin.

## 1.9 Turkiye'de Bu

### Yerel Arastirma Kulturunun Ozellikleri
- Turkiye'de kurumsal sirketler A/B testi yapiyor ancak kucuk ve orta olcekli isletmelerde veriye dayali karar alma henuz yaygin degil
- Universite-sanayi isbirligi zayif, bu nedenle metodolojik bilgi akademiden is dunyasina yeterince akmamaktadir
- Anket ve pazar arastirmasi sirketleri (IPSOS, NielsenIQ, Kantar) Turkiye'de aktif, ancak deneysel tasarim nadiren kullanilir

### Yerel Kaynaklar
- **Turkiye Istatistik Kurumu (TUIK)**: Kamuya acik veri kaynaklari
- **Bilimsel Arastirma Yontemleri** - Prof. Dr. Sener Buyukozturk: Pegem Akademi
- **Istatistiksel Arastirma Yontemleri** - Prof. Dr. Irfan Erdogan: Turkiye'de en cok kullanilan arastirma metodolojisi kitaplarindan biri

---

**Baglantili Moduller:** [Pazar Arastirmasi](02-pazar-arastirmasi.md), [Quantitatif Arastirma](11-quantitatif-arastirma.md), [Karar Analizi](07-karar-analizi.md)
