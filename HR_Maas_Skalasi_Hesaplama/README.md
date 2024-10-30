# Deneyime Göre Maaş Tahmini 

## Lineer ve Polinom Regresyon Uygulaması

---

## İçindekiler
1. [Proje Açıklaması](#proje-açıklaması)
2. [Kullanılan Veri Seti](#kullanılan-veri-seti)
3. [Kullanılan Yöntemler](#kullanılan-yöntemler)
4. [Veri Görselleştirme](#veri-görselleştirme)
5. [Lineer Regresyon Modeli](#lineer-regresyon-modeli)
6. [Polinom Regresyon Modeli](#polinom-regresyon-modeli)
7. [Tahmin Sonuçları](#tahmin-sonuçları)
8. [Kullanılan Kütüphaneler](#kullanılan-kütüphaneler)

---

## Proje Açıklaması
Bu proje, deneyim yılına göre maaş tahmini yapmak için doğrusal ve polinom regresyon modellerini uygulamayı hedeflemektedir. Veriler, çalışanların deneyim yılı ile maaş bilgilerini içermektedir ve amaç, deneyim yılına göre bir maaş tahmin modeli oluşturmaktır.

## Kullanılan Veri Seti
Projede kullanılan veri seti, çalışanların **deneyim yılları ve maaş** bilgilerini içermektedir. Bu veri setinde yer alan veriler, modelin eğitilmesi ve deneyim yılına bağlı maaş tahmini yapılabilmesi için kullanılmıştır.

## Kullanılan Yöntemler
Projede aşağıdaki yöntemler ve adımlar uygulanmıştır:
- **Veri Görselleştirme:** Dağılım grafiği ile verinin genel ilişkisini gözlemlemek.
- **Doğrusal Regresyon (Lineer Regresyon):** Deneyim ile maaş arasındaki ilişkiyi gösteren en uygun doğrusal modeli oluşturmak.
- **Polinom Regresyon:** Veriler doğrusal bir modele tamamen uymadığı için, ikinci dereceden bir polinom regresyon modeli kullanılarak daha iyi bir uyum elde etmek.

## Veri Görselleştirme
Veriler, **Matplotlib** kütüphanesi kullanılarak görselleştirilmiş ve deneyim yılları ile maaş arasındaki ilişki bir dağılım grafiği ile gözlemlenmiştir.

## Lineer Regresyon Modeli
Deneyim ile maaş arasındaki ilişkiyi temel doğrusal regresyon modeli ile incelemek için **LinearRegression** modeli kullanılmıştır. Bu model, verilerin genel eğilimini gösteren basit bir doğru oluşturarak görselleştirilmiştir.

## Polinom Regresyon Modeli
Veriler doğrusal model ile tam olarak açıklanamadığı için, deneyim yılına göre maaş tahminini daha iyi yansıtacak bir **polinom regresyon** modeli (derece 2) oluşturulmuştur. Bu model ile daha iyi bir uyum elde edilmiş ve polinom regresyonun tahminleri ile veriler görselleştirilmiştir.

## Tahmin Sonuçları
Eğitilen polinom regresyon modeli ile, belirli bir deneyim yılı (örneğin, 4.5 yıl) için maaş tahmini yapılmıştır. Bu tahmin, verinin genel eğilimlerine uygun bir değer sunmaktadır.

## Kullanılan Kütüphaneler
- **Pandas:** Veri işleme ve analiz işlemleri için.
- **Matplotlib:** Veri görselleştirme ve grafik oluşturma işlemleri için.
- **Scikit-Learn:** Model oluşturma, eğitim ve tahmin işlemleri için (LinearRegression ve PolynomialFeatures kullanılmıştır).

--- 

Bu proje, lineer ve polinom regresyon modellerini karşılaştırarak deneyim yılına göre maaş tahminini daha doğru bir şekilde gerçekleştirmeyi amaçlamaktadır.
