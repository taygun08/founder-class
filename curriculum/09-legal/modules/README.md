# Alt Modüller: İş Hukuku ve Vergi

Bu dosya, ana modülü oluşturan dört haftalık içeriğin **alt modül (sub-module) yapısını** gösterir. Her alt modül bağımsız olarak ele alınabilir veya diğer modüllerle (Finans, Girişimcilik) birleştirilebilir.

---

## Modül 1: Şirketler Hukuku (Corporate Law)

| Öğe | Açıklama |
|---|---|
| **Etiket** | `legal-corporate` |
| **Süre** | 1 hafta (~8 saat) |
| **Ön Koşul** | Yok |
| **Bağımlı Olduğu Alt Modüller** | Yok |
| **Verdiği Çıktı** | Ana sözleşme taslağı, şirket türü karşılaştırma tablosu |

### Alt Konular (Sub-Topics)

1. **Tüzel Kişilik Türleri** (Types of Legal Entities)
   - Anonim Şirket (A.Ş. / Joint Stock Company)
   - Limited Şirket (Ltd. Şti. / Limited Liability Company)
   - Şahıs İşletmesi (Sole Proprietorship)
   - Kollektif / Komandit Şirket (Partnership / Limited Partnership)
   - Karşılaştırmalı avantaj/dezavantaj tablosu

2. **Kuruluş Süreci** (Incorporation Process)
   - MERSİS kaydı ve e-imza gereksinimi
   - Ana sözleşme hazırlığı
   - Ticaret siciline tescil
   - Vergi dairesi kaydı

3. **Yönetim ve Karar Alma** (Management & Decision-Making)
   - Yönetim kurulu (board of directors) — A.Ş.
   - Müdürler (managers) — Ltd. Şti.
   - Genel kurul (general assembly)
   - Azınlık hakları (minority rights)

4. **Hisse Devri ve Sermaye Değişikliği** (Share Transfer & Capital Change)
   - Hisse devir sözleşmesi (share transfer agreement)
   - Önalım hakkı (pre-emption right / right of first refusal)
   - Esas sermaye artırımı (capital increase) / azaltımı (capital decrease)

### Uygulama Araçları (Tools)

- MERSİS (mersis.gtb.gov.tr)
- Ticaret Sicili Gazetesi sorgulama
- e-Devlet şirket bilgileri sorgulama

### Diğer Modüllerle Entegrasyon

- **Finans Modülü** ile: Öz kaynak/yabancı kaynak dengesi, şirket sermaye yapısı
- **Girişimcilik Modülü** ile: İş planında tüzel kişilik seçimi, ortaklık sözleşmesi

---

## Modül 2: Sözleşme ve Fikri Mülkiyet (Contracts & Intellectual Property)

| Öğe | Açıklama |
|---|---|
| **Etiket** | `legal-contracts-ip` |
| **Süre** | 1 hafta (~8 saat) |
| **Ön Koşul** | `legal-corporate` (önerilen) |
| **Bağımlı Olduğu Alt Modüller** | Yok |
| **Verdiği Çıktı** | NDA şablonu, lisans sözleşmesi taslağı, IP strateji notu |

### Alt Konular (Sub-Topics)

1. **Sözleşme Hukuku Temelleri** (Contract Law Basics)
   - Sözleşme unsurları (teklif / kabul / irade)
   - Şekil şartları (yazılı / noter / resmi)
   - Sözleşme özgürlüğü (freedom of contract) ve sınırları

2. **Temel Sözleşme Türleri** (Key Contract Types)
   - Satış sözleşmesi (sales agreement)
   - Hizmet sözleşmesi (service agreement)
   - Vekâlet sözleşmesi (agency/representation agreement)
   - Kira sözleşmesi (lease agreement)

3. **Ticari Sözleşmeler** (Commercial Contracts)
   - Gizlilik sözleşmesi (Non-Disclosure Agreement — NDA)
   - Lisans sözleşmesi (license agreement)
   - Ortak girişim sözleşmesi (joint venture agreement)
   - Bayilik / distribütörlük sözleşmesi (dealership / distributorship)

4. **Sözleşme İhlali ve Çözüm Yolları** (Breach & Remedies)
   - İfa, kısmi ifa, hiç ifa etmeme
   - Tazminat türleri (olumlu / olumsuz zarar)
   - İhtiyati tedbir (injunction)
   - Arabuluculuk (mediation) — dava şartı

5. **Fikri Mülkiyet Türleri** (Types of IP)
   - Marka (trademark) — SMK md. 4-29
   - Patent ve faydalı model (patent & utility model) — SMK md. 82-118
   - Tasarım (design) — SMK md. 55-81
   - Telif hakkı (copyright) — FSEK md. 1-15

6. **Çalışan Buluşları** (Employee Inventions)
   - 6769 sayılı SMK md. 113-119
   - Buluş bildirimi (invention disclosure)
   - Çalışan-firma arasında telif hakkı devri (assignment of rights)

### Uygulama Araçları (Tools)

- Türk Patent ve Marka Kurumu (turkpatent.gov.tr)
- WIPO IP Portal (wipo.int)
- Sözleşme şablonları (modules/templates/ dizini)

### Diğer Modüllerle Entegrasyon

- **Pazarlama Modülü** ile: Marka stratejisi, isimlendirme (branding)
- **Girişimcilik Modülü** ile: Patent araştırması, fikri mülkiyet analizi

---

## Modül 3: İş Hukuku (Labor Law)

| Öğe | Açıklama |
|---|---|
| **Etiket** | `legal-labor` |
| **Süre** | 1 hafta (~8 saat) |
| **Ön Koşul** | Yok |
| **Bağımlı Olduğu Alt Modüller** | `legal-corporate` ile paralel alınabilir |
| **Verdiği Çıktı** | İş sözleşmesi taslağı, fesih bildirimi örneği, KVKK envanteri |

### Alt Konular (Sub-Topics)

1. **İş Sözleşmesi Türleri ve Kurulması** (Types & Formation)
   - Belirli süreli / belirsiz süreli (fixed-term / indefinite-term)
   - Tam süreli / kısmi süreli (full-time / part-time)
   - Çağrı üzerine çalışma (on-call work)
   - Deneme süresi (probation period)

2. **Çalışma Koşulları** (Working Conditions)
   - Haftalık çalışma süresi (45 saat / weekly working hours)
   - Fazla mesai (overtime) — %50 zamlı ücret
   - Yıllık ücretli izin (annual paid leave — minimum 14 gün)
   - Ulusal bayram ve genel tatil (public holiday) ücreti

3. **İş Sözleşmesinin Sona Ermesi** (Termination)
   - İhbar süreleri (notice periods) — İşK md. 17
   - Kıdem tazminatı (severance pay) — İşK md. 14
   - Haklı fesih (termination for just cause) — İşK md. 25
   - Geçerli fesih (termination for valid reason) — İşK md. 18
   - İş güvencesi (job security) — 30+ çalışan şartı

4. **İş Sağlığı ve Güvenliği** (OHS)
   - Risk değerlendirmesi (risk assessment)
   - İş güvenliği uzmanı (occupational safety specialist)
   - İş yeri hekimi (workplace physician)
   - İş kazası ve meslek hastalığı (work accident & occupational disease)

5. **KVKK ve Çalışan Verisi** (Data Protection & Employee Data)
   - Çalışan rızası yerine hukuki sebep
   - Biyometrik veri (biometric data) işleme şartları
   - VERBİS kaydı yükümlülüğü
   - İş başvurusu verileri (applicant data) — 2 yıl saklama sınırı

6. **Uzaktan Çalışma Düzenlemeleri** (Remote Work)
   - İşK md. 14 (uzaktan çalışmanın tanımı)
   - Ekipman ve gider yükümlülüğü
   - Dijital gözetim / performans takibi sınırları
   - Kayıt dışı çalışma riskleri (undeclared work)

### Uygulama Araçları (Tools)

- SGK e-Bildirge sistemi (sgk.gov.tr)
- e-Devlet iş yeri bildirimleri
- KVKK VERBİS (verbis.kvkk.gov.tr)
- İş Sağlığı ve Güvenliği risk değerlendirme şablonu

### Diğer Modüllerle Entegrasyon

- **Girişimcilik Modülü** ile: Bordro yönetimi, personel el kitabı
- **Finans Modülü** ile: Kıdem tazminatı karşılığı (provision for severance), SGK prim giderleri

---

## Modül 4: Türk Vergi Sistemi (Turkish Tax System)

| Öğe | Açıklama |
|---|---|
| **Etiket** | `legal-tax` |
| **Süre** | 1 hafta (~8 saat) |
| **Ön Koşul** | `legal-corporate` (önerilen) |
| **Bağımlı Olduğu Alt Modüller** | Yok |
| **Verdiği Çıktı** | Vergi beyanname takvimi, kurumlar vergisi hesaplama, teşvik analizi |

### Alt Konular (Sub-Topics)

1. **Gelir Vergisi** (Income Tax)
   - Ticari kazanç (commercial profit) — GVK md. 37-40
   - Serbest meslek kazancı (self-employment income)
   - Ücret geliri (employment income)
   - Artan oranlı tarife (progressive tax brackets — %15 - %40)
   - Yıllık beyanname (annual return) — Mart ayı sonu

2. **Kurumlar Vergisi** (Corporate Tax)
   - Vergi matrahı hesaplaması (tax base calculation)
   - İstisnalar (exemptions) — KVK md. 5
   - İndirimler (deductions) — KVK md. 10
   - Kurumlar vergisi oranı (corporate tax rate — %25)
   - Beyanname dönemi (Nisan ayı sonu)

3. **KDV (Katma Değer Vergisi)** (VAT)
   - KDV mekanizması (KDV matrahı, indirim, mahsup)
   - KDV oranları (%20, %10, %1)
   - KDV istisnaları (KDV exemptions)
   - Ters yüz (reverse charge) — yurt dışı hizmet alımları
   - KDV iadesi (VAT refund)

4. **Stopaj ve Muhtasar Beyanname** (Withholding Tax)
   - Ücret stopajı (wage withholding)
   - Kira stopajı (rental withholding — %20)
   - Serbest meslek stopajı (professional service withholding — %20)
   - Muhtasar beyanname dönemi (her ayın 26'sı)

5. **Vergi Planlaması ve Teşvikler** (Tax Planning & Incentives)
   - Yatırım teşvik belgesi (investment incentive certificate)
   - Bölgesel teşvik sistemi (6 bölge)
   - Ar-Ge merkezi teşviki (R&D center incentives — 5746 sayılı Kanun)
   - Serbest bölge avantajları (free zone advantages)
   - Teknopark / teknoloji geliştirme bölgesi destekleri

6. **Vergi Denetimi ve Cezalar** (Tax Audit & Penalties)
   - Vergi incelemesi (tax audit) türleri
   - Vergi ziyaı cezası (tax loss penalty)
   - Usulsüzlük cezaları (procedural penalties)
   - Uzlaşma (settlement/compromise) müessesesi
   - Pişmanlık (voluntary disclosure) müessesesi

7. **Transfer Fiyatlandırması** (Transfer Pricing)
   - Emsallere uygunluk ilkesi (arm's length principle)
   - İlişkili kişi (related party) tanımı
   - Transfer fiyatlandırması raporu (yıllık)
   - Peşin fiyatlandırma anlaşması (advanced pricing agreement — APA)

### Uygulama Araçları (Tools)

- GİB İnteraktif Vergi Dairesi (intvrg.gib.gov.tr)
- e-Fatura / e-Arşiv / e-Defter portalları
- Hazine ve Maliye Bakanlığı teşvik sorgulama
- SGK teşvik hesaplama modülü

### Diğer Modüllerle Entegrasyon

- **Finans Modülü** ile: Nakit akışı planlaması, vergi optimizasyonu, KDV yönetimi
- **Girişimcilik Modülü** ile: Yatırım teşviklerinin iş planına dahil edilmesi
- **Muhasebe Modülü** ile: Bilanço esası, kayıt düzeni, belge yönetimi

---

## Modüller Arası Entegrasyon Haritası

```
                        ┌──────────────────┐
                        │ Şirketler Hukuku │
                        │ (legal-corporate)│
                        └────────┬─────────┘
                                 │
              ┌──────────────────┼──────────────────┐
              ▼                  ▼                   ▼
   ┌──────────────────┐  ┌──────────────┐  ┌──────────────────┐
   │Sözleşme ve Fikri │  │ İş Hukuku    │  │ Türk Vergi       │
   │Mülkiyet          │  │ (legal-labor)│  │ Sistemi          │
   │(legal-contracts) │  └──────┬───────┘  │ (legal-tax)      │
   └────────┬─────────┘         │          └────────┬─────────┘
            │                  │                     │
            ▼                  ▼                     ▼
   ┌─────────────────────────────────────────────────────┐
   │              FİNAL PROJESİ                          │
   │  Şirket Yapısı + İş Sözleşmesi + Vergi Planı + IP  │
   └─────────────────────────────────────────────────────┘
```

---

## Esnek Kullanım Senaryoları (Flexible Scenarios)

### Senaryo 1: Kısa Girişimcilik Programı (2 Gün)
- Sadece Modül 1 (Şirketler Hukuku) + Modül 2'nin "Fikri Mülkiyet" kısmı
- Çıktı: Şirket türü seçimi + marka başvurusu planı

### Senaryo 2: Finans Profesyonelleri İçin (1 Hafta)
- Sadece Modül 4 (Türk Vergi Sistemi) — yoğunlaştırılmış
- Çıktı: Vergi beyanname takvimi, KDV/stopaj yönetimi, teşvik hesaplamaları

### Senaryo 3: İK Profesyonelleri İçin (1 Hafta)
- Sadece Modül 3 (İş Hukuku) — derinlemesine
- Çıktı: İş sözleşmesi dosyası, fesih prosedürleri, KVKK uyum belgeleri

### Senaryo 4: Tam Modül (4 Hafta)
- Tüm alt modüller sıralı
- Final projesi: Kendi iş fikrini hukuksal/vergisel çerçevede yapılandırma
