
## Proje Özeti

Bu proje, otel rezervasyonları verilerini analiz ederek, konukların rezervasyon iptali üzerindeki etkilerini anlamaya yönelik bir çalışmadır. Proje iki ana bölümden oluşmaktadır: Keşifsel Veri Analizi (EDA) ve Makine Öğrenimi Modelleme.

### 1. Keşifsel Veri Analizi (EDA)
- Veri İncelemesi: Veri setinde, konukların tercih ettiği yemek planları, oda tipleri, araç park yeri talepleri ve özel istekler gibi çeşitli değişkenler bulunmaktadır. Analiz, bu değişkenlerin rezervasyon iptali üzerindeki etkisini değerlendirmektedir.
- Grafiksel Görselleştirme: 
  - Yemek Planı ve Oda Tipi: Konukların çoğunluğunun Yemek Planı 1 ve Oda Tipi 1 tercih ettiği gözlemlenmiştir.
  - Araç Park Yeri İhtiyacı: Çoğu konuk park yeri talep etmemektedir, bu da kamu ulaşımının yaygın kullanıldığını göstermektedir.
  - Özel İstekler: Çoğu konuk özel isteklerde bulunmamaktadır.
  - Öngörülen İptal Oranı: Düşük önceden rezervasyon (1-2 gün öncesinde) ile iptallerin az olduğu, uzun süreli rezervasyonların (2-3 ay öncesinde) ise daha yüksek iptal oranına sahip olduğu gözlemlenmiştir.

### 2. Modelleme
- Veri Ön İşleme: Kategorik değişkenler sayısal verilere dönüştürülmüş ve veriler standartlaştırılmıştır.
- Modeller: 
  - Random Forest, Karar Ağacı ve Lojistik Regresyon modelleri kullanılarak, iptal durumu tahmin edilmiştir.
  - Performans Değerlendirmesi: Random Forest modeli en yüksek başarı oranı (%88) ile en iyi performansı göstermiştir. Karar Ağacı ve Lojistik Regresyon sırasıyla %85 ve %80 başarı oranları elde etmiştir.
- Sonuçlar: Rezervasyon iptalleri, konukların geçmiş rezervasyon davranışları, yemek planı tercihleri ve lead time gibi faktörlerle ilişkilendirilmiştir.

### Sonuç
Proje, otel işletmeciliğinde müşteri davranışlarını anlamak ve rezervasyon iptallerini minimize etmek amacıyla önemli bulgular sunmaktadır. Özellikle müşteri memnuniyetini artırmak ve yeni misafirleri tekrar kazanmak için stratejilerin geliştirilmesi önerilmektedir.
