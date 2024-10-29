## Starbucks Ürünleri Besin Analizi Projesi

### İçindekiler
1. [Konu](#konu)
2. [Veri Seti](#veri-seti)
3. [Yöntemler](#yöntemler)
4. [Veri Görselleştirme](#veri-görselleştirme)
5. [Modelleme ve Doğrulama](#modelleme-ve-dogrulama)
6. [Sonuç](#sonuc)

---

### Konu
Bu projede, Starbucks’a ait ürünlerin besin değerleri analiz edilerek ürünlerin kategorilerinin (ör. bakery, hot breakfast) tahmin edilebilmesi amaçlanmıştır. Besin değerleri, kaloriler, yağ, karbonhidrat, lif ve protein değerlerini içermektedir. Bu veriler kullanılarak ürünlerin besin içeriklerine göre sınıflandırılması yapılmıştır.

---

### Veri Seti
Proje kapsamında kullanılan veri seti, her bir Starbucks ürününe ait besin değerlerini içermektedir:
- **Özellikler**: Kalori, yağ, karbonhidrat, lif ve protein
- **Hedef Değişken**: Ürün türü (örneğin: bakery, sandwich, hot breakfast)

---

### Yöntemler
Proje, aşağıdaki adımlar kullanılarak yürütülmüştür:
1. **Veri Keşfi ve Ön İşleme**: Veri türlerinin, eksik değerlerin ve özet istatistiklerin incelenmesi.
2. **Veri Görselleştirme**: Ürün türlerine göre kalori, protein ve karbonhidrat gibi besin değerlerinin dağılımlarının ve yoğunluk grafiklerinin incelenmesi.
3. **Makine Öğrenmesi Modeli**: Ürün türlerini tahmin edebilmek için bir Karar Ağacı Sınıflandırıcısı (Decision Tree Classifier) oluşturulmuştur.

---

### Veri Görselleştirme
Besin analizinde verileri daha iyi anlamak için görselleştirmeler kullanılmıştır:
- **Ürün Sayıları**: Her ürün türüne göre Starbucks’ta kaç ürün bulunduğunu gösteren grafikler oluşturuldu.
- **Kalori, Protein ve Karbonhidrat Dağılımları**: Kalori, protein, yağ ve karbonhidrat değerlerinin yoğunluk grafikleri incelenmiştir.

Aşağıda bazı örnek görselleştirmeler bulunmaktadır:
- Ürün türlerine göre ürün sayılarının dağılımı (`sns.countplot` ile)
- Kalori, protein, yağ ve karbonhidrat yoğunluk grafikleri (`sns.displot` ile)

---

### Modelleme ve Doğrulama
Proje kapsamında **Karar Ağacı Sınıflandırıcısı** kullanılarak model oluşturulmuştur:
1. **Veri Setinin Bölünmesi**: Veri seti eğitim ve test verisi olarak %80-%20 oranında ayrıldı.
2. **Model Eğitimi**: Karar Ağacı modeli eğitim verisi ile eğitildi.
3. **Doğruluk Hesaplaması**: Modelin test verisindeki doğruluğu hesaplanmıştır ve **%75 doğruluk** oranı elde edilmiştir.
4. **Örnek Tahmin**: Model üzerinde 300 kalori, 3 gram yağ, 60 gram karbonhidrat, 1 gram lif ve 5 gram protein değerine sahip bir ürünün tahmini yapılmış ve model bu ürünü “parfait” olarak sınıflandırmıştır.

#### Karar Ağacı Görselleştirmesi
Modelin karar yapısı görselleştirilerek, ürün sınıflandırmasının nasıl yapıldığı incelenmiştir.

---

### Sonuç
Bu projede, Starbucks ürünlerinin besin değerlerine göre kategorize edilmesi başarılı bir şekilde yapılmıştır. %75 doğruluk oranı ile model, besin özelliklerine göre ürün türü tahmininde oldukça başarılıdır. İlerleyen çalışmalarda model performansı daha karmaşık modellerle iyileştirilebilir. 

