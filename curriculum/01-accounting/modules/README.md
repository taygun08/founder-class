# MUHASEBE MODÜLÜ — MODÜL SİSTEMİ

---

## 1. MODÜL YAPISINA GENEL BAKIŞ

Bu klasör, Muhasebe modülünün haftalık ders içeriklerini, öğretim materyallerini ve değerlendirme araçlarını organize eden alt modülleri içerir. Her hafta, belirli bir öğrenme hedefine yönelik olarak yapılandırılmış bir "alt modül" olarak kabul edilir.

Modüller, muhasebe bilgisinin temelden karmaşığa doğru aşamalı bir şekilde inşa edilmesini sağlayacak şekilde tasarlanmıştır. Her alt modül bir öncekinin üzerine inşa edilir ve bir sonrakine zemin hazırlar.

---

## 2. MODÜL KATEGORİLERİ

Muhasebe modülü 4 ana kategoride organize edilmiştir:

### A. Temel Muhasebe Bilgisi (1.-2. Hafta)
- Muhasebenin kavramsal çerçevesi
- Kayıt sistemi ve dönem sonu işlemleri
- Muhasebenin "dil"ini öğrenme

### B. Finansal Raporlama (3.-5. Hafta)
- Finansal tabloların hazırlanması
- Nakit akış yönetimi
- Muhasebe standartları
- Stok değerleme

### C. Karar Desteği (6.-7. Hafta)
- Maliyet analizi ve karar verme
- Bütçeleme ve performans yönetimi
- Stratejik yönelim

### D. Güvence ve Enflasyon (8. Hafta)
- Denetim ve iç kontrol
- Enflasyon muhasebesi
- Mevzuatsal uyum

---

## 3. ALT MODÜL DOSYA YAPISI

Her hafta için aşağıdaki dosya yapısı önerilir:

```
modules/
  week-01-fundamentals/
    README.md              -- Haftanın içerik özeti
    learning-objectives.md -- Öğrenme hedefleri
    readings.md            -- Okuma listesi (kitap bölümleri, makaleler)
    lecture-notes.md       -- Ders notları / anlatım metni
    slides/                -- Sunum dosyaları (.pdf, .pptx, .md)
      week01-slides.md
    exercises/
      problem-set.md       -- Pratik alıştırmalar
      solutions.md         -- Çözümler
    case-study/
      README.md            -- Vaka çalışması açıklaması
      data/                -- Vaka verileri (Excel, CSV)
    resources/
      turkiyede-bu.md      -- "Türkiye'de Bu" bölümü detayları
      videos.md            -- Video / kurs bağlantıları
      reflection.md        -- Reflection soruları
    assessment/
      quiz.md              -- Kısa sınav
      rubric.md            -- Değerlendirme rubriği
```

Her alt modül standartlaştırılmış bir formatı takip eder. Bu, öğretim üyelerinin içeriği kolayca uyarlamasına, öğrencilerin ise tutarlı bir öğrenme deneyimi yaşamasına olanak tanır.

---

## 4. ÖĞRENME YOLU (LEARNING PATH)

Aşağıdaki akış, öğrencinin modül boyunca izleyeceği öğrenme yolunu gösterir:

```
   1. HAFTA: Muhasebenin Temelleri
         |
   2. HAFTA: Tahakkuk Esası ve Dönem Sonu İşlemleri
         |
   3. HAFTA: Bilanço ve Gelir Tablosu Hazırlama
         |
   4. HAFTA: Nakit Akış Tablosu
         |
   5. HAFTA: TMS/TFRS ve IFRS Temelleri
         |
   6. HAFTA: Maliyet Muhasebesi
         |
   7. HAFTA: Yönetim Muhasebesi
         |
   8. HAFTA: Denetim, İç Kontrol ve Enflasyon Muhasebesi
         |
   [Ara Sınav: Hafta 4 sonu]
         |
   [Final Projesi: Hafta 8 sonu]
         |
   >> Finans Modülü'ne Geçiş
```

---

## 5. ÖĞRETİM YÖNTEMLERİ

Modülde kullanılan başlıca öğretim yöntemleri:

| Yöntem | Oran | Açıklama |
|---|---|---|
| Anlatım (Lecture) | %30 | Konuların yapılandırılmış anlatımı |
| Vaka Çalışması | %25 | Gerçek hayat senaryoları üzerinde uygulama |
| Pratik Alıştırma | %20 | Bireysel problem çözümü |
| Refleksiyon | %10 | Tartışma ve yazılı yansıtma |
| Grup Çalışması | %15 | Ekip halinde vaka ve proje çözümü |

---

## 6. DEĞERLENDİRME ÇERÇEVESİ

Her alt modül için aşağıdaki değerlendirme araçları kullanılır:

| Araç | Frekans | Odak |
|---|---|---|
| Kısa Sınav (Quiz) | Haftalık | Temel kavramları ölçme |
| Pratik Alıştırma | Haftalık | Uygulama becerisi |
| Vaka Raporu | 4 kez (Hafta 2, 4, 6, 8) | Analitik düşünme |
| Ara Sınav | 1 kez (Hafta 4) | İlk 4 hafta bütünleşik |
| Final Projesi | 1 kez (Hafta 8) | Kapsamlı uygulama |

---

## 7. MODÜL GÜNCELLEME TAKVİMİ

- **Yıllık güncelleme:** TMS/TFRS değişiklikleri, SPK düzenlemeleri
- **6 aylık güncelleme:** Vaka çalışmaları ve örnek şirket verileri
- **3 aylık güncelleme:** Ekonomik veriler (TÜFE, TEFE, kurlar)
- **Sürekli güncelleme:** KAP bildirimleri, güncel mevzuat değişiklikleri

---

## 8. EK MATERYALLER

Modül içerisinde kullanılmak üzere hazırlanması planlanan ek materyaller:

- **Hesap Planı Referans Kartı:** Tek düzen hesap planının özet tablosu
- **Muhasebe Denklemi Posteri:** Görsel öğrenme için infografik
- **Finansal Tablo Şeması:** Bilanço, gelir tablosu ve nakit akış tablosu arasındaki ilişkiyi gösteren görsel
- **TMS/TFRS Kontrol Listesi:** Her standart için hatırlatma kartları
- **Excel Şablonları:** Mizan, finansal tablolar, başabaş analizi, bütçeleme için önceden hazırlanmış Excel dosyaları
- **Vaka Veri Seti Paketi:** Tüm vaka çalışmaları için standart veri seti (Excel formatında)
- **KAP İnceleme Rehberi:** KAP üzerinde şirket finansal tablolarını bulma, indirme ve yorumlama adım adım kılavuzu

---

## 9. FİNANS MODÜLÜNE KÖPRÜ

Bu modül, aşağıdaki finans konuları için doğrudan temel oluşturur:

- Finansal Oran Analizi (Likidite, Kaldıraç, Kârlılık, Faaliyet Oranları)
- DuPont Analizi
- Serbest Nakit Akışı (Free Cash Flow) Değerlemesi
- Finansal Modelleme ve Tahminleme
- Şirket Değerleme (DCF, Benzer Şirket, İşlem Benzerleri)
- Birleşme ve Satın Almalar (M&A) Due Diligence
- Sermaye Yapısı ve Ağırlıklı Ortalama Sermaye Maliyeti (WACC)

Öğrenciler bu modülde öğrendikleri finansal tablo yapısı, muhasebe standartları ve maliyet yönetimi bilgilerini Finans modülünde doğrudan kullanacaklardır.
