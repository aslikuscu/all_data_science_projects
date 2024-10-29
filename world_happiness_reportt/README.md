---

# 2021 Dünya Mutluluk Raporu Analizi

Bu proje, **2021 Dünya Mutluluk Raporu** verilerini analiz ederek, mutluluk düzeylerini etkileyen faktörleri incelemeyi amaçlıyor. Veri görselleştirme ve istatistiksel analiz yoluyla mutluluk puanları ile sosyoekonomik göstergeler arasındaki ilişkileri keşfediyoruz.

## İçindekiler

1. [Proje Hakkında](#proje-hakkında)
2. [Veri Seti Bilgisi](#veri-seti-bilgisi)
3. [Yöntemler ve Kütüphaneler](#yöntemler-ve-kütüphaneler)
4. [Analiz ve Görselleştirmeler](#analiz-ve-görselleştirmeler)
5. [Sonuçlar ve Çıkarımlar](#sonuçlar-ve-çıkarımlar)
6. [Kurulum ve Kullanım](#kurulum-ve-kullanım)

---

### Proje Hakkında

Bu analiz, **kişi başına düşen GSYİH**, **sosyal destek**, **sağlıklı yaşam beklentisi** ve **hayat seçimlerinde özgürlük** gibi metrikleri inceleyerek mutluluğa katkıda bulunan temel faktörleri belirlemeyi amaçlar. Projeden elde edilen içgörüler, mutluluğu etkileyen çeşitli faktörlerin küresel çapta nasıl bir etkisi olduğunu anlamaya yardımcı olabilir.

### Veri Seti Bilgisi

Veri seti, **2021 Dünya Mutluluk Raporu**’ndan alınmış olup aşağıdaki başlıca sütunları içerir:
- `Ülke Adı`
- `Bölgesel Gösterge`
- `Merdiven Puanı` (Mutluluk puanı)
- `Kişi Başına Düşen GSYİH`
- `Sosyal Destek`
- `Sağlıklı Yaşam Beklentisi`
- `Hayat Seçimlerinde Özgürlük`
- `Cömertlik`
- `Yolsuzluk Algısı`

### Yöntemler ve Kütüphaneler

Analiz Python’da aşağıdaki kütüphaneler kullanılarak gerçekleştirilmiştir:
- **Numpy** ve **Pandas**: Veri işleme ve hazırlama
- **Seaborn** ve **Matplotlib**: Veri görselleştirme
- **Korelasyon Analizi**: Sayısal değişkenler arasındaki ilişkileri Pearson metodu ile inceleme

### Analiz ve Görselleştirmeler

Projede yer alan başlıca görselleştirmeler ve analizler şunlardır:

1. **Mutluluk Puanı ve Kişi Başına Düşen GSYİH**:
   - GSYİH ve mutluluk puanları arasındaki ilişkiyi bölgelere göre gösteren bir dağılım grafiği.
   
2. **Bölgelere Göre GSYİH Dağılımı**:
   - Kişi başına düşen toplam GSYİH’i gösteren bir pasta grafiği; bölgeler arası ekonomik farkları ortaya koyar.

3. **Bölgelere Göre Yolsuzluk Algısı**:
   - Bölgeler arasındaki ortalama yolsuzluk algısı endeksini gösteren bir çubuk grafiği; şeffaflık seviyelerini öne çıkarır.

4. **En Mutlu ve En Mutsuz 10 Ülkenin Yaşam Beklentisi**:
   - En mutlu ve en mutsuz ülkelerdeki sağlıklı yaşam beklentisini gösteren karşılaştırmalı çubuk grafikleri.

5. **Korelasyon Isı Haritası**:
   - Mutlulukla ilişkili olan faktörleri belirlemek için sayısal değişkenler arasındaki korelasyonları gösteren bir ısı haritası.

### Sonuçlar ve Çıkarımlar

Analiz, birkaç önemli içgörüyü ortaya koymuştur:

- **Kişi başına düşen GSYİH**, özellikle Batı Avrupa ve Kuzey Amerika’da mutlulukla güçlü bir pozitif ilişki göstermektedir.
- **Sosyal destek** ve **hayat seçimlerinde özgürlük** de mutluluk puanlarıyla olumlu ilişkilidir.
- Yüksek **yolsuzluk algısına** sahip bölgelerde mutluluk puanlarının düşük olduğu görülmüştür; bu da şeffaflığın önemini vurgulamaktadır.
- **Yaşam beklentisi**, özellikle en mutlu ülkelerde, mutlulukla ilişkilidir.

Bu içgörüler, ekonomik istikrar, sosyal bağlar ve şeffaflığın mutluluk düzeyine katkı sağlayan temel etkenler olduğunu göstermektedir.

### Kurulum ve Kullanım

1. Bu repoyu klonlayın:
   ```bash
   git clone https://github.com/yourusername/dunya-mutluluk-raporu-2021-analizi.git
   ```
2. Gerekli paketleri yükleyin:
   ```bash
   pip install numpy pandas seaborn matplotlib
   ```
3. Jupyter Notebook veya Python dosyasını çalıştırarak analizleri ve görselleştirmeleri oluşturun.

---
