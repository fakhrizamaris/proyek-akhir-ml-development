# 🖼️ CIFAR-10 Image Classification

Sebuah proyek klasifikasi gambar menggunakan Convolutional Neural Network (CNN) untuk mengenali 10 kategori objek berbeda dari dataset CIFAR-10.

## 📋 Daftar Isi

- [Tentang Proyek](#-tentang-proyek)
- [Dataset](#-dataset)
- [Fitur Utama](#-fitur-utama)
- [Instalasi](#-instalasi)
- [Arsitektur Model](#️-arsitektur-model)
- [Hasil](#-hasil)
- [Struktur File](#-struktur-folder)
- [Teknologi yang Digunakan](#️-teknologi-yang-digunakan)

## 🎯 Tentang Proyek

Proyek ini mengimplementasikan deep learning untuk klasifikasi gambar menggunakan dataset CIFAR-10. Model yang dikembangkan dapat mengenali 10 jenis objek berbeda dengan tingkat akurasi mencapai **~90%**.

## 📊 Dataset

Menggunakan dataset [CIFAR-10](https://www.kaggle.com/datasets/oxcdcd/cifar10) yang berisi:

- **60.000 gambar** berwarna berukuran 32×32 piksel
- **10 kategori** objek yang berbeda
- **50.000 gambar** untuk pelatihan (training)
- **10.000 gambar** untuk pengujian (testing)

### Kategori yang dapat dikenali:

| No  | Kategori                   | Emoji |
| --- | -------------------------- | ----- |
| 1   | Pesawat terbang (airplane) | ✈️    |
| 2   | Mobil (automobile)         | 🚗    |
| 3   | Burung (bird)              | 🐦    |
| 4   | Kucing (cat)               | 🐱    |
| 5   | Rusa (deer)                | 🦌    |
| 6   | Anjing (dog)               | 🐕    |
| 7   | Katak (frog)               | 🐸    |
| 8   | Kuda (horse)               | 🐴    |
| 9   | Kapal (ship)               | 🚢    |
| 10  | Truk (truck)               | 🚛    |

## ✨ Fitur Utama

- **Data Augmentation**: Meningkatkan variasi data pelatihan
- **Early Stopping**: Mencegah overfitting
- **Model Checkpointing**: Menyimpan model terbaik otomatis
- **Multiple Format Export**: Tersedia dalam format Keras, TFLite, dan TensorFlow.js
- **Comprehensive Evaluation**: Laporan detail performa model

## 🚀 Instalasi

### Prasyarat

- Python 3.10+
- GPU T4 x2

### Langkah Instalasi

1. **Clone repository ini**

   ```bash
   git clone https://github.com/username/cifar10-classification.git
   cd cifar10-classification
   ```

2. **Install dependencies**

   ```bash
   pip install tensorflow keras scikit-learn numpy matplotlib seaborn pandas pillow
   ```

3. **Download dataset CIFAR-10**
   - Download dari [Kaggle](https://www.kaggle.com/datasets/oxcdcd/cifar10)
   - Ekstrak ke direktori `data/cifar10/`

## 🏗️ Arsitektur Model

Model CNN yang digunakan memiliki arsitektur sebagai berikut:

### Struktur Layer:

- **4 Blok Konvolusi** dengan filter yang meningkat (32 → 64 → 128 → 256)
- **Batch Normalization** pada setiap layer
- **Dropout** untuk mencegah overfitting
- **Global Average Pooling** untuk mengurangi parameter
- **2 Dense Layer** untuk klasifikasi final

### Spesifikasi Teknis:

- **Total Parameter**: 1,444,650
- **Optimizer**: Adam (learning rate: 0.001)
- **Loss Function**: Categorical Crossentropy
- **Epochs**: Maksimal 100 (early stopping pada epoch 84)

## 📈 Hasil

### Performa Model:

- **Akurasi Validasi**: ~89.75%
- **Akurasi Final**: ~90%
- **Pelatihan**: Berhenti otomatis pada epoch ke-84

### Visualisasi:

- ✅ Confusion Matrix
- ✅ Kurva Loss dan Akurasi
- ✅ Contoh Prediksi
- ✅ Laporan Klasifikasi per Kelas

## 📁 Struktur Folder

```
cifar10-classification/
├── 📓 notebook.ipynb          # Notebook utama
├── 📱 tflite/                 # Model untuk Mobile (tflite)
│   ├── model.tflite
│   └── label.txt
├── 🌐 tfjs_model/             # Model untuk Web
│   ├── model.json
│   └── group1-shard1of2.bin
├── 💾 saved_model/
│   ├── variables
│   └── saved_model.pb          # SavedModel format
└── requirements.txt            # file requirements
```

## 🛠️ Teknologi yang Digunakan

| Kategori             | Teknologi                      |
| -------------------- | ------------------------------ |
| **Deep Learning**    | TensorFlow, Keras              |
| **Data Processing**  | NumPy, Pandas, Scikit-learn    |
| **Visualisasi**      | Matplotlib, Seaborn            |
| **Image Processing** | Pillow (PIL)                   |
| **Model Deployment** | TensorFlow Lite, TensorFlow.js |
