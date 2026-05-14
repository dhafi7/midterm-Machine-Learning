# midterm-Machine-Learning
Repo Pengumpulan UTS Machine Learning

# Fraud Detection in Online Transactions - ML Midterm Project

## 📌 Purpose of the Repository
Repository ini dibuat untuk memenuhi tugas Ujian Tengah Semester (UTS) mata kuliah Machine Learning (Individual Task). Fokus utama dari repository ini adalah mendemonstrasikan implementasi *end-to-end machine learning pipeline*, mulai dari pembersihan data mentah hingga prediksi probabilitas akhir.

## 📖 Project Overview
Proyek ini bertujuan untuk membangun sistem deteksi yang dapat memprediksi probabilitas sebuah transaksi *online* merupakan tindak penipuan (*fraud*) atau bukan. Dataset yang digunakan memiliki tantangan yang signifikan berupa jumlah dimensi yang besar (394 kolom fitur awal) dan ketimpangan kelas (*class imbalance*) yang sangat ekstrem, di mana hanya sekitar 2,7% transaksi yang diklasifikasikan sebagai *fraud*. 

Langkah-langkah *preprocessing* yang diimplementasikan meliputi:
- Menghapus fitur yang memiliki persentase *missing value* lebih dari 50%.
- Melakukan imputasi median untuk fitur numerikal dan modus untuk fitur kategorikal pada sisa data yang kosong.
- Menggunakan *One-Hot Encoding* untuk mengekstraksi fitur kategorikal.
- Menyelaraskan (*alignment*) kolom antara data Train dan Test.
- Mengaplikasikan teknik **SMOTE (Synthetic Minority Over-sampling Technique)** secara eksklusif pada data latih untuk menyeimbangkan kelas tanpa mencemari data validasi.

## 🤖 Models and Matrix Results
Mengingat distribusi kelas yang sangat timpang, metrik evaluasi Akurasi (Accuracy) tidak relevan untuk digunakan. Oleh karena itu, evaluasi model difokuskan pada klasifikasi metrik performa yang lebih sesuai untuk mendeteksi minoritas (*fraud*).

Algoritma yang digunakan adalah **Random Forest Classifier** (`n_estimators=100`, `max_depth=15`). Hasil performa model pada data validasi adalah sebagai berikut:
- **ROC-AUC Score:** `0.8961` (Model memiliki kemampuan pemisahan kelas yang sangat baik).
- **Recall (Class 1 / Fraud):** `0.48` (Model berhasil mendeteksi 48% dari seluruh kasus penipuan yang benar-benar terjadi).
- **Precision (Class 1 / Fraud):** `0.81` (Tingkat akurasi prediksi benar model adalah 81% setiap kali model memvonis sebuah transaksi sebagai penipuan).
- **Confusion Matrix:** Diimplementasikan untuk memvisualisasikan proporsi *True Positive*, *True Negative*, *False Positive* (31 kasus salah tuduh), dan *False Negative* (142 kasus penipuan lolos).

## 🧭 How to Navigate the Repository
Untuk melihat dan menjalankan kode dalam repositori ini, silakan ikuti panduan berikut:
1. `notebook_uts_ml.ipynb`: Merupakan file Jupyter Notebook utama. Anda dapat membukanya secara langsung di GitHub atau mengimpornya ke Google Colab. File ini memuat seluruh langkah kerja secara sistematis dengan penjelasan di setiap *cell*-nya.
2. `submission_uts_ml.csv`: File ini berisi hasil akhir (*output*) dari prediksi probabilitas *fraud* terhadap dataset ujian `test_transaction.csv`. File memuat dua kolom: `TransactionID` dan `isFraud` (probabilitas).
3. **Catatan:** Dataset `train_transaction.csv` dan `test_transaction.csv` tidak disertakan di dalam repository ini karena ukurannya yang besar (>600 MB).

## 👨‍💻 Identification
- **Name:** Dhafi Dzakwan Pratama
- **Class:** TK47-02
- **NIM:** 101032300213
