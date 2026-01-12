# Proposal Tugas Akhir

- **Nama:** Muhammad Irfan Maulana  
- **NIM:** 202310370311480  

---

## 1. Topik Penelitian

### 1.1 Topik Penelitian
**Penerapan Metode Pembelajaran Mesin Tidak Terawasi untuk Deteksi Anomali dalam Data Tabular**

### 1.2 Tujuan Umum (Aim)
Mengembangkan dan mengevaluasi algoritma pembelajaran mesin tidak terawasi untuk deteksi anomali pada data tabular multivariat.

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

*Estimasi waktu mengikuti metode perhitungan effort dan durasi sesuai pedoman Minggu-11, slide 14. Effort menunjukkan jumlah waktu kerja aktual yang dibutuhkan, sedangkan durasi menunjukkan rentang waktu kalender hingga tugas selesai.*

| ID   | Leaf Task (Activity)                                          | Effort (minggu) | Durasi (minggu) | Ketergantungan |
|------|---------------------------------------------------------------|-----------------|-----------------|----------------|
| T1   | Pencarian jurnal deteksi anomali di database akademik         | 1               | 1               | -              |
| T2   | Seleksi dan review artikel relevan (min. 20 artikel)          | 1               | 1               | T1             |
| T3   | Penulisan ringkasan literatur dan identifikasi gap penelitian | 2               | 2               | T2             |
| T4   | Pengumpulan dataset tabular dari ADBench dan ODDS repository  | 1               | 1               | T3             |
| T5   | Preprocessing data (normalisasi, scaling, handling missing)   | 2               | 2               | T4             |
| T6   | Implementasi algoritma EIF, kNN, dan Isolation Forest         | 3               | 3               | T5             |
| T7   | Training dan hyperparameter tuning dengan grid search         | 2               | 2               | T6             |
| T8   | Pengujian model dan perhitungan metrik ROC-AUC dan AP         | 1               | 1               | T7             |
| T9   | Analisis perbandingan performa dan interpretasi hasil         | 1               | 1               | T8             |
| T10  | Penulisan bab pendahuluan dan metodologi                      | 1.5             | 1.5             | T9             |
| T11  | Penulisan bab hasil, pembahasan, dan kesimpulan               | 1.5             | 1.5             | T10            |

**Total Effort:** 17 minggu  
**Total Durasi:** 17 minggu

### 2.3 Critical Path

*Penentuan critical path mengikuti langkah-langkah pada Minggu-11, slide 18-25: (1) menentukan tanggal mulai paling awal untuk setiap aktivitas, (2) bekerja mundur dari akhir ke awal, (3) mengidentifikasi tugas-tugas yang tidak boleh tertunda.*

**Critical Path:** T1 → T2 → T3 → T4 → T5 → T6 → T7 → T8 → T9 → T10 → T11  

**Total Durasi Critical Path:** 17 minggu

**Justifikasi:**  
Seluruh aktivitas dalam proyek ini bersifat sekuensial dengan ketergantungan linear, sehingga setiap tugas harus diselesaikan sebelum tugas berikutnya dapat dimulai. Berdasarkan analisis jaringan aktivitas (Activity-on-Node), tidak terdapat aktivitas yang dapat dilakukan secara paralel karena setiap tugas memiliki satu predecessor. Hal ini berarti seluruh aktivitas berada pada jalur kritis dengan slack = 0. Konsekuensinya, keterlambatan pada satu aktivitas akan langsung berdampak pada waktu penyelesaian proyek secara keseluruhan. Referensi dari Bouman et al. (2024) menunjukkan bahwa evaluasi algoritma deteksi anomali memerlukan urutan kerja yang sistematis mulai dari persiapan data hingga evaluasi metrik[1].

### 2.4 Milestone

*Milestone merupakan langkah-langkah penting menuju penyelesaian proyek (Minggu-11, slide 16, 24, 25). Setiap milestone menandai pencapaian objektif tertentu.*

- **M1: Studi Literatur Selesai** — Minggu ke-4  
  *Deliverable:* Dokumen tinjauan pustaka mencakup minimal 20 artikel tentang teknik deteksi anomali (EIF, kNN, Isolation Forest, diffusion models) dan identifikasi gap penelitian.

- **M2: Data Siap Digunakan** — Minggu ke-7  
  *Deliverable:* Minimal 10 dataset tabular benchmark dari repository ADBench dan ODDS yang sudah melalui preprocessing (normalisasi, scaling, pembersihan data).

- **M3: Model Selesai Dikembangkan** — Minggu ke-12  
  *Deliverable:* Implementasi tiga algoritma (EIF, kNN, Isolation Forest) menggunakan PyOD dengan hyperparameter yang sudah di-tuning.

- **M4: Evaluasi dan Analisis Selesai** — Minggu ke-14  
  *Deliverable:* Hasil evaluasi lengkap dengan metrik ROC-AUC dan Average Precision untuk setiap algoritma pada seluruh dataset, serta analisis perbandingan performa.

- **M5: Laporan Akhir Selesai** — Minggu ke-17  
  *Deliverable:* Dokumen laporan penelitian final yang mencakup pendahuluan, metodologi, hasil, pembahasan, dan kesimpulan.

### 2.5 Activity-on-Node (AON) Diagram

*Diagram Activity-on-Node (AON) dibuat mengikuti pedoman Minggu-11, slide 26-37. Node persegi panjang merepresentasikan tugas, node wajik merepresentasikan milestone, dan panah menunjukkan urutan pelaksanaan tugas. Jalur kritis ditandai dengan warna merah.*

```mermaid
graph LR
  subgraph Phase1[Fase 1: Studi Literatur]
    T1["<b>T1: Pencarian Jurnal</b><br/>Minggu 1<br/>Durasi: 1 minggu"]
    T2["<b>T2: Seleksi Artikel</b><br/>Minggu 2<br/>Durasi: 1 minggu"]
    T3["<b>T3: Penulisan Ringkasan</b><br/>Minggu 3-4<br/>Durasi: 2 minggu"]
  end
  M1{{M1: Studi Literatur Selesai}}

  subgraph Phase2[Fase 2: Persiapan Data]
    T4["<b>T4: Pengumpulan Dataset</b><br/>Minggu 5<br/>Durasi: 1 minggu"]
    T5["<b>T5: Preprocessing Data</b><br/>Minggu 6-7<br/>Durasi: 2 minggu"]
  end
  M2{{M2: Data Siap Digunakan}}

  subgraph Phase3[Fase 3: Pengembangan Model]
    T6["<b>T6: Implementasi EIF, kNN, IF</b><br/>Minggu 8-10<br/>Durasi: 3 minggu"]
    T7["<b>T7: Training & Tuning</b><br/>Minggu 11-12<br/>Durasi: 2 minggu"]
  end
  M3{{M3: Model Siap Diuji}}

  subgraph Phase4[Fase 4: Evaluasi]
    T8["<b>T8: Pengujian Model</b><br/>Minggu 13<br/>Durasi: 1 minggu"]
    T9["<b>T9: Analisis Hasil</b><br/>Minggu 14<br/>Durasi: 1 minggu"]
  end
  M4{{M4: Evaluasi Selesai}}

  subgraph Phase5[Fase 5: Penyusunan Laporan]
    T10["<b>T10: Penulisan Pendahuluan & Metodologi</b><br/>Minggu 14.5-16<br/>Durasi: 1.5 minggu"]
    T11["<b>T11: Penulisan Hasil & Kesimpulan</b><br/>Minggu 16-17<br/>Durasi: 1.5 minggu"]
  end
  M5{{M5: Laporan Akhir Selesai}}

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
  T10 --> T11
  T11 --> M5

  style T1 fill:#ff6b6b,stroke:#333,color:#fff
  style T2 fill:#ff6b6b,stroke:#333,color:#fff
  style T3 fill:#ff6b6b,stroke:#333,color:#fff
  style T4 fill:#ff6b6b,stroke:#333,color:#fff
  style T5 fill:#ff6b6b,stroke:#333,color:#fff
  style T6 fill:#ff6b6b,stroke:#333,color:#fff
  style T7 fill:#ff6b6b,stroke:#333,color:#fff
  style T8 fill:#ff6b6b,stroke:#333,color:#fff
  style T9 fill:#ff6b6b,stroke:#333,color:#fff
  style T10 fill:#ff6b6b,stroke:#333,color:#fff
  style T11 fill:#ff6b6b,stroke:#333,color:#fff
```

*Catatan: Semua node berwarna merah menunjukkan bahwa seluruh aktivitas berada pada jalur kritis (critical path) dengan slack = 0.*

---

## 3. Latar Belakang Penelitian

Deteksi anomali merupakan bidang studi penting dalam pembelajaran mesin yang berfokus pada identifikasi data yang tidak sesuai dengan pola normal yang diharapkan. Dalam era big data saat ini, anomali dapat muncul dalam berbagai domain aplikasi seperti keamanan siber, kesehatan, keuangan, dan proses industri. Menurut Dai, Hwang, dan Fan (2024), deteksi anomali memiliki implikasi yang luas dalam analisis data modern, termasuk deteksi penipuan, deteksi intrusi jaringan, diagnostik medis, dan deteksi ledakan otomatis. Data tabular merupakan bentuk data yang paling umum digunakan dalam berbagai bidang ilmiah dan industri, sehingga pengembangan metode deteksi anomali yang efektif pada data jenis ini menjadi sangat krusial[1]. Pendekatan pembelajaran mesin tidak terawasi (unsupervised) menjadi semakin relevan karena prevalensi data yang tidak berlabel dalam praktik nyata, di mana proses pelabelan data memerlukan biaya dan waktu yang signifikan[2].

Di Indonesia, pemanfaatan metode deteksi anomali pada data tabular masih belum optimal, padahal banyak sektor strategis seperti perbankan, telekomunikasi, dan kesehatan menghasilkan data tabular dalam jumlah besar setiap harinya. Tantangan utama dalam implementasi metode ini di Indonesia adalah terbatasnya ketersediaan data berlabel untuk melatih model supervised learning, serta kompleksitas struktur data yang beragam antar domain. Dataset tabular dunia nyata seringkali mengandung sampel anomali yang dapat mempengaruhi analisis hilir secara negatif[2]. Selain itu, metode-metode tradisional seperti pendekatan berbasis proximitas (KNN, LOF, CBLOF) seringkali rentan terhadap pemilihan ukuran jarak dan kurang optimal pada data berdimensi tinggi, di mana curse of dimensionality menyebabkan jarak menjadi kurang bermakna[2]. Oleh karena itu, diperlukan pengembangan dan evaluasi metode deteksi anomali tidak terawasi yang lebih robust dan dapat beradaptasi dengan karakteristik data lokal di Indonesia.

Beberapa penelitian terdahulu telah memberikan kontribusi signifikan dalam bidang deteksi anomali tidak terawasi. Bouman, Bukhsh, dan Heskes (2024) melakukan studi komparatif terbesar hingga saat ini dengan mengevaluasi 33 algoritma deteksi anomali tidak terawasi pada 52 dataset tabular dunia nyata. Hasil penelitian mereka menunjukkan bahwa algoritma Extended Isolation Forest (EIF) secara signifikan mengungguli algoritma lainnya, dengan algoritma k-Nearest Neighbor (kNN) berkinerja terbaik pada dataset dengan anomali lokal, sementara EIF unggul pada dataset dengan anomali global[1]. Selanjutnya, Zamberg, Salhov, Lindenbaum, dan Averbuch (2023) mengembangkan TabADM, sebuah model probabilistik berbasis diffusion yang efektif untuk deteksi anomali tidak terawasi pada data tabular. Model mereka menggunakan skema penolakan unik untuk melemahkan pengaruh anomali pada estimasi densitas dan menunjukkan kinerja yang relatif stabil terhadap dimensi data tanpa memerlukan penyetelan hyperparameter yang ekstensif[2]. Penelitian terbaru oleh Dai, Hwang, dan Fan (2024) memperkenalkan metode novel berbasis noise evaluation yang mencapai skor AUC rata-rata 92,27% pada lebih dari 60 dataset benchmark, menunjukkan keunggulan dibandingkan 12 metode baseline termasuk state-of-the-art[3].

Pada penelitian ini, metode yang akan digunakan untuk deteksi anomali pada data tabular adalah pendekatan pembelajaran mesin tidak terawasi yang mengkombinasikan beberapa algoritma utama. Berdasarkan temuan dari studi komparatif Bouman et al. (2024), penelitian ini akan mengimplementasikan algoritma Isolation Forest, Extended Isolation Forest (EIF), dan k-Nearest Neighbor (kNN) sebagai metode baseline[1]. Pemilihan algoritma ini didasarkan pada kemampuannya dalam menangani berbagai tipe anomali, baik lokal maupun global. Isolation Forest bekerja dengan prinsip isolasi di mana anomali lebih mudah diisolasi dibandingkan data normal karena berada di region dengan densitas rendah[1]. Sebagai kontribusi utama, penelitian ini akan melakukan evaluasi komprehensif terhadap performa algoritma-algoritma tersebut pada dataset tabular yang relevan dengan konteks Indonesia, serta mengeksplorasi kombinasi optimal dari metode-metode tersebut untuk meningkatkan akurasi deteksi.

Penelitian ini diharapkan dapat memberikan kontribusi praktis dan ilmiah yang signifikan dalam bidang deteksi anomali. Dari sisi praktis, hasil penelitian dapat diaplikasikan untuk meningkatkan keandalan proses analisis data dalam berbagai sektor industri di Indonesia, seperti deteksi transaksi mencurigakan dalam sistem perbankan, identifikasi pola abnormal dalam data kesehatan pasien, dan monitoring kondisi peralatan industri untuk predictive maintenance. Dari sisi ilmiah, penelitian ini akan memberikan pemahaman yang lebih mendalam mengenai karakteristik algoritma deteksi anomali tidak terawasi pada data tabular, serta memberikan rekomendasi praktis mengenai pemilihan algoritma yang sesuai berdasarkan karakteristik dataset. Menurut Bouman et al. (2024), dengan mempertimbangkan kompleksitas komputasional algoritma, sebuah toolbox dengan dua algoritma deteksi anomali tidak terawasi (EIF dan kNN) sudah cukup memadai untuk menemukan anomali dalam koleksi representatif dataset multivariat[1]. Dengan demikian, penelitian ini diharapkan dapat mendukung pengambilan keputusan yang lebih akurat dan efisien dalam berbagai domain aplikasi.

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