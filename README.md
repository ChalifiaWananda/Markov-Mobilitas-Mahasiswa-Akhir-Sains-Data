# Analisis Mobilitas Mahasiswa Menggunakan Rantai Markov

Repositori ini berisi analisis pola mobilitas harian mahasiswa Sains Data angkatan 2022 menggunakan **Model Rantai Markov (Markov Chain)** untuk memodelkan probabilitas perpindahan antar empat state lokasi utama di kampus: **Kelas (C), Kantin (K), Perpustakaan (P), dan Kosan (S)**.

Penelitian ini menggunakan dataset hasil kuesioner aktivitas mahasiswa per-jam pada rentang waktu **07.00–17.00 WIB selama lima hari kerja**, kemudian dilakukan penyusunan **Matriks Probabilitas Transisi**, perhitungan **Probabilitas Multi-Langkah (P², P³, P¹⁰)**, serta penentuan **Distribusi Stasioner (Steady-State Distribution)**.

---


## 📝 Pendahuluan

Mobilitas mahasiswa merupakan bentuk aktivitas perpindahan antar lokasi kampus berdasarkan kebutuhan akademik, sosial, dan personal. Model **Rantai Markov** digunakan untuk memodelkan pola perpindahan probabilistik berdasarkan kondisi saat ini tanpa mempertimbangkan kondisi sebelumnya (*memoryless property*).
Tujuan penelitian ini adalah:

* Mengetahui pola transisi antar lokasi mahasiswa
* Menyusun matriks probabilitas transisi
* Menghitung distribusi steady-state jangka panjang
* Memvisualisasikan pola mobilitas mahasiswa berdasarkan data empiris

---

## Struktur Repository

```
Markov-Mobilitas-Mahasiswa-ITERA-2025
│
├── README.md
├── laporan.pdf
│
├── data
│   ├── raw_data.csv
│
├── R
│   └── Markov-Analysis.R
│
├── gambar
│   ├── diagram_alir.png
│   ├── transition_graph.png
│   └── plot_frekuensi.png
│
└── output
    ├── matrix_transisi.xlsx
    ├── distribusi_stasioner.csv
    └── hasil_P10.csv
```

---

## Dataset

Data yang digunakan berupa hasil kuesioner aktivitas mahasiswa per-jam, direpresentasikan dalam empat state:

| Kode | Lokasi       |
| ---- | ------------ |
| C    | Kelas        |
| K    | Kantin       |
| P    | Perpustakaan |
| S    | Kosan        |

Total Observasi: **5.445 data posisi (99 mahasiswa × 55 waktu observasi)**

---

## Metodologi Analisis

* Penyusunan matriks transisi (N)
* Konversi ke matriks probabilitas transisi (P)
* Probabilitas multi-langkah (P², P³, P¹⁰)
* Distribusi stasioner (Eigenvector)
* Visualisasi graf transisi menggunakan edge weight

---

## Hasil Utama (Steady-State Distribution)

| Lokasi       | Proporsi   |
| ------------ | ---------- |
| Kelas        | **45.83%** |
| Kosan        | **45.27%** |
| Kantin       | **5.93%**  |
| Perpustakaan | **2.96%**  |

**Mahasiswa paling banyak berada di Kelas dan Kosan sebagai dua pusat aktivitas utama.**

---

## Cara Menjalankan Script R

```R
source("R/Markov-Analysis.R")
```

Pastikan package berikut sudah terinstall:

```R
install.packages(c("dplyr", "stringr", "igraph", "expm"))
```

---

## Tools & Library

| Tools/Library | Fungsi              |
| ------------- | ----------------------------- |
| RStudio       | Analisis dan komputasi Markov |
| expm          | Perhitungan Pⁿ                |
| igraph        | Diagram transisi              |
| dplyr         | Manipulasi data               |

---

## Anggota Kelompok

* **Ganiya Syazwa – 122450073**
* **Chalifia Wananda – 122450076**
* **Alvia Asrinda Br Ginting – 122450077**
* **Renisha Putri Giani – 122450079**

---


