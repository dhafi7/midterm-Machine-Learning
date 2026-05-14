# Credit Card Customer Segmentation - Machine Learning Midterm

## 📌 Purpose of the Repository
Repository ini dibuat untuk memenuhi tugas Ujian Tengah Semester (UTS) mata kuliah Machine Learning (Individual Task). Fokus dari repository ini adalah mendemonstrasikan *pipeline Unsupervised Learning* (Clustering) dari tahap pembersihan data hingga visualisasi segmentasi pelanggan.

## 📖 Project Overview
Tujuan utama proyek ini adalah mengelompokkan pelanggan kartu kredit berdasarkan kebiasaan transaksi mereka (seperti saldo, frekuensi pembelian, dan tarik tunai) menggunakan dataset yang berisi 17 fitur perilaku finansial.

Alur kerja (*workflow*) yang diimplementasikan meliputi:
- **Data Preprocessing**: Menghapus kolom identitas (`CUST_ID`) dan menangani *missing values* pada `MINIMUM_PAYMENTS` dan `CREDIT_LIMIT` menggunakan nilai Median.
- **Feature Scaling**: Mengaplikasikan `StandardScaler` agar seluruh fitur memiliki bobot yang setara saat perhitungan jarak Euclidean.
- **Optimal Cluster Selection**: Menggunakan **Metode Elbow** dengan metrik WCSS untuk menentukan jumlah cluster yang paling optimal (k=4).
- **Dimensionality Reduction**: Menggunakan **PCA** (Principal Component Analysis) untuk mereduksi 17 dimensi fitur menjadi 2 komponen utama agar segmentasi dapat divisualisasikan.

## 🤖 Models and Matrix Results
Algoritma utama yang digunakan untuk pengelompokan ini adalah **K-Means Clustering** dengan jumlah cluster $k=4$.

**Hasil Evaluasi:**
- **Silhouette Score:** [Masukkan angka Silhouette Score dari output Colab kamu disini]
- **Visualisasi PCA:** Model berhasil memisahkan pelanggan ke dalam 4 segmen perilaku utama, yang secara visual dapat diamati melalui *scatter plot* distribusi komponen PCA.
- **Cluster Profiling:** Berdasarkan rata-rata fitur per cluster, kita dapat mengidentifikasi perilaku spesifik tiap segmen (misalnya segmen pengguna pasif, segmen pembelanja aktif, segmen pengguna tarik tunai, dan pengguna VIP).

## 🧭 How to Navigate the Repository
1. `notebook_uts_clustering.ipynb`: Merupakan file Jupyter Notebook utama yang memuat keseluruhan kode, narasi pemikiran, serta *output* visualisasi dari Elbow Method dan PCA.
2. **Catatan**: Dataset `clusteringmidterm(1).csv` tidak disertakan di dalam repository ini.

## 👨‍💻 Identification
- **Name:** Dhafi Dzakwan Pratama
- **Class:** S1 Teknik Komputer
- **NIM:** [Masukkan NIM Kamu Disini]
