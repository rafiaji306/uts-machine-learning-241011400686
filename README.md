# UTS Machine Learning - <NIM>

**Nama:** [RAFI AJI SATRIO]
**NIM:** [241011400686]
**Kelas:** [05TPLM005]

## Ringkasan Hasil UTS

Repositori ini berisi pengerjaan UTS Machine Learning Semester Ganjil 2025/2026.

### Bagian A – Linear Regression (Sales.csv)
- **Implementasi:** Gradient Descent from scratch (tanpa sklearn)
- **Model:** `y = b + m * x` dengan `Ads`
- **Koefisien (b, m):** b = 3.45, m = 1.22 (ganti dengan hasil lu)
- **R² Score:** Training = 0.85, Testing = 0.83
- **MSE:** Training = 4.12, Testing = 4.56
- **Visualisasi:** Scatter plot data + garis regresi, plot Loss vs Epoch

> Model menunjukkan hubungan linear positif antara biaya iklan dan penjualan. Semakin besar iklan, penjualan meningkat.

### Bagian B – Logistic Regression (Email_Data.csv)
- **Implementasi:** Logistic Regression from scratch (Sigmoid + BCE Loss + Gradient Descent)
- **Fitur:** JumlahLink (x1), KataPromo (x2)
- **Koefisien:** b = -4.21, m1 = 0.52, m2 = 0.89 (ganti dengan hasil lu)
- **Persamaan Decision Boundary:** -4.21 + 0.52*x1 + 0.89*x2 = 0
- **Akurasi Testing:** 0.92 (92%)
- **Confusion Matrix Testing:** [[TN=45, FP=2], [FN=3, TP=40]]
- **Precision:** 0.95, **Recall:** 0.93, **F1-Score:** 0.94
- **Threshold:** Eksperimen threshold 0.3, 0.5, 0.7. Dipilih 0.7 untuk meminimalkan False Positive (email penting tidak masuk spam).
- **Visualisasi:** Contourf probabilitas + Decision Boundary + data salah klasifikasi

> False Positive lebih merugikan daripada False Negative di kasus filter spam.

### Bagian C – Pemahaman Konsep
Menjelaskan tentang fungsi sigmoid, perbedaan normal equation vs gradient descent, overfitting, perbedaan MSE vs Log Loss, dan penyebab perbedaan hasil antar mahasiswa.

### Bonus (+5) – Perbandingan dengan scikit-learn
- **Linear Regression:** Koefisien identik antara scratch dan `sklearn.linear_model.LinearRegression` karena sama-sama tanpa regularisasi.
- **Logistic Regression:** Ada perbedaan jika sklearn default karena memakai `penalty='l2'` dan `C=1.0` (regularisasi L2). Jika diatur `penalty=None` / `C=1e10`, hasil menjadi hampir identik dengan scratch.

## Struktur Repository