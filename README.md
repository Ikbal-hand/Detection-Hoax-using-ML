# Sistem Deteksi Berita Hoax (Hoax News Detection System)

![.NET](https://img.shields.io/badge/.NET-5C2D91?style=for-the-badge&logo=.net&logoColor=white)
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
![ML.NET](https://img.shields.io/badge/ML.NET-blue?style=for-the-badge)

Repository ini berisi dokumentasi dan source code untuk proyek **Deteksi Berita Hoax** menggunakan Machine Learning. Proyek ini dikembangkan sebagai tugas mata kuliah Machine Learning/AI.

## 📌 Latar Belakang (Case Study)
**Dinas Kominfo Desa Konoha** menghadapi masalah peningkatan penyebaran berita palsu (*hoax*) yang meresahkan warga. Sistem ini dirancang untuk mengotomatisasi proses verifikasi berita yang sebelumnya dilakukan secara manual, guna meningkatkan efisiensi dan akurasi penyaringan informasi.

## 🛠️ Teknologi yang Digunakan
Proyek ini dibangun sepenuhnya di lingkungan **Linux (Ubuntu)** tanpa menggunakan GUI Visual Studio, melainkan memanfaatkan CLI.

* **OS:** Ubuntu 24.04 LTS
* **Framework:** .NET 8.0 SDK
* **ML Tool:** ML.NET CLI (`mlnet`)
* **Bahasa Pemrograman:** C#
* **Algoritma:** Automated ML (AutoML)

## 📂 Dataset & Preprocessing
Dataset yang digunakan terdiri dari judul dan ringkasan berita berbahasa Indonesia.

* **Fitur:** `teks_berita` (String)
* **Label:** `label` (0 = Valid, 1 = Hoax)
* **Strategi Sampling:** Mengingat keterbatasan resource komputasi lokal untuk training ribuan data dalam waktu singkat (300 detik), dilakukan teknik **sampling** dengan mengambil 500 data teratas untuk keperluan *prototyping* dan pembuktian konsep (*Proof of Concept*).

## 📊 Hasil Evaluasi Model
Model dilatih menggunakan ML.NET CLI dengan durasi training **300 detik**.

| Metrik | Hasil |
| :--- | :--- |
| **Algoritma Terbaik** | **FastForestOva** (Fast Forest One-vs-All) |
| **Akurasi (MacroAccuracy)** | **83.33%** |
| **Total Model Dieksplorasi** | 34 Model |

> *Hasil ini membuktikan bahwa model mampu membedakan berita fakta dan hoax dengan tingkat akurasi di atas target 80%.*

## 🚀 Cara Menjalankan Project
Pastikan Anda telah menginstal `.NET SDK 8.0`.

1.  **Clone Repository ini:**
    ```bash
    git clone [https://github.com/username-anda/nama-repo.git](https://github.com/username-anda/nama-repo.git)
    cd nama-repo
    ```

2.  **Masuk ke folder aplikasi konsol:**
    ```bash
    cd ModelHoaxSample
    ```

3.  **Jalankan Aplikasi:**
    ```bash
    dotnet run
    ```

4.  **Input Sampel:**
    Masukkan kalimat berita ketika diminta, dan sistem akan memprediksi apakah itu Hoax atau Bukan.

## 📝 Artikel Terkait
Penjelasan lengkap mengenai langkah-langkah pengerjaan, mulai dari instalasi di Ubuntu hingga penanganan error, dapat dibaca di artikel Medium saya:

👉 **[Baca Artikel Medium Saya Disini]([LINK_MEDIUM_ANDA_DISINI](https://medium.com/@ikbal10222181/mendeteksi-berita-hoax-dengan-ml-net-cli-di-ubuntu-tanpa-coding-rumit-02863d61c291))**

---
**Developed by:**
[Nama Anda] - [NIM Anda]
