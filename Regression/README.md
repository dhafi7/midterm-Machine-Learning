# Music Release Year Prediction - Machine Learning Regression Project

## 📌 Purpose of the Repository
Repository ini dibuat untuk memenuhi tugas Ujian Tengah Semester (UTS) mata kuliah Machine Learning (Individual Task). Proyek ini berfokus pada implementasi *pipeline* regresi *end-to-end* untuk memprediksi nilai kontinu, yaitu tahun rilis sebuah lagu berdasarkan karakteristik audionya.

## 📖 Project Overview
Tujuan dari proyek ini adalah merancang model regresi yang mampu memprediksi tahun rilis lagu menggunakan fitur audio yang bersifat numerik (seperti karakteristik *timbre* dan sinyal musik lainnya). Dataset yang digunakan memiliki 90 fitur audio yang telah dianonimasi.

Komponen utama yang diimplementasikan dalam proyek ini meliputi:
- **Data Preprocessing**: Melakukan pemisahan fitur dan target serta memastikan kualitas data (pengecekan *missing values*).
- **Hyperparameter Tuning (Optuna)**: Menggunakan Optuna untuk mencari kombinasi parameter terbaik secara otomatis guna meminimalkan *error* model.
- **Experiment Tracking (MLFlow)**: Mencatat setiap percobaan (*trial*) selama proses optimasi untuk memantau perkembangan metrik performa.
- **Model Interpretation (LIME)**: Memberikan penjelasan lokal pada hasil prediksi individu untuk memahami fitur mana yang paling memengaruhi keputusan model.

## 🤖 Models and Matrix Results
Model yang digunakan dalam proyek ini adalah **XGBRegressor**. Berdasarkan proses optimasi menggunakan Optuna, model dilatih dengan parameter terbaik (seperti `n_estimators`, `max_depth`, dan `learning_rate`) untuk mencapai performa optimal.

**Hasil Evaluasi:**
- **Best RMSE (Root Mean Squared Error)**: `8.5275` (Model secara rata-rata meleset sekitar 8,5 tahun dalam memprediksi tahun rilis lagu).
- **Interpretation**: Melalui LIME, terlihat bahwa fitur tertentu seperti `feature_1` dan `feature_3` memberikan kontribusi signifikan (baik positif maupun negatif) terhadap pergeseran angka tahun yang diprediksi oleh model.

## 🧭 How to Navigate the Repository
1. `Regression_ML.ipynb`: Jupyter Notebook utama yang berisi seluruh kode mulai dari *loading* data, optimasi Optuna, hingga visualisasi LIME.
2. **Catatan**: Dataset `midterm-regresi-dataset.csv` tidak disertakan dalam repository ini karena batasan ukuran file.

## 👨‍💻 Identification
- **Name**: Dhafi Dzakwan Pratama
- **Class**: S1 Teknik Komputer
- **NIM**: 101032300213
