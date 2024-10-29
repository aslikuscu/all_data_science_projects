
---

# Bank Churn Prediction Project

## Proje Açıklaması
Bu proje, bankacılık sektöründeki müşteri kaybını (churn) tahmin etmek amacıyla geliştirilmiştir. Müşteri verileri analiz edilerek, hangi müşterilerin bankayı terk etme olasılığının yüksek olduğunu belirlemek için makine öğrenimi yöntemleri kullanılmaktadır.

## Veri Seti
Veri seti, müşteri bilgilerini içeren 10,127 satır ve 23 sütun içermektedir. Anahtar özellikler şunlardır:
- **CLIENTNUM**: Müşteri numarası
- **Attrition_Flag**: Müşterinin bankayı terk edip etmediğini gösterir (Attrited/Existing).
- **Customer_Age**: Müşterinin yaşı
- **Gender**: Müşterinin cinsiyeti
- **Dependent_count**: Müşterinin bakmakla yükümlü olduğu kişi sayısı
- **Income_Category**: Müşterinin gelir kategorisi
- **Card_Category**: Müşterinin sahip olduğu kart kategorisi
- **Credit_Limit**: Müşterinin kredi limiti
- **Avg_Utilization_Ratio**: Ortalama kredi kullanım oranı

## Gerekli Kütüphaneler
Projenin çalışması için aşağıdaki Python kütüphanelerine ihtiyaç vardır:
- pandas
- numpy
- matplotlib
- seaborn (isteğe bağlı, görselleştirmeler için)
- scikit-learn (makine öğrenimi modelleri için)

## Kurulum
1. Python 3.x sürümünü bilgisayarınıza kurun.
2. Aşağıdaki komutları kullanarak gerekli kütüphaneleri yükleyin:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```

## Kullanım
1. Projeyi klonlayın veya indirin.
2. `BankChurners.csv` veri dosyasını uygun bir dizine yerleştirin.
3. Jupyter Notebook veya başka bir IDE kullanarak `bank_churn_prediction.py` veya `notebook.ipynb` dosyasını açın.
4. Kodu çalıştırarak müşteri kaybını tahmin edin.

## Sonuçlar
Veri analizi ve modelleme sonuçları, hangi özelliklerin müşteri kaybı üzerinde daha etkili olduğunu gösterir. Bu bilgiler, bankaların müşteri sadakatini artırmak için stratejiler geliştirmelerine yardımcı olabilir.

## Katkıda Bulunanlar
- [Adınız] (GitHub profil bağlantınız)

## Lisans
Bu proje MIT Lisansı altında lisanslanmıştır. Daha fazla bilgi için `LICENSE` dosyasına bakın.

---

