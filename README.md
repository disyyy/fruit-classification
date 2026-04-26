 # 🍊 Fruit Classification: Orange vs Grapefruit

## 📌 Deskripsi Proyek

Proyek ini bertujuan untuk membangun model *machine learning* yang mampu mengklasifikasikan buah menjadi **orange (jeruk)** atau **grapefruit (anggur)** berdasarkan fitur numerik.

Model yang digunakan dan dibandingkan:

* Decision Tree
* Naive Bayes
* Support Vector Machine (SVM)

---

## 📊 Dataset

Dataset yang digunakan berasal dari Kaggle:
Oranges vs Grapefruit Dataset

Dataset terdiri dari fitur:

* `diameter`
* `weight`
* `red`
* `green`
* `blue`

Target:

* `name` → orange / grapefruit

Jumlah data:

* ±10.000 data (balanced)

---

## ⚙️ Tahapan Pengerjaan

### 1. Data Collection

Dataset diunduh dari Kaggle dan disimpan dalam folder `data/`.

---

### 2. Data Understanding (EDA)

Dilakukan eksplorasi data untuk memahami:

* Struktur dataset
* Tipe data
* Distribusi label
* Statistik deskriptif

Hasil:

* Dataset tidak memiliki missing values
* Distribusi kelas seimbang
* Semua fitur berupa numerik

---

### 3. Data Preprocessing

#### a. Encoding Label

Kolom `name` diubah menjadi numerik:

* orange → 1
* grapefruit → 0

#### b. Split Data

Dataset dibagi menjadi:

* Training set (80%)
* Testing set (20%)

#### c. Normalisasi

Dilakukan standardisasi menggunakan `StandardScaler` untuk meningkatkan performa model, terutama pada SVM.

---

### 4. Modeling

#### 🔹 Decision Tree

Model berbasis pohon keputusan yang mudah diinterpretasikan.

#### 🔹 Naive Bayes

Model probabilistik dengan asumsi independensi antar fitur.

#### 🔹 Support Vector Machine (SVM)

Model yang mencari hyperplane optimal untuk memisahkan data.

---

### 5. Evaluasi Model

Evaluasi dilakukan menggunakan:

* Accuracy
* Confusion Matrix
* Classification Report

---

## 📈 Hasil dan Perbandingan

| Model         | Kelebihan         | Kekurangan          |
| ------------- | ----------------- | ------------------- |
| Decision Tree | Mudah dipahami    | Rentan overfitting  |
| Naive Bayes   | Cepat & sederhana | Asumsi independensi |
| SVM           | Akurasi tinggi    | Perlu scaling       |

### 🔍 Insight

* **SVM** memberikan performa terbaik dalam klasifikasi
* **Naive Bayes** unggul dalam kecepatan
* **Decision Tree** unggul dalam interpretasi

---

## 🧠 Kesimpulan

Berdasarkan hasil eksperimen, model **Support Vector Machine (SVM)** memberikan akurasi terbaik dalam mengklasifikasikan buah. Hal ini karena SVM mampu memisahkan data dengan margin optimal.

Namun:

* Naive Bayes cocok untuk komputasi cepat
* Decision Tree cocok untuk interpretasi model

---

## 📂 Struktur Project

```
fruit-classification/
│
├── data/
│   └── citrus.csv
│
├── notebook/
│   └── eksplorasi.ipynb
│
├── src/
│   └── main.py
│
├── README.md
└── requirements.txt
```

---

## ▶️ Cara Menjalankan Program

1. Install dependencies:

```
pip install -r requirements.txt
```

2. Jalankan program:

```
python src/main.py
```

---

## 🛠️ Teknologi yang Digunakan

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn

---

## 📌 Catatan

Proyek ini dibuat sebagai tugas Ujian Tengah Semester (UTS) pada mata kuliah Machine Learning.
