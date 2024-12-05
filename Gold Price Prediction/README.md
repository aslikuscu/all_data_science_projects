# Altın Fiyatları Analizi

## İçindekiler
1. [Proje Amacı](#proje-amacı)
2. [Kullanılan Teknikler](#kullanılan-teknikler)
3. [Veri Seti](#veri-seti)
4. [Kullanılan Metrikler](#kullanılan-metrikler)
5. [Grafikler ve Analiz](#grafikler-ve-analiz)
6. [Sonuçlar](#sonuçlar)

## Proje Amacı
Bu proje, altın fiyatlarının geçmiş verilerini analiz etmeyi ve **GLD** (altın) fiyatlarının dağılımını anlamayı amaçlamaktadır. Veriler kullanılarak fiyat hareketlerinin genel eğilimleri ve volatilite yapıları incelenmiş ve altın fiyatlarının diğer ekonomik göstergelerle olan korelasyonları araştırılmıştır.

## Kullanılan Teknikler
- **Python**: Veri analizi ve görselleştirme için ana programlama dili.
- **Pandas**: Verilerin işlenmesi, temizlenmesi ve analizi için kullanıldı.
- **Matplotlib & Seaborn**: Grafikler ve görselleştirmeler için kullanıldı. Çekirdek yoğunluk tahmini (KDE) grafiklerinin oluşturulması ve analizi yapıldı.
- **NumPy**: Sayısal hesaplamalar için yardımcı kütüphane olarak kullanıldı.
- **Jupyter Notebook**: Verilerin işlenmesi ve görselleştirilmesi için kullanılan ortam.
  
## Veri Seti
Veri seti, 2008 yılına ait **altın (GLD)** fiyatları ve diğer ekonomik göstergelere ait günlük kapanış verilerinden oluşmaktadır. Veriler aşağıdaki öğeleri içermektedir:
- **Tarih**: Verinin alındığı tarih.
- **SPX**: S&P 500 endeksinin kapanış değeri.
- **GLD**: Altın fiyatlarına ilişkin kapanış değeri.
- **USO**: Petrol fiyatları.
- **SLV**: Gümüş fiyatları.
- **EUR/USD**: Euro/Dolar döviz kuru.

## Kullanılan Metrikler
Projede kullanılan başlıca metrikler ve analiz araçları şunlardır:

- **Korelasyon Katsayıları**: 
  - Veriler arasındaki ilişkinin gücünü belirlemek için Pearson korelasyon katsayısı kullanıldı. Örneğin, **GLD** ile **SLV** arasındaki korelasyon yüksek (0.87), bu da altın ve gümüş fiyatlarının güçlü bir şekilde birbirini takip ettiğini gösteriyor.
  
- **Çekirdek Yoğunluk Tahmini (KDE)**:
  - **GLD** fiyatlarının dağılımı incelenerek, fiyatların yoğunluk eğrisi çizildi. Bu, altın fiyatlarının hangi değerlerde yoğunlaştığını ve ne sıklıkla ekstrem değerlere ulaştığını görselleştirmek amacıyla kullanıldı.
  
- **Ortalama ve Standart Sapma**:
  - **GLD** fiyatlarının ortalama değeri ve dağılımın genişliğini ölçmek için kullanıldı. Bu metrik, verinin merkezine ve ne kadar yayılma gösterdiğine dair bilgi verir.

- **Dağılım Grafikleri (Histogram, KDE)**:
  - Verilerin dağılımını anlamak ve yoğunlukları görselleştirmek için histogramlar ve KDE eğrileri kullanıldı. Bu metrik, fiyat hareketlerinin genel yapısını ortaya koymaya yardımcı oldu.

## Grafikler ve Analiz
Grafiklerde, **GLD** verilerinin dağılımı gösterilmiş ve çekirdek yoğunluk tahmini (KDE) grafiği ile bu dağılımın nasıl şekillendiği analiz edilmiştir. Altın fiyatlarının 120 civarında yoğunlaştığı ve uç noktalarda daha düşük sıklıkta olduğu görülmüştür. Ayrıca, veri seti üzerindeki korelasyonlar da incelenerek, altın ve gümüş fiyatlarının güçlü bir şekilde ilişkili olduğu, ancak altın ile S&P 500, petrol ve EUR/USD arasındaki ilişkilerin çok zayıf olduğu ortaya konmuştur.

## Sonuçlar
- **GLD** verileri, genellikle 100-140 arasında yoğunlaşmış olup, bazı dönemlerde yüksek volatilite ile 180'e kadar çıkabilmektedir. Bu, altın fiyatlarının çoğunlukla istikrarlı bir seviyede bulunduğunu, ancak belirli koşullarda büyük dalgalanmaların olabileceğini gösterir.
- **GLD** ve **SLV** arasında güçlü bir pozitif korelasyon bulunmuştur, bu da altın ve gümüş fiyatlarının genellikle paralel hareket ettiğini gösterir.
- **SPX**, **USO** ve **EUR/USD** ile ise GLD arasında zayıf ilişkiler gözlemlenmiştir, bu da altın fiyatlarının bu ekonomik göstergelerle çok sıkı bir bağlantısı olmadığını ortaya koymaktadır.

Bu analiz, altın piyasasının genel yapısını anlamak ve olası piyasa hareketlerini öngörmek için önemli bilgiler sunmaktadır.
