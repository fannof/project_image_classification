# Laporan Proyek Machine Learning - Novan Nur Hidayat

# Submission Akhir: Membuat Model Machine Learning untuk Klasifikasi Gambar Kendaraan

## Latar Belakang

Kendaraan adalah sebuah alat atau sarana transportasi yang digunakan untuk memindahkan orang atau barang dari satu tempat ke tempat lain. Kendaraan sendiri memiliki berbagai jenis, mulai dari kendaraan darat, air, hingga udara. Seiring dengan perkembangan zaman, kendaraan juga mengalami berbagai perkembangan teknologi yang membuatnya semakin canggih dan efisien dalam memenuhi kebutuhan transportasi manusia. Namun, dengan meningkatnya kebutuhan akan klasifikasi dan analisis data kendaraan, teknologi berbasis kecerdasan buatan (AI) seperti Machine Learning menjadi sangat relevan dalam mempermudah pengelompokan jenis kendaraan secara akurat. Proyek ini bertujuan untuk mengembangkan model Machine Learning yang mampu mengklasifikasikan gambar kendaraan secara otomatis dengan akurasi tinggi.

## Rumusan Masalah
Berdasarkan latar belakang diatas, dapat disimpulkan bahwa rumusan masalahnya adalah sebagai berikut:
- Apa saja tahapan dalam membangun model machine learning berbasis image classification yang mampu mengklasifikasi jenis gambar kendaraan?
- Arsitektur deep learning yang digunakan meliputi berapa layer dan terdiri dari layer apa saja?
- Berapa nilai akurasi dan loss dari model machine learning yang telah dibuat dengan arsitektur yang sudah ditentukan?

## Dataset
- **Sumber Dataset**: [Transportation Dataset](https://www.kaggle.com/datasets/yst990102/multi-class-transportation-dataset).  
- **Deskripsi**: Setiap kategori gambar kendaraan terdiri dari 1000 gambar data latih dan 200 gambar data uji yang dibagi menjadi 6 kelas (kapal, pesawat, mobil, truk sampah, kapal layar, dan sepeda).

## Arsitektur Model
Model yang digunakan dalam proyek ini adalah **Convolutional Neural Network (CNN)**, dengan detail sebagai berikut:  
- **Framework**: TensorFlow.  
- **Lapisan Model**:
  - Convolutional layers dengan filter dan ukuran kernel. Berisi 3 lapisan dengan filter (32) dan ukuran kernel (3x3, 4x4, 7x7).
  - Batch Normalization untuk normalisasi data antar lapisan yang digunakan setelah setiap Convolutional Layer.
  - MaxPooling untuk pengurangan dimensi fitur dengan ukuran pooling (2x2) untuk pengurangan dimensi.
  - Dense Layer yang berisi 128 unit dan 64 unit dengan aktivasi ReLU.
  - Dropout untuk mencegah overfitting dengan tingkat dropout 50% dan 30%.
- **Optimizer**: Adam.  
- **Loss Function**: Categorical Crossentropy yang digunakan untuk mengoptimalkan klasifikasi multi-kelas.
- 
