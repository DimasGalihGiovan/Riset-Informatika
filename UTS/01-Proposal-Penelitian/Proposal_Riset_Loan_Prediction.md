# Proposal Riset Kecil: Komparasi Algoritma Random Forest dan Logistic Regression dengan Teknik SMOTE untuk Prediksi Risiko Gagal Bayar Pinjaman

## 1. Latar Belakang
Pertumbuhan layanan keuangan digital (*FinTech*) dan pinjaman mikro menuntut sistem penilaian kelayakan kredit yang cepat dan akurat untuk meminimalkan risiko gagal bayar (*loan default*). Namun, data historis pengajuan pinjaman umumnya bersifat tidak seimbang (*imbalanced dataset*), di mana jumlah peminjam yang membayar lancar jauh lebih banyak dibandingkan peminjam yang ditolak atau berisiko gagal bayar. Kondisi ketimpangan kelas ini sering menyebabkan model *Machine Learning* standar bias terhadap kelas mayoritas sehingga kurang sensitif mendeteksi pengajuan yang berisiko.

## 2. Rumusan Masalah
1. Bagaimana pengaruh penerapan teknik *Synthetic Minority Over-sampling Technique* (SMOTE) dalam mengatasi ketidakseimbangan kelas pada dataset pengajuan pinjaman?
2. Bagaimana perbandingan performa algoritma *Random Forest* dan *Logistic Regression* (ditinjau dari *Accuracy, Precision, Recall, F1-Score,* dan *ROC-AUC*) dalam memprediksi risiko kelayakan pinjaman sebelum dan sesudah penerapan SMOTE?

## 3. Tujuan Penelitian
* Menerapkan tahapan *data preprocessing* dan penyeimbangan kelas menggunakan metode SMOTE secara terisolasi pada data latih untuk mencegah kebocoran data (*data leakage*).
* Membandingkan kinerja klasifikasi antara model *Logistic Regression* dan *Random Forest* dalam mendeteksi kelas minoritas (pengajuan berisiko/ditolak).
* Menentukan kombinasi metode terbaik untuk mendukung pengambilan keputusan kelayakan kredit secara objektif.

## 4. Metodologi Penelitian
1. **Pengumpulan Data:** Mengunduh dataset publik *Loan Prediction Problem Dataset* berformat `.csv` dari Kaggle.
2. **Data Preprocessing:** Menghapus kolom ID (`Loan_ID`), menangani nilai kosong (*missing values*) dengan imputasi modus dan median, melakukan pengkodean fitur kategorikal (*Binary Mapping* & *One-Hot Encoding*), serta menormalisasi skala fitur menggunakan `StandardScaler`.
3. **Data Splitting & Resampling:** Membagi dataset menjadi 80% data latih dan 20% data uji secara *stratified*, kemudian menerapkan **SMOTE** khusus pada data latih.
4. **Modeling:** Melatih empat skenario pembanding (*Logistic Regression* dan *Random Forest*, masing-masing tanpa SMOTE dan dengan SMOTE).
5. **Evaluasi:** Mengukur kinerja model pada data uji menggunakan *Confusion Matrix* (*Accuracy, Precision, Recall, F1-Score*) dan *ROC-AUC*.
