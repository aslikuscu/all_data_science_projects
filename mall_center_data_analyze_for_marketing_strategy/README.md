
---

# Small Mall Satış Analiz Projesi

Bu proje, bir perakende mağazasının satış verilerini kullanarak çeşitli analizler yapmayı amaçlamaktadır. Farklı ürün kategorilerinin satış performansları, müşteri tipine göre satış değişimleri, vergi etkisi gibi konular incelenmiştir. Görselleştirmeler yardımıyla satış trendlerini ve müşteri davranışlarını daha iyi anlamak hedeflenmiştir.

## İçindekiler

1. [Konu](#konu)
2. [Yöntemler](#yöntemler)
3. [Analiz ve Bulgular](#analiz-ve-bulgular)
   - Ürün Satışları
   - Müşteri Tipine Göre Satışlar
   - Şehir ve Şube Bazlı Satışlar
   - Satışların Mevsimsel Değişimleri
   - Cinsiyete Göre Satın Alma Davranışları
   - Müşteri Memnuniyeti
4. [Sonuç](#sonuç)

## Konu

Bu proje, bir perakende mağazasında satılan ürünler, müşteri türleri, ödeme türleri gibi bilgileri analiz ederek:
- Ürün kategorileri arasındaki satış farklılıklarını,
- Müşteri türlerine göre satış değişikliklerini,
- Şubelerin performansını,
- Mevsimsel etkileri,
- Cinsiyete göre satın alma davranışlarını ve müşteri memnuniyetini ortaya koymayı amaçlar.

## Yöntemler

Veri analizi ve görselleştirme için **Python** programlama dili ve **Pandas**, **Matplotlib** ve **Seaborn** kütüphaneleri kullanılmıştır. Veriyi daha anlaşılır ve görsel olarak çekici hale getirmek için:
- Satış miktarları ve müşteri dağılımları **bar** ve **pie** grafiklerle sunulmuştur,
- Zaman serisi analizleri **çizgi** grafikleri ile yapılmıştır,
- Müşteri memnuniyeti **boxplot** grafikleri ile incelenmiştir.

## Analiz ve Bulgular

### 1. Ürün Satışları
Belirli ürün kategorilerinin satış performansları değerlendirilmiştir. En çok satılan ürünler **Electronic Accessories** ve **Food and Beverages** olmuştur. En az satılan ise **Health and Beauty** kategorisidir.

### 2. Müşteri Tipine Göre Satışlar
Müşteri tipine göre toplam satışlar analiz edilmiştir. **Üye (Member)** olan müşteriler toplam satışların büyük bir kısmını oluştururken, **Normal** müşterilerin katkısı daha düşük kalmaktadır.

### 3. Şehir ve Şube Bazlı Satışlar
Şubeler bazında satış miktarları incelendiğinde, **Yangon** şubesi en yüksek satışlara sahiptir. Şubelerin ürün bazında başarıları da değerlendirilmiştir.

### 4. Satışların Mevsimsel Değişimleri
Aylık satış verileri incelendiğinde, yılın belirli aylarında (örneğin Ocak ve Mart) satışlarda artış gözlemlenmiştir. Bu mevsimsel değişimler mağaza için önemli stratejik bilgiler sunmaktadır.

### 5. Cinsiyete Göre Satın Alma Davranışları
Cinsiyete göre satın alma miktarları karşılaştırılmıştır. Erkek müşterilerin satın alma oranı kadınlara göre biraz daha yüksektir.

### 6. Müşteri Memnuniyeti
Müşteri memnuniyeti (rating) ile müşteri tipi, ürün hattı ve zaman arasındaki ilişki incelenmiştir. **Üye müşteriler** genellikle daha yüksek bir memnuniyet puanı bildirmiştir.

## Sonuç

Bu analiz sonucunda, ürün satış performansları ve müşteri tercihleri hakkında önemli çıkarımlar yapılmıştır. Mağaza yöneticileri, bu bilgileri stratejik planlamalar ve pazarlama faaliyetlerinde kullanabilirler. Özellikle:
- Ürün bazında stok yönetimi,
- Hedef müşteri gruplarına özel kampanyalar,
- Şube bazında iyileştirmeler
gibi alanlarda bu analizler faydalı olabilir.

--- 

Bu şekilde, README, projeyi kullanacak veya inceleyecek kişilere genel bir bakış ve analiz sonuçları hakkında bilgi sunacaktır.
