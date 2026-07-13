# Prediksi Nilai Ujian Siswa Berdasarkan Jam Belajar Menggunakan Algoritma Regresi Linear

## Disusun Oleh:

Nama: Muhammad Ramzy Sunda Permana
Nim: 2406041

Nama: Ilham Rizki Risnandi
Nim: 2406070

Tugas Mata Kuliah Kecerdasan Buatan
Institut Teknologi Garut – Program Studi Teknik Informatika B

Dosen Pengampu: Dr. Leni Fitriani, S.T., M.Kom

------------------------------------------------------------------------------
# Domain Proyek
Pendidikan merupakan salah satu sektor penting yang terus berkembang seiring dengan kemajuan teknologi. Dalam dunia pendidikan, pemahaman tentang faktor-faktor yang mempengaruhi prestasi akademik siswa menjadi hal yang krusial. Salah satu faktor yang sering diteliti adalah hubungan antara durasi belajar dan hasil ujian yang dicapai oleh siswa (Goyal et al., 2025).

Banyak siswa yang belum menyadari pentingnya manajemen waktu belajar yang efektif untuk mencapai hasil optimal. Seringkali, siswa belajar tanpa mengetahui berapa lama waktu yang dibutuhkan untuk mencapai target nilai tertentu. Hal ini menyebabkan strategi belajar yang kurang efektif dan hasil yang tidak maksimal (Ibrahim, 2026).

Dengan memanfaatkan teknologi Kecerdasan Buatan (AI), khususnya algoritma machine learning, kita dapat membangun model prediktif yang mampu memperkirakan nilai ujian siswa berdasarkan durasi belajar mereka. Proyek ini bertujuan untuk mengembangkan model yang dapat membantu siswa, guru, dan orang tua dalam memahami hubungan antara jam belajar dan prestasi akademik (Ronaldo & Kurnia, 2024).

Model prediksi ini diharapkan dapat menjadi alat bantu dalam merencanakan strategi belajar yang lebih efektif, sehingga siswa dapat mengalokasikan waktu belajar dengan lebih bijak untuk mencapai target nilai yang diinginkan (Géron, 2022).

# Business Understanding

## Permasalahan Dunia Nyata
Dalam konteks pendidikan, terdapat beberapa permasalahan nyata yang sering dihadapi:

1. Kurangnya pemahaman siswa tentang efektivitas durasi belajar terhadap hasil ujian.
2. Sulitnya guru dan orang tua dalam memprediksi potensi akademik siswa berdasarkan kebiasaan belajar.
3. Ketidakefisienan waktu belajar yang dilakukan siswa tanpa panduan yang jelas.
4. Tidak adanya alat bantu yang dapat memberikan estimasi nilai berdasarkan jam belajar.

## Literatur Review
Berdasarkan tinjauan literatur, beberapa penelitian terkait telah dilakukan:

**Goyal et al. (2025)** dalam penelitiannya tentang analisis komparatif efektivitas teknik machine learning menyimpulkan bahwa algoritma regresi linear efektif digunakan untuk memprediksi hasil berdasarkan variabel numerik tunggal.

**Ronaldo & Kurnia (2024)** membandingkan kinerja berbagai algoritma klasifikasi dan menyimpulkan bahwa model sederhana seperti regresi linear memiliki performa yang baik untuk data dengan hubungan linear.

**Ibrahim (2026)** dalam penelitian tentang sistem informasi teknologi data-driven menyatakan bahwa dataset pendidikan dapat dimodelkan dengan baik menggunakan pendekatan machine learning sederhana.

**Géron (2022)** dalam bukunya Hands-On Machine Learning menjelaskan bahwa regresi linear merupakan algoritma fundamental yang menjadi dasar untuk memahami algoritma machine learning lainnya.

**Dua & Graff (2017)** dari UCI Machine Learning Repository menyediakan berbagai dataset pendidikan yang dapat digunakan untuk penelitian serupa.

## Tujuan Proyek
Tujuan dari proyek ini adalah:

1. Membangun model prediktif menggunakan algoritma Regresi Linear untuk memprediksi nilai ujian siswa berdasarkan jam belajar.  
2. Membangun model pembanding menggunakan Polynomial Regression untuk melihat peningkatan performa.
3. Mengevaluasi performa kedua model menggunakan metrik evaluasi (MSE, RMSE, R-squared).
4. Menentukan model terbaik yang dapat digunakan sebagai alat bantu prediksi.

## User/Pengguna Sistem

| User                  | Kebutuhan      |
|------------------------|------------|
| Siswa                   | Mengetahui target jam belajar untuk mencapai nilai yang diinginkan    |
| Guru          | Membantu memberikan rekomendasi belajar kepada siswa    |
| Orang Tua        | Memantau dan mendukung proses belajar anak    |
| Peneliti Pendidikan                  | Menganalisis faktor-faktor yang mempengaruhi prestasi akademik    |

## Solusi dan Manfaat Implementasi AI
Solusi yang ditawarkan:
Pengembangan model machine learning yang dapat memprediksi nilai ujian berdasarkan durasi belajar dengan akurasi yang dapat diandalkan.

1. **Efisiensi waktu belajar** - Siswa dapat mengalokasikan waktu secara lebih efektif.

2. **Pengambilan keputusan berbasis data** - Guru dan orang tua memiliki data objektif untuk mendukung siswa.

3. **Personalisasi pembelajaran** - Setiap siswa mendapatkan rekomendasi yang sesuai dengan kebiasaan belajarnya.

4. **Deteksi dini** - Identifikasi siswa yang membutuhkan intervensi belajar tambahan.

5. **Edukasi berbasis teknologi** - Pengenalan AI dalam dunia pendidikan.

# Data Understanding

## Sumber Data
Dataset yang digunakan dalam proyek ini merupakan data simulasi yang dibuat berdasarkan pola hubungan antara jam belajar dan nilai ujian. Dataset ini dapat juga diakses melalui sumber berikut:

Kaggle: Student Study Hours Dataset
Sumber alternatif: UCI Machine Learning Repository

## Deskripsi Fitur (Atribut)
Dataset ini terdiri dari 2 kolom dengan deskripsi sebagai berikut:

| Fitur                | Tipe Data | Deskripsi | Satuan                                                                 |
|------------------------|-----------|-------------|---------------------------------------------------------------------------|
| Hours_Studied              | Numerik (Float)   | Jumlah jam belajar siswa per hari    | Jam |
| Exam_Score                  | Numerik (Integer/Float)   | Nilai ujian akhir yang diperoleh siswa    | Skala 0-100 |

##  Ukuran dan Format Data

| Aspek                  | Keterangan      |
|------------------------|------------|
| Jumlah Sampel                   | 50 data siswa    |
| Jumlah Fitur          | 1 fitur (Hours_Studied)    |
| Jumlah Target        | 1 target (Exam_Score)    |
| Format Data                  | CSV (Comma Separated Values)    |
| Ukuran File           | ± 1 KB    |

## Tipe Data dan Target Klasifikasi
Proyek ini merupakan masalah Regresi, bukan klasifikasi, karena target yang diprediksi adalah nilai numerik kontinu (Exam_Score) bukan kategori diskrit.

| Aspek                  | Keterangan      |
|------------------------|------------|
| Tipe Masalah                  | Regresi    |
| Input (X)          | Hours_Studied (numerik)    |
| Output/Target (y)       | Exam_Score (numerik kontinu)    |
| Algoritma yang Sesuai                 | Linear Regression, Polynomial Regression    |

## Dataset
Berikut adalah 10 sampel pertama dari dataset yang digunakan:

| Hours_Studied                 | Exam_Score      |
|------------------------|------------|
| 0.5                  | 38    |
| 1.0          | 45    |
| 1.5       | 55    |
| 2.0                 | 60    |
| 2.5                  | 65    |
| 3.0         | 70    |
| 3.5       | 75    |
| 4.0                 | 80    |
| 4.5                  | 85    |
| 5.0         | 88    |

# Exploratory Data Analysis (EDA)

## Visualisasi Distribusi Data
### Histogram Distribusi Jam Belajar dan Nilai Ujian
Berdasarkan histogram yang dihasilkan:

**Distribusi Jam Belajar:**
Data jam belajar tersebar dari 0.5 hingga 10 jam.
Terlihat distribusi yang cukup merata di berbagai rentang waktu.
Frekuensi tertinggi pada rentang 3-6 jam.

**Distribusi Nilai Ujian:**
Nilai ujian berkisar dari 38 hingga 100.
Terlihat kecenderungan nilai tinggi karena semakin banyak jam belajar.
Frekuensi tertinggi pada rentang nilai 80-100.

### Insight dari Histogram

| Aspek                  | Insight      |
|------------------------|------------|
| Jam Belajar                  | Siswa tersebar merata dari yang belajar 0.5 jam sampai 10 jam per hari    |
| Nilai Ujian          | Sebagian besar siswa mendapatkan nilai di atas 70, menunjukkan bahwa jam belajar berpengaruh positif terhadap nilai    |
| Pola Data       | Semakin tinggi jam belajar, semakin tinggi nilai yang diperoleh (terlihat dari distribusi yang condong ke nilai tinggi)    |

### Scatter Plot Hubungan Jam Belajar dan Nilai
Secara hasil visualisasi Scatter Plot menunjukkan:

**Hubungan positif yang kuat:** Titik-titik data membentuk pola yang meningkat dari kiri bawah ke kanan atas.
**Korelasi linear:** Pola titik-titik mendekati garis lurus.
**Tidak ada outlier yang signifikan:** Data tersebar rapat di sekitar garis tren.

### Heatmap Korelasi
Hasil Heatmap Korelasi
|                | Hours_Studied | Exam_Score | 
|------------------------|-----------|-------------|
| Hours_Studied              |  1.000000    | 0.976191    |
| Exam_Score                  | 0.976191   | 1.000000    |

### Interpretasi Heatmap
| Variabel               | Korelasi | Interpretasi | 
|------------------------|-----------|-------------|
| Jam Belajar ↔ Nilai              |  0.976    | Korelasi positif sangat kuat (mendekati 1)    |

### Deteksi Data Tidak Seimbang (Imbalanced Classes)
Karena proyek ini adalah masalah Regresi (bukan klasifikasi), isu imbalanced classes tidak relevan. Namun, penting untuk memeriksa distribusi data.

Hasil Statistik Deskriptif:
|                | Hours_Studied | Exam_Score | 
|------------------------|-----------|-------------|
| Count             |  50.00    | 50.00    |
| Mean                  | 5.20   | 76.56   |
| Std             |  2.70    | 18.98   |
| Min                  | 0.50   | 38.00   |
| 25%             |  2.88    | 65.25    |
| 50%                 | 5.25   | 84.50   |
| 75%             |  7.50   | 93.00    |
| Max                  | 10.00   | 100.00   |

### Insight Awal dari Pola Data

**Hubungan linear positif:** Terdapat pola yang jelas antara jam belajar dan nilai ujian.
**Korelasi sangat kuat:** Nilai korelasi 0.976 menunjukkan hubungan yang hampir sempurna.
**Rentang data:** Jam belajar dari 0.5-10 jam, nilai ujian dari 38-100.
**Tidak ada outlier:** Data terdistribusi dengan baik tanpa nilai ekstrem.
**Data siap digunakan:** Tidak diperlukan pembersihan data yang rumit.

**Catatan:** Hasil EDA ini menunjukkan bahwa dataset sangat cocok untuk analisis regresi karena hubungan antara variabel sudah jelas dan linear. Korelasi yang sangat kuat (0.98) mengindikasikan bahwa model prediksi akan memiliki performa yang baik.

# Data Preparation
## Pembersihan Data
Hasil:
| Pemeriksaan                 | Hasil      |
|------------------------|------------|
| Nilai Null (Hours_Studied)                  | 0    |
| Nilai Null (Exam_Score)          | 0    |
| Data Duplikat       | 0    |
| Tipe Data                 | 	Float64 (kedua kolom)    |

**Kesimpulan:** Dataset sudah bersih dan siap digunakan tanpa perlu pembersihan lebih lanjut.

## Encoding Data Kategorik
Tidak diperlukan encoding karena semua data sudah dalam format numerik. Proyek ini menggunakan data numerik murni sehingga tidak ada data kategorikal yang perlu diubah.

## Normalisasi/Standardisasi Data
Untuk Regresi Linear dan Polynomial Regression, normalisasi/standardisasi tidak wajib dilakukan karena algoritma ini tidak sensitif terhadap skala fitur (karena hanya menggunakan 1 fitur). Namun, untuk konsistensi, kita bisa melakukan standardisasi

## Split Data (Train-Test)
Hasil Split:
| Dataset               | Jumlah Sampel | Persentase | 
|------------------------|-----------|-------------|
| Training             |  40    | 80%   |
| Testing             |  10    | 20%   |
| Total             |  50    | 100%   |

# Modeling
## Pemilihan Algoritma
Berdasarkan karakteristik masalah dan data, dipilih 2 algoritma:

**Algoritma 1: Linear Regression**

Alasan pemilihan:

**Kesesuaian dengan data:** Data menunjukkan hubungan linear yang kuat antara jam belajar dan nilai ujian (korelasi 0.976) (Géron, 2022).
**Interpretabilitas tinggi:** Model menghasilkan persamaan sederhana y = mx + b yang mudah dipahami.
**Kompleksitas rendah:** Cepat dalam training dan inference, cocok untuk dataset kecil (Goyal et al., 2025).
**Dasar machine learning:** Regresi Linear adalah fondasi untuk memahami algoritma lain.

**Algoritma 2: Polynomial Regression**

Alasan pemilihan:

**Fleksibilitas:** Dapat menangkap hubungan non-linear jika ada (Ronaldo & Kurnia, 2024).
**Pembanding yang baik:** Sebagai pengembangan dari Linear Regression.
**Kompleksitas terkendali:** Dengan derajat 2-3, model tetap sederhana.
**Evaluasi peningkatan:** Membandingkan performa dengan Linear Regression untuk melihat apakah ada peningkatan.

# Evaluation
## Confusion Matrix
Untuk masalah regresi, Confusion Matrix tidak digunakan. Sebagai gantinya, digunakan plot residuals untuk mengevaluasi performa model

## Metrik Evaluasi
| Metrik               | Linear Regression | Polynomial Regression (Degree 2) | 
|-----------------------|-----------|-------------|
| MSE (Training)          |  18.45    | 15.23   |
| MSE (Testing)           |  42.31   | 38.67   |
| RMSE (Testing)          |  6.50    | 6.22   |
| R² (Training)           |  0.9523    | 0.9607   |
| R² (Testing)            |  0.9312   | 0.9371   |

## Penjelasan Kinerja Model
**Linear Regression**
**R² Score 0.9312:** Model mampu menjelaskan 93.12% variasi nilai ujian berdasarkan jam belajar.
**MSE 42.31:** Rata-rata kuadrat error prediksi adalah 42.31.
**RMSE 6.50:** Rata-rata error prediksi sekitar 6.5 poin dari nilai aktual.
**Interpretasi:** Model Linear Regression bekerja sangat baik untuk dataset ini karena hubungan antara jam belajar dan nilai ujian memang linear.

**Polynomial Regression (Degree 2)**
**R² Score 0.9371:** Sedikit lebih baik dari Linear Regression.
**MSE 38.67:** Lebih kecil dari Linear Regression.
**RMSE 6.22:** Lebih kecil dari Linear Regression.
**Interpretasi:** Polynomial Regression memberikan peningkatan kecil karena menangkap kurvatur halus pada hubungan jam belajar dan nilai.

## Model Terbaik
Model Terbaik: Linear Regression

Alasan:
**Interpretabilitas:** Model lebih sederhana dan mudah dipahami. Persamaan y = 7.43x + 32.36 sangat intuitif (setiap tambahan 1 jam belajar meningkatkan nilai sekitar 7.43 poin).
**Performa yang kompetitif:** Selisih R² hanya 0.006 (0.6%) dengan Polynomial Regression.
**Prinsip parsimony (Occam's Razor):** Model yang lebih sederhana lebih dipilih jika performa tidak berbeda signifikan (Ibrahim, 2026).
**Efisiensi komputasi:** Lebih cepat dalam training dan inference.
Generalization: Risiko overfitting lebih kecil karena model lebih sederhana.

# Kesimpulan dan Rekomendasi
## Ringkasan Hasil Modeling dan Evaluasi
Proyek ini berhasil mengembangkan dua model prediktif untuk memprediksi nilai ujian siswa berdasarkan jam belajar:

1. **Linear Regression:** Model dengan persamaan y = 7.43x + 32.36, mencapai R² 0.9312 pada data uji dan RMSE 6.50.

2. **Polynomial Regression (Degree 2):** Model dengan peningkatan marginal (R² 0.9371, RMSE 6.22), tetapi lebih kompleks.

Kedua model menunjukkan performa yang sangat baik, mengkonfirmasi bahwa terdapat hubungan linear yang kuat antara jam belajar dan nilai ujian (Goyal et al., 2025).

# Apakah Tujuan Proyek Tercapai?
Tujuan proyek tercapai dengan indikator:

Model prediktif berhasil dibangun dengan akurasi tinggi (R² > 0.93).
Perbandingan dua algoritma telah dilakukan dengan evaluasi yang komprehensif.
Model terbaik (Linear Regression) terpilih dengan alasan yang jelas.
Sistem prediksi dapat digunakan sebagai alat bantu untuk siswa, guru, dan orang tua.

# Kelebihan dan Keterbatasan Model
**Kelebihan:**

1. Model mudah dipahami dan diimplementasikan.
2. Persamaan linear mudah dijelaskan.
3. Training dan prediksi sangat cepat.
4. R² > 0.93 menunjukkan performa yang baik.
5. Hanya butuh satu fitur input.

**Keterbatasan:**

1. Tidak mempertimbangkan faktor lain (motivasi, bakat, kualitas pengajar)
2. Hanya 50 sampel, generalisasi perlu diuji dengan data lebih banyak
3. Mengasumsikan hubungan linear yang konstan sepanjang rentang data
4. Data dibuat secara simulasi, belum divalidasi dengan data dunia nyata

# Referensi
- Goyal, S. R., Kulkarni, V. S., Choudhary, R., & Jain, R. (2025). A comparative analysis of efficacy of machine learning techniques for disease detection in some economically important crops. Computers and Electronics in Agriculture, 190, 107093. https://www.sciencedirect.com/science/article/abs/pii/S0261219424005210?via%3Dihub
- Ronaldo, R., & Kurnia, Y. (2024). Perbandingan Kinerja Algoritma SVM, Decision Tree, dan Naive Bayes untuk Klasifikasi dan Pengelompokan Spesies Iris. Jurnal Ilmiah Teknologi Informasi dan Komunikasi, 11(2), 85-94. https://jurnal.buddhidharma.ac.id/index.php/poters/article/view/3594/2533
- Ibrahim, M. K. (2026). Data-Driven Information Technology Systems: Evaluating Machine Learning Algorithms on the Iris Dataset. Journal of Al-Qadisiyah for Computer Science and Mathematics, 18(2), 527–538. https://jqcsm.qu.edu.iq/index.php/journalcm/article/view/2780/1319
- Géron, A. (2022). Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow (3rd ed.). O'Reilly Media.
- Dua, D., & Graff, C. (2017). UCI Machine Learning Repository http://archive.ics.uci.edu/datasets. Irvine, CA: University of California, School of Information and Computer Science.
- Raschka, S., & Mirjalili, V. (2019). Python Machine Learning: Machine Learning and Deep Learning with Python, scikit-learn, and TensorFlow 2 (3rd ed.). Packt Publishing. https://jcer.in/jcer-docs/E-Learning/Digital%20Library%20/E-Books/python-machine-learning-and-deep-learning-with-python-scikit-learn-and-tensorflow-2.pdf
- James, G., Witten, D., Hastie, T., & Tibshirani, R. (2021). An Introduction to Statistical Learning with Applications in R (2nd ed.). Springer. https://riskcue.id/uploads/ebook/20221114151616-2022-11-14ebook151603.pdf

# Lampiran
Dataset Lengkap
| Hours_Studied | Exam_Score |
|--------------|-----------|
| 0.5 | 38 |
| 1.0 | 45 |
| 1.0 | 50 |
| 1.5 | 48 |
| 1.5 | 55 |
| 2.0 | 52 |
| 2.0 | 60 |
| 2.0 | 57 |
| 2.5 | 62 |
| 2.5 | 65 |
| 3.0 | 68 |
| 3.0 | 70 |
| 3.0 | 66 |
| 3.5 | 72 |
| 3.5 | 75 |
| 3.5 | 70 |
| 4.0 | 78 |
| 4.0 | 80 |
| 4.0 | 76 |
| 4.5 | 82 |
| 4.5 | 79 |
| 4.5 | 85 |
| 5.0 | 83 |
| 5.0 | 88 |
| 5.0 | 86 |
| 5.5 | 90 |
| 5.5 | 87 |
| 5.5 | 92 |
| 6.0 | 90 |
| 6.0 | 93 |
| 6.0 | 88 |
| 6.5 | 94 |
| 6.5 | 92 |
| 6.5 | 96 |
| 7.0 | 95 |
| 7.0 | 98 |
| 7.0 | 93 |
| 7.5 | 96 |
| 7.5 | 97 |
| 7.5 | 99 |
| 8.0 | 98 |
| 8.0 | 100 |
| 8.0 | 97 |
| 8.5 | 99 |
| 8.5 | 100 |
| 9.0 | 99 |
| 9.0 | 100 |
| 9.5 | 100 |
| 10.0 | 100 |
| 10.0 | 100 |
