# 💤 Sleep Disorder Prediction

## 📌 Deskripsi
Project ini bertujuan untuk memprediksi gangguan tidur (Sleep Disorder) pada responden berdasarkan data gaya hidup dan faktor kesehatan. Gangguan tidur yang diprediksi mencakup:

- Insomnia
- Sleep Apnea
- None (tidak ada gangguan tidur)

Dengan memanfaatkan algoritma machine learning seperti **Random Forest**, **Support Vector Machine (SVM)**, **K-Nearest Neighbors (KNN)**, **Naive Bayes**, dan **Decision Tree**, project ini berupaya membandingkan performa model dalam mengidentifikasi pola yang berhubungan dengan kualitas tidur.

---

## 📂 Dataset

### 📑 Sumber Data
Dataset diperoleh dari Kaggle:  
🔗 [Sleep Disorder Diagnosis Dataset](https://www.kaggle.com/datasets/mdsultanulislamovi/sleep-disorder-diagnosis-dataset/data)  

### 📊 Keterangan Data
Beberapa variabel utama yang digunakan:

| Kolom                     | Deskripsi                                                      |
|----------------------------|----------------------------------------------------------------|
| Sleep Duration (hours)     | Lama tidur per hari responden                                   |
| Quality of Sleep (1–10)   | Skor kualitas tidur subjektif                                   |
| Physical Activity Level    | Aktivitas fisik harian dalam menit                              |
| Stress Level (1–10)        | Skor stres subjektif                                           |
| BMI Category               | Klasifikasi Indeks Massa Tubuh (Underweight, Normal, Overweight, Obese) |
| Occupation                 | Pekerjaan atau profesi responden                                |
| Sleep Disorder             | Label target: Insomnia, Sleep Apnea, None                     |

---

## 🧹 Tahapan Analisis

### 1. Definisi Library 📚
Mengimpor library Python yang dibutuhkan seperti `pandas`, `numpy`, `matplotlib`, `seaborn`, dan `scikit-learn`.

### 2. Baca Dataset 📂
Membaca data mentah, memahami struktur, serta memeriksa isi dataset.

### 3. Pembersihan Data 🧹
- **⭕ Cek Nilai Kosong** → Identifikasi missing values  
- **🗑️ Penghapusan Data** → Menghapus data yang tidak lengkap atau duplikat

### 4. EDA (Exploratory Data Analysis) 🔎
Analisis eksploratif untuk memahami pola data, seperti:
- Distribusi responden per Occupation 👩‍💼
- Distribusi responden per Gender 👥
- Distribusi BMI Category ⚖️
- Distribusi Sleep Disorder 💤
- Sleep Disorder vs Occupation 👩‍⚕️
- Sleep Disorder vs Gender 👨‍👩‍👧
- Sleep Disorder vs BMI Category 🏥

### 5. Correlation Matrix 🔢
Visualisasi korelasi antar variabel numerik untuk mengetahui hubungan fitur. Contohnya:
- Sleep Duration ↔ Quality of Sleep (positif sangat kuat)  
- Stress Level ↔ Quality of Sleep (negatif sangat kuat)

### 6. Data Mining ⛏️
- Mengubah kategori seperti Occupation dan BMI menjadi numerik (Label Encoding)
- Menstandarisasi fitur numerik (StandardScaler)

### 7. Implementasi Model 🤖
Menerapkan beberapa algoritma utama:
- **🌲 Random Forest**
- **⚡ Support Vector Machine (SVM)**
- **👟 K-Nearest Neighbors (KNN)**
- **🔬 Naive Bayes**
- **🌳 Decision Tree**

Evaluasi model dilakukan dengan **Confusion Matrix** dan **Classification Report**.

---

## 📈 Hasil Prediksi

### Perbandingan Akurasi Model

| Model                 | Accuracy | Keterangan Singkat                                                                 |
|-----------------------|----------|----------------------------------------------------------------------------------|
| Random Forest 🌲      | 90.32%   | Akurasi tertinggi dan performa seimbang antar kelas                                |
| SVM ⚡                | 80.65%   | Recall Sleep Apnea rendah, kadang salah klasifikasi                                |
| KNN 👟                 | 87.10%   | Performa seimbang, akurasi sedikit di bawah Random Forest                          |
| Naive Bayes 🔬         | 83.87%   | Bagus untuk mendeteksi Insomnia, kurang optimal untuk Sleep Apnea                  |
| Decision Tree 🌳       | 87.10%   | Mudah diinterpretasikan, performa seimbang tapi akurasi sedikit di bawah Random Forest |

**Kesimpulan:**  
Random Forest dipilih sebagai model utama karena akurasi tertinggi, performa seimbang, dan kemampuan menangkap pola non-linear antar fitur.

---
