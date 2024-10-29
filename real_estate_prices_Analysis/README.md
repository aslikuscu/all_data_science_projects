## İçindekiler

1. [Konu](#Konu)
2. [Yöntemler](#Yöntemler)
3. [Veri Seti](#Veri-Seti)
4. [Sonuç](#Sonuç)

---

### Konu
Bu proje, çoklu doğrusal regresyon yöntemi ile ev fiyatlarının tahmin edilmesine odaklanmaktadır. Ev alanı, oda sayısı ve bina yaşı gibi bağımsız değişkenleri kullanarak evin fiyatını öngören bir model oluşturulmuştur.

---

### Yöntemler
Bu çalışmada `Scikit-learn` kütüphanesi kullanılarak bir doğrusal regresyon modeli oluşturulmuştur. Yöntemler aşağıdaki adımları içermektedir:
1. Veri hazırlama: Ev özelliklerinin olduğu veri seti `pandas` ile okunup analiz edilmiştir.
2. Model Eğitimi: `Scikit-learn` doğrusal regresyon modeli (`LinearRegression`) ile veri setine göre eğitilmiştir.
3. Tahmin: Eğitilen model ile yeni bir evin fiyatı tahmin edilmiştir.

#### Koddan Kısa Bir Örnek
```python
# Doğrusal regresyon modelinin kurulması
reg = linear_model.LinearRegression()
reg.fit(df[['alan', 'odasayisi', 'binayasi']], df['fiyat'])
# Örnek tahmin
tahmin = reg.predict([[275, 3, 10]])
print("Tahmin edilen fiyat:", tahmin[0])
```

---

### Veri Seti
Kullanılan veri setinde, evlere ait `alan`, `oda sayısı`, `bina yaşı` ve `fiyat` gibi özellikler bulunmaktadır.

Örnek:
| Alan (m²) | Oda Sayısı | Bina Yaşı | Fiyat (TL) |
| --------- | ---------- | --------- | ---------- |
| 180       | 5          | 10        | 510,000    |
| 225       | 4          | 18        | 508,000    |
| ...       | ...        | ...       | ...        |

---

### Sonuç
Doğrusal regresyon modeli kullanılarak ev fiyatlarının tahmininde %75 oranında doğruluk elde edilmiştir. Aşağıda bazı bağımsız değişken değerleri verilerek tahmin edilen fiyatlar gösterilmiştir:

- **Örnek 1**: (Alan: 275 m², Oda Sayısı: 3, Bina Yaşı: 10) → **Fiyat Tahmini**: 561,204 TL
- **Örnek 2**: (Alan: 230 m², Oda Sayısı: 6, Bina Yaşı: 0) → **Fiyat Tahmini**: 586,098 TL
