# Alt Moduller

Finans modulu, 8 ana konu basligi altinda yapilandirilmis alt modullerden olusmaktadir. Her alt modul, bagimsiz olarak ele alinabilecek sekilde tasarlanmis olmakla birlikte, modulun butunlugu icinde birbirini tamamlayacak sekilde siralanmistir.

---

## Alt Modul Listesi

### M1-FIN01: Finansal Okuryazarlik ve Finansal Tablolar
- **Haftalar:** 1-2
- **Temel Odak:** Uc temel finansal tablonun okunmasi, finansal oran analizi, DuPont analizi, nakit donusum dongusu
- **On Kosul:** Yok
- **Cikti Yetkinlik:** Bir sirketin finansal tablolarini okuma, yorumlama ve temel oran analizini yapabilme
- **Entegrasyon:** Muhasebe moduluyle dogrudan baglantili

### M1-FIN02: Makroekonomi Temelleri
- **Hafta:** 3
- **Temel Odak:** Faiz-enflasyon iliskisi, para politikasi, merkez bankaciligi, IS-LM modeli temelleri, doviz kuru mekanizmalari
- **On Kosul:** Yok (1. modulle es zamanli baslanabilir)
- **Cikti Yetkinlik:** Makroekonomik gostergeleri okuma, TCMB politikalari analiz etme
- **Entegrasyon:** Tum finansal kararlarin makroekonomik cercevede degerlendirilmesi

### M1-FIN03: Kurumsal Finansman (Corporate Finance)
- **Haftalar:** 4-6
- **Temel Odak:** Sermaye butcelemesi (NPV/IRR), WACC, sermaye yapisi (Modigliani-Miller), DCF degerleme, carpan analizi, M&A
- **On Kosul:** M1-FIN01
- **Cikti Yetkinlik:** Bir sirketin DCF modeliyle degerlemesini yapabilme ve yatirim kararlarini degerlendirebilme
- **Entegrasyon:** Finansal modelleme ve portfoy teorisi icin temel olusturur

### M1-FIN04: Finansal Modelleme ve Excel
- **Hafta:** 7
- **Temel Odak:** Entegre 3-statement model, Excel renk kodlama standartlari, duyarlilik analizi, senaryo yonetimi, bakiye kontrol mekanizmalari
- **On Kosul:** M1-FIN03 (DCF modelleme icin WACC ve degerleme bilgisi)
- **Cikti Yetkinlik:** Sifirdan entegre finansal model kurma ve profesyonel standartlarda dokumante etme
- **Entegrasyon:** Tum finansal analizlerin Excel uzerinde uygulanmasi

### M1-FIN05: Yatirim ve Portfoy Teorisi
- **Haftalar:** 8-9
- **Temel Odak:** Modern Portfoy Teorisi (Markowitz), CAPM, Fama-French faktor modelleri, portfoy performans olcumu, tahvil degerleme
- **On Kosul:** M1-FIN03 (WACC ve risk-getiri kavramlari)
- **Cikti Yetkinlik:** Bir portfoyun risk/getiri profilini hesaplama, beta hesaplama ve portfoy optimizasyonu yapabilme
- **Entegrasyon:** Davranissal finans ve startup finansmani icin temel olusturur

### M1-FIN06: Davranissal Finans
- **Hafta:** 10
- **Temel Odak:** Bilissel onyargilar, Beklenti Teorisi, sinirli arbitraj, piyasa anomalileri, mental muhasebe, suru psikolojisi
- **On Kosul:** M1-FIN01 (temel finansal okuryazarlik yeterli)
- **Cikti Yetkinlik:** Kendi yatirim kararlarindaki onyargilari tespit etme, piyasa anomalilerini tanima
- **Entegrasyon:** Geleneksel finans teorilerine elestirel bakis; yatirim kararlarinda psikolojik faktorlerin dikkate alinmasi

### M1-FIN07: Startup Finansmani
- **Hafta:** 11
- **Temel Odak:** Yakma orani ve pist, birim ekonomisi (LTV/CAC), cap table yonetimi, SAFE notlari, girisim sermayesi fonlama turlari, yatirimci sunumu
- **On Kosul:** M1-FIN01, M1-FIN03
- **Cikti Yetkinlik:** Bir startup icin finansal model olusturma, cap table yonetimi ve yatirimci sunumu hazirlama
- **Entegrasyon:** Girisimcilik moduluyle dogrudan baglantili

### M1-FIN08: Turkiye'de Finans (Butunlesik Bakis)
- **Hafta:** 12
- **Temel Odak:** BIST yapisi, SPK duzenlemeleri, enflasyon muhasebesi (TMS 29), KAP kullanimi, IPO sureci, Turkiye'de kurumsal finansman
- **On Kosul:** Tum onceki moduller (butunlesik sentez haftasi)
- **Cikti Yetkinlik:** Bir BIST sirketinin finansal analizini Turkiye ozelinde yapabilme ve SPK standartlarinda raporlama
- **Entegrasyon:** Tum modulun Turkiye odakli sentezi; final projesi icin temel

---

## Alt Modul Akis Semasi

```
Hafta 1-2:  M1-FIN01 (Finansal Okuryazarlik)
                 |
Hafta 3:    M1-FIN02 (Makroekonomi) ----> Hafta 1-2 ile es zamanli
                 |
Hafta 4-6:  M1-FIN03 (Kurumsal Finansman)
                 |
Hafta 7:    M1-FIN04 (Finansal Modelleme)
                 |
Hafta 8-9:  M1-FIN05 (Yatirim ve Portfoy)
                 |
Hafta 10:   M1-FIN06 (Davranissal Finans)
                 |
Hafta 11:   M1-FIN07 (Startup Finansmani)
                 |
Hafta 12:   M1-FIN08 (Turkiye'de Finans - Butunlesik)
```

---

## Harici Baglantilar

| Alt Modul | Baglantili Modul / Alan | Baglanti Turu |
|-----------|-------------------------|---------------|
| M1-FIN01 Finansal Okuryazarlik | **Muhasebe Modulu** (finansal tablo uretimi) | On kosul / Devami |
| M1-FIN02 Makroekonomi | **Genel Is Dunyasi Modulu** (is ortami analizi) | Es zamanli |
| M1-FIN03 Kurumsal Finansman | **Strateji Modulu** (sirket degerleme) | Devami |
| M1-FIN04 Finansal Modelleme | **Veri Analizi Modulu** (ileri Excel/Python) | Devami |
| M1-FIN05 Yatirim ve Portfoy | **Sermaye Piyasasi Modulu** (ileri portfoy) | Devami |
| M1-FIN06 Davranissal Finans | **Psikoloji / Karar Bilimi Modulu** | Paralel |
| M1-FIN07 Startup Finansmani | **Girisimcilik Modulu** (is plani, yatirimci) | Dogrudan bagimli |
| M1-FIN08 Turkiye'de Finans | **Hukuk / Vergi Modulu** (SPK, KVK) | Devami |

Her alt modulun detayli haftalik icerigi icin: [syllabus.md](../syllabus.md)
Tum kaynaklar icin: [references.md](../references.md)
Modul genel bakis icin: [README.md](../README.md)
