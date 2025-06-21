
# Buğday Verimi Zaman Serisi Analizi 🌾📈

Bu projede Türkiye'nin 1990–2023 yılları arasındaki buğday verimi, sıcaklık ve yağış verileri kullanılarak çeşitli zaman serisi modelleme yöntemleri uygulanmış ve en başarılı model belirlenmiştir.

---

## 📁 Veri

- Kaynak: `bugday_2.xlsx`
- Değişkenler:
  - `yield`: Buğday verimi (kg/dekar)
  - `temperature`: Yıllık ortalama sıcaklık (°C)
  - `precipitation`: Yıllık toplam yağış (mm)

---

## ⚙️ Kullanılan Modeller

- Doğrusal Regresyon (trend + sıcaklık)
- Holt’s Damped Trend Modeli
- SplineF
- Naive Model
- Kübik Polinom Model
- ETS (Error-Trend-Seasonal)
- ARIMA
- Dinamik Regresyon (ARIMA + dışsal değişkenler)

---

## 📊 Model Karşılaştırması

- Tüm modeller test verisi üzerinde RMSE değeri ile karşılaştırıldı.
- Sonuçlar görselleştirilerek sunuldu.
- **En düşük RMSE değerine sahip model seçildi.**

---

## ✅ Nihai Model

```math
\hat{Y} = 307.634 + 3.912 \cdot \text{trend} - 10.102 \cdot \text{sıcaklık}
