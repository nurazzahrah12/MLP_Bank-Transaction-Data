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

Proyek ini mencakup dua tahap utama:
1. **Clustering**: Mengelompokkan transaksi berdasarkan pola menggunakan K-Means.
2. **Klasifikasi**: Memprediksi cluster (target) berdasarkan fitur transaksi menggunakan Decision Tree dan Random Forest.

Model dan pipeline dibangun berdasarkan kriteria dari `Kriteria Submission.txt`, dengan tujuan memenuhi level evaluasi tertinggi (**Advanced**) dalam setiap kategori.

---

## Langkah-langkah yang Dilakukan

### 1. Exploratory Data Analysis (EDA)
- Melihat struktur dan ringkasan data (`head()`, `info()`, `describe()`)
- Visualisasi: korelasi, histogram, label yang rapi

### 2. Preprocessing
- Pembersihan null dan duplikat
- Scaling (MinMaxScaler)
- Encoding (LabelEncoder/get_dummies)
- Drop kolom ID
- Handling outlier dan binning

### 3. Clustering
- Visualisasi Elbow Method (`KElbowVisualizer`)
- Algoritma: `KMeans`, dilanjutkan PCA
- Evaluasi: `Silhouette Score`
- Model disimpan:
  - `model_clustering.h5`
  - `PCA_model_clustering.h5`

### 4. Interpretasi Clustering
- Deskripsi tiap cluster (min, max, mean)
- Inverse scaling & encoding
- Simpan hasil akhir: `data_clustering_inverse.csv`

### 5. Klasifikasi
- Target: `Target` hasil clustering
- Split data (`train_test_split`)
- Model:
  - Decision Tree → `decision_tree_model.h5`
  - Random Forest → `explore_random_forest_classification.h5`
  - Tuning → `tuning_classification.h5`
- Evaluasi: Akurasi, Presisi, Recall, F1-score

---

## File Penting

| Nama File | Deskripsi |
|-----------|-----------|
| `bank_transactions_data_edited.csv` | Dataset awal yang telah dibersihkan |
| `data_clustering.csv` | Data hasil clustering |
| `data_clustering_inverse.csv` | Data clustering setelah inverse transform |
| `model_clustering.h5` | Model KMeans akhir |
| `PCA_model_clustering.h5` | Model clustering dengan PCA |
| `decision_tree_model.h5` | Model klasifikasi Decision Tree |
| `explore_random_forest_classification.h5` | Model klasifikasi terbaik |
| `tuning_classification.h5` | Model klasifikasi setelah tuning |

---

## Cara Menjalankan

1. Buka Jupyter Notebook atau Google Colab
2. Jalankan:
   - `[Clustering]_Submission_Akhir_BMLP_*.ipynb`
   - `[Klasifikasi]_Submission_Akhir_BMLP_*.ipynb`
3. Pastikan package berikut terinstal:
   - `pandas`, `sklearn`, `matplotlib`, `seaborn`, `joblib`, `yellowbrick`
