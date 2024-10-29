
---

# SmallMall Verisi Analiz Projesi

Bu proje, **SmallMall veri seti** kullanılarak müşteri davranışları, satış trendleri, ve ürün kategorilerinin satışlara olan etkisini analiz etmeyi amaçlamaktadır. Veriler, ürün kategorileri, müşteri demografisi, satın alma yöntemleri ve zamana bağlı satış trendleri gibi çeşitli alanlarda analiz edilmiştir.

## İçindekiler

1. [Proje Hakkında](#proje-hakkında)
2. [Veri Seti Bilgisi](#veri-seti-bilgisi)
3. [Analiz ve Sonuçlar](#analiz-ve-sonuçlar)
4. [Görselleştirmeler](#görselleştirmeler)
5. [Kurulum ve Kullanım](#kurulum-ve-kullanım)
6. [Geliştirme](#geliştirme)

---

### Proje Hakkında

Bu proje, müşterilerin satın alma davranışlarını ve satışları etkileyen faktörleri inceleyerek pazarlama stratejileri ve satış politikalarını optimize etmeyi amaçlamaktadır. **SmallMall** verilerinden elde edilen analizlerle, hangi gün ve saatlerde satışların arttığı, müşteri memnuniyeti ile harcama arasında bir ilişki olup olmadığı gibi sorulara yanıt aranmaktadır.

### Veri Seti Bilgisi

Veri seti, her bir alışveriş işlemi için aşağıdaki bilgileri içermektedir:
- **Fatura Kimliği (Invoice ID)**: Her bir işlemi benzersiz kılan bir kimlik.
- **Şube (Branch)**: A, B, ve C şubeleri olarak farklı bölgelerdeki satış mağazaları.
- **Ürün Çizgisi (Product line)**: Satılan ürünlerin kategorileri.
- **Müşteri Tipi (Customer type)**: Üye (Member) veya Normal müşteri.
- **Ödeme Yöntemi (Payment)**: Nakit, kredi kartı veya dijital cüzdan.
- **Tarih (Date) ve Saat (Time)**: Satışın gerçekleştiği tarih ve saat bilgisi.
- **Toplam Satış (Total)**: Her işlemin toplam satış tutarı.
- **Müşteri Memnuniyeti (Rating)**: Satın alım sonrası müşteri memnuniyet puanı.

### Analiz ve Sonuçlar

Aşağıda bazı temel analiz ve çıkarımlar bulunmaktadır:

#### 1. Ürün Kategorileri ve Satışlar
- **Toplam Gelir**: En yüksek toplam gelir "Gıda ve İçecek" kategorisindedir, onu "Spor ve Seyahat" kategorisi takip etmektedir.
- **Düşük Satış Yapan Kategoriler**: "Moda Aksesuarları", "Ev ve Yaşam Tarzı", ve "Sağlık ve Güzellik" kategorileri daha düşük satış rakamlarına sahiptir. Bu kategorilerde satışları artırmak için pazarlama stratejileri uygulanabilir.

#### 2. Müşteri Tipi ve Satın Alma Davranışı
- **Üye Müşteriler**: Daha fazla satın alım gerçekleştirmekte ve "Gıda ve İçecek" kategorisine yönelmektedir.
- **Normal Müşteriler**: Satın alımlar arasında daha yüksek satış adetleri görülmektedir. Üye müşterilere özel promosyonlarla satışlar arttırılabilir.

#### 3. Zaman Bazlı Satış Analizi
- **Günlük Satışlar**: Cumartesi günleri en yüksek satış günü olarak öne çıkmaktadır.
- **Hafta İçi vs Hafta Sonu**: Hafta sonu, hafta içine göre daha fazla satış yapılmaktadır. Hafta sonlarına özel indirimler ve promosyonlar düşünülebilir.
- **Saatlik Satışlar**: En yoğun satış saatleri 13:00 ve 19:00 saatleridir. Öğlen ve akşamüstü saatlerinde özel promosyonlar ile satışlar daha da artırılabilir.

#### 4. Müşteri Memnuniyeti ve Satışlar
- **Yüksek Memnuniyet Puanı**: Yüksek müşteri memnuniyeti puanı alan işlemler toplam satışları artırmaktadır. Yüksek memnuniyet sağlayan ürünler veya şubelere dair veriler gözden geçirilerek müşteri memnuniyeti odaklı pazarlama yapılabilir.

#### 5. Şube Performans Analizi
- **Toplam Satış**: C şubesi, ortalama satış miktarında ilk sırada yer almaktadır. Bu şube için ek stratejiler veya genişleme düşünülebilir.
  
### Görselleştirmeler

Projede verileri anlamlandırmak için aşağıdaki görselleştirmeler kullanılmıştır:
1. **Ürün Çizgisi Bazında Toplam Satış Grafikleri**
2. **Günlük Satış Dağılım Grafikleri**
3. **Saatlik Satış Dağılımı**
4. **Müşteri Memnuniyeti ve Satış İlişkisi**

### Kurulum ve Kullanım

1. Proje dosyasını klonlayın:
   ```bash
   git clone https://github.com/kullaniciadi/SmallMall-Veri-Analiz.git
   ```
2. Gerekli Python paketlerini yükleyin:
   ```bash
   pip install pandas matplotlib seaborn
   ```
3. `smallmall_analysis.ipynb` veya `analysis.py` dosyasını çalıştırarak analizleri inceleyebilirsiniz.

### Geliştirme

Bu projeyi geliştirmek için yapılabilecek bazı eklemeler:
- **Yeni Kategoriler Ekleme**: Ürün çizgisi kategorilerine göre daha ayrıntılı analiz.
- **Makine Öğrenmesi ile Tahminleme**: Zaman bazlı satış tahminleri.
- **Dinamik Raporlama**: Pandas Profiling veya benzeri araçlarla detaylı raporlar üretme.

---

Projede yer alan analizler, SmallMall’un satış trendlerini daha iyi anlamak için veri analitiği çözümleri sunar. Satış, müşteri memnuniyeti ve zamana göre satış trendleri bu projede temel odak noktalarını oluşturmaktadır.
