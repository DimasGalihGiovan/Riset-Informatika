# Rencana Evaluation Metric

Karena dataset pengajuan pinjaman memiliki distribusi kelas yang tidak seimbang (*68,73% lancar vs 31,27% berisiko*), evaluasi model difokuskan pada ketepatan mendeteksi kelas minoritas (`Loan_Status = N` / berisiko) menggunakan metrik berikut:

## 1. Metrik Berbasis Confusion Matrix
* **Accuracy:** Mengukur rasio prediksi benar secara keseluruhan dari total data uji.
  $$\text{Accuracy} = \frac{TP + TN}{TP + TN + FP + FN}$$
* **Precision (Kelas Berisiko):** Mengukur ketepatan model saat memprediksi suatu pengajuan berisiko/ditolak (mencegah kesalahan menolak pemohon yang sebenarnya layak).
  $$\text{Precision} = \frac{TP}{TP + FP}$$
* **Recall / Sensitivity (Kelas Berisiko):** Mengukur seberapa banyak pengajuan berisiko yang berhasil dikenali oleh model (krusial untuk menekan risiko gagal bayar).
  $$\text{Recall} = \frac{TP}{TP + FN}$$
* **F1-Score:** Rata-rata harmonik dari *Precision* dan *Recall* sebagai indikator keseimbangan performa pada dataset tidak seimbang.
  $$\text{F1-Score} = 2 \times \frac{\text{Precision} \times \text{Recall}}{\text{Precision} + \text{Recall}}$$

## 2. Metrik Probabilitas Klasifikasi
* **ROC-AUC (*Area Under the Receiver Operating Characteristic Curve*):** Mengukur kemampuan model dalam membedakan kelas positif dan negatif di seluruh variasi ambang batas (*threshold*) probabilitas dengan rentang nilai `0.0` hingga `1.0`.
