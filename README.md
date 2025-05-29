# Sentimen-Analisis-Ulasan

## Deskripsi Poyek
Proyek ini bertujuan untuk mengidentifikasi dan mengevaluasi opini pengguna terhadap aplikasi Alfagift melalui analisis sentimen ulasan yang diambil dari Google Play Store. Dengan memahami sentimen pengguna (positif atau negatif), perusahaan dapat memperoleh insight yang bermanfaat untuk meningkatkan pengalaman pengguna dan kualitas layanan aplikasi.

## Dataset
Data dikumpulkan secara mandiri melalui proses web scraping dari halaman ulasan aplikasi Alfagift di Play Store, dengan rincian sebagai berikut:
* Jumlah data: ± 5.000 ulasan
* Fitur:
  - Tanggal dan Waktu
  - Skor (Rating)
  - Ulasan (teks dari pengguna)

## Metodologi
### 1. Preprocessing Teks
Data ulasan yang dikumpulkan diproses melalui beberapa tahapan pembersihan dan transformasi teks agar siap digunakan untuk pelatihan model machine learning, yaitu:
* Cleaning: Menghapus mentions (@username), hashtag (#tag), retweet (RT), URL/link, angka, tanda baca, dan spasi kosong berlebih.
* Case Folding: Mengubah seluruh teks menjadi huruf kecil (lowercase).
* Tokenizing: Memecah kalimat menjadi kata-kata individual (token).
* Stopword Removal: Menghapus kata-kata umum (stopwords) dalam Bahasa Indonesia dan Inggris yang tidak memiliki nilai informasi signifikan.
* Stemming: Mengubah kata ke bentuk dasarnya menggunakan stemmer Bahasa Indonesia (Sastrawi).
* Reconstruction: Menggabungkan kembali token hasil filter menjadi kalimat bersih untuk keperluan pelabelan dan pelatihan model.

### 2. Metode Pelabelan
   Untuk memberikan label sentimen pada setiap ulasan pengguna, proyek ini menggunakan pendekatan berbasis kamus (lexicon-based approach) dalam Bahasa Indonesia. Setiap kata dalam kamus ini memiliki nilai/skor. Tujuannya adalah untuk membantu sistem menilai apakah sebuah ulasan bernada positif atau negatif berdasarkan kata-katanya.

### 3. Model Machine Learning
Model yang digunakan adalah Support Vector Machine (SVM), dengan hasil performa sebagai berikut:
* Akurasi Pelatihan: 88%
* Akurasi Pengujian: 85%
  
## Hasil
### Distribusi Sentimen
![image](https://github.com/user-attachments/assets/37a32f01-b661-4a1f-a0a6-f752380c4fcb)
### Word Cloud Ulasan
![image](https://github.com/user-attachments/assets/8a6846ad-f8de-42db-ba5e-5b5255b156c6)
### Word Cloud Ulasan Positif
![image](https://github.com/user-attachments/assets/923bba1c-4316-4da2-a41e-a6da1c45aaec)
### Word Cloud Ulasan Negatif
![image](https://github.com/user-attachments/assets/28a17a88-ba21-4717-9590-3f2631280f2c)
### Distribusi Panjang Teks
![image](https://github.com/user-attachments/assets/e05c5a87-49cd-41d2-96b3-4180ec5ddb11)
### Distribusi Kata
![image](https://github.com/user-attachments/assets/381dbb62-a65e-4288-929f-2dbf0fdc63a9)

## Demo Prediksi Sentimen Ulasan
![image](https://github.com/user-attachments/assets/c294b152-1142-4ec6-879d-b5970665a915)
