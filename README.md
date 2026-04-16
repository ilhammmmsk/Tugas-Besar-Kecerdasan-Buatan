# 📊 Prediksi Subscriber Netflix dengan Linear Regression

Proyek **Tugas Besar Kecerdasan Buatan** — Prediksi jumlah subscriber Netflix menggunakan algoritma **Linear Regression** berbasis data kuartal 2013–2024.

---

## 🎯 Tujuan Proyek

Membangun model machine learning yang mampu:
1. Menganalisis tren pertumbuhan subscriber Netflix dari 2013 hingga 2024
2. Memprediksi jumlah subscriber pada periode yang akan datang
3. Mengevaluasi performa model menggunakan metrik MAE dan RMSE

---

## 📁 Struktur Proyek

```
📦 Tugas-Besar-Kecerdasan-Buatan
 ┣ 📓 Tugas_Besar_Kecerdasan_Buatan.ipynb   ← Notebook utama (versi 1)
 ┣ 📓 cobacoba.ipynb                         ← Notebook utama (versi 2 / revisi)
 ┣ 📊 dataset_netflix_bulanan2.csv           ← Dataset subscriber bulanan
 ┗ 📄 README.md                              ← Dokumentasi proyek
```

---

## 📂 Dataset

| Kolom | Deskripsi |
|-------|-----------|
| `Date` | Tanggal akhir kuartal |
| `Quarter` | Label kuartal (contoh: Q1 2013) |
| `Subscribers` | Jumlah subscriber dalam juta |

**Sumber data:** Statista — *Quarterly Netflix Subscribers Count Worldwide 2013–2024*

**Rentang waktu:** Q1 2013 – Q4 2024 (48 titik data kuartal → diinterpolasi menjadi 142 titik data bulanan)

---

## 🧠 Metodologi

```
Raw Data (Quarterly)
        ↓
  Preprocessing
  - Parsing tanggal kuartal → Timestamp
  - Konversi subscriber ke float
        ↓
  Interpolasi Linear
  - Resampling dari kuartal → bulanan
  - Menghasilkan 142 titik data
        ↓
  Feature Engineering
  - Month_Index (0, 1, 2, ...)
  - Lag_1 (nilai bulan sebelumnya)
        ↓
  Train / Test Split (80:20, shuffle=False)
        ↓
  Linear Regression Training
        ↓
  Evaluasi Model (MAE, RMSE)
        ↓
  Forecasting 1 Tahun ke Depan
```

---

## 📈 Hasil Evaluasi Model

| Metrik | Nilai |
|--------|-------|
| **MAE** | ~7.24 juta subscriber |
| **RMSE** | ~8.12 juta subscriber |
| **R² (kecocokan)** | 0.9952 (99.52%) |
| **MAPE** | 0.48% |

> Model menunjukkan tingkat akurasi yang sangat tinggi dengan MAPE < 1%.

---

## 🔮 Hasil Forecasting (2025)

| Bulan | Prediksi Subscriber |
|-------|---------------------|
| Januari 2025 | ~303.65 juta |
| Februari 2025 | ~305.68 juta |
| Maret 2025 | ~307.71 juta |
| April 2025 | ~309.75 juta |
| Mei 2025 | ~311.80 juta |
| Juni 2025 | ~313.85 juta |
| Juli 2025 | ~315.90 juta |
| Agustus 2025 | ~317.96 juta |
| September 2025 | ~320.03 juta |
| Oktober 2025 | ~322.10 juta |
| November 2025 | ~324.18 juta |
| Desember 2025 | ~326.26 juta |

---

## 🛠️ Teknologi & Library

```python
Python 3.x
├── pandas          # Manipulasi data
├── numpy           # Komputasi numerik
├── matplotlib      # Visualisasi data
├── scikit-learn    # Linear Regression & evaluasi
└── Google Colab    # Environment eksekusi
```

---

## 🚀 Cara Menjalankan

### 1. Buka di Google Colab
Klik badge di bawah atau buka notebook secara manual:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ilhammmmsk/Tugas-Besar-Kecerdasan-Buatan/blob/main/cobacoba.ipynb)

### 2. Upload Dataset
Upload file `dataset_netflix_bulanan2.csv` ke session Colab.

### 3. Jalankan Semua Cell
`Runtime` → `Run all` atau jalankan sel satu per satu secara berurutan.

---

## 📊 Visualisasi

Notebook menghasilkan 3 visualisasi utama:

1. **Grafik Data Historis** — Tren subscriber Netflix 2013–2024 (per semester)
2. **Grafik Prediksi vs Aktual** — Perbandingan data test dengan prediksi model
3. **Grafik Forecasting** — Proyeksi subscriber 1 tahun ke depan (2025)

---

## 📝 Catatan

- Dataset menggunakan data kuartal yang diinterpolasi secara linear menjadi data bulanan
- Model Linear Regression dipilih karena tren data yang sangat linear
- Fitur utama: `Time_Index` dan `Lag_1` (nilai subscriber bulan sebelumnya)

---

## 👤 Author

**Ilham Surya Kusuma**  
Mahasiswa Teknik Komputer — Telkom University  
🔗 [LinkedIn](https://www.linkedin.com/in/ilhamsuryakusuma/) | 🐙 [GitHub](https://github.com/ilhammmmsk)

---

*Tugas Besar Mata Kuliah Kecerdasan Buatan — Telkom University*
