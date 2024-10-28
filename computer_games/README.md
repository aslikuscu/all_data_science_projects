### Proje Başlığı: Bilgisayar Oyunları Veri Analizi

#### Proje Açıklaması:
Bu proje, bilgisayar oyunları hakkında çeşitli verilerin analiz edilmesine odaklanmaktadır. Amacımız, oyunların geliştirici firmaları, yapımcıları, oyun türleri ve kullanılan işletim sistemleri gibi çeşitli kategorilere göre sınıflandırılması ve bu verilerin görselleştirilmesidir. Veri seti toplamda 1095 satır ve 6 sütundan oluşmakta olup her bir satır bir bilgisayar oyununa aittir. Veri setindeki sütunlar arasında oyun adı, geliştirici, yapımcı, tür, işletim sistemi ve yayınlanma tarihi gibi bilgiler bulunmaktadır.

#### Veri Seti İçeriği:
- **Adı (Name)**: Oyunun adı.
- **Geliştirici (Developer)**: Oyunu geliştiren firma veya şirket.
- **Yapımcı (Producer)**: Oyunun yayıncılığını üstlenen firma veya şirket.
- **Tür (Genre)**: Oyunun türü (örneğin, FPS, RPG, spor).
- **İşletim Sistemi (Operating System)**: Oyunun çalıştığı işletim sistemleri.
- **Yayınlanma Tarihi (Date Released)**: Oyunun piyasaya sürüldüğü tarih.

#### Yapılan Analizler:
1. **Eksik Veri Analizi**: Veri setinde eksik bilgi olup olmadığı kontrol edildi ve eksiksiz olduğu gözlemlendi.
2. **Geliştirici Şirketlerin Analizi**:
   - En fazla oyun geliştiren ilk 10 şirket belirlendi ve yatay çubuk grafik ile görselleştirildi.
3. **Yapımcı Şirketlerin Analizi**:
   - En çok oyun üreten ilk 10 yapımcı incelendi ve yatay çubuk grafik ile gösterildi.
4. **Oyun Türleri Analizi**:
   - En popüler 10 oyun türü belirlendi ve bu türlerin dağılımı görselleştirildi.
5. **İşletim Sistemi Analizi**:
   - En yaygın kullanılan 10 işletim sistemi sıralandı ve grafiksel olarak sunuldu.

#### Görselleştirme Teknikleri:
- **Çubuk Grafik (Bar Plot)**: Geliştirici, yapımcı ve oyun türü analizleri için yatay çubuk grafikleri kullanılarak en popüler şirketler ve türler gösterildi.
- **Pasta Grafik (Pie Chart)**: Şirketlerin ve oyun türlerinin yüzdelik dağılımları hesaplanarak görsel olarak sunuldu.

#### Kullanılan Araçlar ve Kütüphaneler:
- **Python**: Veri analizi ve görselleştirme işlemleri için kullanıldı.
- **Pandas**: Veri işleme ve analiz işlemleri için kullanıldı.
- **Matplotlib**: Grafik oluşturma ve veri görselleştirme amacıyla kullanıldı.
- **Plotly**: Etkileşimli grafikler oluşturmak için kullanıldı.

#### Sonuçlar:
- En fazla oyun geliştiren şirket **Maxis** olup, en popüler oyun türü **First-person shooter** (FPS) olarak belirlendi.
- **Microsoft Windows**, en yaygın kullanılan işletim sistemi olarak öne çıkmaktadır.

Bu projede, oyun sektörü hakkında önemli istatistiksel bilgiler elde edilmiş ve sektörün genel eğilimleri hakkında bir fikir edinilmiştir.

