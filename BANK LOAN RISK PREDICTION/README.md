# Banka Kredisi Risk Tahmini

Bu proje, banka kredisi risk tahmini yapmak icin veri analizi ve makine öğrenimi modelleri geliştirmeyi amaçlar. Aşağıda, projenin ayrıntıları, özellikleri ve kullanılan teknikler hakkında bilgiler bulabilirsiniz.

---

## İçindekiler
- [Projeye Genel Bakış](#projeye-genel-bakış)
- [Kurulum](#kurulum)
- [Veri Ön işleme](#veri-ön-işleme)
- [Veri Analizi ve Görselleştirme](#veri-analizi-ve-görselleştirme)
- [Makine Öğrenimi Modelleri](#makine-öğrenimi-modelleri)
  - [K En Yakın Komşu (KNN)](#k-en-yakın-komşu-knn)
  - [Karar Ağaçları](#karar-ağaçları)
- [Sonuçlar ve Değerlendirme](#sonuçlar-ve-değerlendirme)
- [Katkıda Bulunma](#katkıda-bulunma)

---

## Projeye Genel Bakış
Banka kredisi tahmini projesi, bir bireyin kredi talebinin kabul edilip edilmeyeceğini ve temerrüt riskini öngörmeyi amaçlar. Veri seti, kişisel bilgiler, gelir seviyesi, kredi geçmişi gibi çeşitli değişkenleri içermektedir. Projede aşağıdaki adımlar uygulanmıştır:

1. Verilerin ön işlenmesi (eksik değerlerin doldurulması, aykırı değerlerin ele alınması)
2. Veri analizi ve görselleştirme
3. KNN ve Karar Ağaçları gibi makine öğrenimi modellerinin uygulanması
4. Modellerin performansının değerlendirilmesi

---

## Kurulum
Bu projeyi çalıştırmak için aşağıdaki adımları izleyin:

1. **Gereksinimleri Yükleyin**
   Proje için gerekli Python kütüphaneleri:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn
   ```

2. **Veri Setini Yükleyin**
   Veri seti `credit_risk.csv` dosyası olarak projeye dahil edilmiştir.

3. **Projeyi Çalıştırın**
   Python betiğini aşağıdaki komutla çalıştırın:
   ```bash
   python main.py
   ```

---

## Veri Ön İşleme

Veri ön işleme, projenin kritik bir bölümüdür ve aşağıdaki adımları kapsar:

- **Eksik Verilerin Doldurulması:**
  - `Emp_length` ve `Rate` gibi kolonlardaki eksik değerler ortalamalar ile dolduruldu.

- **Aykırı Değerlerin Tespiti ve Ele Alınması:**
  - `Age`, `Income` gibi kolonlarda kutu grafikleri ve histogramlar kullanılarak aykırı değerler incelendi.

- **Veri Dönüştürme:**
  - `Home` ve `Intent` gibi kategorik veriler, etiketleme (“Label Encoding”) ile sayısal verilere dönüştürüldü.

- **Dengesiz Veri Setinin Ele Alınması:**
  - SMOTE (Synthetic Minority Over-sampling Technique) kullanılarak veri setindeki dengesizlik giderildi.

---

## Veri Analizi ve Görselleştirme

### Görüntüleme Teknikleri

1. **Histogramlar:**
   - Yaş, gelir ve kredi miktarı gibi sayısal değişkenlerin dağılımını anlamak için kullanıldı.

2. **Kutu Grafikleri (Boxplots):**
   - Aykırı değerleri tespit etmek için kullanıldı.

3. **Korelasyon Matrisi:**
   - Değişkenler arasındaki ilişkileri incelemek için korelasyon matrisi ve ısı haritaları oluşturuldu.

---

## Makine Öğrenimi Modelleri

### K En Yakın Komşu (KNN)

- **Modelin Oluşturulması:**
  - En iyi komşu sayısı (k) belirlendi.

- **Doğruluk Analizi:**
  - KNN modeli %84 doğruluk oranına ulaştı.

- **Karışıklık Matrisi:**
  - Modelin çıktılarının çoğunlukla doğru tahmin ettiği gözlemlendi.

### Karar Ağaçları

- **Modelin Oluşturulması:**
  - Maksimum derinlik parametresi optimize edildi.

- **Doğruluk Analizi:**
  - Karar ağaçları modeli %83 doğruluk oranına ulaştı.

- **Model İçgörüleri:**
  - Kredi talebiyle yaş, kredi geçmişi ve gelir gibi faktörlerin etkisi görüldü.

---

## Sonuçlar ve Değerlendirme

- **KNN Modeli:** Test seti doğruluğu: %84
- **Karar Ağaçları Modeli:** Test seti doğruluğu: %83

Her iki model de benzer performans sergilemiş ve bankaların kredi risk tahminlerinde başarı için uygun kararlar almasında yardımcı olabilecek düzeydedir. KNN modeli, daha yüksek bir doğruluk oranına sahip olması nedeniyle tercih edilebilir. Ancak, her iki modelin de performansı geliştirilebilir:

- **Daha Karmaşık Modeller:** Örneğin, rastgele ormanlar veya gradyan artırmalı ağaçlar gibi yöntemler kullanılabilir.
- **Hiperparametre Optimizasyonu:** KNN ve karar ağaçlarının performansını artırmak için Grid Search veya Random Search yöntemleri uygulanabilir.
- **Daha Fazla Veri:** Veri setinin genişletilmesi, özellikle dengesiz sınıf problemlerinin çözümüne katkı sağlayabilir.

Bu değerlendirmeler ışığında, modellerin sonuçlarının pratikte nasıl uygulandığını görmek ve bankaların karar verme süreçlerinde fayda sağlamak için ileri analizler yapılabilir.

--- 

## Katkıda Bulunma
Projeye katkıda bulunmak için lütfen bir **pull request** oluşturun veya bir **issue** açın. Her türlü görüş ve geri bildirim memnuniyetle karşılanır.

---
