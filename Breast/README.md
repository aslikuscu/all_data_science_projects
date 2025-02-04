# Meme Kanseri Sınıflandırma Projesi

Bu proje, meme kanseri teşhis verilerini kullanarak hastalığın sınıflandırılması üzerine odaklanmaktadır. Veri seti, çeşitli özellikleri içeren 569 gözlemden oluşmaktadır. Amacımız, **karar ağaçları** ve **lojistik regresyon** gibi makine öğrenimi algoritmalarını kullanarak, hastalığın varlığını belirlemektir.

## Veri Seti

*   **Özellikler**: `radius_mean`, `texture_mean`, `perimeter_mean`, `area_mean`, vb.
*   **Hedef Değişken**: `diagnosis` (M: Malign, B: Benign)
*   Gereksiz sütunlar temizlendi ve `diagnosis` değerleri sayısal değerlere dönüştürüldü.

## Veri Ön İşleme

1.  **Gereksiz Sütunların Kaldırılması**: `Unnamed: 32` ve `id` sütunları veri setinden çıkarıldı.
2.  **Eksik Değerlerin Kontrolü**: Veri setinde eksik değer bulunmamaktadır.
3.  **Korelasyon Analizi**: `diagnosis` ile diğer özellikler arasındaki korelasyon hesaplandı ve görselleştirildi.

## Modelleme

### 1. Karar Ağaçları

*   Model, eğitim verisi ile eğitildi ve test verisi üzerinde doğruluğu %92.98 olarak elde edildi.
*   Tahmin edilen ve gerçek değerler karşılaştırıldı.

### 2. Lojistik Regresyon

*   Model, eğitim verisi ile eğitildi ve test verisi üzerindeki doğruluğu %97.08 olarak kaydedildi.
*   Lojistik regresyon modeli, daha yüksek bir geri çağırma (recall) değerine sahip olduğu için, karar ağacına göre daha iyi performans gösterdi.

## Sonuç

Her iki modelde de yüksek doğruluk oranları elde edilmiştir, ancak lojistik regresyon modeli, %97 geri çağırma değeri ile karar ağacından daha üstün performans göstermektedir. Bu sonuçlar, meme kanseri teşhisinde makine öğrenimi uygulamalarının potansiyelini göstermektedir.
