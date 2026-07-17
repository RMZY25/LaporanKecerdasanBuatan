# Prediksi Nilai Ujian Siswa Berdasarkan Jam Belajar Menggunakan Algoritma Regresi Linear

Repository ini merupakan bagian dari Ujian Akhir Semester (UAS) mata kuliah Kecerdasan Buatan

Dosen Pengampu: Dr. Leni Fitriani, S.T., M.Kom

Disusun Oleh:
- Muhammad Ramzy Sunda Permana (2406041)
- Ilham Rizki Risnandi (2406070)

Informatika B – Institut Teknologi Garut


##  Deskripsi Proyek

Proyek ini bertujuan untuk membangun model prediktif yang dapat memperkirakan nilai ujian siswa berdasarkan durasi waktu belajar menggunakan algoritma **Regresi Linear** dan **Polynomial Regression**. Model ini diharapkan dapat membantu siswa, guru, dan orang tua dalam merencanakan strategi belajar yang lebih efektif.

##  Tujuan Proyek

1. Membangun model prediktif menggunakan Regresi Linear untuk memprediksi nilai ujian berdasarkan jam belajar.
2. Membangun model pembanding menggunakan Polynomial Regression.
3. Mengevaluasi dan membandingkan performa kedua model.
4. Menentukan model terbaik sebagai alat bantu prediksi.


##  Langkah-Langkah Pengerjaan

Berikut adalah langkah-langkah yang dilakukan dalam pengerjaan proyek ini:

### 1. Business Understanding (Pemahaman Bisnis)

Kegiatan yang dilakukan:
- Mengidentifikasi permasalahan dunia nyata terkait hubungan jam belajar dan nilai ujian.
- Melakukan tinjauan literatur dari 5+ sumber ilmiah untuk mendukung penelitian.
- Menentukan tujuan proyek secara spesifik.
- Mengidentifikasi user/pengguna sistem (siswa, guru, orang tua, peneliti).
- Merumuskan solusi dan manfaat implementasi AI dalam konteks pendidikan.

Output: Bab Business Understanding dalam laporan.

### 2. Data Understanding (Pemahaman Data)

Kegiatan yang dilakukan:
- Mengumpulkan dataset dari sumber yang relevan (simulasi/Kaggle/UCI).
- Menganalisis deskripsi setiap fitur (Hours_Studied dan Exam_Score).
- Menentukan ukuran dan format data (50 sampel, format CSV).
- Mengidentifikasi tipe data dan target masalah (regresi).

Output: Bab Data Understanding dalam laporan.

### 3. Exploratory Data Analysis (EDA) – Analisis Data Eksploratif

Kegiatan yang dilakukan:
- Membuat visualisasi distribusi data:
  - Histogram distribusi jam belajar dan nilai ujian.
  - Scatter plot hubungan jam belajar dan nilai ujian.
- Melakukan analisis korelasi antar fitur menggunakan heatmap.
- Mendeteksi data tidak seimbang (untuk regresi, dicek distribusi data).
- Mengambil insight awal dari pola data yang terlihat.

Output: Bab EDA dalam laporan + visualisasi grafik.

### 4. Data Preparation (Persiapan Data)

Kegiatan yang dilakukan:
- Pembersihan data: mengecek dan menghapus nilai null serta data duplikat.
- Encoding data kategorik (tidak diperlukan karena semua data numerik).
- Normalisasi/standardisasi data numerik (tidak wajib untuk Regresi Linear).
- Split data menjadi training set (80%) dan testing set (20%).

Output: Bab Data Preparation dalam laporan.

### 5. Modeling (Pemodelan)

Kegiatan yang dilakukan:
- Memilih 2 algoritma:
  - Algoritma 1: Regresi Linear (karena hubungan data linear, interpretabilitas tinggi).
  - Algoritma 2: Polynomial Regression Degree 2 (sebagai pembanding).
- Mengimplementasikan model dengan kode Python di notebook.
- Melatih model menggunakan data training.
- Membandingkan hasil kedua model.

Output: Bab Modeling dalam laporan + file `uas_model.ipynb`.

### 6. Evaluation (Evaluasi)

Kegiatan yang dilakukan:
- Menghitung metrik evaluasi:
  - Mean Squared Error (MSE)
  - Root Mean Squared Error (RMSE)
  - R-squared (R²)
- Menjelaskan kinerja model berdasarkan metrik tersebut.
- Menentukan model terbaik:
  - Linear Regression dipilih sebagai model terbaik karena:
    - Performa kompetitif (R² 0.9312).
    - Interpretabilitas tinggi.
    - Lebih sederhana dan efisien.
    - Risiko overfitting lebih kecil.

Output: Bab Evaluation dalam laporan.

### 7. Kesimpulan dan Rekomendasi

**Kegiatan yang dilakukan:**
- Merangkum hasil modeling dan evaluasi.
- Menyimpulkan apakah tujuan proyek tercapai.
- Menyebutkan kelebihan dan keterbatasan model.
- Memberikan rekomendasi perbaikan untuk pengembangan ke depan.

Output:*Bab Kesimpulan dan Rekomendasi dalam laporan.

### 8. Pembuatan Laporan dan Dokumentasi

Kegiatan yang dilakukan:
- Menyusun laporan lengkap dalam format Markdown (`.md`).
- Menyiapkan referensi minimal 5 sumber ilmiah dengan format APA.
- Membuat notebook implementasi (`uas_model.ipynb`).
- Mengunggah seluruh file ke repository GitHub public.
  
Output: Laporan lengkap + repository GitHub.

## 📊 Hasil Akhir

| Metrik | Linear Regression | Polynomial Regression (Degree 2) |
|--------|-------------------|----------------------------------|
| R² Testing | 0.9312 | 0.9371 |
| RMSE Testing | 6.50 | 6.22 |
| MSE Testing | 42.31 | 38.67 |

Model Terbaik: Linear Regression
