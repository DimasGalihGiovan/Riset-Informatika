# Analisis Research Gap

## 1. Pemetaan Penelitian Terdahulu
| No | Peneliti & Tahun | Judul / Fokus Penelitian | Metode yang Digunakan | Keterbatasan (*Research Gap*) |
| :---: | :--- | :--- | :--- | :--- |
| 1 | Kumar et al. (2022) | *Loan Approval Prediction Using Machine Learning Algorithms* | *Decision Tree* & *Naive Bayes* | Tidak menangani ketidakseimbangan distribusi kelas (*imbalanced dataset*), sehingga nilai *Recall* pada kelas ditolak/berisiko rendah. |
| 2 | Wijaya & Santoso (2023) | *Analisis Kelayakan Kredit Nasabah Menggunakan Regresi Logistik* | *Logistic Regression* | Evaluasi hanya berfokus pada metrik *Accuracy* secara umum yang dapat bias pada data tidak seimbang. |
| 3 | Rahman et al. (2024) | *Credit Risk Classification with Ensemble Learning* | *Random Forest* | Melakukan proses *oversampling* sebelum pembagian data latih dan uji (*train-test split*), sehingga berpotensi menimbulkan kebocoran data (*data leakage*). |

## 2. Posisi Kebaruan Riset Ini
Penelitian kecil ini mengisi celah penelitian terdahulu dengan:
1. Menerapkan teknik penyeimbangan data **SMOTE secara ketat hanya pada partisi data latih** setelah proses *stratified train-test split* (80:20) agar evaluasi pada data uji mencerminkan kondisi data nyata.
2. Melakukan komparasi langsung antara model linear (*Logistic Regression*) dan model *ensemble* (*Random Forest*) sebelum dan sesudah SMOTE menggunakan metrik evaluasi spesifik kelas minoritas (**Precision, Recall, F1-Score,** dan **ROC-AUC**).
