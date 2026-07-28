# M1-FIN05: Yatirim ve Portfoy Teorisi

## Ogrenme Hedefleri
- Markowitz ortalama-varyans optimizasyonu ile efektif sinir ve minimum varyans portfoyunu hesaplamak
- CAPM'in teorik temellerini, beta katsayisini ve Fama-French cok faktorlu modellerini anlamak
- Temel turev urun turlerini (forward, futures, opsiyon, swap) tanimak ve fiyatlama mantigini kavramak
- Riske Maruz Deger (VaR) hesaplama yontemlerini uygulamak
- Alternatif yatirim araclari (GYO, emtia, private equity) ve portfoy cesitlendirmesini degerlendirmek

## Okuma Listesi
- **Bodie, Z., Kane, A. & Marcus, A.** — *Investments* (12. Baski, McGraw-Hill), Bolum 6-9
- **Palomar, D.P.** — *Portfolio Optimization: Theory and Application* (Cambridge, 2025), Bolum 1-5
- **Hull, J.C.** — *Options, Futures, and Other Derivatives* (11. Baski, Pearson), Bolum 1-4, 10-12
- **Jorion, P.** — *Value at Risk* (3. Baski, McGraw-Hill), Bolum 1-5
- **Markowitz, H.** — "Portfolio Selection" (1952), *The Journal of Finance*

## Vaka Calismasi: "Berkshire Hathaway Portfoyu ve Buffett'in CAPM Elestirisi"
Warren Buffett, CAPM'in piyasa riskini tek faktorle aciklamasini elestirir. Berkshire Hathaway portfoyunun betasi genellikle 1'in altindadir ancak uzun vadeli getirileri piyasanin uzerindedir. Fama-French 3 faktor modelinin deger (HML) faktoru, Buffett'in basarisini aciklamada CAPM'den daha basarilidir. Ayrica 2008 kuresel finans krizinde risk yonetimindeki basarisizliklar ve kriz sonrasi duzenleyici degisiklikler analiz edilir.

## Pratik Alistirma
- Python (opsiyonel) veya Excel ile Markowitz efektif sinir hesaplamasi: BIST 50'den sectiginiz 5 hisse senedi icin beklenen getiri, standart sapma, korelasyon matrisi ve 10.000 farkli portfoy kombinasyonu ile efektif siniri cizin.
- Bir BIST sirketinin beta'sini 3 yillik haftalik veri ile hesaplayin ve CAPM'de kullanarak beklenen getiriyi bulun.
- Bir portfoy icin %95 ve %99 guven duzeyinde gunluk VaR hesaplamasi yapin.

## Turkiye'de Bu
BIST, gelismekte olan bir piyasa olarak yuksek volatilite ve sinirli cesitlendirme imkani sunar. BIST 100 endeksi genellikle birkac sektorun agirligini tasir. Turev urun islemleri Borsa Istanbul bunyesindeki VIOP platformunda gerceklesir. Turk sirketleri icin en yaygin turev urun kullanimi, doviz kuru riskinden korunma amacli forward ve swap sozlesmeleridir. TCMB ve BDDK, turev urun piyasasinin istikrarli isleyisi icin duzenleyici cerceveyi belirler.
