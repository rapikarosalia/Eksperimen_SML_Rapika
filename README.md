# Eksperimen SML Rapika
# Laporan Proyek Machine Learning - Rapika Rosalia Depari

## 1. Domain Proyek
Proyek ini berfokus pada bidang agrikultur, khususnya dalam proses klasifikasi otomatis varietas kacang Pistachio berdasarkan fitur-fitur fisik atau karakteristik morfologinya. Mengingat varietas yang berbeda memiliki nilai ekonomi dan kualitas yang berbeda, otomatisasi menggunakan Machine Learning ini diharapkan dapat membantu proses sortir pascapanen secara cepat dan akurat.

## 2. Business Understanding
* **Problem Statement**: Bagaimana cara mengklasifikasikan varietas kacang Pistachio secara akurat tanpa harus melakukan sortir manual yang memakan waktu lama?
* **Goals**: Membangun model prediksi klasifikasi yang dapat membedakan varietas Pistachio dengan tingkat akurasi yang tinggi.
* **Solution Statement**: Menggunakan algoritma **Random Forest Classifier** yang dikenal sangat stabil dan akurat untuk data tabular/terstruktur.

## 3. Data Understanding
Dataset yang digunakan adalah **Pistachio Dataset** yang memiliki 16 fitur karakteristik fisik dari kacang Pistachio (seperti Area, Perimeter, MajorAxisLength, MinorAxisLength, dll) dan 1 kolom target bernama `Class` yang berisi dua varietas utama:
1.  **Kirmizi**
2.  **Siirt**

## 4. Data Preprocessing
Tahap preprocessing yang dilakukan meliputi:
* Pemisahan fitur data ($X$) dan target/label ($y$).
* **Label Encoding**: Mengubah data kategorikal (teks "Kirmizi" dan "Siirt") pada kolom target menjadi representasi angka 0 dan 1 agar dapat diproses oleh model AI.
* **Data Splitting**: Membagi dataset menjadi **80% untuk data pelatihan (Training)** dan **20% untuk data pengujian (Testing)** dengan `random_state=42` untuk menjaga konsistensi hasil.

## 5. Modeling
Model dikembangkan menggunakan algoritma **Random Forest Classifier** dengan konfigurasi parameter standar `n_estimators=100`. Algoritma ini bekerja dengan membuat banyak pohon keputusan (decision trees) untuk menentukan hasil prediksi akhir berdasarkan voting terbanyak.

## 6. Evaluation
Berdasarkan hasil pengujian pada data testing, model berhasil mendapatkan performa yang sangat baik:
* **Akurasi Model**: **88.60%**
* Model juga telah diuji menggunakan satu data baru secara acak dan berhasil menebak varietas asli kacang dengan tepat dan benar (*Valid*).