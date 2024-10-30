# Öğrenci Başarı Analizi 

### Veriye Dayalı İstatistiksel İnceleme ve Görselleştirme

---

## İçindekiler
1. [Proje Açıklaması](#proje-açıklaması)
2. [Kullanılan Veri Seti](#kullanılan-veri-seti)
3. [Kullanılan Yöntemler](#kullanılan-yöntemler)
4. [Veri Ön İşleme](#veri-ön-i̇şleme)
5. [Veri Analizi ve Görselleştirme](#veri-analizi-ve-görselleştirme)
6. [Sonuçlar](#sonuçlar)
7. [Kullanılan Kütüphaneler](#kullanılan-kütüphaneler)

---

## Proje Açıklaması
Bu proje, öğrencilerin başarı düzeyini etkileyen çeşitli sosyo-ekonomik ve akademik faktörleri analiz etmek amacıyla hazırlanmıştır. Öğrencilerin matematik, okuma ve yazma puanlarını etkileyen etmenler incelenmiş; ebeveyn eğitimi, etnik grup ve haftalık çalışma süresi gibi değişkenler göz önünde bulundurulmuştur.

## Kullanılan Veri Seti
Projedeki analizlerde, öğrencilerin sosyo-ekonomik özellikleri ve akademik başarıları ile ilgili çeşitli bilgilerin bulunduğu bir veri seti kullanılmıştır. Bu veri setinde, öğrencilerin **cinsiyetleri, ebeveyn eğitim düzeyleri, haftalık çalışma saatleri, kardeş sayısı, ulaşım şekilleri** gibi birçok değişken yer almaktadır.

## Kullanılan Yöntemler
Projede, verilerin analiz edilmesi ve görselleştirilmesi için aşağıdaki yöntem ve tekniklerden yararlanılmıştır:
- **Veri Temizleme:** Eksik veri yönetimi, veri türlerinin dönüştürülmesi.
- **Tanımlayıcı İstatistik:** Verinin genel yapısını anlamak amacıyla tanımlayıcı istatistiklerin hesaplanması.
- **Veri Görselleştirme:** Veri dağılımını daha iyi analiz edebilmek için Seaborn ve Matplotlib ile görselleştirme.
- **Grup Bazlı Analiz:** Ebeveyn eğitim seviyesi, cinsiyet ve etnik grup gibi kategorik değişkenler ile puanlar arasındaki ilişkiyi inceleme.

## Veri Ön İşleme
Eksik veriler aşağıdaki şekilde yönetilmiştir:
- **Eksik Verilerin Yönetimi:** Eksik veri bulunan sütunlar analiz edilmiş ve bazıları göz ardı edilerek, uygun olanları veri setinden çıkarılmıştır.
- **Veri Dönüşümleri:** Bazı kategorik değişkenlerin belirli aralıklara göre gruplandırılması yapılmıştır (örneğin, çalışma saati aralıkları).

## Veri Analizi ve Görselleştirme
1. **Cinsiyet Dağılımı:** Öğrencilerin cinsiyet dağılımı analiz edilmiştir.
2. **Ebeveyn Eğitimi ve Akademik Başarı:** Ebeveyn eğitim düzeyinin öğrencilerin başarı puanları üzerindeki etkisi analiz edilmiştir.
3. **Etnik Grup Dağılımı:** Öğrencilerin etnik grup dağılımı incelenmiş ve puanlar arasındaki dağılım görselleştirilmiştir.
4. **Puan Dağılımları:** Matematik, okuma ve yazma puanlarının dağılımı ayrı ayrı kutu grafikleri ile analiz edilmiştir.

## Sonuçlar
Veri analiz sonuçlarına göre, öğrencilerin başarılarını etkileyen önemli faktörler belirlenmiş ve bunlar detaylı olarak incelenmiştir. Ebeveyn eğitimi yüksek olan öğrencilerin akademik başarı puanlarının daha yüksek olduğu gözlemlenmiştir. Ayrıca, çalışma saatlerinin de başarıya etkisi analiz edilmiştir.

## Kullanılan Kütüphaneler
- **Pandas:** Veri işleme ve veri temizleme işlemleri için.
- **NumPy:** Matematiksel işlemler ve veri manipülasyonu için.
- **Matplotlib & Seaborn:** Veri görselleştirme ve grafik oluşturma işlemleri için.

--- 

Bu proje, öğrenci başarılarını etkileyen faktörleri daha iyi anlayabilmek adına bir rehber niteliğindedir.
