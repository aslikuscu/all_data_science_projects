
# Kredi Tahmin Projesi

Bu proje, bir kredi başvuru veri setini kullanarak kredi tahmin modelleri oluşturmayı amaçlamaktadır. Farklı makine öğrenmesi algoritmaları ile kredi başvurusunun onaylanıp onaylanmayacağını tahmin etmeye çalışıyoruz.

## İçindekiler

1. [Gereksinimler](#gereksinimler)
2. [Veri Kümesi](#veri-kümesi)
3. [Veri Ön İşleme](#veri-ön-işleme)
4. [Keşifsel Veri Analizi (EDA)](#keşifsel-veri-analizi-eda)
5. [Modelleme](#modelleme)
6. [Model Değerlendirmesi](#model-değerlendirmesi)
7. [Sonuçlar ve Çıkarımlar](#sonuçlar-ve-çıkarımlar)

## Gereksinimler

Projeyi çalıştırmadan önce aşağıdaki Python kütüphanelerinin yüklü olduğundan emin olun:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`

Gerekli kütüphaneleri şu komutla yükleyebilirsiniz:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## Veri Kümesi

Veri kümesi, kredi başvurusunda bulunan kişilere ait aşağıdaki özellikleri içermektedir:

- **Loan_ID:** Kredi başvuru numarası
- **Gender:** Cinsiyet
- **Married:** Medeni durum
- **Dependents:** Bağımlı kişi sayısı
- **Education:** Eğitim durumu
- **Self_Employed:** Serbest meslek durumu
- **ApplicantIncome:** Başvuru sahibinin geliri
- **CoapplicantIncome:** Eş başvuru sahibinin geliri
- **LoanAmount:** Kredi miktarı
- **Loan_Amount_Term:** Kredi vadesi
- **Credit_History:** Kredi geçmişi
- **Property_Area:** Mülk alanı (Kırsal, Şehir, Banliyö)
- **Loan_Status:** Kredi durumu (Onaylandı / Reddedildi)

## Veri Ön İşleme

Veri kümesindeki eksik değerler dolduruldu ve kategorik değişkenler sayısal değerlere dönüştürüldü. Bu süreçte kullanılan bazı adımlar:

1. Eksik değerlerin mod veya medyan gibi uygun değerlerle doldurulması.
2. Kategorik değişkenlerin `LabelEncoder` ile sayısal değerlere dönüştürülmesi.
3. Yeni özellikler oluşturulması (`TotalIncome` gibi).

## Keşifsel Veri Analizi (EDA)

Veri analizi aşamasında, verilerin dağılımı ve kredi durumu ile ilişkisi incelenmiştir. Bazı adımlar:

- Kategorik değişkenlerin yüzdesel dağılımı.
- Kredi onayı oranlarının çeşitli faktörlere göre incelenmesi (Cinsiyet, Eğitim, Kredi Geçmişi vb.).
- Özelliklerin histogramları ve bar grafikleri.

Örnek Grafikler:
- Kredi geçmişine göre kredi onayı yüzdesi.
- Eğitim durumuna göre kredi durumu dağılımı.

## Modelleme

Çeşitli makine öğrenmesi algoritmaları kullanılarak kredi tahmin modelleri oluşturulmuştur:

- **Lojistik Regresyon**
- **Karar Ağaçları**
- **Bagging Classifier**
- **AdaBoost Classifier**
- **Random Forest**

Veri seti, %70 eğitim ve %30 test olarak ayrılmıştır. Modellerin başarımı eğitim ve test seti üzerinde ölçülmüştür.

## Model Değerlendirmesi

Modeller, doğruluk ve F1 skoru gibi metriklerle değerlendirildi. Ek olarak, `confusion matrix` ve `classification report` kullanılarak daha ayrıntılı analizler yapıldı.

| Model                  | Eğitim Doğruluğu | Test Doğruluğu  |
|------------------------|------------------|-----------------|
| Lojistik Regresyon     | 0.80             | 0.83            |
| Karar Ağaçları          | 1.00             | 0.73            |
| Bagging Classifier     | 0.85             | 0.82            |
| AdaBoost Classifier    | 0.80             | 0.81            |
| Random Forest          | 0.87             | 0.84            |

## Sonuçlar ve Çıkarımlar

- Kredi geçmişi, kredi onayı üzerinde en önemli etkiye sahiptir.
- Lojistik regresyon ve rastgele orman algoritmaları, diğer modellere göre daha iyi performans göstermiştir.
- Eğitim doğruluğunun test doğruluğuna kıyasla çok yüksek olması durumunda, modelin aşırı öğrenme (`overfitting`) yapmış olabileceği gözlemlenmiştir.

