# Dataset Rencana Riset Kecil

## 1. Identitas & Sumber Dataset
* **Nama Dataset:** Loan Prediction Problem Dataset (Dream Housing Finance)
* **Platform Sumber:** Kaggle (`https://www.kaggle.com/datasets/altruistdelhite04/loan-prediction-problem-dataset`)
* **Format & Dimensi:** File tabular `.csv` dengan jumlah **614 baris data** dan **13 kolom atribut** (ukuran file < 50 KB).
* **Proporsi Kelas Target:** 422 data berlabel `Y` (Disetujui/Lancar — 68,73%) dan 192 data berlabel `N` (Ditolak/Berisiko — 31,27%).

## 2. Struktur Fitur (Atribut) Dataset
| No | Nama Kolom | Tipe Data | Keterangan |
| :---: | :--- | :--- | :--- |
| 1 | `Loan_ID` | Kategorikal | Kode unik pemohon pinjaman (dihapus saat pemodelan) |
| 2 | `Gender` | Kategorikal | Jenis kelamin pemohon (`Male` / `Female`) |
| 3 | `Married` | Kategorikal | Status pernikahan (`Yes` / `No`) |
| 4 | `Dependents` | Kategorikal | Jumlah tanggungan keluarga (`0`, `1`, `2`, `3+`) |
| 5 | `Education` | Kategorikal | Pendidikan terakhir (`Graduate` / `Not Graduate`) |
| 6 | `Self_Employed` | Kategorikal | Status wiraswasta (`Yes` / `No`) |
| 7 | `ApplicantIncome` | Numerik | Pendapatan bulanan pemohon utama |
| 8 | `CoapplicantIncome` | Numerik | Pendapatan bulanan penjamin/pasangan |
| 9 | `LoanAmount` | Numerik | Jumlah pinjaman yang diajukan (dalam ribuan) |
| 10 | `Loan_Amount_Term` | Numerik | Jangka waktu pelunasan pinjaman (dalam bulan) |
| 11 | `Credit_History` | Biner (`0`/`1`) | Riwayat kelayakan kredit sebelumnya (`1` = memenuhi syarat, `0` = tidak) |
| 12 | `Property_Area` | Kategorikal | Lokasi properti agunan (`Urban`, `Semiurban`, `Rural`) |
| 13 | **`Loan_Status`** | **Biner (`Y`/`N`)** | **Variabel Target: `Y` (Disetujui/Lancar) vs `N` (Ditolak/Berisiko)** |
