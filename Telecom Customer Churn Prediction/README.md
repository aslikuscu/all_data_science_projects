# Müşteri Churn Tahmini ve Makine Öğrenmesi

Bu proje, müşteri kaybı (churn) tahminini gerçekleştirmek için makine öğrenmesi modelleri kullanarak bir analiz süreci sunmaktadır. Amaç, çeşitli özellikler (sözleşme tipi, aylık ücret, süre vb.) üzerinden bir model oluşturarak, hangi müşterilerin kaybolacağı tahmin edilmeye çalışılmaktadır.

## İçindekiler
1. [Proje Amacı](#proje-amacı)
2. [Veri Seti](#veri-seti)
3. [Veri Analizi (EDA)](#veri-analizi-eda)
4. [Model Kurulumu](#model-kurulumu)
5. [Model Değerlendirmesi](#model-değerlendirmesi)
6. [Özelliklerin Önem Derecesi](#özelliklerin-önem-derecesi)
7. [Sonuçlar](#sonuçlar)

## Proje Amacı
Bu projede, müşteri verilerini kullanarak müşterilerin kayıp (churn) olup olmayacağını tahmin etmeyi amaçladık. Bunun için üç farklı makine öğrenmesi sınıflandırma modeli kullanıldı:
- **Karar Ağacı (Decision Tree Classifier)**
- **Rastgele Orman (Random Forest Classifier)**
- **K En Yakın Komşu (KNN - K Nearest Neighbors)**

Bu modellerin her biri, **GridSearchCV** kullanılarak hiperparametre optimizasyonuna tabi tutuldu ve model değerlendirmeleri yapıldı.

## Veri Seti
Veri seti, müşterilerin çeşitli özelliklerini içermektedir. Öne çıkan bazı özellikler şunlardır:
- **Tenure (Süresi)**: Müşterinin şirkette geçirdiği ay sayısı
- **Sözleşme Türü**: Müşterinin sözleşme tipi (aylık, yıllık, 2 yıllık)
- **Aylık Ücret (Monthly Charges)**
- **Toplam Ücret (Total Charges)**
- **Diğer Müşteri Özellikleri**: Cinsiyet, bağımlı durumu, yaş gibi.

Hedef değişkenimiz **Churn** (müşteri kaybı) olup, bu değişken 0 (churn yok) veya 1 (churn var) olarak etiketlenmiştir.

## Veri Analizi (EDA)
Veri setini inceledikten sonra bazı önemli gözlemler yapıldı:
- **Yaşlı müşteriler** genellikle daha düşük churn oranına sahip.
- **Kısa süreli müşteriler (5 aydan az)** daha yüksek churn oranına sahip.
- **Aylık sözleşmesi olan müşteriler**, yıllık sözleşmesi olanlara göre daha yüksek churn oranına sahip.
- **Aylık ücret** yüksek, fakat **toplam ücret** düşük olan müşteriler churn yapma eğiliminde.

Veri seti, görselleştirmeler ve istatistiksel analizlerle derinlemesine incelenmiştir. Bu analizler doğrultusunda, churn tahmini için önemli özellikler belirlendi.

## Model Kurulumu

### Veri Bölme
Veri seti, eğitim ve test verileri olmak üzere %80-%20 oranında ikiye ayrıldı. Eğitim verisi ile modeller eğitildi, test verisi ile değerlendirmeler yapıldı.

### Karar Ağacı (Decision Tree)
**Karar Ağacı**, sınıflandırma problemlerinde popüler ve anlaşılması kolay bir modeldir. Bu model, veriyi sınıflara ayırırken bir ağaç yapısı kullanır. Hyperparametreler **GridSearchCV** ile optimize edilmiştir.

### Rastgele Orman (Random Forest)
**Rastgele Orman**, birden çok karar ağacının birleşiminden oluşur ve genellikle daha yüksek doğruluk sağlar. Bu model, karar ağaçlarının çeşitli varyasyonlarıyla birleştirilerek daha güçlü tahminler yapmayı sağlar. Özellikle, **overfitting** (aşırı uyum) problemini daha iyi yönetir.

#### Neden Rastgele Orman Kullanıldı?
- **Yüksek doğruluk**: Rastgele Orman, genellikle diğer temel modellerden daha yüksek doğruluk sağlar çünkü birden fazla karar ağacını birleştirir.
- **Özelliklerin önemini değerlendirme**: Rastgele Orman, veri setindeki önemli özellikleri belirlemede güçlüdür.
- **Aşırı uyum riski yok**: Diğer modellere göre daha genellenebilir sonuçlar elde edilir.

### K En Yakın Komşu (KNN)
**KNN**, sınıflandırma için basit bir algoritmadır. Veri setindeki her bir örneğin, en yakın K komşusuna göre sınıflandırma yapılır. Bu modelin en büyük avantajı, veriye hızlı bir şekilde uyum sağlayabilmesidir.

## Model Değerlendirmesi
Her bir modelin performansı, **karışıklık matrisi** ve **sınıflandırma raporu** ile değerlendirildi. Karışıklık matrisi, modelin doğru ve yanlış sınıflandırmalarını görselleştirirken, sınıflandırma raporu precision, recall, F1 skorları gibi metrikleri sunar.

### En İyi Model
**Rastgele Orman Modeli**, diğer modellere kıyasla daha yüksek doğruluk (82%) ve F1 skoru sağladı. Ayrıca, **karışıklık matrisi** ve **sınıflandırma raporlarına** göre daha düşük yanlış pozitif ve negatif sonuçlar verdi. Bu nedenle, en iyi sonuçları bu model verdi.

## Özelliklerin Önem Derecesi
Hem **Karar Ağacı** hem de **Rastgele Orman** modelleri, hangi özelliklerin daha önemli olduğunu belirlemek için kullanıldı. Öne çıkan özellikler şunlardır:
- **Tenure (Süresi)**: Müşterinin şirketteki süresi churn tahmininde önemli bir faktördür.
- **Aylık Ücret**: Aylık ücret arttıkça, müşterinin churn yapma olasılığı artmaktadır.
- **Toplam Ücret**: Düşük toplam ücret, churn oranını artırmaktadır.

## Sonuçlar
Bu analizden ve model sonuçlarından çıkarılabilecek birkaç önemli noktayı şu şekilde özetleyebiliriz:

1. **Rastgele Orman Modeli** en yüksek doğruluğa ve F1 skoruna sahip olup, churn tahmininde en iyi performansı sergileyen modeldir.
2. **Tenure, Aylık Ücret ve Toplam Ücret** churn tahmininde en önemli faktörlerdir. Şirket, bu özellikler üzerinde çalışarak churn oranını düşürebilir.
3. **Kısa süreli sözleşmeler** ve **aylık sözleşme** sahiplerinin churn yapma olasılığı daha yüksektir. Şirket, bu tür müşterilere yönelik stratejiler geliştirerek churn oranını azaltabilir.
4. **Yaşlı müşteriler** ve **yıllık sözleşmelere sahip müşteriler**, daha düşük churn oranına sahip oldukları için bu tür müşteriler üzerinde odaklanmak faydalı olabilir.
5. **Rastgele Orman**, genellikle yüksek doğruluk ve genellenebilir sonuçlar sunduğu için tercih edilmiştir.

Bu sonuçlarla birlikte, müşteri kaybı (churn) tahmini için önemli stratejik adımlar atılabilir ve şirketin müşteri tutma çabaları daha etkili hale getirilebilir.

