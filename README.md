# 🍊 Fruit Classification: Orange vs Grapefruit

## 📌 Deskripsi Proyek

Proyek ini bertujuan untuk membangun model *machine learning* yang mampu mengklasifikasikan buah menjadi **orange (jeruk)** atau **grapefruit** berdasarkan karakteristik fisik seperti ukuran dan warna.

Tiga algoritma yang digunakan:

* Decision Tree
* Naive Bayes
* Support Vector Machine (SVM)

---

## 🎯 Tujuan

* Melakukan klasifikasi buah berbasis data numerik
* Membandingkan performa beberapa algoritma
* Menentukan model terbaik berdasarkan evaluasi

---

## 📊 Dataset

Dataset diambil dari Kaggle: **Oranges vs Grapefruit**

Fitur:

* `diameter`
* `weight`
* `red`, `green`, `blue`

Target:

* `name` (orange / grapefruit)

Karakteristik:

* Data seimbang
* Tidak ada missing value
* Cocok untuk klasifikasi

---

## 🔍 Exploratory Data Analysis (EDA)

### 📊 Distribusi Kelas

Menunjukkan bahwa jumlah data untuk setiap kelas seimbang.

```markdown id="img1"
![Distribusi Kelas](images/distribusi_kelas.png)
```

---

### 📊 Correlation Matrix

Digunakan untuk melihat hubungan antar fitur numerik.

```markdown id="img2"
![Correlation Matrix](images/correlation_matrix.png)
```

Insight:

* `diameter` dan `weight` memiliki korelasi sangat tinggi
* Fitur warna memiliki korelasi lebih rendah

---

## ⚙️ Preprocessing

Tahapan yang dilakukan:

* Label Encoding pada target
* Train-test split (80:20)
* Standardisasi menggunakan StandardScaler

---

## 🤖 Modeling

Model yang digunakan:

* Decision Tree
* Naive Bayes
* SVM

---

## 📈 Hasil Evaluasi

| Model         | Accuracy  |
| ------------- | --------- |
| Decision Tree | **0.944** |
| Naive Bayes   | 0.920     |
| SVM           | 0.937     |

---

### 📊 Visualisasi Perbandingan Model

```markdown id="img3"
![Perbandingan Model](images/perbandingan_model.png)
```

---

## 🧠 Analisis

* Decision Tree memiliki performa terbaik karena mampu menangkap pola berbasis threshold
* SVM menunjukkan performa yang stabil dan kompetitif
* Naive Bayes memiliki keterbatasan karena asumsi independensi fitur

---

## 🧾 Kesimpulan

Model **Decision Tree** merupakan pilihan terbaik untuk dataset ini, diikuti oleh SVM dan Naive Bayes.

Dataset yang seimbang membantu meningkatkan performa model secara keseluruhan.

---

## 📂 Struktur Project

```id="1dzzlf"
fruit-classification/
│
├── data/
│   └── citrus.csv
│
├── notebook/
│   └── model.ipynb
│
├── src/
│   └── main.py
│
├── images/
│   ├── distribusi_kelas.png
│   ├── correlation_matrix.png
│   └── perbandingan_model.png
│
├── README.md
└── requirements.txt
```

---

## ▶️ Cara Menjalankan

```id="tgqqmt"
pip install -r requirements.txt
python src/main.py
```

---

## ✅ Status

Program telah dijalankan tanpa error dan menghasilkan output evaluasi model.

---

## 📌 Catatan

Dibuat sebagai tugas Ujian Tengah Semester (UTS) Machine Learning.
