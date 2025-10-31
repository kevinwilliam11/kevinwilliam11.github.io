---
title: "Strategi Testing"
date: 2025-08-25 07:30:00
categories: [Software Testing and Quality Assurance]
tags: [STQA]
image: /assets/images/STQA/strategi-testing.png
---

# Strategi Pengujian Perangkat Lunak

Pengujian adalah proses mengevaluasi perangkat lunak untuk menemukan cacat (bug) dan memastikan sistem memenuhi kebutuhan fungsional dan non-fungsional. Berikut ringkasan strategi dan klasifikasi pengujian yang umum digunakan.

---

### Tujuan Pengujian

* Menemukan dan memperbaiki cacat sebelum rilis.
* Verifikasi & validasi terhadap kebutuhan.
* Mengurangi risiko kegagalan dan meningkatkan kepercayaan pemangku kepentingan.
* Memastikan keamanan, performa, dan pengalaman pengguna.

---

### Siklus Hidup Pengujian Perangkat Lunak (STLC) — Langkah Utama

1. **Perencanaan** — buat rencana pengujian, identifikasi lingkungan, estimasi waktu/biaya.
2. **Perancangan** — identifikasi dan tulis test case, siapkan data pengujian.
3. **Eksekusi** — jalankan test case (manual/otomatis), catat hasil.
4. **Pelaporan & Analisis** — laporkan bug, tingkat keparahan, dan rekomendasi perbaikan.
5. **Penutupan** — evaluasi cakupan pengujian dan dokumentasi akhir.

---

### Klasifikasi menurut Tingkat Abstraksi

* **Unit Testing**: menguji fungsi/metode terkecil (contoh: memeriksa fungsi perhitungan diskon).
* **Integration Testing**: menguji interaksi antar modul (mis. modul login ↔ profil).
* **System Testing**: pengujian menyeluruh sistem (fungsional & non-fungsional).
* **Acceptance Testing**: pengujian oleh pengguna/klien untuk persetujuan akhir.

---

### Klasifikasi menurut Fungsi

* **Functional Testing** — verifikasi fitur sesuai spesifikasi (login, transaksi).
* **Non-Functional Testing** — pengujian performa, keamanan, keandalan, kegunaan.

---

### Klasifikasi menurut Domain

* **Performance Testing** — load/throughput/waktu respons.
* **Security Testing** — cek kerentanan (SQLi, XSS, dll.).
* **Usability Testing** — kemudahan penggunaan oleh pengguna akhir.

---

### Klasifikasi menurut Struktur

* **Black-box Testing** — fokus pada input/output tanpa melihat kode.
* **White-box Testing** — memeriksa alur kode, cakupan, dan jalur logis.

---

### Contoh Strategi Singkat

* Prioritaskan test case untuk fitur kritis (pembayaran, otentikasi).
* Gabungkan tes otomatis (unit + integration) untuk regresi.
* Jalankan tes beban saat tahap system testing sebelum go-live.
* Gunakan daftar prioritas bug (severity/priority) untuk perbaikan.

---

### Kesimpulan

Pengujian adalah bagian esensial dari SDLC untuk memastikan kualitas perangkat lunak. Kombinasi perencanaan yang baik, test case yang tertulis rapi, dan eksekusi terstruktur akan meminimalkan risiko saat rilis.

---