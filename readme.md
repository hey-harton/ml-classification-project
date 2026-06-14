# Machine Learning Classification Project

![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-latest-orange)

## Deskripsi Proyek
Proyek ini merupakan Tugas Akhir untuk mata kuliah **Supervised Learning**. Tujuan utama dari proyek ini adalah membangun *end-to-end Machine Learning Pipeline* untuk menyelesaikan permasalahan klasifikasi *multi-class* menggunakan tiga algoritma pemelajaran mesin:
1. **Naïve Bayes Classifier**
2. **K-Nearest Neighbors (KNN)**
3. **Decision Tree**

Eksperimen klasifikasi dilakukan pada tiga dataset publik dari UCI Machine Learning Repository yang memiliki karakteristik dan tantangan berbeda (seperti *imbalanced data*):
- **[Ecoli Dataset (Protein Localization)](https://archive.ics.uci.edu/dataset/39/ecoli)**
- **[Glass Dataset (Glass Identification)](https://archive.ics.uci.edu/dataset/42/glass+identification)**
- **[Thyroid Dataset (Thyroid Disease Classification)](https://archive.ics.uci.edu/dataset/102/thyroid+disease)**

Eksperimen klasifikasi dilakukan pada tiga dataset publik yang memiliki karakteristik dan tantangan berbeda (seperti *imbalanced data*):
- **Ecoli Dataset** (Protein Localization)
- **Glass Dataset** (Glass Identification)
- **Thyroid Dataset** (Thyroid Disease Classification)

## Struktur Repositori
Proyek ini disusun dengan struktur direktori yang rapi untuk memisahkan antara data mentah, data olahan, model, dan skrip analisis:

```text
ml-classification-project/
├── datasets/
│   ├── raw/                 # Data mentah (.csv) hasil unduhan
│   ├── processed/           # Data hasil cleansing & label encoding
│   └── engineered/          # Data hasil scaling & handling imbalanced data (SMOTE)
├── models/                  # File model terlatih berformat (.pkl)
├── notebooks/               # Jupyter Notebooks untuk eksperimen
│   ├── 01.data-processing.ipynb
│   ├── 02.feature-engineering.ipynb
│   ├── 03.model-training.ipynb
│   ├── 04.model-evaluation.ipynb
│   └── 05.analysis-conclusions.ipynb
├── reports/                 # Hasil evaluasi (CSV) dan visualisasi grafik (PNG)
├── requirements.txt         # Daftar dependencies library Python
└── README.md                # Dokumentasi proyek
```

## Alur Kerja (Pipeline)

1. **Data Processing (`01`)**: Melakukan pembersihan data (*handling missing values* & duplikat), pemisahan *train-test split* (80:20), dan transformasi label (Label Encoding).
2. **Feature Engineering (`02`)**: Melakukan standarisasi fitur menggunakan `StandardScaler` dan mengatasi ketidakseimbangan kelas (*imbalanced data*) menggunakan pendekatan *Hybrid Resampling* (`SMOTETomek` untuk Ecoli & Glass, `SMOTEENN` untuk Thyroid).
3. **Model Training (`03`)**: Melatih kesembilan model secara otomatis dan mengekspor objek model ke dalam format `.pkl` (Joblib).
4. **Model Evaluation (`04`)**: Menguji model pada *test set* menggunakan metrik performa (*Accuracy, Precision, Recall, F1-Score* dengan konfigurasi *weighted average*).
5. **Analysis & Conclusion (`05`)**: Memvisualisasikan hasil perbandingan akurasi antarmodel dan membuat *Confusion Matrix* untuk mengevaluasi model terbaik (MVP) di masing-masing dataset.

## Instalasi & Cara Penggunaan

Untuk menjalankan proyek ini di mesin lokal, silakan ikuti langkah-langkah berikut:

**1. Clone repositori ini:**

```bash
git clone [https://github.com/hey-harton/ml-classification-project.git](https://github.com/hey-harton/ml-classification-project.git)
cd ml-classification-project

```

**2. Buat dan aktifkan *Virtual Environment* (Direkomendasikan):**

* **Windows:**
```bash
python -m venv venv
.\venv\Scripts\activate
```


* **Linux / macOS:**
```bash
python3 -m venv venv
source venv/bin/activate
```



**3. Instal *dependencies*:**

```bash
pip install -r requirements.txt
```

**4. Jalankan Notebook:**
Buka folder `notebooks/` menggunakan Jupyter Notebook atau VS Code, lalu eksekusi file secara berurutan mulai dari `01` hingga `05`.
