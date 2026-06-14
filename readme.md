# Supervised Learning Final Project

![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)

## 📌 Deskripsi
Proyek ini merupakan tugas akhir mata kuliah **Supervised Learning**.  
Tujuan utama adalah membangun salah satu model klasifikasi menggunakan tiga algoritma:
- Naïve Bayes Classifier
- K-Nearest Neighbors (KNN)
- Decision Tree

Dataset yang digunakan:
- **Ecoli**
- **Thyroid**
- **Glass**

## 📂 Struktur Repository
```
├── 01.data-preprocessing.ipynb
├── 02.feature-engineering.ipynb
├── 03.model-training.ipynb
├── 04.model-evaluation.ipynb
├── 05.analysis-conclusion.ipynb
├── requirements.txt
└── README.md
```

## ⚙️ Instalasi
Clone repository ini dan install dependencies:
```bash
git clone https://github.com/hey-harton/ml-classification-project.git
cd ml-classification-project
pip install -r requirements.txt
```

## 🚀 Cara Menjalankan
1. Buka Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
2. Jalankan notebook sesuai urutan:
   - `01.data-preprocessing.ipynb` → cleaning & normalisasi data  
   - `02.feature-engineering.ipynb` → feature selection & extraction  
   - `03.model-training.ipynb` → training model (Naïve Bayes, KNN, Decision Tree)  
   - `04.model-evaluation.ipynb` → evaluasi (accuracy, precision, recall)  
   - `05.analysis-conclusion.ipynb` → analisis hasil & kesimpulan  

## 📊 Evaluasi
Setiap model akan dievaluasi menggunakan metrik:
- Accuracy
- Precision
- Recall

## 📝 Kesimpulan
Analisis singkat terhadap kinerja tiap model pada tiap dataset akan disajikan di notebook `05.analysis-conclusion.ipynb`.

