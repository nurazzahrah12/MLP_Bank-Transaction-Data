# Proyek Machine Learning untuk Pemula: Clustering & Klasifikasi Transaksi

## Struktur Folder

```
├── [Clustering]_Submission_Akhir_BMLP_Nur_Salamah_Azzahrah.ipynb
├── [Klasifikasi]_Submission_Akhir_BMLP_Nur_Salamah_Azzahrah.ipynb
├── bank_transactions_data_edited.csv
├── data_clustering.csv
├── data_clustering_inverse.csv
├── decision_tree_model.h5
├── explore_random_forest_classification.h5
├── model_clustering.h5
├── PCA_model_clustering.h5
├── tuning_classification.h5
├── Kriteria Submission.txt
```

---

## Deskripsi Proyek

Proyek ini mencakup dua pendekatan utama:
1. **Clustering (Unsupervised Learning)** untuk mengelompokkan transaksi berdasarkan pola.
2. **Klasifikasi (Supervised Learning)** untuk memprediksi cluster dari fitur transaksi.

Proyek dikembangkan sesuai kriteria penilaian untuk mencapai level **Advanced**, mencakup preprocessing lengkap, EDA, model training, interpretasi, dan dokumentasi.

---

## Langkah-langkah Proyek

### 1. Exploratory Data Analysis (EDA)
- Visualisasi korelasi, histogram, distribusi target
- Visualisasi rapi tanpa label overlap

### 2. Preprocessing
- Cek null & duplikat (`isnull()`, `duplicated()`)
- Scaling (MinMaxScaler)
- Encoding (LabelEncoder)
- Drop ID-related columns
- Handling outlier dan binning (disertai encoding hasil binning)

### 3. Clustering
- Metode: `KMeans`, evaluasi dengan `Silhouette Score`
- Menentukan jumlah cluster optimal menggunakan `KElbowVisualizer`
- Menyimpan model clustering (`model_clustering.h5`)
- Model PCA disimpan: `PCA_model_clustering.h5` ✅

### 4. Interpretasi Hasil Clustering
- Inverse transform fitur & label
- Agregasi per klaster (mean, min, max, modus)
- Simpan hasil akhir `data_clustering_inverse.csv`
- Deskripsi karakteristik tiap klaster

### 5. Klasifikasi
- Dataset: hasil clustering dengan kolom `Target`
- Algoritma:
  - Decision Tree
  - Random Forest
- Hyperparameter tuning dilakukan
- Evaluasi: Akurasi, Presisi, Recall, F1-score
- Simpan model terbaik (`tuning_classification.h5`)

---

## File Penting

| File | Deskripsi |
|------|-----------|
| `bank_transactions_data_edited.csv` | Dataset awal |
| `data_clustering.csv` | Hasil clustering |
| `data_clustering_inverse.csv` | Hasil inverse clustering |
| `model_clustering.h5` | Model KMeans |
| `PCA_model_clustering.h5` | Model clustering dengan PCA |
| `decision_tree_model.h5` | Model klasifikasi awal |
| `explore_random_forest_classification.h5` | Model RF terbaik |
| `tuning_classification.h5` | Model klasifikasi ter-tuning |

---

## Umpan Balik Reviewer

**Semua kriteria utama terpenuhi dengan baik**:
- EDA menyeluruh dengan visualisasi rapi
- Preprocessing lengkap: scaling, encoding, handling outlier, binning
- Clustering dan interpretasi klaster disertai penyimpanan model
- Klasifikasi lengkap dengan tuning dan evaluasi
- Dokumentasi Jupyter Notebook sangat rapi

**Saran untuk pengembangan lebih lanjut:**
- Lakukan Grid Search, Random Search, atau Bayesian Optimization untuk tuning lebih mendalam
- Tambahkan Cross Validation untuk hasil evaluasi yang stabil
- Analisis error untuk memahami kesalahan prediksi
- Coba beberapa algoritma baru untuk pembanding
- Evaluasi performa pada data nyata
- Tambahkan `data storytelling` agar hasil lebih komunikatif

---

## Cara Menjalankan

1. Buka Jupyter Notebook / Google Colab
2. Jalankan dua file utama:
   - `[Clustering]_Submission_Akhir_BMLP_*.ipynb`
   - `[Klasifikasi]_Submission_Akhir_BMLP_*.ipynb`
3. Pastikan library berikut tersedia:
   - `pandas`, `numpy`, `sklearn`, `matplotlib`, `seaborn`, `joblib`, `yellowbrick`

---

## Kesimpulan

Proyek ini menunjukkan pemahaman mendalam tentang supervised dan unsupervised learning. Dengan EDA yang rapi, preprocessing yang lengkap, serta evaluasi yang jelas, proyek ini siap dikembangkan lebih lanjut menuju level machine learning lanjutan.
