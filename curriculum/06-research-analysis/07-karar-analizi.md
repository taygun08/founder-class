# 7. Karar Analizi

## 7.1 Giris

Is dunyasinda her gun belirsizlik altinda kararlar aliriz: "Bu urunu piyasaya surmeli miyiz?", "Fiyati ne kadar artirmaliyiz?", "Hangi pazara girmeliyiz?" Karar analizi, bu tur belirsizlikleri yonetmek icin kullanilan kantitatif ve kalitatif yontemler butunudur.

## 7.2 Karar Agaclari (Decision Trees)

### Temel Yapi
Karar agaci, bir karar problemi icin mumkun tum secenekleri ve sonuclarini gorsel olarak haritalar.

```
                                 [Karar]
                                /       \
                         [Secenek A]  [Secenek B]
                          /    \         /    \
                      [Iyi]  [Kotu]   [Iyi]  [Kotu]
                      p=0.6  p=0.4   p=0.3  p=0.7
                      +$10M  -$2M    +$20M  -$5M

         Expected Value (A) = 0.6*10 + 0.4*(-2) = $5.2M
         Expected Value (B) = 0.3*20 + 0.7*(-5) = $2.5M
         Karar: A secenegi
```

### Expected Value (Beklenen Deger) Hesabi

**Expected Monetary Value (EMV)** = Sum(olasilik x deger)

Ornek bir urun lansmani:
- Pazarda basarili olma olasiligi: %40
- Basarili olursa kar: $50M
- Basarisiz olursa kayip: $10M
- EMV = 0.40 x $50M + 0.60 x (-$10M) = $20M - $6M = **$14M**

Eger EMV pozitifse proje degerlendirmeye alinabilir, ancak bu sadece bir baslangic noktasidir.

### Karar Agaci Olusturma Adimlari

1. **Problemi tanimla**: Net bir karar sorusu belirle
2. **Alternatifleri belirle**: Mumkun tum secenekler
3. **Belirsizlikleri haritala**: Her secenegin altindaki olasilikli sonuclar
4. **Degerleri ata**: Her sonucun finansal (veya diger) degeri
5. **Olasiliklari ata**: Her belirsizlik icin gercekci olasiliklar (gorsel: ek bilgi topla)
6. **Geriye dogru hesapla**: En sagdan baslayip sola dogru expected value'lari hesapla
7. **Hassasiyet analizi yap**: Olasilik ve deger varsayimlarini test et

### Sinirlamalar
- Olasilik atamalari subjektiftir
- Karmasik problemlerde agac cok buyur
- Tek bir metrik (para) odagi, diger boyutlari ihmal edebilir
- Insan karar onceliklerini (risk tercihi) tam yansitmayabilir

## 7.3 Monte Carlo Simulasyonu

### Ne Ise Yarar?
Monte Carlo simulasyonu, belirsiz girdilere sahip bir modelin binlerce (hatta milyonlarca) kez calistirilarak, ciktilarin olasilik dagilimini olusturmasidir. John Von Neumann tarafindan Manhattan Projesi sirasinda gelistirilmistir.

### Calisma Prensibi

1. **Modeli kur**: Karar probleminin matematiksel modeli (orn: NPV = Cash Flow / (1+r)^t)
2. **Belirsiz degiskenleri tanimla**: Her degisken icin bir olasilik dagilimi (normal, uniform, log-normal, ucgen, vb.)
3. **Binlerce kez simule et**: Her tekrarda, her degiskenden rastgele bir deger sec, sonucu hesapla
4. **Dagilimi analiz et**: Sonuclarin histogrami, ortalamasi, varyansi, Value-at-Risk (VaR) gibi metrikleri

### Excel'de Monte Carlo (Basit Ornek)

Bir yatirim getirisini modellemek icin:

```
1. Adim: Varsayimlar
   - Pazar buyuklugu: 50M +/- 10M (ucgen dagilim)
   - Pazar payi: %10 +/- %5 (normal dagilim)
   - Kar marji: %20 +/- %3 (normal dagilim)

2. Adim: Formul
   Gelir = Pazar_Buyuklugu * Pazar_Payi
   Kar = Gelir * Kar_Marji

3. Adim: 10,000 simulasvon (Excel'de Data Table ile)
4. Adim: Sonuclar histogrami
```

### Gercek Dunya Uygulamalari
- **Enerji sektoru**: Petrol fiyati ve rezerv belirsizliginde yatirim kararlari
- **Ilac Ar-Ge**: Klinik deney basari olasiligi ve gelir potansiyeli modellemesi
- **Insaat projeleri**: Butce ve zaman asimi riskleri
- **Gemi insasi**: Bir calismada Monte Carlo tabanli yaklasimin beklenen NPV'yi %18.6 artirdigi ve varyansi %23 azalttigi gosterilmistir

### Python'da Basit Monte Carlo

```python
import numpy as np
import matplotlib.pyplot as plt

n_simulations = 10000
market_size = np.random.triangular(40, 50, 60, n_simulations)  # Milyon $
market_share = np.random.normal(0.10, 0.03, n_simulations)
profit_margin = np.random.normal(0.20, 0.03, n_simulations)

revenue = market_size * market_share * 1e6  # $
profit = revenue * profit_margin

# Value at Risk (%5)
var_95 = np.percentile(profit, 5)
print(f"Beklenen kar: ${profit.mean():,.0f}")
print(f"%95 VaR: ${var_95:,.0f}")  # %5 ihtimalle bu degerin altinda
```

## 7.4 Hassasiyet Analizi (Sensitivity Analysis)

### Ne Ise Yarar?
"Sonuc, hangi degiskendeki degisimden en cok etkileniyor?" sorusunu cevaplar. Bu sayede hangi bilgiyi daha kesinlestirmeniz gerektigini bilirsiniz.

### Turleri

1. **One-Way Sensitivity**: Bir degiskeni degistirirken digerlerini sabit tutmak
   - "Fiyat %10 artarsa NPV ne olur?"
   - "Musteri kazanma maliyeti %20 artarsa ne olur?"

2. **Two-Way Sensitivity**: Iki degiskeni ayni anda degistirirken bir heatmap olusturmak
   - Fiyat x Satis Hacmi matrixi: her hucrede kar

3. **Tornado Diagram**: Tum degiskenlerin etkisini tek bir gorselde gostermek
   - En genis cubuktan en dara: hangi degisken en cok etkiliyor?

### Tornado Diagram Ornegi

```
                NPV (Baz: $10M)
Pazar Buyuklugu |========         |  $5M - $15M
Kar Marj        |======           |  $7M - $13M
Pazar Payi      |====             |  $8M - $12M
Indirim Orani   |=                |  $9M - $11M
```

## 7.5 Bayes Karar Analizi

### Olasiliklari Guncelleme
Bayes teoremi, yeni bilgi geldikce olasiliklari nasil guncelleyecegimizi gosterir.

**Is dunyasi uygulamasi:**
- Bir musteri segmentinin %10'unun churn riski altinda oldugunu dusunuyordunuz (prior)
- AI modeliniz, bir musterinin churn yapacagini %80 dogrulukla tahmin ediyor (likelihood)
- Test pozitif cikan bir musteri icin guncel churn olasiligi: **posterior = %31** (Bayes ile hesaplanir)

Bu, kararlarinizi "sezgi" yerine sistematik olasilik guncellemeyle vermenizi saglar.

## 7.6 Karar Verme Tuzaklari

- **Overconfidence (Asiri Guven)**: Olasiliklari gercekte oldugundan daha kesin gorme. Cozum: referans sinif tahmini
- **Anchoring (Capa Etkisi)**: Ilk duyulan bilgiye asiri baglanma. Cozum: once base rate, sonra detay
- **Confirmation Bias (Dogrulama Yanliligi)**: Kendi onyarginizi destekleyen verileri agirliklandirma. Cozum: "premortem" tekniGi
- **Sunk Cost (Batik Maliyet)**: Gecmis harcamalari telafi etmek icin mantiksiz kararlar. Cozum: sadece gelecege bak
- **Groupthink**: Ekip icinde fikir birligi uzerinde asiri baski. Cozum: "red team" atamasi, oncelikle sessizlik

## 7.7 En Iyi Kaynaklar

### Kitaplar
1. **"Decision Quality"** - Carl Spetzler, Hannah Winter, Jennifer Meyer (Wiley, 2016) — Karar analizinin en kapsamli kaynagi, Strategic Decisions Group metodolojisi
2. **"Thinking in Bets"** - Annie Duke (Portfolio, 2018) — Poker profesyonelinden karar verme dersleri
3. **"The Flaw of Averages"** - Sam Savage (Wiley, 2012) — Ortalamalarin neden yaniltici oldugu ve Monte Carlo'nun onemi
4. **"How to Measure Anything"** - Douglas Hubbard (Wiley, 2014) — Belirsizlik altinda olcum sanati
5. **"Superforecasting"** - Philip Tetlock & Dan Gardner (Crown, 2015) — Forecasting ve olasiliksal dusunce
6. **"The Power of Experiments"** - Michael Luca & Max Bazerman (MIT Press, 2020) — Deney bazli karar verme

### Online Kaynaklar
- **Cornell eCornell - SHA574**: Modeling Uncertainty and Risk (Monte Carlo, expected utility)
- **Khan Academy - Probability**: Olasiliksal dusunce temelleri
- **McKinsey RTS**: McKinsey'in karar verme egitim programi
- **Palisade @Risk**: Excel icin Monte Carlo eklentisi
- **The Decision Lab** (thedecisionlab.com): Karar verme bilimi uzerine kapsamli kaynak

## 7.8 Vaka Calismalari

### Vaka 1: Netflix Karar Agaclari
Netflix, icerik yatirim kararlarinda karar agaclari ve Monte Carlo simulasyonu kullanir. Bir dizinin yapimina karar verirken:
- Talesi seviyesindeki izleyici sayisi
- Reyting ve kullanim olasiligi
- Devam ettirilme olasiligi
- Uluslararasi dagitim potansiyeli

Her degisken icin olasilik dagilimlari olusturulur ve 10.000+ simulasyonla NPV dagilimi hesaplanir.

### Vaka 2: Shell'in Senaryo Planlamasi
Shell, 1970'lerden beri Monte Carlo simulasyonu ve senaryo planlamasini birlestirerek buyuk olcekli enerji yatirim kararlari alir. Sirket, petrol fiyatlarinin 2020'de $30-$150 araliginda olabilecegini modellemis ve her senaryo icin portfolyo optimizasyonu yapmistir. Bu, Shell'in 2008 krizinde ve 2020 pandemi doneminde rakiplerine gore daha dayanikli olmasini saglamistir.

### Vaka 3: Amazon'un Expected Value Kultur
Jeff Bezos'un mektuplarinda sikca gecen "expected value" mantigi: "Amazon'da %70 olasilikla basarili olacagina inandigimiz bir projeyi onaylariz. %30 basarisizlik olasiligi kabul edilebilir cunku basarisizligin maliyeti sinirli, basarinin getirisi ise cok buyuk olabilir." Bu mentalite, Amazon'un AWS, Kindle, Alexa gibi yuksek riskli projelere yatirim yapmasini saglamistir.

## 7.9 Pratik Alistirmalar

### Alistirma 1: Karar Agaci Olusturma
Bir ilac sirketinin yeni bir ilaci icin Ar-Ge yatirim kararini degerlendirin:
- Klinik deney basari olasiligi: Evre 1'de %60, Evre 2'de %40, Evre 3'te %70
- Basarili olursa gelir: Yillik $500M (10 yil)
- Ar-Ge maliyeti: Her evre icin $50M
- Basarisizlikta ilac tamamen kaybedilir
- Karar: Hangi asamada devam edilmeli?

### Alistirma 2: Monte Carlo Modeli
Excel'de veya Python'da basit bir yatirim modeli kurun:
- Degisken 1: Pazar buyuklugu ($100M +/- %30)
- Degisken 2: Pazar payi (%5 +/- %2)
- Degisken 3: Fiyat ($10 +/- $2)
- Degisken 4: Degisken maliyet ($6 +/- $1)
- Sabit maliyet: $2M
- 10.000 simulasyon calistirin
- NPV dagilimini ve %95 VaR'yi hesaplayin

### Alistirma 3: Hassasiyet Analizi
Bir girisimin degerlemesini yaptiginizi dusunun. Asagidaki varsayimlarin hangisi en kritiktir? (Hassasiyet siralamasi yapin):
- Pazar buyume hizi: %10 +/- %5
- Pazar payi: %15 +/- %8
- Kar marji: %25 +/- %10
- Indirim orani: %15 +/- %3
- Customer churn: %5 +/- %2

### Alistirma 4: Bayes Guncellemesi
Bir ise alim surecinde adaylarin %30'unun uygun oldugunu biliyorsunuz. Testiniz, uygun adaylari %90 dogrulukla tespit ediyor, uygun olmayanlari ise %20 yanlis pozitifle eliyor. Testten gecen bir adayin gercekten uygun olma olasiligi nedir?

## 7.10 Turkiye'de Bu

### Karar Analizi Kulturunun Durumu
- Turkiye'de kucuk ve orta olcekli isletmelerde kararlar genellikle sezgiye ve "gobrek" (gut feeling)'e dayanir
- Buyuk sirketlerde ve danismanlik firmalarinda kantitatif yontemler daha yaygin
- Turkiye'de enflasyon ve doviz kuru belirsizligi, Monte Carlo simulasyonunu ozellikle degerli kilmaktadir
- Risk yonetimi (Basel III/IV cercevesi) bankacilik sektorunde zorunlu, diger sektorlerde henuz yaygin degil

### Yerel Uygulama Ornekleri
- BIST-30 sirketleri: Yatirim kararlarinda DCF ve senaryo analizi yaygin
- Gida perakende sektoru: Fiyatlama kararlarinda maliyet artisi ve talep belirsizligini modelleme
- E-ticaret: Envanter yonetimi icin talep tahmini ve Monte Carlo kullanimi

---

**Baglantili Moduller:** [Problem Solving](09-problem-solving.md), [Elestirel Dusunce](08-elestirel-dusunce.md), [Stratejik Ongoru](10-stratejik-ongoru.md)
