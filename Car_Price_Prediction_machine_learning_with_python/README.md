# Projenin Amacı
Bu proje, çeşitli özelliklere dayalı olarak ikinci el araçların fiyatlarını tahmin etmek için bir makine öğrenimi modelinin geliştirilmesini amaçlamaktadır. Amaç, kullanıcıların araçlarını en uygun fiyatla satmalarına veya en uygun fiyatla almalarına yardımcı olmaktır.

## Adımlar ve Uygulamalar
### Gerekli Kütüphanelerin Kurulumu:

Projede kullanılan kütüphaneler kuruldu. category_encoders, xgboost, matplotlib, seaborn, pandas gibi kütüphaneler araç fiyat tahmini için gerekli veri işleme, modelleme ve görselleştirme işlemleri için kullanıldı.
### Veri Yükleme:

Araç fiyatları ile ilgili veriler bir CSV dosyasından yüklendi. Bu veri setinde 19237 satır ve 18 sütun bulunmaktadır. Sütunlar, aracın fiyatı, üretim yılı, marka, model, motor hacmi, kilometre durumu gibi çeşitli bilgileri içermektedir.
### Veri Temizleme:

Veri setindeki tekrarlayan satırlar çıkarıldı.
Eksik veya geçersiz değerler için işlemler yapıldı. Örneğin, Levy sütunundaki - karakteri 0 ile değiştirildi.
Mileage ve Engine volume gibi sütunlarda gerekli dönüşümler yapılarak sayısal değerlere dönüştürüldü.
### Aykırı Değer Analizi:

Sayısal sütunlar için çeyrekler arası aralık (IQR) kullanılarak aykırı değerler belirlendi ve temizleme işlemleri yapıldı.
### Görselleştirme:

Verinin dağılımı ve özellikleri ile ilgili grafikler oluşturuldu. Histogramlar ve sayım grafikleri ile verinin genel durumu görselleştirildi.
Korelasyon matrisleri kullanılarak sayısal değişkenler arasındaki ilişkiler incelendi.
### Kategorik ve Sayısal Değişkenlerin Ayrılması:

Veri setindeki kategorik ve sayısal değişkenler ayrı olarak tanımlandı. Kategorik değişkenler için one-hot encoding gibi yöntemler uygulanabilir.
### Model Geliştirme:

Makine öğrenimi modelleri (örneğin, karar ağaçları, rastgele ormanlar, AdaBoost, XGBoost) oluşturularak, bu modeller aracılığıyla araç fiyatlarını tahmin etmek amacıyla çalışıldı.
### Model Değerlendirme:

Modellerin performansı, çeşitli metrikler (ortalama mutlak hata, R² skoru gibi) kullanılarak değerlendirildi. Bu, hangi modelin en iyi sonuçları verdiğini belirlemeye yardımcı oldu.
# Sonuç
Bu projede araç fiyatlarını tahmin etmek için verinin işlenmesi, temizlenmesi ve modelleme süreçleri uygulanarak makine öğrenimi teknikleriyle doğru fiyat tahminleri elde edilmeye çalışıldı. Proje, veri bilimi ve makine öğrenimi uygulamalarını bir araya getirerek pratik bir örnek oluşturdu.
