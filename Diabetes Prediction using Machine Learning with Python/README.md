# README.md

## **Proje Başlığı: Diyabet Tespiti Modeli**

Bu proje, diyabet hastalığını sınıflandırmak amacıyla bir makine öğrenimi modeli geliştirmek için hazırlanmıştır. Kullanıcıdan alınan verilerle, kişinin diyabet hastası olup olmadığı tahmin edilmektedir. 

---

## **Amaç**

Bu projenin amacı, belirli biyometrik verilere dayalı olarak, bir kişinin diyabet hastası olup olmadığını tahmin etmektir. Kullanıcıdan alınan yaş, kan şekeri, vücut kitle indeksi gibi verilerle, diyabet riski tahmin edilerek sağlık yönetimi için bir yardımcı sistem oluşturulması hedeflenmiştir.

---

## **Kullanılan Yöntemler ve Nedenleri**

1. **Veri Toplama ve Hazırlık**
   - Projede, Pima Indians Diabetes veri seti kullanılmıştır. Bu veri seti, çeşitli biyometrik parametreler ve diyabet sonucu (1: Diyabetli, 0: Diyabetsiz) içerir.
   
2. **Veri Ön İşleme**
   - **Veri Temizleme:** Eksik veya hatalı veriler temizlenmiş, veri seti homojen hale getirilmiştir.
   - **Veri Standardizasyonu:** Verilerin daha doğru bir şekilde işlenebilmesi için `StandardScaler` kullanılarak veriler standardize edilmiştir. Bu işlem, modelin tüm parametreler üzerinde eşit ağırlıkta çalışmasını sağlar.
   
3. **Veri Setinin Eğitim ve Test Olarak Ayrılması**
   - Veri seti, eğitim ve test olarak ikiye ayrılmıştır. Eğitim seti %80, test seti ise %20 oranında belirlenmiştir. Bu sayede modelin doğruluğu test edilebilir.
   
4. **Model Seçimi ve Eğitimi**
   - **Destek Vektör Makineleri (SVM):** Modelin temelini, doğrusal kernel kullanılan bir SVM sınıflandırıcısı oluşturmuştur. SVM, sınıflandırma problemleri için güçlü bir model olup, veri setindeki özellikler arasındaki sınırları en iyi şekilde bulmayı amaçlar.
   
5. **Model Değerlendirmesi**
   - Modelin doğruluğu, eğitim ve test verisi üzerinde yapılan tahminler ile ölçülmüştür. Eğitim veri setindeki doğruluk %78.66, test veri setindeki doğruluk ise %77.27 olarak belirlenmiştir.

---

## **Sonuçlar**

Proje sonunda, geliştirdiğimiz modelin doğruluk oranları şu şekildedir:
- Eğitim Verisi Doğruluğu: **78.66%**
- Test Verisi Doğruluğu: **77.27%**

Model, yeni veriler üzerinde doğru tahminler yapabilme kapasitesine sahip olup, diyabetin erken teşhisi için kullanılabilir.

---

## **Kullanım**

### **Veri Girişi ve Tahmin Yapma**
Yeni bir hasta için diyabet tahmini yapmak için aşağıdaki gibi veriler girilebilir:

```python
input_data = (1, 103, 30, 38, 83, 43.3, 0.183, 33)
```
Bu veri setinde:
- **Pregnancies**: Hamilelik sayısı
- **Glucose**: Kan şekeri seviyesi
- **BloodPressure**: Kan basıncı
- **SkinThickness**: Cilt kalınlığı
- **Insulin**: İnsülin seviyesi
- **BMI**: Vücut kitle indeksi
- **DiabetesPedigreeFunction**: Diyabet soybilim fonksiyonu
- **Age**: Yaş

Yukarıdaki veriler girildiğinde, model kullanıcının diyabet hastası olup olmadığını tahmin edecektir.

---

## **Teknik Detaylar ve Kütüphaneler**

- **Pandas**: Veri manipülasyonu ve analizi için kullanıldı.
- **NumPy**: Sayısal hesaplamalar ve matris işlemleri için kullanıldı.
- **Scikit-learn**: Veri ön işleme, model eğitimi ve değerlendirmesi için kullanıldı. Özellikle `SVC` sınıfı, modelin eğitiminde kullanıldı.
- **StandardScaler**: Veri standardizasyonu için kullanıldı.

---

Bu proje, diyabet hastalığının erken teşhisi ve sağlık yönetimi konusunda faydalı bir araç olabilir. Modelin doğruluğu zamanla daha fazla veri ile geliştirilebilir.
