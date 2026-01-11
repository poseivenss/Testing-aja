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
Proyek Penelitian Deteksi Anomali Data Tabular
├── 1. Studi Literatur
│   ├── 1.1 Pencarian Literatur
│   │   ├── 1.1.1 Pencarian jurnal internasional
│   │   └── 1.1.2 Pencarian prosiding konferensi
│   └── 1.2 Tinjauan dan Sintesis Literatur
│       ├── 1.2.1 Seleksi artikel relevan
│       └── 1.2.2 Penulisan ringkasan dan gap penelitian
├── 2. Persiapan Data
│   ├── 2.1 Akuisisi Dataset
│   │   ├── 2.1.1 Identifikasi sumber dataset tabular
│   │   └── 2.1.2 Pengunduhan dan validasi dataset
│   └── 2.2 Pra-pemrosesan Data
│       ├── 2.2.1 Pembersihan data (missing & outlier awal)
│       └── 2.2.2 Normalisasi dan transformasi fitur
├── 3. Pengembangan Model
│   ├── 3.1 Implementasi Metode
│   │   ├── 3.1.1 Implementasi Isolation Forest
│   │   ├── 3.1.2 Implementasi Autoencoder
│   │   └── 3.1.3 Implementasi Local Outlier Factor
│   └── 3.2 Pelatihan dan Penyetelan Model
│       ├── 3.2.1 Pelatihan model
│       └── 3.2.2 Penyetelan hyperparameter
├── 4. Evaluasi dan Analisis
│   ├── 4.1 Pengujian Model
│   │   ├── 4.1.1 Pengujian pada data uji
│   │   └── 4.1.2 Penghitungan metrik evaluasi
│   └── 4.2 Analisis Hasil
│       ├── 4.2.1 Analisis perbandingan performa model
│       └── 4.2.2 Interpretasi hasil eksperimen
└── 5. Penyusunan Laporan
    ├── 5.1 Penulisan Dokumen
    │   ├── 5.1.1 Penulisan bab pendahuluan dan metodologi
    │   └── 5.1.2 Penulisan bab hasil dan pembahasan
    └── 5.2 Finalisasi Laporan
        ├── 5.2.1 Revisi berdasarkan masukan pembimbing
        └── 5.2.2 Penyusunan laporan akhir



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

