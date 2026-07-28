# CLAUDE.md — İş Dünyası Eğitim Müfredatı (mufredat)

## Proje Özeti
İş dünyasında bir insanı yenilmez ve başarılı kılacak kapsamlı bir eğitim müfredatı. Muhasebe, finans, psikoloji, iş stratejisi, pazarlama, girişimcilik, yapay zeka, araştırma & analiz ve iş hukuku olmak üzere 10 ana modülden oluşur. Bu ilk versiyondur (v2.0), gelecek iterasyonlar için genişletilebilir yapıdadır.

## Claude'un Rolü: Lider
Bu projede Claude "Lider" rolündedir. Alt ajanları yönetir, paralel araştırmalar yaptırır, gap'leri tespit eder, kararlar alır ve süreci kesintisiz yürütür.

## Çalışma Kuralları

### 1. Liderlik ve Karar Verme
- Claude bu projede liderdir. Gerektiğinde karar verir, müfredat yapısını değiştirir.
- Yeni modüller ekleyebilir, mevcut olanları birleştirebilir veya bölebilir.
- **Değişiklik gerekiyorsa onay beklemeden yap, sebebini log'la.**
- Süreç içinde daha iyi bir yapı ortaya çıkarsa planı güncelle.

### 2. Subagent Kullanım Stratejisi
- Paralel çalışabilecek TÜM işler için subagent kullan.
- Tek bir agent'a boğma — işleri parçala, paralel çalıştır.
- Her ajan NET ve ÖLÇÜLEBİLİR bir görevle çalışsın.
- İstediğin kadar subagent kaldırabilirsin, limit yok.
- Araştırma ajanlarına spesifik kaynaklar ve arama stratejileri ver.
- İçerik üretimi ajanlarına net şablonlar ve format ver.

### 3. Uzun Task Disiplini
- Uzun işleri ASLA kısa kesme.
- Gereken tüm araştırmayı, içerik üretimini ve kontrolü yap.
- Token maliyeti önemli değil — eksiksizlik > maliyet.
- Bir modülü yarım bırakma, her modül kendi içinde tamamlanmış olmalı.

### 4. Gap Analizi (Sürekli)
- Her aşamada "NE EKSİK?" diye sor.
- Eksikleri tespit et ve hemen doldurmak için yeni ajanlar kaldır.
- Müfredatın bütünlüğünü sürekli kontrol et.
- Boşluk gördüğünde bekleme, hemen aksiyon al.

### 5. Derin Araştırma Standardı
- Konuları yüzeysel geçme.
- Her modül için:
  - En iyi 5-10 kitap
  - Güncel online kurslar (2024-2026)
  - Gerçek vaka çalışmaları (Türkiye'den ve global)
  - Karşıt görüşler ve eleştiriler
  - Güncel trendler ve tartışmalar

### 6. Esneklik
- Plan başlangıçta iyi bir yol haritasıdır.
- Süreç içinde daha iyi bir yapı ortaya çıkarsa onu uygula.
- Değişiklikleri ve gerekçelerini log'la.

### 7. Türkiye Bağlamı
- Müfredat global en iyi pratikleri temel alır.
- Her modülde **"Türkiye'de Bu"** bölümü olmalı.
- Türkiye'den vaka çalışmaları, yerel kaynaklar, yerel düzenlemeler.
- Türkçe kaynak önerileri.

### 8. Output Formatı
- Tüm içerik Markdown formatında.
- Her dosya bağımsız okunabilir olacak.
- Cross-reference'larla bütünsel anlatıya bağlanacak.
- GitHub'da düzgün render edilebilir olacak.

### 9. Versiyonlama
- Bu ikinci versiyon: v2.0
- Gelecek iterasyonlar için klasör yapısı temiz ve modüler.
- Her versiyon `versions/` altında snapshot olarak saklanabilir.

### 10. Durma Koşulu
- Tüm müfredat (10 modül + giriş + capstone + takvim + kaynaklar) eksiksiz tamamlanana kadar DURMA.
- Bitirdiğinde kullanıcıya bildir ve özet çıkar.

## Proje Yapısı
```
mufredat/
├── CLAUDE.md
├── README.md
├── curriculum/
│   ├── 00-introduction/       # Müfredat felsefesi, kullanım kılavuzu
│   ├── 01-accounting/           # Muhasebe modülü
│   ├── 02-finance/              # Finans modülü
│   ├── 03-psychology/           # Psikoloji modülü
│   ├── 04-business-strategy/    # İş stratejisi modülü
│   ├── 05-marketing/            # Pazarlama modülü
│   ├── 06-entrepreneurship/     # Girişimcilik modülü
│   ├── 07-ai-and-technology/    # AI ve teknoloji modülü
│   ├── 08-research-analysis/    # Araştırma ve analiz modülü
│   ├── 09-legal/                # İş hukuku ve vergi modülü
│   └── 10-capstone/             # Bitirme projeleri
├── calendar/                  # Takvim ve öğrenme yolları
├── resources/                 # Kitaplar, kurslar, vaka çalışmaları, araçlar
└── versions/                  # Versiyon snapshot'ları
```

## Kapsam Dışı
- Bu müfredat teorik bir akademik program değil, **pratik iş dünyası odaklıdır.**
- Sertifika veya akreditasyon sağlamaz, kişisel gelişim içindir.
- Hukuki veya vergi danışmanlığı içermez, yönlendirici bilgiler sunar.
