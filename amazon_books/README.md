# Kitap Veri Seti Analizi Projesi

Bu proje, veri bilimi, makine öğrenimi, istatistik ve programlama konularında yazılmış çeşitli kitapların analizini içermektedir. Projenin temel amacı, veri setinde bulunan kitaplar arasındaki ilişkileri incelemek, kümeler oluşturarak benzer özellikteki kitapları gruplamak ve kullanıcıların kitap seçimlerine yönelik anlamlı bilgiler elde etmektir.

## Proje İçeriği

Veri seti, kitaplara ait başlık, fiyat, sayfa sayısı, ortalama inceleme puanı, inceleme sayısı, dil ve yayınevi gibi çeşitli bilgileri içermektedir. Bu veriler kullanılarak şu analizler gerçekleştirilmiştir:

- Kitap fiyatlarının dağılımının incelenmesi ve kitap sayısının fiyatla ilişkisinin analizi.
- Ortalama inceleme puanlarına göre kitapların sıklık dağılımının belirlenmesi.
- Yayınevlerine göre en yüksek fiyatlı kitapların özelliklerinin analizi.
- Kitap başlıklarının metin analizi ve TF-IDF yöntemi ile kelime vektörlerinin oluşturulması.
- KMeans algoritması kullanılarak kitapların kümelenmesi ve her küme için kelime bulutlarının oluşturulması.
- Kümelerin anlamlandırılması ve kitap türlerine göre sınıflandırılması.

## Proje Amacı

Projenin amacı, veri setindeki kitapları anlamlı bir şekilde analiz ederek aşağıdaki çıktıları elde etmektir:

1. **Kitaplar Arasındaki İlişkiler:** Kitapların fiyat, sayfa sayısı ve inceleme puanları gibi özellikleri arasındaki ilişkileri keşfetmek.
2. **Kümeleme ile Gruplama:** Kitapları başlıklarına göre kümelere ayırarak hangi türlerin ön planda olduğunu belirlemek.
3. **Kelime Bulutları Oluşturma:** Her bir küme için kelime bulutları oluşturarak kitapların hangi konulara yoğunlaştığını görselleştirmek.
4. **Kullanıcıya Öneriler Sunma:** Çıkarılan sonuçlar ışığında, kullanıcılara popüler veya uygun fiyatlı kitap önerileri sunabilmek.

## Kullanılan Yöntemler ve Teknolojiler

- **Python Programlama Dili:** Veri analizi ve görselleştirme işlemleri için kullanıldı.
- **Pandas ve NumPy:** Veri işleme ve analiz süreçlerinde temel kütüphaneler olarak kullanıldı.
- **Matplotlib ve Seaborn:** Görselleştirme işlemleri için kullanıldı.
- **scikit-learn:** TF-IDF ve KMeans kümeleme algoritması gibi makine öğrenimi yöntemlerinin uygulanması için kullanıldı.
- **WordCloud:** Kelime bulutlarının oluşturulması için kullanıldı.

## Sonuçlar

- Kitap fiyatlarının geniş bir aralıkta değiştiği, ancak bazı yayınevlerinin daha yüksek fiyatlı kitaplara sahip olduğu gözlemlendi.
- Ortalama inceleme puanlarına göre kitapların büyük çoğunluğunun yüksek puan aldığı görüldü.
- KMeans algoritması ile kitaplar 6 kümede toplandı ve bu kümeler genellikle "İstatistik", "Makine Öğrenimi", "Python", "Veri Analizi", "Veri Bilimi" ve "Yapay Zeka" gibi konuları temsil etti.
- Oluşturulan kelime bulutları, her bir kümenin hangi konulara odaklandığını açıkça gösterdi.

## Kurulum ve Çalıştırma

1. Proje dosyalarını [GitHub sayfasından](https://github.com/kullanici/kitap-analizi) indirin veya klonlayın.
2. Gerekli Python kütüphanelerini yükleyin:
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn wordcloud
    ```
3. `main.py` dosyasını çalıştırarak projeyi başlatın:
    ```bash
    python main.py
    ```

## Lisans

Bu proje [MIT Lisansı](LICENSE) ile lisanslanmıştır.

---

Projenin geliştirilmesi veya katkıda bulunmak isteyenler için lütfen pull request gönderin veya iletişime geçin.
