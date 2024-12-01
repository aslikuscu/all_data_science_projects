# Sonar Verisi ile Kaya ve Mayın Tespiti  

Bu proje, sonar sinyalleri kullanarak kayaları ve mayınları doğru bir şekilde ayırt etmek amacıyla geliştirilmiştir. Sinyallerin analiz edilmesi, deniz tabanındaki mayınların tespiti gibi güvenlik açısından kritik uygulamalar için önemlidir.  

---

## İçindekiler  
1. [Proje Amacı](#proje-amacı)  
2. [Kullanılan Teknik ve Nedenleri](#kullanılan-teknik-ve-nedenleri)  
3. [Sonuç ve Değerlendirme](#sonuç-ve-değerlendirme)  
4. [Gelecekteki Geliştirmeler](#gelecekteki-geliştirmeler)  

---

## Proje Amacı  
Sonar sinyalleri, su altındaki nesnelerin tespitinde yaygın olarak kullanılır. Bu projenin amacı, kayaların ve mayınların sonar sinyalleri aracılığıyla otomatik olarak sınıflandırılmasıdır. Bu, özellikle mayınların güvenli bir şekilde tespit edilmesi ve etkisiz hale getirilmesi için kritik bir adımdır.  

---

## Kullanılan Teknik ve Nedenleri  
Proje kapsamında **Logistic Regression (Lojistik Regresyon)** algoritması tercih edilmiştir. Bunun nedenleri:  

- **Basit ve Etkili:** Lojistik regresyon, doğrusal olarak ayrılabilen veri setlerinde güçlü sonuçlar verir. Sonar sinyalleri gibi yüksek boyutlu verilerde dahi genellikle başarılıdır.  
- **Yorumlanabilirlik:** Modelin parametreleri kolayca yorumlanabilir, bu da sınıflandırma kararlarının anlaşılmasını sağlar.  
- **Hızlı ve Hafif:** Eğitim süreci hızlıdır ve büyük veri setleri için dahi uygun bir yöntemdir.  

Alternatif yöntemler (karar ağaçları, sinir ağları) daha karmaşık olmasına rağmen, lojistik regresyon temel bir sınıflandırma problemi için yeterli performans göstermiştir.  

---

## Sonuç ve Değerlendirme  
- **Doğruluk (Accuracy):** Model, test verisi üzerinde %85 doğruluk oranı elde etmiştir.  
- **Kaya ve Mayın Ayrımı:** Özellikle mayınların doğru tespit edilmesi konusunda başarılı sonuçlar elde edilmiştir.  
- **Yanlış Pozitif/Negatifler:** Modelin bazı durumlarda kayaları mayın olarak veya tam tersi şekilde sınıflandırdığı gözlemlenmiştir. Bu, gelecekte iyileştirme gerektiren bir alan olarak öne çıkmaktadır.  

Sonuç olarak, proje sonar verisi ile mayın ve kaya ayrımında güvenilir bir sınıflandırma sağlamıştır. Bu, gerçek dünya uygulamaları için umut verici bir adımdır.  

---

## Gelecekteki Geliştirmeler  
- **Daha Karmaşık Modeller:** Destek vektör makineleri (SVM) veya derin öğrenme modelleri ile doğruluk artırılabilir.  
- **Özellik Mühendisliği:** Frekans bileşenlerinden anlamlı özellikler çıkarılarak model performansı geliştirilebilir.  
- **Veri Artırma:** Daha fazla sonar sinyali eklenerek modelin genelleme yeteneği artırılabilir.  

Bu proje, sonar sinyallerinin analizinde temel bir başlangıç sunmaktadır ve daha ileri çalışmalar için güçlü bir temel oluşturur.
