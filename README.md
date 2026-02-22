# 🍄 Mushroom Edible vs Poisonous Classification  
## Attention-Guided Pruning & Quantization on :contentReference[oaicite:0]{index=0}

Repository ini berisi proses pengembangan dan eksperimen model deep learning untuk klasifikasi citra jamur **edible** dan **poisonous** menggunakan arsitektur MobileNetV3.

Penelitian ini berfokus pada penerapan teknik kompresi model berupa:

- **Attention-Guided Structured Pruning**
- **Post-Training Quantization (PTQ)**

Tujuan utama penelitian adalah menghasilkan model yang tetap memiliki akurasi tinggi namun lebih ringan, lebih cepat, dan efisien untuk diimplementasikan pada perangkat mobile.

Repository ini hanya mencakup proses:

- Training  
- Evaluasi  
- Analisis performa  
- Optimasi model  

Seluruh eksperimen tersedia dalam bentuk **Jupyter Notebook (.ipynb)** dan repository ini terpisah dari repository aplikasi (deployment).

---

# 🎓 Konteks Penelitian Skripsi

Penelitian ini dilakukan sebagai bagian dari skripsi dengan judul:

> **“Penerapan Attention-Guided Pruning dan Quantization pada MobileNetV3 untuk Klasifikasi Jamur Edible dan Poisonous.”**

Penelitian menganalisis secara sistematis:

- Pengaruh pruning terhadap performa klasifikasi  
- Dampak quantization terhadap ukuran model dan kecepatan inferensi  
- Trade-off antara efisiensi komputasi dan akurasi  
- Efektivitas model hybrid dibandingkan baseline  

Evaluasi dilakukan tidak hanya berdasarkan akurasi, tetapi juga mempertimbangkan efisiensi model sebagai bagian dari studi kompresi.

---

# 🧠 Ruang Lingkup Pengembangan Model

## 1️⃣ Baseline Model

Model awal yang digunakan:

- MobileNetV3 Small  
- MobileNetV3 Large  

Model baseline digunakan sebagai pembanding dari sisi:

- Akurasi  
- Precision  
- Recall  
- F1-Score  
- Waktu inferensi  
- Ukuran model  

Baseline menjadi fondasi sebelum dilakukan optimasi lanjutan.

---

## 2️⃣ Attention-Guided Structured Pruning

Penerapan structured pruning dilakukan untuk:

- Mengurangi jumlah parameter  
- Menghilangkan filter dengan kontribusi rendah  
- Meningkatkan efisiensi komputasi  
- Menekan ukuran model  

Eksperimen dilakukan pada beberapa tingkat sparsity untuk menganalisis pengaruhnya terhadap stabilitas dan performa model.

---

## 3️⃣ Post-Training Quantization (PTQ)

Optimasi lanjutan dilakukan menggunakan beberapa skema quantization:

- FP16  
- INT16  
- INT8  

Tujuan kuantisasi adalah meningkatkan efisiensi inferensi dan mengurangi ukuran model tanpa penurunan performa yang signifikan.

---

## 4️⃣ Hybrid Model (Final Model)

Model akhir merupakan kombinasi dari:

- MobileNetV3 Large  
- Attention-Guided Structured Pruning  
- Quantization (FP16 / INT16)  

Model ini dipilih berdasarkan keseimbangan terbaik antara:

- Akurasi klasifikasi  
- Ukuran model  
- Kecepatan inferensi  
- Stabilitas performa  

Model final dikonversi ke format **TensorFlow Lite (.tflite)** untuk implementasi pada perangkat mobile.

---

# 📊 Output Penelitian

Repository ini menghasilkan:

- Model baseline  
- Model hasil pruning  
- Model hasil quantization  
- Model hybrid terbaik  
- Model final dalam format `.tflite`  

Seluruh proses eksperimen dan analisis tersedia dalam bentuk notebook (.ipynb) sesuai metodologi penelitian skripsi.

---

# 📱 Implementasi Mobile (Flutter Deployment)

Model `.tflite` hasil penelitian ini digunakan pada aplikasi mobile berbasis Flutter.

🔗 **Repository Aplikasi Flutter:**  
https://github.com/dinnaaaa/Jamur-apps.git

Aplikasi tersebut memungkinkan:

- Pengambilan gambar melalui kamera  
- Pemilihan gambar dari galeri  
- Inferensi langsung di perangkat (on-device AI)  
- Menampilkan hasil klasifikasi edible atau poisonous beserta confidence relatif  

Dengan demikian:

- Repository ini berperan sebagai **core research & model development**
- Repository Flutter berperan sebagai **implementation & deployment layer**

---

# 📝 Catatan

- Repository ini berfokus pada eksperimen dan pengembangan model, bukan pada antarmuka aplikasi.  
- Seluruh konfigurasi training dan preprocessing disesuaikan dengan kebutuhan penelitian skripsi.  
- Evaluasi model mempertimbangkan performa dan efisiensi sebagai bagian dari studi kompresi model berbasis deep learning.
