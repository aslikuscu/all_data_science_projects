### Proje Başlığı: Kredi Kartı Müşteri Segmentasyonu

Bu projede, bir kredi kartı müşteri veri setini analiz ederek kullanıcıları farklı özelliklere göre gruplamak amaçlanmıştır. Proje kapsamında, veri ön işleme, temel istatistiksel analizler ve kümeleme yöntemleri kullanılarak müşteri segmentleri belirlenmiştir.

---

## İçindekiler

- [Veri Seti ve Problem Tanımı](#veri-seti-ve-problem-tanımı)
- [Veri Analizi ve İstatistiksel Bilgiler](#veri-analizi-ve-istatistiksel-bilgiler)
- [Kullanılan Yöntemler ve Modeller](#kullanılan-yöntemler-ve-modeller)
- [Kümeleme Analizi](#kümeleme-analizi)
- [Proje Sonuçları](#proje-sonuçları)

---

### Veri Seti ve Problem Tanımı

Bu veri seti, kredi kartı kullanıcılarına ait çeşitli özellikleri içermektedir. Amacımız, bu verileri kullanarak kullanıcıları benzer davranışsal özelliklere göre gruplamak ve müşteri segmentlerini belirlemektir.

**Veri setinde yer alan bazı özellikler:**
- **BALANCE:** Kullanıcının bakiyesi
- **PURCHASES:** Toplam alışveriş tutarı
- **CASH_ADVANCE:** Nakit avans kullanımı
- **CREDIT_LIMIT:** Kredi kartı limiti
- **PAYMENTS:** Ödemeler
- **TENURE:** Müşterinin kaç dönemdir kredi kartını kullandığı

### Veri Analizi ve İstatistiksel Bilgiler

Veri seti üzerinde öncelikle eksik değerlerin doldurulması ve özelliklerin dağılımlarının incelenmesi için istatistiksel analizler yapılmıştır. Aşağıdaki analizlerden bazıları gerçekleştirilmiştir:

1. **Korelasyon Analizi:** 
   - Kredi kartı limiti ve bakiye arasındaki korelasyon
   - Alışveriş sıklığı ve nakit avans kullanımı arasındaki ilişki
2. **Müşteri Segmentleri:** 
   - En yüksek kredi limiti ve en uzun süreli müşterilerin analizi
3. **Ödeme Alışkanlıkları ve Alışveriş Türü Analizi:** 
   - Ödeme oranı, minimum ödemeler ve alışveriş sıklıkları analiz edilmiştir.

### Kullanılan Yöntemler ve Modeller

Proje kapsamında **K-means kümeleme algoritması** kullanılarak müşteri segmentasyonu gerçekleştirilmiştir. Bu süreçte:

1. **Veri Normalizasyonu:** `StandardScaler` kullanılarak veriler ölçeklendirilmiştir.
2. **K-means Kümeleme:** Kullanıcıların davranışsal özellikleri dikkate alınarak 4 farklı segment belirlenmiştir.

### Kümeleme Analizi

Her küme için en iyi ve en kötü özellikler belirlenmiştir. Bu özellikler, kümelerin hangi kullanıcı davranış özellikleri üzerinde yoğunlaştığını anlamamıza yardımcı olmuştur. Kümeleme sonuçlarına göre:

- **Cluster 0:** En iyi özellik `CREDIT_LIMIT`, en kötü özellik `INSTALLMENTS_PURCHASES`
- **Cluster 1:** En iyi özellik `CREDIT_LIMIT`, en kötü özellik `CASH_ADVANCE`
- **Cluster 2:** En iyi özellik `PAYMENTS`, en kötü özellik `CASH_ADVANCE`
- **Cluster 3:** En iyi özellik `CREDIT_LIMIT`, en kötü özellik `INSTALLMENTS_PURCHASES`

### Proje Sonuçları

Bu analiz sonucunda, kredi kartı müşterilerinin özelliklerine göre segmentasyonu yapılarak her bir müşteri grubunun davranış eğilimleri ortaya konmuştur. Bu segmentasyon, şirketlerin müşteri yönetimi, pazarlama ve strateji geliştirme süreçlerinde yol gösterici olabilir.

--- 

> Projenin detayları, veri işleme adımları ve kullanılan algoritmaların kodları hakkında daha fazla bilgi için bu deposundaki ilgili Python dosyasına göz atabilirsiniz.
