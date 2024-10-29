
---

# Bank Churn Prediction Project

## Proje Açıklaması
Bu proje, bankacılık sektöründeki müşteri kaybını (churn) tahmin etmek amacıyla geliştirilmiştir. Müşteri verileri analiz edilerek, hangi müşterilerin bankayı terk etme olasılığının yüksek olduğunu belirlemek için makine öğrenimi yöntemleri kullanılmaktadır.

## İçindekiler
1. **Veri Seti**  
2. **Yöntemler**  
3. **Konu**  
4. **Sonuç**  

## Veri Seti
Veri seti, müşteri bilgilerini içeren 10,127 satır ve 23 sütun içermektedir. Anahtar özellikler şunlardır:
- **CLIENTNUM**: Müşteri numarası
- **Attrition_Flag**: Müşterinin bankayı terk edip etmediğini gösterir (Attrited/Existing).
- **Customer_Age**: Müşterinin yaşı
- **Gender**: Müşterinin cinsiyeti
- **Dependent_count**: Müşterinin bakmakla yükümlü olduğu kişi sayısı
- **Income_Category**: Müşterinin gelir kategorisi
- **Card_Category**: Müşterinin sahip olduğu kart kategorisi
- **Credit_Limit**: Müşterinin kredi limiti
- **Avg_Utilization_Ratio**: Ortalama kredi kullanım oranı

## Yöntemler
Müşteri kaybını tahmin etmek için kullanılan yöntemler:
- **Veri Ön İşleme**: Eksik değerlerin yönetimi ve verilerin normalizasyonu.
- **Keşifsel Veri Analizi (EDA)**: Müşteri özelliklerinin görselleştirilmesi ve ilişkilerin incelenmesi.
- **Makine Öğrenimi Modelleri**: 
  - Lojistik Regresyon
  - Rastgele Orman
  - Destek Vektör Makineleri (SVM)
  - Karar Ağaçları
- **Model Değerlendirme**: Doğruluk, F1 skoru, ROC eğrisi gibi metriklerin kullanımı.

## Konu
Bu proje, bankaların müşteri kaybını önlemek amacıyla stratejiler geliştirmesine yardımcı olacak veriye dayalı bilgiler sağlamayı hedeflemektedir. Müşteri davranışlarının analizi, bankaların daha iyi hizmet sunmalarına ve müşteri sadakatini artırmalarına katkıda bulunacaktır.

## Sonuç
Veri analizi ve modelleme sonuçları, hangi özelliklerin müşteri kaybı üzerinde daha etkili olduğunu göstermektedir. Özellikle, gelir durumu, kredi limiti ve ortalama kredi kullanım oranı gibi faktörler müşteri kaybını etkileyen önemli belirleyicilerdir. Bu bilgiler, bankaların müşteri sadakatini artırmak için stratejiler geliştirmelerine yardımcı olabilir.

## Katkıda Bulunanlar
- [Adınız] (GitHub profil bağlantınız)

## Lisans
Bu proje MIT Lisansı altında lisanslanmıştır. Daha fazla bilgi için `LICENSE` dosyasına bakın.

---

