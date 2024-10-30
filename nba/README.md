

# NBA Oyuncu İstatistikleri Analizi (1950-2021)

Bu proje, 1950-2021 yılları arasında NBA'de oynayan basketbolcuların sezon bazlı istatistiklerinin analizini içermektedir. Proje kapsamında veri temizleme, veri ön işleme, eksik veri analizi ve temel istatistiksel analizler gerçekleştirilmiştir.

## İçindekiler
- [Gereksinimler](#gereksinimler)
- [Veri Seti Hakkında](#veri-seti-hakkinda)
- [Veri Ön İşleme ve Temizleme](#veri-on-isleme-ve-temizleme)
- [Eksik Değer Analizi](#eksik-deger-analizi)
- [Örnek Analizler](#ornek-analizler)
- [Kullanım](#kullanim)
- [Katkıda Bulunma](#katkida-bulunma)
- [Lisans](#lisans)

## Gereksinimler
Projeyi çalıştırmak için aşağıdaki Python paketleri gereklidir:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`

İlgili paketleri yüklemek için:
```bash
pip install pandas numpy matplotlib seaborn
```

## Veri Seti Hakkında
- `player_data.csv`: Oyunculara ait genel bilgileri içeren veri seti (örn. isim, pozisyon).
- `seasons_stats.csv`: 1950-2021 yılları arasında sezon bazlı oyuncu istatistikleri (örn. sayı, asist, ribaund) içeren veri seti.

Veri setleri Kaggle platformundan alınmıştır ve NBA'de oynayan oyuncuların performanslarını analiz etmek amacıyla kullanılmıştır.

## Veri Ön İşleme ve Temizleme
Veri ön işleme adımları şunlardır:
1. Yinelenen oyuncu kayıtlarının kaldırılması.
2. Eksik değerlerin analiz edilmesi ve gerekli temizleme işlemlerinin yapılması.
3. Belirli yıl aralığında (1980 sonrası) istatistiklerin filtrelenmesi.

Yinelenen satırların kaldırılması için:
```python
players = players[~players.duplicated()]  # Yinelenen kayıtları kaldır
```

Eksik değer analizi:
```python
total = df.isnull().sum().sort_values(ascending=False)
percent = (df.isnull().sum()/df.isnull().count()*100).round(2).sort_values(ascending=False)
missing_data = pd.concat([total, percent], axis=1, keys=['Total Missing', 'Percent Missing'])
```

## Eksik Değer Analizi
Eksik değerlerin çoğunlukla modern dönemde daha az bulunduğu gözlemlendi. Özellikle üç sayılık atış yüzdesi (`3P%`) gibi istatistikler, 1980 öncesinde eksik olabiliyor.

Eksik değer oranlarının örneği:
| Sütun Adı | Eksik Değer | Yüzde |
| --------- | ----------- | ----- |
| `3P%`     | 3693        | 17.05%|
| `FT%`     | 908         | 4.19% |

## Örnek Analizler
- Belirli bir sezon veya yıl aralığındaki en yüksek verimlilik puanına (`PER`) sahip oyuncuların analizi.
- Eksik değerlerin dağılımı ve eksik verilerin olduğu oyuncuların analizi.
- Modern dönemdeki (1980 sonrası) oyuncuların üç sayı istatistikleri üzerine analizler.

```python
df = seasons_stats.loc[seasons_stats['Year'] > 1979]  # 1980 sonrası veriyi filtreleme
```

## Kullanım
Proje Jupyter Notebook veya herhangi bir Python IDE'sinde çalıştırılabilir. İlgili verileri indirip, yukarıdaki veri temizleme adımlarını izleyerek çalıştırabilirsiniz.




