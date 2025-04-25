
# Proyek Klasifikasi Gambar: Driver Inattention

### Deskripsi
Proyek ini bertujuan untuk membuat model klasifikasi gambar yang dapat mengidentifikasi perilaku pengemudi yang tidak fokus, seperti gangguan, mengantuk, atau perhatian yang teralihkan. Dataset yang digunakan berisi gambar yang menggambarkan berbagai kondisi pengemudi yang kurang waspada. Model ini dibangun menggunakan **Convolutional Neural Networks (CNN)** untuk mengklasifikasikan gambar ke dalam salah satu dari enam kategori berikut:

1. DangerousDriving (Mengemudi berbahaya)
2. Distracted (Terganggu)
3. Drinking (Sedang minum)
4. SafeDriving (Mengemudi aman)
5. SleepyDriving (Mengemudi dalam keadaan mengantuk)
6. Yawn (Mengantuk atau menguap)

### Langkah-langkah Proyek

1. **Pra-pemrosesan Data**:
   - Gambar diubah ukurannya menjadi 224x224 piksel.
   - Augmentasi gambar diterapkan pada data pelatihan untuk meningkatkan kemampuan generalisasi model.
   - Data dibagi menjadi set pelatihan, validasi, dan pengujian dengan proporsi 70%, 15%, dan 15% masing-masing.

2. **Membangun Model**:
   - Model CNN dirancang menggunakan lapisan Conv2D, MaxPooling2D, Dropout, dan Dense untuk klasifikasi gambar.
   - Optimizer yang digunakan adalah **Adam**, dengan fungsi loss **categorical crossentropy**.

3. **Evaluasi Model**:
   - Model diuji dengan menggunakan metrik akurasi, confusion matrix, dan classification report.

4. **Penyimpanan Model dalam Berbagai Format**:
   - **SavedModel**: Format standar TensorFlow untuk menyimpan dan memuat model kembali.
   - **TF-Lite**: Format yang lebih kecil dan dioptimalkan untuk perangkat mobile dan edge.
   - **TFJS**: Format untuk aplikasi web menggunakan TensorFlow.js.

5. **Menyimpan dan Mengunduh Model**:
   - Model disimpan dalam tiga format terpisah di folder masing-masing: `saved_model`, `tflite`, dan `tfjs_model`.
   - File model kemudian dikompresi menjadi satu file ZIP untuk memudahkan pengunduhan.

### Struktur Folder

- `/content/saved_model`: Model dalam format TensorFlow SavedModel.
- `/content/tflite`: Model dalam format TensorFlow Lite, beserta file `label.txt` untuk klasifikasi.
- `/content/tfjs_model`: Model dalam format TensorFlow.js untuk aplikasi berbasis web.

### Cara Menggunakan Model

1. **Menggunakan SavedModel**:
   - Model dapat dimuat kembali menggunakan `tensorflow.keras.models.load_model()` untuk melakukan prediksi atau pelatihan lebih lanjut.

2. **Menggunakan TF-Lite**:
   - Model dapat digunakan pada perangkat mobile dengan mengimpor file `.tflite` ke dalam aplikasi.

3. **Menggunakan TFJS**:
   - Model dapat dijalankan di browser menggunakan TensorFlow.js.

### Instalasi

Instalasi
Pastikan Python dan pip sudah terpasang di sistem Anda. Install semua dependensi yang dibutuhkan dengan menjalankan perintah berikut:

```bash
pip install -r requirements.txt
```


