# Sahte Haber Tespit Projesi

## İçindekiler
- [Amaç](#amaç)
- [Aşamalar](#aşamalar)
- [Kullanılan Yöntemler](#kullanılan-yöntemler)
- [Sonuçlar](#sonuçlar)

---

## Amaç
Bu projenin amacı, metinsel içeriği analiz ederek sahte haberleri tespit edebilen bir makine öğrenimi modeli geliştirmektir. Model, haber veri setinden çıkarılan metinsel özelliklere dayanarak bir haberin gerçek mi yoksa sahte mi olduğunu tahmin eder.

---

## Aşamalar
1. **Veri Yükleme**: 
   - Haber makalelerini içeren veri seti (başlıklar, yazarlar ve etiketler) yüklendi.

2. **Veri Ön İşleme**: 
   - Eksik değerler boş string ile dolduruldu.
   - İlgili metin alanları (ör. yazar ve başlık) analiz için tek bir özellikte birleştirildi.
   - Gereksiz kelimeleri kaldırmak ve kelimeleri köklerine indirgemek için metin temizleme ve kökleme işlemleri yapıldı.

3. **Metin Vektörleştirme**: 
   - Metinsel veriler, makine öğrenimi için sayısal temsillere dönüştürülmek üzere `TfidfVectorizer` kullanıldı.

4. **Veri Bölme**:
   - Veri seti, etiket dağılımını korumak için katmanlı örnekleme ile eğitim (%80) ve test (%20) setlerine ayrıldı.

5. **Model Eğitimi**:
   - Eğitim verilerini kullanarak Lojistik Regresyon modeli eğitildi.

6. **Model Değerlendirmesi**:
   - Modelin hem eğitim hem de test veri setlerindeki performansı doğruluk puanları ile değerlendirildi.

7. **Tahmin**:
   - Yeni veriler için etiket tahmini yapıldı ve gerçek değerlerle karşılaştırıldı.

---

## Kullanılan Yöntemler
- **Metin Ön İşleme**:
  - Özel karakterlerin kaldırılması.
  - Küçük harfe dönüştürme.
  - Stop kelimelerin kaldırılması.
  - Porter Stemmer kullanılarak kökleme işlemi.

- **Özellik Çıkarımı**:
  - Terim Frekansı-Ters Doküman Frekansı (TF-IDF) vektörizasyonu.

- **Makine Öğrenimi**:
  - İkili sınıflandırma (gerçek vs. sahte haberler) için Lojistik Regresyon sınıflandırıcısı.

---

## Sonuçlar
- **Eğitim Doğruluğu**: %98.66
- **Test Doğruluğu**: %97.91

Model, yüksek doğruluk oranıyla çalışmakta olup, gerçek ve sahte haberleri etkili bir şekilde ayırt edebilmektedir.

### Örnek Tahmin
- **Girdi**: Haber metni (vektörleştirilmiş).
- **Çıktı**: `Gerçek` veya `Sahte`
- **Örnek**:
  - **Tahmin**: Gerçek
  - **Gerçek**: Gerçek

---


