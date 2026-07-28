# Veri Analizi (Data Analysis)

## 1. Giris

Veri analizi, gunumuz is dunyasinda rekabet avantaji elde etmenin temel taslarindan biridir. Sirketler her saniye musteri davranislari, satis trendleri, operasyonel metrikler ve finansal gostergeler hakkinda muazzam miktarda veri uretmektedir. Ancak ham veri basli basina bir anlam ifade etmez; onu anlamli icgoruye donusturecek analitik yaklasim gereklidir.

**Veri analizinin is kararlarindaki rolu:**

- **Kanita Dayali Karar Alma (Data-Driven Decision Making):** Sezgi ve gecmis deneyimlerin yaninda, verinin sagladigi objektif kanitlarla karar almak hata payini dusurur.
- **Trend ve Oruntu Kesfi:** Musteri davranislarindaki mevsimsel trendler, urun tercihlerindeki degisimler veya pazar dinamikleri gibi oruntuleri kesfetmek.
- **Optimizasyon:** Pazarlama butcelerinden tedarik zincirine kadar her alanda kaynaklarin en verimli sekilde kullanilmasi.
- **Tahmin ve Projeksiyon:** Gecmis veriye dayanarak gelecege yonelik tahminler yapmak (sales forecasting, demand planning).
- **Olcme ve Degerlendirme:** Kampanyalarin, stratejik insiyatiflerin ve operasyonel degisikliklerin etkisini olcmek.

**Veri Analizi Yontem Turleri:**

| Tur | Aciklama | Ornek |
|-----|----------|-------|
| **Descriptive (Tanimlayici)** | "Ne oldu?" sorusunu yanitlar | Gecen ayki satislarin ozeti |
| **Diagnostic (Teshis)** | "Neden oldu?" sorusunu yanitlar | Satis dustu, sebebi ne? |
| **Predictive (Tahmin Edici)** | "Ne olacak?" sorusunu yanitlar | Gelecek ay satis tahmini |
| **Prescriptive (Yonlendirici)** | "Ne yapmaliyiz?" sorusunu yanitlar | Stok seviyesi optimum kac olmali? |

---

## 2. Istatistik Temelleri

Istatistik, veri analizinin omurgasidir. Iyi bir veri analisti olmak icin istatistiksel kavramlara hakim olmak sarttir.

### 2.1 Tanimlayici Istatistikler (Descriptive Statistics)

Tanimlayici istatistikler, bir veri setinin temel ozelliklerini ozetler:

**Merkezi Egilim Olcutleri (Central Tendency):**

- **Ortalama (Mean):** Tum degerlerin toplaminin gozlem sayisina bolumu.
  - `x̅ = (Σxi) / n`
  - Aykiraya karsidir (outlier'lara). Ornegin 10 kisi icinde 1 milyarder varsa ortalama gelir yaniltici olur.
- **Medyan (Median):** Veri siralandiginda tam ortadaki deger.
  - Aykiraya dayaniklidir. Gelir dagiliminda ortalama yerine medyan kullanmak daha gercekci bir tablo cizer.
- **Mod (Mode):** En sik tekrar eden deger.
  - Kategorik veriler icin kullanisli. Ornegin en cok satan urun kategorisi.

**Yayilim Olcutleri (Dispersion):**

- **Varyans (Variance):** Veri noktalarinin ortalamadan ne kadar saptiginin olcusu.
- **Standart Sapma (Standard Deviation):** Varyansin karekokudur. Verinin ne kadar daginik oldugunu gosterir.
  - Finansta volatilite olcutu olarak kullanilir.
- **Ceyreklikler (Quartiles) ve IQR:** Veriyi dort esit parcaya boler. Outlier tespitinde kullanilir.
- **Cap (Range):** Maksimum - Minimum deger.

### 2.2 Cikarimsal Istatistikler (Inferential Statistics)

Orneklem (sample) verisinden ana kutle (population) hakkinda cikarim yapmayi saglar.

**Temel Kavramlar:**

- **Population (Ana Kutle):** Uzerinde calisilan tum grup.
- **Sample (Orneklem):** Population'dan secilen alt grup.
- **Sampling Distribution:** Bir istatistigin (ornegin ortalama) tekrarli orneklemelerdeki dagilimi.

### 2.3 Dagilimlar (Distributions)

- **Normal Dagilim (Gaussian):** Cansuyu egrisi. Bircok dogal olay normal dagilima uyar. 68-95-99.7 kurali: ortalamadan 1 std sapma icinde verinin %68'i, 2 std sapma icinde %95'i, 3 std sapma icinde %99.7'si bulunur.
- **Binomial Dagilim:** Iki sonuclu deneylerde (basari/basarisizlik) kullanilir. Ornek: bir reklamin tiklanma olasiligi.
- **Poisson Dagilim:** Belirli bir zaman diliminde gerceklesen olay sayisini modeller. Ornek: bir cagri merkezine saatte gelen cagri sayisi.
- **Skewness (Carpiklik):** Verinin simetrik olup olmadigini belirtir.
- **Kurtosis (Basiklik):** Verinin kuyruk yapisini olcer.

### 2.4 Merkezi Limit Teoremi (Central Limit Theorem)

**CLT, istatistigin en onemli teoremlerinden biridir.** Her bir gozlem normal dagilmasa bile, yeterli buyuklukteki bir orneklemin ortalamasinin dagilimi normal dagilima yaklasir. Bu sayede:
- Orneklem ortalamasi uzerinden ana kutle hakkinda cikarim yapabiliriz.
- Orneklem buyuklugu genelde n >= 30 yeterli kabul edilir.
- z-test, t-test, ANOVA gibi testlerin temelini olusturur.

### 2.5 Guven Araliklari (Confidence Intervals)

Bir parametrenin (ornegin ortalama) hangi aralikta oldugunu belirli bir guven duzeyinde ifade eder.

- **%95 Guven Araligi:** "100 kez ornekleme yapsak, 95'inde gercek ortalama bu araligin icinde olur."
- Formul: `CI = x̅ ± z * (σ / √n)`
- **Margin of Error (Hata Payi):** `z * (σ / √n)`

**Is Dunyasinda Ornek:**
Bir e-ticaret sitesinin ortalama siparis degeri 150 TL, std sapma 40 TL, 100 musterilik orneklem:
- %95 CI = 150 ± 1.96 * (40 / 10) = 150 ± 7.84 = [142.16, 157.84]

---

## 3. Regresyon Analizi

Regresyon, bagimli bir degisken ile bir veya daha fazla bagimsiz degisken arasindaki iliskiyi modellemek icin kullanilir.

### 3.1 Basit Lineer Regresyon

`Y = β₀ + β₁X + ε`

- **Y:** Bagimli degisken (hedef)
- **X:** Bagimsiz degisken (tahmin edici)
- **β₀:** Kesim noktasi (intercept)
- **β₁:** Egim (slope) — X'teki 1 birimlik degisimin Y'deki karsiligi
- **ε:** Hata terimi

**Yorumlama:** β₁ = 2.5 ise, X 1 birim arttiginda Y ortalama 2.5 birim artar.

### 3.2 Coklu Regresyon (Multiple Regression)

`Y = β₀ + β₁X₁ + β₂X₂ + ... + βₖXₖ + ε`

Birden fazla bagimsiz degisken ile model kurulur.

**Ornek (Pazarlama):**
```
Satis = β₀ + β₁(TV reklam) + β₂(Dijital reklam) + β₃(Sosyal medya) + ε
```

**Katsayi Yorumu:** β₁ = 0.8 ise, TV reklamina yapilan 1000 TL'lik artis, diger degiskenler sabitken, satisi ortalama 800 TL artirir.

### 3.3 Lojistik Regresyon (Logistic Regression)

Bagimli degisken kategorik oldugunda kullanilir (ornegin musteri kaybi: evet/hayir).

`log(p/(1-p)) = β₀ + β₁X₁ + ... + βₖXₖ`

- p, olayin gerceklesme olasiligidir
- **Odds Ratio (Olasilik Orani):** `exp(β₁)` — X'teki 1 birimlik artisin olasilik uzerindeki carpan etkisi
- Ornek: exp(β₁) = 1.5 ise, X 1 birim arttiginda musteri kaybetme olasiligi %50 artar

### 3.4 Model Degerlendirme Metrikleri

| Metrik | Aciklama | Kullanimi |
|--------|----------|-----------|
| **R² (R-squared)** | Bagimli degisken varyansinin ne kadarinin model tarafindan aciklandigi | 0-1 arasi, yuksek iyi |
| **Adjusted R²** | Degisken sayisina gore cezalandirma uygular | Coklu regresyonda R²'den daha guvenilir |
| **p-value** | Her bir katsayinin istatistiksel olarak anlamli olup olmadigini gosterir | p < 0.05 genelde anlamli kabul edilir |
| **F-test** | Modelin genel olarak anlamli olup olmadigini test eder | Tum katsayilarin ayni anda sifir olmadigini test eder |
| **RMSE** | Tahminlerin gercek degerlerden ortalama sapmasi | Daha dusuk daha iyi |
| **MAE** | Ortalama mutlak hata | RMSE'ye gore aykiraya daha dayanikli |

### 3.5 Dogru Regresyon Turunu Secmek

| Durum | Kullanilacak Model |
|-------|-------------------|
| Bagimli degisken surekli (ornek: fiyat, satis) | Lineer Regresyon |
| Bagimli degisken ikili (ornek: kaybetti/kaybetmedi) | Lojistik Regresyon |
| Birden fazla bagimli degisken | Coklu Regresyon |
| Bagimli degisken sayma verisi (ornek: musteri ziyareti sayisi) | Poisson Regresyon |
| Zaman boyutu var (ornek: aylik satis) | Zaman Serisi (ARIMA, Prophet) |

### 3.6 Dikkat Edilmesi Gereken Konular

- **Multicollinearity (Coklu Baginti):** Bagimsiz degiskenler birbiriyle yuksek korelasyonlu oldugunda ortaya cikar. VIF (Variance Inflation Factor) ile tespit edilir. VIF > 5-10 problemlidir.
- **Overfitting:** Model egitim verisine cok iyi uyum saglar ancak yeni veride basarisiz olur. Cross-validation ve regularization (Ridge, Lasso) ile engellenir.
- **Heteroscedasticity:** Hata terimlerinin varyansi sabit degildir. Log donusumu veya weighted least squares cozum olabilir.
- **Outlier'larin Etkisi:** Uctaki degerler regresyon dogrusunu cok fazla etkileyebilir. Robust regression yontemleri kullanilabilir.

---

## 4. Korelasyon vs Nedensellik

Istatistikteki en kritik ayrimlardan biri: **korelasyon nedensellik anlamina gelmez.**

### 4.1 Korelasyon (Correlation)

Iki degisken arasindaki iliskinin yonunu ve siddetini olcer.

- **Pearson r:** -1 ile +1 arasi. -1 tam negatif, 0 iliski yok, +1 tam pozitif iliski.
  - r = -0.8: Guclu negatif iliski (ornek: fiyat arttikca talep azalir)
  - r = 0.3: Zayif pozitif iliski
- **Spearman's rho:** Sirali (ranked) veriler icin kullanilir, monotonic iliskileri yakalar.

### 4.2 Spurious Correlations (Sahte Iliskiler)

Iki degisken arasinda gozlenen ancak gercekte hicbir nedensel baglantinin olmadigi iliskiler.

**Unlu Ornekler:**
- Filmlerde Nicolas Cage'in rol aldigi film sayisi ile havuzda bogulan insan sayisi arasinda yuksek korelasyon
- ABD'de yillik peynir tuketimi ile yatak carsaflarina dolanan kisilerin sayisi arasindaki korelasyon
- Dondurma satislari ile bogulma vakalari arasindaki korelasyon (gercek sebep: sicak hava)

**Turk is dunyasindan sahte korelasyon riski:**
- Bir pazarlama kampanyasiyla es zamanli olarak satis artisi olmasi, kampanyanin basarili oldugu anlamina gelmez. Mevsimsel etki, rakip eylemleri veya ekonomik faktorler de satisi etkilemis olabilir.

### 4.3 Confounding Variables (Karistirici Degiskenler)

Gozlenen iliskinin aslinda ucuncu bir degiskenden kaynaklanmasi.

**Is Dunyasinda Ornek:**
```
Sirket, calisan egitim saatleri ile verimlilik arasinda pozitif korelasyon buldu.
Confounding variable: Calisanin kidemi. Kidemli calisanlar hem daha cok egitim aliyor 
hem de zaten daha verimli. Egitimin tek basina etkisi dusuk olabilir.
```

### 4.4 Simpson's Paradox

Gruplara ayrildiginda gozlenen iliskinin, gruplar birlesince tersine donmesi.

**Klasik Ornek (Berkeley Universitesi):**
- Genel kabul oranina bakildiginda kadinlar erkeklere gore daha dusuk kabul oranina sahip gibi gorunuyordu.
- Ancak her bolume ayri ayri bakildiginda kadinlar daha yuksek kabul oranina sahipti.
- Nedeni: Kadinlar kabul orani dusuk bolumlere (ornegin Muhendislik) daha fazla basvuruyordu.

**Turk is dunyasinda Simpson Paradox:**
- Bir sirket genel musteri memnuniyeti anketinde puani dustugu halde her bir musteri segmentinde puani artmis olabilir. Sebep: dusuk puanli segmentin toplam icindeki payinin artmasi.

### 4.5 Nedensellik Test Etme Yontemleri

- **Randomized Controlled Trials (RCT):** Kontrol ve tedavi gruplari rastgele atanir. Altin standart.
- **A/B Testi:** RCT'nin dijital versiyonu.
- **Difference-in-Differences (DiD):** Tedavi goren ve gormeyen gruplarin zaman icindeki karsilastirmasi.
- **Instrumental Variables:** Confounding'i engellemek icin ara degisken kullanimi.
- **Granger Causality:** Zaman serilerinde bir degiskenin digerini tahmin edip edemedigini test eder.

---

## 5. Excel / Google Sheets Analizi

Excel ve Google Sheets, kurumsal dunyada en yaygin kullanilan veri analizi araclari olmaya devam etmektedir. Iyi bir Excel kullanicisi olmak, her analist icin temel bir yetkinliktir.

### 5.1 Pivot Tables (Pivot Tablolar)

Pivot tablolar, buyuk veri setlerini saniyeler icinde ozetlemenin en hizli yoludur.

**Temel Kullanim:**

1. Veri secilir -> Insert -> PivotTable
2. **Rows:** Kategorik degisken (ornek: sehir, urun kategorisi)
3. **Values:** Ozetlenecek metrik (SUM of Satis, AVERAGE of Fiyat)
4. **Columns:** Ikinci bir kategorik gruplama
5. **Filters:** Veriyi filtrelemek icin

**Ornek:** Sehir bazinda aylik satis ozeti

| Sehir | Ocak | Subat | Mart | Genel Toplam |
|-------|------|-------|------|-------------|
| Istanbul | 1.2M | 1.4M | 1.1M | 3.7M |
| Ankara | 0.8M | 0.7M | 0.9M | 2.4M |
| Izmir | 0.5M | 0.6M | 0.5M | 1.6M |

**Ileri Pivot Teknikleri:**
- **Calculated Field:** Pivot icinde yeni metrik olusturma
- **Slicers:** Gorsel filtreleme
- **Timeline:** Tarih bazli filtreleme
- **GETPIVOTDATA:** Pivot sonuclarini baska hucrelerde kullanma

### 5.2 VLOOKUP / XLOOKUP / INDEX-MATCH

**VLOOKUP (Vertical Lookup):**
Bir tabloda anahtar degere gore arama yapar.

```
=VLOOKUP(A2, $F$2:$G$100, 2, FALSE)
```
- A2: Aranan deger
- F2:G100: Tablo dizisi
- 2: Dondurulecek sutun numarasi
- FALSE: Tam eslesme

**VLOOKUP Limitasyonlari:**
- Sadece saga dogru arama yapabilir
- Eslesen deger en soldaki sutunda olmalidir
- Sutun sirasi degisirse bozulur

**XLOOKUP (Excel 365 / Google Sheets):**

```
=XLOOKUP(A2, $F$2:$F$100, $G$2:$G$100)
```
VLOOKUP'un tum limitasyonlarini cozer: sola dogru da arama yapabilir, varsayilan tam eslesme, dizi dondurabilir.

**INDEX-MATCH (Daha eski Excel surumleri icin):**

```
=INDEX($G$2:$G$100, MATCH(A2, $F$2:$F$100, 0))
```
Daha esnek ve hizlidir (VLOOKUP'tan daha az hesaplama gerektirir).

### 5.3 Conditional Formatting (Kosullu Bicimlendirme)

Verideki oruntuleri gorsel olarak vurgulamak icin kullanilir.

**Yaygin Kullanim Senaryolari:**
- **Color Scales:** Yuksek-dusuk degerleri renk skalasi ile gosterme (heatmap)
- **Data Bars:** Bar grafi benzeri gorsellestirme
- **Icon Sets:** Yuksek/dusuk degerleri simgelerle gosterme
- **Custom Formula:** Kendi kosul formulunuzu yazma
  - `=A1>ORTALAMA($A$1:$A$100)` — Ortalamanin ustundekileri yesil yap

### 5.4 Data Validation (Veri Dogrulama)

Kullanicilarin hatali veri girmesini engellemek icin kritik bir araclar.

- **Dropdown Listeler:** Acilir menuden secim (`Data -> Data Validation -> List`)
- **Custom Formulas:** Kendi dogrulama kurallari
- **Input Messages:** Kullaniciya bilgi mesaji
- **Error Alerts:** Hatali giris uyarilari

**Is Dunyasi Ornegi:** Satis formunda "Bolge" alanina sadece belirlenen bolgelerin girilebilmesi icin dropdown list; "Tarih" alanina sadece gecerli tarihler girilebilmesi icin validation.

### 5.5 What-If Analysis (What-If Analizi)

**Goal Seek (Hedef Ara):**
Belirli bir sonuca ulasmak icin hangi girdinin gerekli oldugunu bulur.

```
Ornek: 100,000 TL kar icin kac adet urun satmaliyim?
Goal Seek: Hedef hucre = Kar, Hedef deger = 100000, Degisen hucre = Satis adedi
```

**Scenario Manager (Senaryo Yoneticisi):**
Farkli senaryolari karsilastirarak karar vermeye yardimci olur.

| Senaryo | Fiyat | Adet | Maliyet | Kar |
|----------|-------|------|---------|-----|
| Iyimser | 150 TL | 10,000 | 800,000 TL | 700,000 TL |
| Beklenen | 130 TL | 7,000 | 600,000 TL | 310,000 TL |
| Kotumser | 110 TL | 4,000 | 450,000 TL | -10,000 TL |

**Data Tables:**
Bir veya iki degiskenin farkli degerlerinin sonucu nasil etkiledigini gosterir.

### 5.6 Keyboard Shortcuts (Hizli Tushar)

| Kisa Yol | Excel | Google Sheets |
|----------|-------|---------------|
| Hizli toplam | `Alt + =` | `Alt + =` |
| Pivot tablo | `Alt + N + V` | `(Yok)` |
| Filtre ekle | `Ctrl + Shift + L` | `Ctrl + Shift + L` |
| Goto ozel | `F5 -> Alt + S` | `Ctrl + Shift + ;` |
| Deger yapistir | `Ctrl + Alt + V` | `Ctrl + Shift + V` |
| Yeni satir ekle | `Ctrl + Shift + +` | `Ctrl + Shift + +` |
| Sutun gizle | `Ctrl + 0` | `Ctrl + 0` |
| Hucre format | `Ctrl + 1` | `(Menuden)` |
| Secili alan | `Ctrl + A` | `Ctrl + A` |
| Power Query | `Alt + A + P + T` | `(Yok)` |

---

## 6. Python ile Veri Analizi (Temel)

Python, veri analizi dunyasinda en populer programlama dillerinden biri haline gelmistir. Pandas kutuphanesi, veri manipulasyonu icin R'deki data.frame mantigini Python'a getirmistir.

### 6.1 Pandas Temelleri

**Veri Yukleme:**

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# CSV okuma
df = pd.read_csv('satis_verisi.csv')

# Excel okuma
df_excel = pd.read_excel('satis_raporu.xlsx', sheet_name='Sheet1')

# Veriye ilk bakis
print(df.head(10))        # Ilk 10 satir
print(df.info())          # Sutun tipleri ve NULL sayilari
print(df.describe())      # Istatistiksel ozet
```

**Veri Temizleme:**

```python
# NULL deger kontrolu
df.isnull().sum()

# NULL degerleri doldurma
df['fiyat'].fillna(df['fiyat'].median(), inplace=True)

# Duplicate satirlari kaldirma
df.drop_duplicates(inplace=True)

# Sutun tipini degistirme
df['tarih'] = pd.to_datetime(df['tarih'])

# Outlier temizleme (IQR yontemi)
Q1 = df['satis'].quantile(0.25)
Q3 = df['satis'].quantile(0.75)
IQR = Q3 - Q1
df_clean = df[(df['satis'] >= Q1 - 1.5*IQR) & (df['satis'] <= Q3 + 1.5*IQR)]
```

**Groupby ve Ozetleme:**

```python
# Sehir bazinda ortalama satis
df.groupby('sehir')['satis'].mean()

# Coklu metrik
ozet = df.groupby(['sehir', 'kategori']).agg({
    'satis': ['sum', 'mean', 'count'],
    'kar': 'sum'
}).round(2)

print(ozet)
```

**Merge (Birlestirme):**

```python
musteri = pd.read_csv('musteri.csv')
siparis = pd.read_csv('siparis.csv')

# LEFT JOIN gibi
df_merged = musteri.merge(siparis, on='musteri_id', how='left')

# Birlestirme turleri: how='inner', 'outer', 'left', 'right'
```

**Pivot Table:**

```python
# Excel pivot benzeri
pivot = pd.pivot_table(
    df,
    values='satis',
    index='sehir',
    columns='ay',
    aggfunc='sum',
    fill_value=0
)
```

### 6.2 Scipy ile Temel Istatistik

```python
from scipy import stats

# Normal dagilim testi
stat, p = stats.normaltest(df['satis'])
print(f'p-value: {p}')

# t-test (iki grup karsilastirmasi)
grupA = df[df['kampanya'] == 'A']['satis']
grupB = df[df['kampanya'] == 'B']['satis']
t_stat, p_value = stats.ttest_ind(grupA, grupB)

# Korelasyon
r, p = stats.pearsonr(df['reklam_harcamasi'], df['satis'])
print(f'Pearson r: {r}, p-value: {p}')
```

### 6.3 Basit Regresyon

```python
from sklearn.linear_model import LinearRegression
from sklearn.model_selection import train_test_split

X = df[['reklam_harcamasi', 'indirim_orani']]
y = df['satis']

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)

model = LinearRegression()
model.fit(X_train, y_train)

print(f'Katsayilar: {model.coef_}')
print(f'Intercept: {model.intercept_}')
print(f'R² Skor: {model.score(X_test, y_test):.3f}')
```

---

## 7. SQL Temelleri

SQL (Structured Query Language), veri analistlerinin en temel aracidir. Kurumsal verilerin cogu relasyonel veritabanlarinda saklanir ve SQL bunlara erismenin standart yoludur.

### 7.1 Neden Her Is Insani SQL Ogrenmeli?

- **Self-Serve Analytics:** Analistler ve is kullanicilari, muhendislere bagimli olmadan kendi sorgularini yazabilir.
- **Veriye Dogrudan Erisim:** Excel'e export edilmis dar bir veri yerine, tum veritabanina erisim.
- **Daha Hizli:** Excel'de acilamayacak buyuklukteki verileri saniyeler icinde isleme.
- **Dogruluk:** Manuel manipulasyon hatalarini azaltir.
- **Her Yerde:** SQL bilgisi, MySQL, PostgreSQL, BigQuery, Snowflake, Redshift gibi tum platformlarda calisir.

### 7.2 SELECT ve Filtreleme

```sql
-- Temel sorgu
SELECT musteri_id, ad, sehir, kayit_tarihi
FROM musteriler
WHERE sehir = 'Istanbul'
  AND kayit_tarihi >= '2025-01-01'
ORDER BY kayit_tarihi DESC;

-- DISTINCT (benzersiz degerler)
SELECT DISTINCT sehir FROM musteriler;

-- LIMIT (ilk N satir)
SELECT * FROM siparisler LIMIT 100;
```

### 7.3 GROUP BY ve Ozetleme

```sql
-- Sehir bazinda musteri sayisi
SELECT 
    sehir,
    COUNT(*) AS musteri_sayisi,
    ROUND(AVG(harcama), 2) AS ortalama_harcama,
    SUM(harcama) AS toplam_harcama,
    MAX(harcama) AS en_yuksek_harcama
FROM musteriler
GROUP BY sehir
HAVING COUNT(*) > 100  -- GROUP BY sonrasi filtre
ORDER BY toplam_harcama DESC;
```

**Not:** `WHERE` satir bazinda filtre, `HAVING` ise gruplama sonrasi filtre icindir.

### 7.4 JOIN'ler

```sql
-- INNER JOIN: Her iki tabloda da eslesen kayitlar
SELECT s.siparis_id, s.tarih, m.ad, m.sehir
FROM siparisler s
INNER JOIN musteriler m ON s.musteri_id = m.musteri_id;

-- LEFT JOIN: Sol tablodaki tum kayitlar (eslesmeyenler NULL)
SELECT m.ad, s.siparis_id, s.tutar
FROM musteriler m
LEFT JOIN siparisler s ON m.musteri_id = s.musteri_id;

-- Siparis vermemis musterileri bulma
SELECT m.ad, m.email
FROM musteriler m
LEFT JOIN siparisler s ON m.musteri_id = s.musteri_id
WHERE s.siparis_id IS NULL;
```

### 7.5 Window Functions

Window fonksiyonlari, her satir icin o satirin grubundaki diger satirlarla ilgili hesaplamalar yapar.

```sql
-- Satir numarasi (ranking)
SELECT 
    musteri_id,
    harcama,
    ROW_NUMBER() OVER (PARTITION BY sehir ORDER BY harcama DESC) AS sehir_sirasi
FROM musteriler;

-- Kümülatif toplam
SELECT 
    ay,
    satis,
    SUM(satis) OVER (ORDER BY ay ROWS BETWEEN UNBOUNDED PRECEDING AND CURRENT ROW) AS kumulatif_satis
FROM aylik_satislar;

-- Hareketli ortalama (3 aylik)
SELECT 
    ay,
    satis,
    AVG(satis) OVER (ORDER BY ay ROWS BETWEEN 2 PRECEDING AND CURRENT ROW) AS 3ay_hareketli_ortalama
FROM aylik_satislar;

-- Onceki aya gore degisim
SELECT 
    ay,
    satis,
    LAG(satis, 1) OVER (ORDER BY ay) AS onceki_ay,
    satis - LAG(satis, 1) OVER (ORDER BY ay) AS degisim
FROM aylik_satislar;
```

### 7.6 CTE (Common Table Expressions)

Karmasik sorgulari daha okunabilir hale getirir:

```sql
WITH musteri_ozet AS (
    SELECT 
        musteri_id,
        COUNT(*) AS siparis_sayisi,
        SUM(tutar) AS toplam_harcama
    FROM siparisler
    GROUP BY musteri_id
),
segmentler AS (
    SELECT 
        musteri_id,
        toplam_harcama,
        CASE 
            WHEN toplam_harcama > 10000 THEN 'Premium'
            WHEN toplam_harcama > 5000 THEN 'Gold'
            WHEN toplam_harcama > 1000 THEN 'Silver'
            ELSE 'Bronze'
        END AS segment
    FROM musteri_ozet
)
SELECT segment, COUNT(*) AS musteri_sayisi, AVG(toplam_harcama) AS ortalama
FROM segmentler
GROUP BY segment
ORDER BY ortalama DESC;
```

---

## 8. Exploratory Data Analysis (EDA)

EDA, bir veri setini analiz etmeye baslamanin ilk adimidir. Ama: veriyi anlamak, oruntuleri kesfetmek, hipotezler olusturmak ve veri kalitesini degerlendirmek.

### 8.1 EDA Adimlari

**Adim 1: Veriye Genel Bakiş**

```python
# Boyut
print(f'Satir: {df.shape[0]}, Sutun: {df.shape[1]}')

# Sutun isimleri
print(df.columns.tolist())

# Veri tipleri
print(df.dtypes)

# Ilk/ son satirlar
print(df.head())
print(df.tail())
```

**Adim 2: Eksik Veri Kontrolu**

```python
# Eksik veri yuzdesi
eksik_yuzde = (df.isnull().sum() / len(df)) * 100
eksik_df = pd.DataFrame({'sutun': df.columns, 'eksik_yuzde': eksik_yuzde})
eksik_df = eksik_df[eksik_df['eksik_yuzde'] > 0].sort_values('eksik_yuzde', ascending=False)
print(eksik_df)
```

**Adim 3: Tekil Degerler ve Dagitim**

```python
# Sayisal sutunlar icin
for col in df.select_dtypes(include=['float64', 'int64']).columns:
    print(f'\n{col}:')
    print(f'  Min: {df[col].min()}, Max: {df[col].max()}')
    print(f'  Ortalama: {df[col].mean():.2f}, Medyan: {df[col].median():.2f}')
    print(f'  Std: {df[col].std():.2f}')
    print(f'  Skewness: {df[col].skew():.2f}')
    
# Kategorik sutunlar icin
for col in df.select_dtypes(include=['object']).columns:
    print(f'\n{col}:')
    print(df[col].value_counts().head(10))
```

**Adim 4: Gorsel Kesif**

```python
import matplotlib.pyplot as plt
import seaborn as sns

# Histogram
plt.figure(figsize=(10, 6))
plt.hist(df['satis'], bins=50, edgecolor='black', alpha=0.7)
plt.title('Satis Dagitimi')
plt.xlabel('Satis Miktari')
plt.ylabel('Frekans')
plt.show()

# Box plot - outlier tespiti
plt.figure(figsize=(10, 6))
sns.boxplot(data=df[['satis', 'kar', 'maliyet']])
plt.title('Deger Dagilimlari (Box Plot)')
plt.show()

# Korelasyon heatmap
plt.figure(figsize=(12, 8))
korelasyon = df.select_dtypes(include=['float64', 'int64']).corr()
sns.heatmap(korelasyon, annot=True, cmap='coolwarm', center=0)
plt.title('Korelasyon Matrisi')
plt.show()

# Scatter plot
plt.figure(figsize=(10, 6))
plt.scatter(df['reklam_harcamasi'], df['satis'], alpha=0.5)
plt.xlabel('Reklam Harcamasi')
plt.ylabel('Satis')
plt.title('Reklam vs Satis Iliskisi')
plt.show()
```

### 8.2 Outlier Tespit Yontemleri

| Yontem | Aciklama | Ne Zaman Kullanilir |
|--------|----------|-------------------|
| **IQR Yontemi** | Q1 - 1.5*IQR ve Q3 + 1.5*IQR disindaki degerler | Genel kullanim, normal dagilmayan veri |
| **Z-Score** | Ortalamadan 3 std sapma otesindeki degerler | Normal dagilan veri |
| **Isolation Forest** | Makine ogrenmesi tabanli | Yuksek boyutlu veri |
| **DBSCAN** | Yogunluk tabanli kumeleme | Karmasik oruntuler |

### 8.3 EDA Raporu Template

Bir EDA raporunda bulunmasi gereken basliklar:

1. **Veri Seti Bilgisi:** Kaynak, zaman araligi, satir/sutun sayisi
2. **Veri Kalitesi:** Eksik degerler, duplikatlar, veri tipleri
3. **Univariate Analiz:** Her sutunun tek basina dagilimi
4. **Bivariate Analiz:** Degiskenler arasi iliskiler
5. **Korelasyon Analizi:** Korelasyon matrisi, anlamli iliskiler
6. **Outlier Tespiti:** Aykiri degerler ve degerlendirmesi
7. **On Bulgular:** Kesfedilen oruntuler ve hipotezler
8. **Veri Temizleme Onerileri:** Bir sonraki adim icin

---

## 9. A/B Testi Analizi

A/B testi (split test), iki veya daha fazla varyasyonu karsilastirarak hangisinin daha iyi performans gosterdigini belirleme yontemidir. Dijital pazarlama, urun gelistirme ve UX tasariminda en kritik karar alma araclarindan biridir.

### 9.1 A/B Testi Temel Kavramlar

- **Kontrol Grubu (A):** Mevcut versiyon
- **Tedavi Grubu (B):** Degistirilmis versiyon
- **Hipotez:**
  - H₀ (Null Hipotez): A ile B arasinda fark yoktur
  - H₁ (Alternative Hipotez): A ile B arasinda fark vardir
- **Alpha (α):** Tip I hata riski (genelde 0.05 = %5)
- **Beta (β):** Tip II hata riski (genelde 0.20, guc = 0.80)
- **p-value:** H₀ dogruyken bu sonucu alma olasiligi. p < α ise H₀ reddedilir.

### 9.2 Numune Buyuklugu Hesaplama (Sample Size)

Testin guvenilir olmasi icin yeterli orneklem buyuklugu gerekir.

```
n = (Zα/2 + Zβ)² * [p₁(1-p₁) + p₂(1-p₂)] / (p₂ - p₁)²
```

**Kullanisli Calculator:** `https://www.evanmiller.org/ab-testing/sample-size.html`

**Yaklasik Degerler (Donusum Orani icin):**

| Mevcut Donusum | Minimum Detectable Effect | Onerilen Orneklem |
|----------------|--------------------------|------------------|
| %5 | %1 (%20 relative) | 4,500 / varyasyon |
| %10 | %2 (%20 relative) | 7,000 / varyasyon |
| %20 | %2 (%10 relative) | 23,000 / varyasyon |

### 9.3 t-test vs z-test

| Kriter | t-test | z-test |
|--------|--------|--------|
| Orneklem buyuklugu | Kucuk (n < 30) | Buyuk (n >= 30) |
| Population std sapma | Bilinmiyor | Biliniyor veya yeterli n |
| Kullanim | Genel A/B test analizi | Donusum orani, click-through rate |

### 9.4 Chi-Square Test

Kategorik degiskenler arasindaki iliskiyi test etmek icin kullanilir.

**Ornek (Kampanya Etkisi):**

```
                Satin Aldi  Satin Almadi  Toplam
Kampanya A        400          600         1000
Kampanya B        450          550         1000
```

```python
from scipy.stats import chi2_contingency

# Contingency table
table = [[400, 600], [450, 550]]
chi2, p, dof, expected = chi2_contingency(table)

print(f'Chi²: {chi2:.3f}, p-value: {p:.3f}')

# p > 0.05 ise kampanyalar arasinda istatistiksel olarak anlamli fark yok
```

### 9.5 Multiple Testing Correction (Coklu Test Duzeltmesi)

Birden fazla hipotez test edildiginde Tip I hata riski artar.

**Ornek:** Ayni anda 10 farkli KPI'yi test ederseniz, sadece sans eseri bile birinde "anlamli" sonuc bulma olasiliginiz yuksektir.

**Duzeltme Yontemleri:**

- **Bonferroni Correction:** α / n (en muhafazakar)
  - 10 test icin: 0.05 / 10 = 0.005
  - Avantaj: Cok basit. Dezavantaj: cok konservatif, gercek farklari kacirabilir.
- **Benjamini-Hochberg (FDR):** False Discovery Rate'i kontrol eder. Daha az konservatif.
- **Holm-Bonferroni:** Bonferroni'den daha guclu, ayni kontrolu saglar.

### 9.6 Pratik Anlamlilik vs Istatistiksel Anlamlilik

- **Istatistiksel Anlamlilik:** p < 0.05. Fark gercekten var mi?
- **Pratik Anlamlilik (Practical Significance):** Fark ise deger mi?

**Turk Is Dunyasindan Ornek:**
```
Bir e-ticaret sitesi, buton rengini degistirerek donusum oranini %3.2'den %3.3'e cikardi.
p-value = 0.01 (istatistiksel olarak anlamli)
100,000 ziyaretcide ek 100 siparis.
Degisimin maliyeti: 500,000 TL (yeniden tasarim, test, dokuman).
Fayda: 100 * 200 TL (ortalama kar) = 20,000 TL.
Pratik anlamlilik: DUSUK. Degisime degmez.
```

---

## 10. Kohort Analizi

Kohort analizi, kullanicilari ortak bir ozellik veya deneyime gore gruplayarak zaman icindeki davranislarini inceleme yontemidir. Ozellikle SaaS ve abonelik bazli is modellerinde hayati bir analiz aracidir.

### 10.1 Kohor Türleri

**Zamansal Kohortlar (Acquisition Cohorts):**
Kullanicilarin ne zaman kaydolduguna gre gruplama.

**Davranissal Kohortlar (Behavioral Cohorts):**
Kullanicilarin belirli bir eylem yapip yapmamasina gora gruplama.

- "Ilk haftada 3 kez uygulamayi acanlar" vs "acmayanlar"
- "Sepete urun ekleyenler" vs "eklemeyenler"

**Segment Bazli:**
- "Premium uyeler" vs "ucretsiz kullanicilar"
- "Mobil kullanicilar" vs "web kullanicilari"

### 10.2 Retention Cohorts (Tutma Kohortlari)

En yaygin kohort analizi turudur. Bir donemde edinilen kullanicilarin sonraki donemlerde ne kadarinin aktif kaldigini olcer.

**Excel'de Retention Coharti:**

```
            Ay 0   Ay 1   Ay 2   Ay 3   Ay 4
Ocak 2025   100%   45%    32%    28%    24%
Subat 2025  100%   48%    35%    30%    -
Mart 2025   100%   42%    30%    -      -
Nisan 2025  100%   50%    -      -      -
Mayis 2025  100%   -      -      -      -
```

**Kohort Analizi Yorumlama:**

- **Duz cizgi:** Kohortlar benzer sekilde davraniyor. Urun veya pazar degismiyor.
- **Yukselen trend:** Son kohortlar daha iyi retention gosteriyor. Urun iyilesiyor veya daha dogru kullanicilar geliyor.
- **Dusen trend:** Son kohortlar daha kotu retention. Rekabet artiyor, urun bozuluyor veya pazar doyuma ulasiyor.

### 10.3 SaaS Icin Kritik Kohort Metrikleri

| Metrik | Tanim | Saglikli Deger |
|--------|-------|---------------|
| **D1 Retention** | 1. gun aktif kullanim | >%60 |
| **W1 Retention** | 1. hafta aktif kullanim | >%40 |
| **M1 Retention** | 1. ay aktif kullanim | >%30 |
| **Churn Rate** | Aylik kayip orani | <%5-7 |
| **Net Revenue Retention** | Gelir bazli tuma orani | >%100 (expansion > churn) |

### 10.4 Kohort Analizi Uygulama Adimlari (Python)

```python
import pandas as pd
import datetime as dt

# Ornek veri: kullanici_id, kayit_tarihi, aktivite_tarihi
df = pd.read_csv('kullanici_etkinlik.csv')

# Ay bazina cevirme
df['kayit_ayi'] = df['kayit_tarihi'].dt.to_period('M')
df['aktivite_ayi'] = df['aktivite_tarihi'].dt.to_period('M')

# Kohort indeksi (kacinci ay)
df['kohort_indeks'] = (df['aktivite_ayi'] - df['kayit_ayi']).apply(lambda x: x.n)

# Her kohorttaki benzersiz kullanici sayisi
kohort_data = df.groupby(['kayit_ayi', 'kohort_indeks'])['kullanici_id']\
                .nunique().reset_index()

# Kohort buyuklugu (0. ay)
kohort_buyukluk = kohort_data[kohort_data['kohort_indeks'] == 0]\
                  [['kayit_ayi', 'kullanici_id']]
kohort_buyukluk.columns = ['kayit_ayi', 'kohort_buyuklugu']

# Retention orani
kohort_data = kohort_data.merge(kohort_buyukluk, on='kayit_ayi')
kohort_data['retention'] = kohort_data['kullanici_id'] / kohort_data['kohort_buyuklugu']

# Pivot tablo
retention_pivot = kohort_data.pivot(
    index='kayit_ayi',
    columns='kohort_indeks',
    values='retention'
)
```

### 10.5 Neden Kohort Analizi?

- **Hayati Segmentasyon:** Yeni ve eski musterilerin farkli davrandigini goruruz.
- **Zaman Icerisinde Degisim:** Urun degisikliklerinin, pazarlama kampanyalarinin etkisini olcebiliriz.
- **Tahmin:** Historical cohort'lardan yola cikarak LTV (Customer Lifetime Value) tahmini yapabiliriz.
- **Erken Uyari:** Retention'daki dusus, churn'daki artis erken tespit edilip aksiyon alinabilir.

---

## 11. Modern Veri Analizi Araclari (2025)

### 11.1 Power BI

**Durum:** En yaygin kullanilan BI araci (Gartner Magic Quadrant lideri).

**Guclu Yanlari:**
- Microsoft ekosistemiyle tam uyum (Excel, Azure, SQL Server)
- Dogal dil sorgulama (Q&A ozelligi)
- DAX (Data Analysis Expressions) ile ileri analitik
- Power Query ile guclu veri donusumu
- Ucretsiz desktop surumu var

**Kimler Icin:** Microsoft dunyasinda yasayan kurumlar. Orta ve buyuk olceki sirketler.

### 11.2 Tableau

**Durum:** Karmasik gorsellestirme konusunda sektor standardi.

**Guclu Yanlari:**
- Gorsel analitikte esi benzeri yok
- Drag-drop ile sezgisel kullanim
- Hesaplamali alanlar ve parametreler
- Tableau Prep ile veri temizleme
- Topluluk ve kaynak zenginligi

**Kimler Icin:** Veri gorsellestirmeye cok onem veren, Tableau Server/Cloud'a yatirim yapabilen sirketler.

### 11.3 Looker / Looker Studio

**Durum:** Looker (Google Cloud), modern BI'in onculerinden.

**Guclu Yanlari:**
- **LookML:** Kod tabanli semantik katman — tutarlı metrik tanımları
- BigQuery ile dogal entegrasyon
- Gercek zamanli veri erisimi (in-database architecture)
- Embedded analytics icin ideal
- Looker Studio (eski Data Studio): ucretsiz, basit raporlama

**Kimler Icin:** Google Cloud kullanan, cloud-native sirketler.

### 11.4 Hex

**Durum:** Yukselen yildiz. Notebook-native BI platformu.

**Guclu Yanlari:**
- Python ve SQL'i ayni ortamda birlestirir
- Interaktif dashboard'lar dogrudan notebook'tan
- Dagittima hazir (publish one click)
- Isbirligi ozellikleri (gercek zamanli)
- AI destekli (Magic ile kod uretimi)

**Kimler Icin:** Veri ekipleri Python/SQL agirlikli calisan sirketler. Geleneksel BI'dan notebook dunyasina gecis yapmak isteyenler.

### 11.5 Python Veri Analizi Stack'i (2025)

| Kutuphane | Kullanim Alani | Durum |
|-----------|---------------|-------|
| **Pandas 3.0** | Veri manipulasyonu | 3.0 surumuyle buyuk performans iyilestirmeleri |
| **Polars** | Pandas alternatifi, daha hizli | Buyuk veri setleri icin ideal |
| **Scikit-learn 1.6+** | Makine ogrenmesi | Sektor standardi |
| **PyCaret** | AutoML (otomatik model secimi) | Hizli prototipleme icin |
| **XGBoost / LightGBM** | Gelismis regresyon/klasifikasyon | Kaggle yarismalarinda favori |
| **Plotly / Express** | Interaktif gorsellestirme | Dashboard icin ideal |
| **Streamlit** | Python'dan hizli web uygulamasi | Prototip ve internal araclar |

**Python vs R Secimi (2025):**

| Kriter | Python | R |
|--------|--------|-------|
| Ogrenme egrisi | Daha kolay | Daha dik |
| Istatistik | Scipy, Statsmodels ile yeterli | ggplot2, dplyr, tidyr ile rakipsiz |
| Uretim ortami | ML pipeline, API, backend entegrasyon | Zor |
| Topluluk | Cok genis | Akademik ve istatistik agirlikli |
| Karar: Ogrenme sureniz kisitli ise Python; istatistik agirlikli calisacaksaniz R ekleyin |

---

## 12. En Iyi Kaynaklar

### 12.1 Kitaplar

| Kitap | Yazar | Neden Okunmali |
|-------|-------|----------------|
| **Naked Statistics** | Charles Wheelan | Istatistigi eglenceli ve sezgisel anlatir. Matematikten korkanlar icin ideal. |
| **Python for Data Analysis** | Wes McKinney | Pandas'in yaratıcisindan veri analizi. Her Python veri analistinin basucu kitabi. |
| **R for Data Science** | Hadley Wickham | R ekosisteminin en kapsamli kaynagi. Tidyverse felsefesi. |
| **Data Science for Business** | Provost & Fawcett | Is dunyasi perspektifinden veri bilimi. Kod yok, kavramlar var. |
| **Storytelling with Data** | Cole Knaflic | Veri gorsellestirme ve sunum. Is dunyasinda en kritik beceri: veriyle hikaye anlatmak. |
| **Naked Money** | Charles Wheelan | Ekonomi ve veri okuryazarligi bir arada. |
| **The Signal and the Noise** | Nate Silver | Tahmin modelleri ve belirsizlik. FiveThirtyEight kurucusundan. |

### 12.2 Online Egitimler

- **Coursera - Data Science Specialization (Johns Hopkins):** Kapsamli, proje tabanli. R ogrenmek icin en iyi baslangic.
- **Coursera - Google Data Analytics Certificate:** 6 aylik profesyonel sertifika. Is odakli.
- **DataCamp:** Interaktif ogrenme. Python, R, SQL, Power BI.
- **Kaggle Learn:** Ucretsiz, kisa moduller. Pratik odakli.
- **MEF University Data Science Programs:** Turkiye'de akademik kalite.
- **Turkcell Gelecegi Yazanlar:** Ucretsiz, Turkce veri analizi ve Python egitimleri.

### 12.3 YouTube Kanallari

- **StatQuest ile Josh Starmer:** Istatistik ve ML kavramlarini sade ve anlasilir anlatir.
- **sentdex:** Python ile veri analizi ve finans uygulamalari.
- **Luke Barousse:** Veri analizi kariyeri, pratik SQL ve Python.
- **Alex The Analyst:** Veri analistligine giris, portfolyo olusturma.

---

## 13. Vaka Calismalari

### 13.1 Amazon's Recommendation System

**Problem:** 300 milyon musteriye kisisellestirilmis urun onerileri sunmak.

**Veri:**
- Gecmis satin almalar
- Sepet verileri
- Urun goruntuleme gecmisi
- Arama sorgulari
- Degerlendirme ve yorumlar

**Coziim:**
- **Item-to-Item Collaborative Filtering:** "Bu urunu alanlar sunlari da aldi"
- **Real-time Pipeline:** Kafka + Spark Streaming ile anlik oneriler
- **A/B Test Altyapisi:** Her degisiklik kontrollu test edilir

**Sonuc:**
- Amazon gelirinin tahmini %35'i onerme sisteminden gelir
- Her musteriye saniyede binlerce urun arasindan en relevant olanlari gosterir

### 13.2 Spotify Data-Driven Personalization

**Problem:** 500 milyon kullaniciya kisisellestirilmis muzik deneyimi.

**Coziim:**
- **Discover Weekly:** Haftalik kisisel calma listesi. Collaborative filtering + NLP (sarki sozu analizi) + audio features.
- **AI DJ:** Yapay zeka ile kisisel radyo deneyimi. Kullanici tercihlerine gore anlik calma listesi olusturma.
- **Wrapped:** Yillik kisisel veri ozeti. Kullanicilarin en cok dinledigi sanatcilar, turler, dakikalar.

**Veri Kaynaklari:**
- Ses ozellikleri (tempo, enerji, dans edilebilirlik, acousticness)
- Dinleme gecmisi (skip, replay, add to playlist)
- Kullanicilar arasi iliskiler (collaborative filtering)

**Is Dunyasi Dersi:** Veriyi sadece optimizasyon icin degil, musteri deneyimini donusturmek icin kullan.

### 13.3 Turkiye'den: Getir'in Operasyonel Veri Analitigi

**Problem:** Dakikalar icinde teslimat yapan bir operasyonda stok, rota ve talep yonetimi.

**Coziim:**
- **Talep Tahmini:** Her bolge icin saatlik talep tahmini. Machine learning modelleri ile.
- **Dinamik Fiyatlandirma:** Talebin yuksek oldugu zamanlarda fiyat ayarlamasi (surge pricing).
- **Rota Optimizasyonu:** En kisa mesafe / en hizli rota hesaplamasi.
- **Stok Yonetimi:** Her depositoda hangi urunlerden kac adet bulunmasi gerektigi.

**Kullanilan Araclar:**
- Apache Kafka (gercek zamanli veri akisi)
- Python (ML modelleri)
- Looker (is zekasi ve dashboard)

**Is Dunyasi Dersi:** Veri analitigi sadece raporlama degildir; operasyonel kararlari anlik olarak yonlendirmelidir.

### 13.4 Moneyball: Veriyle Donusumun Klasik Ornegi

**Ozet:** Oakland Athletics beyzbol takimi, sinirli butceyle nasil rekabetci olunur sorusuna veri analiziyle cevap verdi.

**Yaklasim:**
- Geleneksel "yildiz oyuncu" yaklasimi yerine, istatistiksel olarak degeri dusuk ama verimli oyunculari kesfetti
- **Sabermetrics:** Oyunun geleneksel metrikleri (batting average) yerine daha anlamli metrikler (on-base percentage, slugging percentage) kullandi
- Takim butcesi ligde en dusuklerden biri olmasina ragmen playoff'a kalmayi basardi

**Is Dunyasi Dersleri:**
- Geleneksel metrikleri sorgulayin. Gercekten onemli olani olcuyor muyum?
- Veri, kariyerli gozlemcilerin kacirdigi firsatlari gosterebilir.
- Rekabet avantaji, herkesin baktigi veriye farkli bakmaktan gelir.

### 13.5 Google People Analytics (Project Oxygen)

**Problem:** Google'da en iyi yoneticileri digerlerinden ayiran ozellikler nelerdir?

**Veri:**
- Performans degerlendirmeleri
- Calisan anketleri (Googlegeist)
- Terfi verileri
- Yonetici geri bildirimleri

**Bulgular (En Iyi Yoneticilerin 8 Ozelligi):**
1. Iyi bir koc (coach) olmak
2. Takimi guclendirmek, mikro-yonetimden kacınmak
3. Calisan refahina ve basarisina onem vermek
4. Productive olmak ve sonuc odakli olmak
5. Iyi bir iletisimci olmak, takimi dinlemek
6. Calisanlara kariyer gelisiminde yardimci olmak
7. Takim icin net bir vizyon ve strateji belirlemek
8. Takim uzerinde teknik uzmanliga sahip olmak

**Is Dunyasi Dersi:** "Insan" konulari bile veriyle analiz edilebilir. People analytics, insan kaynaklari fonksiyonunu donusturuyor.

---

## 14. Pratik Alistirmalar

### Alistirma 1: EDA ile Veri Kesfi

**Adimlar:**
1. Kaggle'dan bir veri seti indirin (ornegin: "Online Retail" veya "Titanic")
2. Veriyi Python veya Excel'de acin
3. Eksik degerleri, outlier'lari, dagilimlari inceleyin
4. 5 farkli gorsellestirme yapin
5. Bulgularinizi 1 sayfalik bir rapor haline getirin

**Beklenen Cikti:** Temizlenmis veri seti + kesif raporu + 5 gorsellestirme.

### Alistirma 2: Regresyon Modeli ile Satis Tahmini

**Adimlar:**
1. Bir sirketin aylik satis, reklam harcamasi, indirim orani, musteri sayisi verilerini iceren bir CSV olusturun
2. Python'da LinearRegression ile model kurun
3. R², p-value, katsayilari yorumlayin
4. Hangi degisken satisi en cok etkiliyor?
5. Modelin overfit olup olmadigini kontrol edin (train-test split ile)

**Beklenen Cikti:** Calisan model, katsayi yorumlari, model dogruluk raporu.

### Alistirma 3: Chi-Square Testi ile Kampanya Analizi

**Adimlar:**
1. Iki farkli pazarlama kampanyasina maruz kalan musterilerin satin alma verilerini olusturun
2. Bir contingency table hazirlayin
3. Python'da `chi2_contingency` ile testi calistirin
4. p-value'u yorumlayin: kampanyalar arasinda anlamli fark var mi?
5. Sonucu bir PowerPoint slaytina sigacak sekilde ozetleyin

**Beklenen Cikti:** Chi-square test sonucu + is yorumu + 1 slayt ozet.

### Alistirma 4: Excel'de Retention Coharti

**Adimlar:**
1. Her ay kaydolan kullanicilarin sonraki aylardaki aktif kullanim sayisini iceren bir tablo olusturun
2. Pivot table ile her kohortun retention oranini hesaplayin
3. Conditional formatting ile coharti gorsellestirin (renk skalasi)
4. Hangi kohortun retention'i en iyi? Neden olabilir?
5- Trendi yorumlayin: son kohortlar daha mi iyi, daha mi kotu?

**Ornek Veri:**

```
Kayit Ayi  | 0. Ay | 1. Ay | 2. Ay | 3. Ay | 4. Ay
Ocak 2025  | 1000  | 450   | 320   | 280   | 240
Subat 2025 | 1200  | 576   | 420   | 360   | -
Mart 2025  | 900   | 378   | 270   | -     | -
```

**Beklenen Cikti:** Renklendirilmis cohort matrisi + yorum + aksiyon onerileri.

---

## 15. Turkiye'de Veri Analizi

### 15.1 Veri Analizi Olgunlugu

Turkiye'de sirketlerin veri analizi olgunlugu sektore ve olcege gore degismektedir:

| Seviye | Ozellik | Ornek Sirketler |
|--------|---------|-----------------|
| **1. Geleneksel Raporlama** | Excel raporlari, statik dashboard | Kucuk ve orta olcekli firmalar |
| **2. Temel Analitik** | Veri ambarı, Power BI kullanımı | Bankalar, telekom sirketleri |
| **3. Gelismis Analitik** | ML modelleri, A/B test altyapısı | Trendyol, Getir, Hepsiburada |
| **4. Veri Kulturû** | Data-driven karar alma, self-serve | Bazi fintech ve teknoloji sirketleri |

**Genel Gorunum:** Turkiye'de veri okuryazarligi artiyor ancak hala gelismis ulkelere kiyasla erken asamada. En olgun sektorler: finans, telekom, e-ticaret.

### 15.2 Populer Araclar

Turkiye'de en yaygin kullanilan veri analizi araclari:

1. **Excel** — Her sirkette, her departmanda. En yaygin.
2. **Power BI** — Kurumsal dunyada lider. Dusuk maliyet, Microsoft entegrasyonu.
3. **Tableau** — Buyuk olcekli sirketlerde, pazarlama ve satis ekiplerinde.
4. **Looker Studio** — Startup ve KOBi'lerde, ozellikle dijital pazarlama ajanslarinda.
5. **Google Analytics / GA4** — Web ve mobil analitik icin sektor standardi.
6. **Python** — Buyuyeora, ozellikle finans ve teknoloji sirketlerinde.
7. **SQL** — Her veri analistinin olmazsa olmazi.

### 15.3 Talent Market (Yetli Piyasası)

**Talep:** Turkiye'de veri analisti talebi son 3 yilda %200 artti (Kariyer.net verileri).

**Maas Araliklari (2025, brut TL):**

| Pozisyon | Giris Seviyesi | Orta | Kdemli |
|----------|---------------|------|--------|
| Veri Analisti | 25,000 - 35,000 | 35,000 - 55,000 | 55,000 - 80,000 |
| Is Zekasi Uzmani | 30,000 - 40,000 | 40,000 - 60,000 | 60,000 - 85,000 |
| Veri Bilimci | 40,000 - 55,000 | 55,000 - 80,000 | 80,000 - 130,000+ |

**Aranan Beceriler:**
- SQL (ileri seviye)
- Python veya R
- Power BI veya Tableau
- Istatistik bilgisi
- Is domain bilgisi

### 15.4 Turkiye'de Veri Analizi Ekosistemi

**Egitim:**
- Universitelerde veri bilimi bolumleri aciliyor (MEF, Ozyegin, ITU, Bogazici)
- Bootcampler: Patika.dev, Kodluyoruz, Miuul
- Sirket icinegitim programlari: Turkcell Akademi, Isbank Veri Akademisi

**Topluluklar:**
- **Veri Bilimi Dernegi** (veribilimidernegi.org)
- **Data Science Istanbul** Meetup grubu
- **Kaggle Turkiye** toplulugu
- **PyData Istanbul**

**Zorluklar:**
- Veri kalitesi sorunlari (eksik, tutarsiz, structural data eksikligi)
- Data-driven kulturun henuz tam oturmamasi
- Veri gizligi (KVKK) ile veri kullanimi arasindaki denge
- Yetenek acigi: yetistirilmis veri profesyoneli sayisi talebin gerisinde

**Firsatlar:**
- Geleneksel sektorlerde (perakende, uretim, lojistik) dijital donusum potansiyeli
- Acik veri kaynaklarinin artmasi
- Bulut BI cozumlerinin yayginalasmasi (maliyet avantaji)
- AI destekli analiz araclariyla veri analizinin demokratiklesmesi

---

## 16. Web Scraping Etigi

Web scraping, internet uzerindeki verileri otomatik olarak toplama yontemidir. Ancak bu guclu yontem, yasal ve etik sinirlar dahilinde kullanilmalidir.

### 16.1 robots.txt

Web sitelerinin `robots.txt` dosyasi, hangi bolumlerinin taranabilecegini belirtir:

```
User-agent: *
Disallow: /admin/
Disallow: /private/
Allow: /products/
Crawl-delay: 10
```

- `robots.txt` yasal bir zorunluluk degil, bir nezaket kuralidir
- Ancak buna uymamak, sitenin sizi IP engeline takmasina yol acabilir
- Ticari scraping projelerinde robots.txt'ye uymak hukuki acidan tavsiye edilir

### 16.2 Terms of Service (ToS)

Cogu web sitesi, kullanim kosullarinda (ToS) otomatik veri toplamayi yasaklar:

- **Ihlal Durumu:** ToS'u ihlal ederek veri toplamak, size karsi hukuki yaptirimlara yol acabilir (Sozlesme Ihlali)
- **Ornek:** LinkedIn vs hiQ Labs davasinda, acik profil verilerinin scraping'i serbest bulunmustur ancak bu her site icin gecerli degildir
- **Onlem:** Ticari bir scraping projesine baslamadan once mutlaka site ToS'unu inceleyin

### 16.3 Hukuki Sinirlar

- **KVKK (Turkiye):** Kisisel verilerin izinsiz toplanmasi KVKK kapsaminda suctur
- **GDPR (AB):** AB vatandaslarinin verilerini scraping yoluyla toplamak, GDPR'un acik riza sarti nedeniyle risklidir
- **DMCA:** Icerik korumali sitelerden veri kopyalamak telif hakki ihlali olabilir
- **Veri Deposu Olusturma:** Toplanan veriyi tekrar satmak veya bir veri tabani olarak sunmak ayri bir hukuki sorumluluk dogurur

**Is Dunyasi Icin Cikarim:** Veri toplama surecinde "yapabiliyorum" ile "yapmali miyim?" arasindaki farki anlamak, hem etik hem hukuki acidan kritiktir.

---

## 17. ML Temelleri (Is Insanlari Icin)

Makine ogrenmesi (ML), veri analizinden farkli olarak, oruntuleri insan mudahalesi olmadan ogrenen ve tahmin yapan sistemlerdir. Is insanlarinin ML'in temel kavramlarini anlamasi, veri ekipleriyle saglikli iletisim kurmak icin kritiktir.

### 17.1 Overfitting (Asiri Uyum)

Overfitting, bir ML modelinin egitim verisine cok iyi uyum saglamasi ancak yeni (gorulmemis) veride basarisiz olmasidir.

**Ornek:**
```python
# Ogrenci sinav tahmin modeli
# Overfit model: Her ogrencinin gecmis 10 sinavini ezberler
# Iyi model: Ogrencinin calisma suresi, uyku duzeni gibi genel egilimleri ogrenir
```

**Overfitting Belirtileri:**
- Egitim basarisi cok yuksek (%99) ama test basarisi dusuk (%60)
- Model, verideki gurultuyu (noise) de "ogrenir"
- Karmaik modeller (cok fazla parametre) overfit'e daha yatkindir

**Cozum:**
- **Cross-validation:** Veriyi birden fazla parcaya bolup her parcada ayri ayri test etme
- **Regularization:** Modeli basit tutmaya zorlayan ceza mekanizmasi (L1, L2)
- **Daha fazla veri:** Overfit genelde az veriyle cok parametre oldugunda olusur
- **Early stopping:** Model egitimini fazla ilerletmeden durdurma

### 17.2 Cross-Validation (Capraz Dogrulama)

Bir modelin ne kadar iyi oldugunu guvenilir sekilde olcme yontemidir.

**k-Fold Cross-Validation:**
```
Veri seti: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

Fold 1: Egitim [2-10] -> Test [1]
Fold 2: Egitim [1, 3-10] -> Test [2]
...
Fold 5: Egitim [1-5, 7-10] -> Test [6]
```

Her fold'dan alinan basari orani ortalamasi, modelin gercek performansini gosterir.

**Is Dunyasinda Cross-Validation:**
- Bir kredi risk modeli, musterilerin %80'inde egitilip %20'sinde test edilmelidir
- Mevsimsel verilerde, zaman serisi cross-validation kullanilmalidir (gelecekteki veriyi egitimde kullanma)
- Marketing attribution modellerinde cross-validation, kampanya etkisinin gercekci olculmesini saglar

### 17.3 Feature Importance (Ozellik Onemi)

Feature importance, bir ML modelinde hangi degiskenlerin tahmin uzerinde en cok etkiye sahip oldugunu gosterir.

**Is Dunyasi Ornegi (Musteri Kayip Tahmini):**

| Ozellik (Feature) | Onem Skoru | Yorum |
|-------------------|------------|-------|
| Son 30 gun icinde giris sayisi | 0.35 | En kritik faktor |
| Musteri yas (tenure) | 0.22 | Uzun sureli musteriler daha az kaybediyor |
| Destek talebi sayisi | 0.18 | Cok talep eden musteriler risk altinda |
| Ortalama harcama | 0.15 | Dusuk harcama kayip sinyali |
| Referans sayisi | 0.10 | Referans veren musteriler daha sadik |

**Kullanim Alani (Is Insanlari Icin):**
- Feature importance, "hangi musteri segmentine odaklanmaliyiz?" sorusuna veriye dayali yanit verir
- Kaynak tahsisinde onceliklendirme yapmayi saglar (ornegin, en onemli ozellige gore aksiyon plani)
- Black-box modellerde aciklanabilirlik saglar (hangi faktorlerin karari etkiledigini gosterir)

---

## 18. Behavioral Analytics

Behavioral analytics, kullanicilarin bir urun veya hizmet icindeki davranislarini anlamak icin kullanilan analitik yontemlerdir. Geleneksel analitikten (sayfa gosterimi, tekil ziyaretci) farkli olarak, kullanicinin "ne yaptigina" odaklanir.

### 18.1 Funnel Analizi (Huni Analizi)

Funnel analizi, kullanicilarin belirli bir aksiyona (ornegin: satin alma, kayit olma) ulasana kadar gectigi asamalari inceler.

**Ornek: E-ticaret Donusum Hunisi**
```
1. Ana sayfa ziyareti      100,000 (%100)
2. Urun sayfasi inceleme    35,000 (%35)
3. Sepete ekleme            12,000 (%12)
4. Odeme baslatma            5,000 (%5)
5. Satin alma tamamlama      3,200 (%3.2)
```

**Funnel Analizi Sorulari:**
- Hangi asamada en cok kullanici kaybi var? (2. asamada %65 kayip)
- Bu kayip sektor ortalamasina gore yuksek mi?
- Belirli segmentler (mobil vs desktop) arasinda fark var mi?
- Son 3 ayda funnel iyilesti mi, kotulesti mi?

### 18.2 Event Tracking (Olay Takibi)

Event tracking, kullanicinin dijital bir urun icindeki her eylemini kaydetme yontemidir.

**Temel Event Strukturu:**
```json
{
  "event": "button_click",
  "properties": {
    "button_name": "satinal",
    "page": "odeme_sayfasi",
    "user_id": "12345",
    "device": "mobile",
    "timestamp": "2026-07-15T14:30:00Z"
  }
}
```

**Takip Edilmesi Gereken Temel Event'ler:**
- **Page View:** Sayfa gorumutuleme
- **Click:** Tiklamalar (buton, link, goruntu)
- **Form Submission:** Form gonderimi
- **Scroll:** Sayfa kaydirma derinligi
- **Session Start/End:** Oturum baslangici/bitisi
- **Purchase:** Satin alma islemi
- **Error:** Karsilasilan hatalar

### 18.3 Mixpanel / Amplitude Gibi Platformlar

Bu platformlar, event-based analitigin en populer araclari arasindadir.

**Mixpanel:**
- Kullanicilari event dizileri uzerinden segmentlere ayirma
- Retention, funnel, ve revenue analizleri
- Kullanim alani: Urun ekipleri, growth ekipleri
- **Turkiye'de:** Ozellikle teknoloji startup'lari arasinda populer

**Amplitude:**
- **Behavioral Graph:** Kullanicilarin urun icindeki dogal akisini haritalama
- **Microscope:** Kucuk kullanici gruplarindaki davranis farkliliklarini analiz
- **Predictive Analytics:** ML tabanli churn tahmini, LTV tahmini
- **Kullanim alani:** Urun yonetimi, veri ekipleri

**Sectiginiz Platformun Ozet Karsilastirmasi:**

| Kriter | Mixpanel | Amplitude | Google Analytics |
|--------|----------|-----------|-----------------|
| Event-based | Evet | Evet | Sinirli |
| Funnel | Gelismis | Gelismis | Temel |
| Retention | Gelismis | Gelismis | Temel |
| User segments | Guclu | Guclu | Orta |
| Fiyatlandirma | Kullanim bazli | Kullanim bazli | Ucretsiz (GA4) |
| AI/ML ozellikleri | Sinirli | Guclu | Sinirli |

### 18.4 Behavioral Analytics Is Dunyasi Icin Neden Onemli?

- **Urun Gelistirme:** Hangi ozelliklerin kullanildigini ve hangilerinin kullanilmadigini gosterir
- **Aktivasyon:** Yeni kullanicilari "Aha!" anina goturen en kisa yol haritasini cikartir
- **Retention:** Kullanicilari elde tutan eylemleri belirler ve churn oncesi uyari verir
- **Monetizasyon:** Hangi davranislarin satin alma ile sonuclandigini gosterir
- **Segmentasyon:** Kullanicilari davranis sekillerine gore gruplar (power user, casual user, dormant)

---

## 19. Veri Kalitesi Cercevesi

Veri kalitesi, veri analizinin en kritik ama en sik goz ardi edilen boyutudur. "Cop giren, cop cikar" (garbage in, garbage out) prensibi geregi, kalitesiz veriyle yapilan analizler yaniltici sonuclar verir.

### 19.1 DQ Dimensions (Veri Kalitesi Boyutlari)

Veri kalitesi 6 temel boyutta degerlendirilir:

| Boyut | Tanim | Ornek Soru | Olcum Yontemi |
|-------|-------|-----------|---------------|
| **Accuracy (Dogruluk)** | Verinin gercegi yansitma derecesi | "Musteri adresi dogru mu?" | Gercek veriyle karsilastirma |
| **Completeness (Butunluk)** | Eksik veri orani | "Kac musteri telefon numarasi eksik?" | NULL deger yuzdesi |
| **Consistency (Tutarlilik)** | Verinin farkli kaynaklarda ayni olmasi | "CRM'deki musteri adi faturadakiyle ayni mi?" | Kaynaklar arasi karsilastirma |
| **Timeliness (Guncellik)** | Verinin ne kadar guncel oldugu | "Son guncelleme ne zaman yapildi?" | Zaman damgasi kontrolu |
| **Validity (Gecerlilik)** | Verinin belirlenen formata uygunlugu | "E-posta adresi format olarak dogru mu?" | Regex format kontrolu |
| **Uniqueness (Benzersizlik)** | Tekrar eden kayit orani | "Ayni musteri kac kez kaydedilmis?" | Duplicate tespiti |

### 19.2 Is Dunyasinda Veri Kalitesi Problemleri

**Yaygin Sorunlar:**
- **Insan Hatasi:** Manuel veri girisi hatalari (yanlis yazilan isimler, yanlis fiyat girisi)
- **Sistem Entegrasyonu:** Farkli sistemlerden gelen verilerin format uyusmazligi
- **Data Drift:** Zaman icinde veri tanimlarinin degismesi (ornegin: "aktif musteri" tanimi)
- **Orphan Records:** Silinen bir musterinin hala kayitlarda olmasi
- **Duplication:** Ayni musterinin farkli ID'lerle sistemde bulunmasi

**Ornek: Veri Kalitesinin Maliyeti**
```
Bir banka, musteri adres verisinin %15'inin hatali oldugunu tespit etti.
Bu hata:
- Posta gonderimlerinde her yil 500,000 TL israf
- Kredi risk degerlendirmesinde %8 hata payi
- Musteri memnuniyetinde %3 puan dususu
```

### 19.3 Veri Kalitesi Metrikleri ve Hedef Degerler

| Metrik | Formul | Hedef Deger |
|--------|--------|-------------|
| DQ Skoru | (Dogru kayit sayisi / Toplam kayit) x 100 | >%95 |
| Eksik Veri Orani | (Eksik alan sayisi / Toplam alan x kayit) x 100 | <%5 |
| Benzersizlik Orani | (Benzersiz kayit / Toplam kayit) x 100 | >%98 |
| Guncellik Skoru | (Son N gunde guncellenen kayit / Toplam) x 100 | Sektore gore degisir |

### 19.4 Veri Kalitesi Yonetimi

**Adim 1: Degerlendirme (Assessment)**
- Mevcut verinin kalite boyutlarinda olculmesi
- Kritik veri unsurlarinin belirlenmesi (Critical Data Elements)

**Adim 2: Temizlik (Cleansing)**
- Duplicate kayitlarin birlestirilmesi (deduplication)
- Eksik verilerin doldurulmasi veya temizlenmesi
- Standart disi formatlarin duzeltilmesi

**Adim 3: Izleme (Monitoring)**
- Otomatik DQ kontrol mekanizmalari kurulmasi
- Hata alarm sistemleri olusturulmasi
- Periyodik DQ raporlari

**Adim 4: Yonetisim (Governance)**
- Veri sahiplerinin (data owner) belirlenmesi
- Veri kalitesi sorumluluk matrisi
- DQ politikasi ve prosedurlerinin olusturulmasi

### 19.5 Turk Sirketlerinde Veri Kalitesi

Turkiye'de veri kalitesi, ozellikle geleneksel sektorlerde (perakende, uretim, lojistik) ciddi bir sorundur:

- **Eksik veya guncel olmayan veri:** Kucuk ve orta olcekli firmalarda veri girisi duzgun yapilmamaktadir
- **Farkli sistemlerde tutarsiz veri:** Ayni musteri, CRM'de baska, ERP'de baska adla kayitli olabilir
- **KVKK uyumlulugu:** Veri temizligi ayni zamanda KVKK kapsaminda zorunludur (yanlis veya guncel olmayan verilerin silinmesi gerekebilir)

**Firsat:** Veri kalitesine yatirim yapan sirketler, ayni sektordeki rakiplerine gore %20-30 daha dogru analiz yapabilir ve bu dogrudan karar kalitesine yansir.

---

*"Without data, you're just another person with an opinion." — W. Edwards Deming*
