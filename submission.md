# Proposal Tugas Akhir

- **Nama:** Muhammad Irfan Maulana  
- **NIM:** 202310370311480  

---

## 1. Topik Penelitian

### 1.1 Topik Penelitian
**Penerapan Metode Pembelajaran Mesin Tidak Terawasi untuk Deteksi Anomali dalam Data Tabular**

### 1.2 Tujuan Umum (Aim)
Tujuan umum dari penelitian ini adalah mengembangkan dan mengevaluasi metode pembelajaran mesin tidak terawasi yang mampu mendeteksi anomali secara efektif pada data tabular sehingga dapat meningkatkan keandalan proses analisis data dan mendukung pengambilan keputusan yang lebih akurat.

### 1.3 Tujuan Khusus (Objectives)
- Mengumpulkan dan mempersiapkan dataset tabular yang relevan dalam waktu 3 minggu.
- Mengimplementasikan minimal tiga metode pembelajaran mesin tidak terawasi untuk deteksi anomali dalam waktu 4 minggu.
- Melakukan pelatihan dan penyetelan parameter model secara sistematis dalam waktu 2 minggu.
- Mengevaluasi kinerja setiap model menggunakan metrik evaluasi yang sesuai dalam waktu 2 minggu.
- Menyusun laporan akhir penelitian secara lengkap dan sistematis dalam waktu 3 minggu.

---

## 2. Perencanaan Pengerjaan Proyek

### 2.1 Work Breakdown Structure (WBS)

![Work Breakdown Structure](WBS.png)



### 2.2 Estimasi Waktu Leaf Task

| ID  | Leaf Task                        | Effort (minggu) | Durasi (minggu) | Ketergantungan |
|-----|----------------------------------|----------------|----------------|---------------|
| T1  | Pencarian jurnal                 | 1              | 1              | -             |
| T2  | Seleksi artikel                  | 1              | 1              | T1            |
| T3  | Penulisan ringkasan literatur    | 2              | 2              | T2            |
| T4  | Pengumpulan dataset              | 1              | 1              | T3            |
| T5  | Preprocessing data               | 2              | 2              | T4            |
| T6  | Implementasi model               | 3              | 3              | T5            |
| T7  | Training & tuning model          | 2              | 2              | T6            |
| T8  | Pengujian model                  | 1              | 1              | T7            |
| T9  | Analisis hasil                   | 1              | 1              | T8            |
| T10 | Penulisan laporan                | 3              | 3              | T9            |

### 2.3 Critical Path
Critical path proyek ini adalah:  
**T1 → T2 → T3 → T4 → T5 → T6 → T7 → T8 → T9 → T10**  
Total durasi proyek adalah **17 minggu**. Seluruh aktivitas pada jalur ini tidak memiliki slack sehingga keterlambatan satu aktivitas akan langsung mempengaruhi penyelesaian proyek.

### 2.4 Milestone
- **M1:** Studi literatur selesai (minggu ke-4)
- **M2:** Data siap digunakan (minggu ke-7)
- **M3:** Model selesai dikembangkan (minggu ke-12)
- **M4:** Evaluasi dan analisis selesai (minggu ke-14)
- **M5:** Laporan akhir selesai (minggu ke-17)

### 2.5 Activity-on-Node (AON) Diagram

*AON*
```mermaid
graph LR
  T1["<b>T1: Pencarian Jurnal</b><br/>Start: Minggu 1<br/>Durasi: 1 minggu"]
  T2["<b>T2: Seleksi Artikel</b><br/>Start: Minggu 2<br/>Durasi: 1 minggu"]
  T3["<b>T3: Penulisan Ringkasan Literatur</b><br/>Start: Minggu 3<br/>Durasi: 2 minggu"]
  M1{{Milestone 1: Studi Literatur Selesai}}

  T4["<b>T4: Pengumpulan Dataset</b><br/>Start: Minggu 5<br/>Durasi: 1 minggu"]
  T5["<b>T5: Preprocessing Data</b><br/>Start: Minggu 6<br/>Durasi: 2 minggu"]
  M2{{Milestone 2: Data Siap Digunakan}}

  T6["<b>T6: Implementasi Model</b><br/>Start: Minggu 8<br/>Durasi: 3 minggu"]
  T7["<b>T7: Training & Tuning Model</b><br/>Start: Minggu 11<br/>Durasi: 2 minggu"]
  M3{{Milestone 3: Model Siap Diuji}}

  T8["<b>T8: Pengujian Model</b><br/>Start: Minggu 13<br/>Durasi: 1 minggu"]
  T9["<b>T9: Analisis Hasil</b><br/>Start: Minggu 14<br/>Durasi: 1 minggu"]
  M4{{Milestone 4: Evaluasi Selesai}}

  T10["<b>T10: Penulisan Laporan</b><br/>Start: Minggu 15<br/>Durasi: 3 minggu"]
  M5{{Milestone 5: Laporan Akhir Selesai}}

  T1 --> T2
  T2 --> T3
  T3 --> M1
  M1 --> T4
  T4 --> T5
  T5 --> M2
  M2 --> T6
  T6 --> T7
  T7 --> M3
  M3 --> T8
  T8 --> T9
  T9 --> M4
  M4 --> T10
  T10 --> M5



## 3. Latar Belakang Penelitian

Kanker kulit adalah penyakit mematikan yang menyerang orang-orang di seluruh dunia. Menurut Organisasi Kesehatan Dunia (WHO), lebih dari 160.000 orang menderita penyakit kulit setiap hari di dunia. Australia memiliki tingkat penyakit kulit yang lebih tinggi dibandingkan negara lain, beberapa kali lebih tinggi dibandingkan Amerika Serikat. Menurut data Badan Pengukuran Australia, 32,6% dari seluruh warga Australia yang terkena pertumbuhan ganas juga menderita penyakit kulit. Terdapat 971.279 kasus penyakit kulit pada tahun 2012, dan 2.162 kasus diantaranya berakibat fatal. Sementara itu, data Habitats for Infectious Prevention and Control menunjukkan 8.885 orang meninggal akibat kanker kulit di Amerika Serikat pada tahun 2015.

Di Indonesia, hampir tidak ada korban kanker kulit dibandingkan dengan negara-negara kedua tersebut. Bagaimana pun penyakit kulit ini harus mendapat perhatian sesegera mungkin, karena selain dapat menimbulkan kerugian yang dapat merusak penampilan, namun juga dapat menyebabkan kematian bila sampai pada tahap tingkat tinggi. Dikutip dari Pusat Penelitian Sumber Daya dan Pelayanan Kesehatan Kemenkes Indonesia, pada tahun 2012, diperkirakan terdapat 14 juta kasus penyakit baru dan 8,2 juta kematian akibat pertumbuhan ganas di planet ini[1]. Selain itu, di Indonesia, berdasarkan data dari Disease Enrollment Organization, Hubungan Ahli Patologi Indonesia, dari 1.530 kasus kanker kulit, kasus terbanyak adalah karsinoma sel basal, tepatnya 39,93%. Oleh karena itu, kami sangat menginginkan suatu aplikasi produk yang dapat dimanfaatkan untuk membantu membedakan penyakit kulit secara dini tanpa adanya masalah. Aplikasi produk ini diyakini dapat membantu masyarakat secara umum dalam membedakan masalah kulit, terlepas dari apakah masalah tersebut termasuk dalam klasifikasi penyakit. Dengan cara ini, orang tidak akan tahu apa-apa tentang jenis masalah kulitnya, sehingga mereka dapat berkonsultasi dengan spesialis, khususnya ahli kulit dan kelamin yang terlatih[2].

Pertumbuhan sel kulit yang tidak normal dapat dibedakan menjadi dua jenis, yaitu benign (jinak) dan malignant (ganas). Pertumbuhan sel benign cenderung berlangsung lebih lambat dibandingkan dengan pertumbuhan sel malignant, karena pertumbuhan sel malignant dapat lebih cepat menyebar ke seluruh tubuh sebagai akibat infeksi[3]. Penelitian yang dilakukan oleh Bagus Mitra Sujatmiko, dkk. menunjukkan bahwa dengan melakukan preprocessing citra, augmentasi data, dan klasifikasi menggunakan 3 arsitektur model ResNet yaitu ResNet-18, ResNet-50, dan ResNet-101, masing-masing hasil akurasi dari ketiga arsitektur tersebut adalah 100%, 95%, dan 100%[8]. Selanjutnya penelitian dalam pendeteksian kanker kulit menggunakan image processing yang dilakukan oleh Aarushi Shah, dkk. menunjukkan bahwa proses preprocessing, segmentasi, feature extraction, classification menggunakan ANN dan CNN menghasilkan tingkat akurasi rata-rata sebesar 96.8% dan 92%[10]. Penelitian lain oleh Nur Alyyu, dkk dengan judul "Klasifikasi Kanker Kulit Ganas Dan Jinak Menggunakan Metode Convolutional Neural Network" menunjukkan nilai performa validasi akurasi sebesar 99% dengan parameter terbaik menggunakan optimizer AdaMax, Learning rate 0.0001, batch size 64 dan epoch sebanyak 50[11].

Pada penelitian ini metode yang digunakan untuk melakukan segmentasi dan klasifikasi kanker kulit berbasis pengolahan citra digital, yaitu Convolutional Neural Network dengan menggunakan Arsitektur Model ResNet-50. Convolutional Neural Network (CNN) dapat menangani permasalahan data yang berbentuk grid, seperti data gambar dan citra. CNN adalah metode terbaik dibandingkan dengan teknik lainnya karena dapat memperoleh fakta, meringkas model yang diperoleh, dan kualitas informasi dinamis[4][5]. CNN umumnya memiliki kemampuan untuk melakukan transfer learning dengan baik, dimana model yang telah dilatih pada dataset besar seperti ImageNet dapat digunakan sebagai titik awal (pre-trained model) untuk tugas-tugas penglihatan komputer lainnya dengan melakukan fine-tuning pada dataset yang lebih kecil[6]. Arsitektur model ResNet merupakan salah satu arsitektur model dari CNN untuk melatih jaringan yang sangat dalam tanpa mengalami masalah degradasi kinerja yang umumnya terjadi pada jaringan yang lebih dalam[7]. Arsitektur ini memiliki berbagai jenis model yang dibedakan berdasarkan jumlah layer, mulai dari 18 layer, 34 layer, 50 layer, 101 layer dan 152 layer[8]. ResNet telah berhasil digunakan di berbagai tugas machine learning dan penglihatan komputer, termasuk klasifikasi gambar, deteksi objek, dan segmentasi gambar[9].

Alasan memakai model CNN adalah memiliki kemampuan pembelajaran yang kuat sehingga dapat memodelkan hubungan kompleks antara input dan output, menjadikannya cocok untuk berbagai masalah prediksi dan klasifikasi termasuk yang tidak memiliki pola yang jelas. CNN dapat mendeteksi pola dan fitur-fitur penting yang mungkin sulit ditemukan oleh metode klasifikasi tradisional. CNN dapat disesuaikan dengan berbagai ukuran dan kompleksitas serta memiliki kemampuan untuk generalisasi, yang berarti dapat memprediksi dengan baik pada data yang belum pernah dilihat sebelumnya. Hal ini penting dalam pengujian model di luar sampel pelatihan[11][12]. Dengan penelitian ini, diharapkan dapat memberikan kontribusi dalam pengembangan sistem deteksi dini kanker kulit yang akurat dan dapat membantu tenaga medis serta masyarakat umum dalam mengidentifikasi potensi kanker kulit secara lebih cepat dan efisien.

---

## 4. Daftar Pustaka
*Gunakan format sitasi konsisten (APA atau IEEE). Masukkan minimal lima referensi utama dan urutkan sesuai pedoman di Minggu-11. Contoh format:*

- *NamaBelakang, Inisial. (Tahun). Judul artikel. Nama Jurnal, Volume(Nomor), halaman. DOI/URL.*

---

## 5. Prompt AI yang Digunakan
*Salin seluruh prompt dan ringkas respons AI yang relevan dengan penyusunan proposal. Gunakan format bernomor (Prompt 1, Prompt 2, dst.) seperti panduan dokumentasi AI pada README. Jika ada percakapan yang tidak dipakai, cantumkan tetap sebagai bukti penggunaan AI.*

---

> Checklist akhir:
> - [ ] Semua instruksi telah diganti dengan konten final.
> - [ ] Referensi berasal dari sumber akademik kredibel dan terdaftar di bagian ini.
> - [ ] Daftar prompt dan respons AI sudah didokumentasikan lengkap.
> - [ ] Seluruh bagian mematuhi ketentuan penggunaan AI hanya sebagai teman diskusi.