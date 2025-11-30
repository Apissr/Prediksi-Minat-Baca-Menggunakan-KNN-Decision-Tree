# 📚 Analisis & Prediksi Tingkat Kegemaran Membaca (TGM)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Library](https://img.shields.io/badge/Library-Pandas%20|%20Scikit--Learn%20|%20Seaborn-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

Proyek ini bertujuan untuk menganalisis tren literasi di Indonesia dan membangun model Machine Learning untuk memprediksi kategori **Tingkat Kegemaran Membaca (Reading Interest)** provinsi berdasarkan perilaku membaca dan akses internet.

## 📌 Latar Belakang
Tingkat literasi adalah indikator penting kemajuan pendidikan. Proyek ini menggunakan dataset **TGM (2020-2023)** untuk:
1. Menganalisis pola dan tren minat baca di 35 provinsi.
2. Membandingkan performa algoritma **K-Nearest Neighbors (KNN)** dan **Decision Tree**.
3. Menemukan faktor utama (Key Drivers) yang mempengaruhi skor literasi.

## 📂 Dataset
Dataset yang digunakan mencakup data provinsi di Indonesia dengan fitur utama:
* `Reading Frequency per week`: Frekuensi membaca per minggu.
* `Daily Reading Duration`: Durasi membaca harian (menit).
* `Internet Access Frequency`: Frekuensi akses internet (data tersedia 2021-2023).
* `Tingkat Kegemaran Membaca`: Skor Indeks (Target Regresi).
* `Category`: Label kelas (High, Moderate, Low, etc).

> **Catatan Data Cleaning:** Data tahun 2020 dihapus pada tahap modeling karena *missing values* pada kolom akses internet.

## 🛠️ Metodologi
Proyek ini mengikuti siklus **Data Science Life Cycle**:
1. **Data Cleaning:** Konversi format angka & penanganan *missing values*.
2. **EDA:** Analisis distribusi, tren tahunan, dan korelasi (Heatmap).
3. **Feature Engineering:** Membuat fitur baru `Weekly_Reading_Minutes` dan melakukan *Standard Scaling*.
4. **Modeling:** Komparasi algoritma Supervised Learning.
5. **Evaluation:** Menggunakan Akurasi, Confusion Matrix, dan Feature Importance.

## 📊 Hasil Evaluasi
Berdasarkan pengujian dengan pembagian data 80:20, diperoleh hasil:

| Model | Akurasi | Keterangan |
| :--- | :--- | :--- |
| **K-Nearest Neighbors (KNN)** | **76%** | ✅ Model Terbaik |
| Decision Tree | 67% | - |

**Temuan Utama:**
* **Durasi Membaca Harian** adalah fitur paling berpengaruh terhadap tingginya kategori minat baca, lebih signifikan daripada frekuensi membaca atau akses internet.
* Model KNN terbukti lebih efektif dalam mengklasifikasikan kategori minat baca dibandingkan Decision Tree.

## 🚀 Cara Menjalankan (Installation)
1. Clone repository ini:
   ```bash
   git clone [https://github.com/username-kamu/nama-repo.git](https://github.com/username-kamu/nama-repo.git)

1. Install library yang dibutuhkan:
Bash
pip install pandas numpy matplotlib seaborn scikit-learn
2. Jalankan file notebook/script:
Bash
python main_analysis.py
# Atau buka file .ipynb di Google Colab/Jupyter Notebook

👥 Author
Nama: Muhammad Hafizh Shafa

NIM: 24111814053

Matkul: Kecerdasan Buatan (Artificial Intelligence)
