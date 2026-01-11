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
Proyek Penelitian
├── Studi Literatur
│ ├── Pengumpulan Referensi
│ │ ├── Pencarian jurnal
│ │ └── Seleksi artikel
│ └── Penyusunan Ringkasan Literatur
│ ├── Klasifikasi topik
│ └── Penulisan ringkasan
├── Persiapan Data
│ ├── Pengumpulan Dataset
│ │ ├── Unduh dataset
│ │ └── Validasi dataset
│ └── Preprocessing Data
│ ├── Pembersihan data
│ └── Normalisasi
├── Pengembangan Model
│ ├── Implementasi Model
│ │ ├── Isolation Forest
│ │ ├── Autoencoder
│ │ └── Local Outlier Factor
│ └── Training & Tuning Model
│ ├── Pelatihan model
│ └── Penyetelan parameter
├── Evaluasi dan Analisis
│ ├── Pengujian model
│ └── Analisis hasil
└── Penyusunan Laporan
├── Penulisan laporan
└── Revisi akhir


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

3. Latar Belakang Penelitian

Perkembangan teknologi informasi telah menghasilkan data dalam jumlah besar dengan struktur yang kompleks, terutama dalam bentuk data tabular yang banyak digunakan di bidang keuangan, kesehatan, manufaktur, dan keamanan. Di dalam data tersebut sering terdapat anomali yang dapat mengganggu proses analisis dan menyebabkan kesalahan dalam pengambilan keputusan apabila tidak terdeteksi dengan baik.

Masalah utama dalam deteksi anomali adalah keterbatasan data berlabel, sehingga metode supervised sulit diterapkan. Oleh karena itu, pendekatan pembelajaran mesin tidak terawasi menjadi solusi yang menjanjikan karena mampu mempelajari pola data normal dan mendeteksi penyimpangan tanpa memerlukan label.

Beberapa penelitian terdahulu menunjukkan efektivitas metode unsupervised learning seperti Isolation Forest dan Autoencoder dalam mendeteksi anomali pada data berdimensi tinggi (Liu et al., 2008; Chalapathy & Chawla, 2019).

Penelitian ini berfokus pada penerapan dan perbandingan beberapa metode pembelajaran mesin tidak terawasi untuk deteksi anomali pada data tabular dengan tujuan memperoleh model yang paling efektif dan stabil.

Hasil penelitian ini diharapkan dapat memberikan kontribusi praktis dalam meningkatkan keandalan sistem analisis data dan memberikan referensi ilmiah bagi penelitian selanjutnya di bidang deteksi anomali.

4. Daftar Pustaka

Liu, F. T., Ting, K. M., & Zhou, Z. H. (2008). Isolation Forest. IEEE International Conference on Data Mining.

Chalapathy, R., & Chawla, S. (2019). Deep Learning for Anomaly Detection: A Survey. ACM Computing Surveys.

Aggarwal, C. C. (2017). Outlier Analysis. Springer.

Zong, B., et al. (2018). Deep Autoencoding Gaussian Mixture Model for Unsupervised Anomaly Detection. ICLR.

Chandola, V., Banerjee, A., & Kumar, V. (2009). Anomaly Detection: A Survey. ACM Computing Surveys.

5. Prompt AI yang Digunakan

Prompt 1: Diskusi penentuan topik dan tujuan penelitian.
Prompt 2: Penyusunan Work Breakdown Structure dan estimasi waktu.
Prompt 3: Penyusunan latar belakang penelitian dan referensi akademik.
Prompt 4: Penyempurnaan perencanaan proyek dan AON diagram.