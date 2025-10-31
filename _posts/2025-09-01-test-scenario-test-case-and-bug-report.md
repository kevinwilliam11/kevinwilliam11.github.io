---
title: "Test Scenario, Test Case, and Bug Report"
date: 2025-09-01 08:30:00
categories: [Software Testing and Quality Assurance]
tags: [STQA]
image: /assets/images/STQA/test-scenario-test-case-and-bug-report.png
---

# Test Scenario, Test Case, and Bug Report

Dokumen ini menerjemahkan dan menggabungkan materi kelompok tentang *Test Scenario*, *Test Case*, dan *Bug Reporting* ke dalam referensi berbahasa Indonesia yang bisa digunakan kembali. Isinya mencakup template, contoh konkret skenario dan kasus uji untuk aplikasi BMI, contoh laporan bug, panduan tingkat *severity/priority*, serta praktik terbaik untuk mencegah bug.

---

## Gambaran Umum — Definisi

- **Skenario Uji (Test Scenario)** — Deskripsi tingkat tinggi tentang apa yang harus diuji; menggambarkan fungsi atau *user story* yang perlu divalidasi.  
- **Kasus Uji (Test Case)** — Instruksi detail langkah demi langkah untuk menjalankan pengujian, mencakup input, kondisi awal, hasil yang diharapkan, dan kriteria lulus/gagal.  
- **Laporan Bug (Bug Report)** — Laporan terstruktur yang mendeskripsikan cacat (*defect*) yang ditemukan selama pengujian, mencakup langkah reproduksi, hasil aktual vs ekspektasi, lingkungan, tingkat keparahan (*severity*), dan prioritas.

---

## Template Sederhana

### Template Skenario Uji

| Kolom | Deskripsi |
|---|---|
| ID Skenario | Identitas unik skenario (contoh: TS001) |
| Deskripsi | Ringkasan singkat skenario yang diuji |
| Modul / Fitur | Modul atau fitur yang diuji |

### Template Kasus Uji

| Kolom | Deskripsi |
|---|---|
| ID Kasus Uji | Identitas unik kasus uji (contoh: TC001) |
| Deskripsi | Penjelasan singkat tentang pengujian |
| Kondisi Awal | Kondisi sistem sebelum pengujian dimulai |
| Langkah Uji | Langkah-langkah yang harus dilakukan |
| Data Uji | Data input spesifik yang digunakan |
| Hasil yang Diharapkan | Hasil yang seharusnya muncul jika sistem benar |
| Hasil Aktual | Hasil yang diamati setelah dijalankan |
| Status | Lulus / Gagal (diisi saat pengujian) |

---

## Contoh: Aplikasi BMI — Skenario Uji

**ID** | **Deskripsi** | **Modul / Fitur**
---:|---|---
TS001 | Verifikasi perilaku slider input | Slider berat & tinggi badan  
TS002 | Verifikasi perhitungan dan klasifikasi BMI | Perhitungan & klasifikasi BMI  
TS003 | Verifikasi penyimpanan riwayat BMI | Riwayat BMI (penyimpanan/tampilan)

*(Skenario ini diambil dari rencana pengujian proyek.)*

---

## Contoh: Aplikasi BMI — Kasus Uji

> Catatan: Rumus BMI adalah `BMI = berat(kg) / (tinggi(m))^2`. Nilai ekspektasi dibulatkan hingga **2 desimal**.

| ID | Kasus Uji | Kondisi Awal | Langkah Uji | Data Uji | Hasil yang Diharapkan |
|---:|---|---|---|---:|---|
| TC001 | Verifikasi slider berat memperbarui label berat | Aplikasi terbuka | 1. Geser slider berat. 2. Amati label berat. | Slider → 60 kg | Label berat menampilkan `60 kg` sesuai posisi slider. |
| TC002 | Verifikasi slider tinggi memperbarui label tinggi | Aplikasi terbuka | 1. Geser slider tinggi. 2. Amati label tinggi. | Slider → 170 cm | Label tinggi menampilkan `170 cm` sesuai posisi slider. |
| TC003 | Verifikasi perhitungan BMI sesuai rumus standar | Aplikasi terbuka | 1. Atur tinggi → 170 cm. 2. Atur berat → 65 kg. 3. Tekan “Hitung”. | Tinggi = 170 cm, Berat = 65 kg | BMI ≈ **22.49** → hasil perhitungan benar. |
| TC004 | Verifikasi klasifikasi BMI: Kurus (Underweight) | Aplikasi terbuka | 1. Tinggi → 170 cm. 2. Berat → 45 kg. 3. Tekan “Hitung”. | Tinggi = 170 cm, Berat = 45 kg | BMI ≈ **15.57** → kategori `Underweight`. |
| TC005 | Verifikasi klasifikasi BMI: Normal | Aplikasi terbuka | 1. Tinggi → 165 cm. 2. Berat → 60 kg. 3. Tekan “Hitung”. | Tinggi = 165 cm, Berat = 60 kg | BMI ≈ **22.04** → kategori `Normal`. |
| TC006 | Verifikasi klasifikasi BMI: Overweight | Aplikasi terbuka | 1. Tinggi → 170 cm. 2. Berat → 75 kg. 3. Tekan “Hitung”. | Tinggi = 170 cm, Berat = 75 kg | BMI ≈ **25.95** → kategori `Overweight`. |
| TC007 | Verifikasi klasifikasi BMI: Obesitas | Aplikasi terbuka | 1. Tinggi → 165 cm. 2. Berat → 90 kg. 3. Tekan “Hitung”. | Tinggi = 165 cm, Berat = 90 kg | BMI ≈ **33.06** → kategori `Obese`. |
| TC008 | Verifikasi penyimpanan BMI terbaru ke Riwayat | Aplikasi terbuka | 1. Atur berat & tinggi. 2. Tekan “Simpan Riwayat”. 3. Buka halaman Riwayat. | Tinggi = 170 cm, Berat = 65 kg | Pengguna diarahkan ke Riwayat dan entri BMI terbaru tersimpan serta terlihat. |
| TC009 | Verifikasi penyimpanan banyak entri riwayat tanpa kehilangan data | Aplikasi terbuka & riwayat sudah ada | 1. Simpan beberapa hasil BMI berurutan. 2. Buka halaman Riwayat. | Serangkaian hasil BMI | Semua entri tersimpan berurutan tanpa kehilangan data. |

**Catatan:**  
Nilai ekspektasi BMI telah disesuaikan berdasarkan rumus standar dan pembulatan dua desimal.

---

## Laporan Bug — Template dan Contoh

### Template Laporan Bug
- **ID Bug:** identitas unik (misal: BMI-001)  
- **Judul:** deskripsi singkat masalah  
- **Pelapor:** nama / peran (misal: QA)  
- **Penanggung Jawab:** pengembang / tim terkait  
- **Severity:** Low / Minor / Major / Critical (tingkat dampak)  
- **Priority:** P1 (Mendesak) / P2 (Tinggi) / P3 (Sedang) / P4 (Rendah)  
- **Lingkungan:** OS / Browser / Versi Aplikasi / Nomor Build / Perangkat  
- **Langkah Reproduksi:** langkah-langkah untuk memunculkan bug  
- **Hasil Aktual:** perilaku yang muncul (sertakan screenshot/log jika perlu)  
- **Hasil Diharapkan:** perilaku yang seharusnya sesuai kebutuhan  
- **Build / Versi:** versi aplikasi di mana bug ditemukan  
- **Tanggal Pelaporan:** tanggal ditemukan  
- **Status:** Open / In Progress / Resolved / Closed

### Contoh Laporan Bug (Aplikasi BMI)
- **Bug ID:** BMI-001  
- **Judul:** Hasil BMI salah untuk berat 60 kg dan tinggi 170 cm  
- **Pelapor:** QA  
- **Penanggung Jawab:** Developer  
- **Severity:** Major — logika perhitungan salah, aplikasi tetap berjalan  
- **Priority:** P2 — Tinggi  
- **Lingkungan:** Android (Model perangkat), Versi App 1.0.0, Build 1.0.0  
- **Langkah Reproduksi:**  
  1. Buka aplikasi BMI.  
  2. Masukkan berat `60`.  
  3. Masukkan tinggi `170`.  
  4. Tekan tombol `Hitung`.  
- **Hasil Aktual:** BMI ditampilkan `12.50`.  
- **Hasil Diharapkan:** BMI seharusnya ≈ **20.76** (60 / 1.70² = 20.76).  
- **Tanggal Pelaporan:** 31 Agustus 2025  
- **Status:** Open  

> 💡 *Saran:* Sertakan screenshot hasil salah dan log aplikasi jika tersedia.

---

## Panduan Cepat — Severity & Priority

**Severity (dampak):**
- **Low:** Masalah kosmetik/minor; tidak memengaruhi fitur.  
- **Minor / Medium:** Gangguan kecil dalam pengalaman pengguna.  
- **Major / High:** Fungsi utama terganggu, aplikasi masih bisa digunakan sebagian.  
- **Critical:** Aplikasi crash, kehilangan data, atau fitur utama gagal total.

**Priority (urutan perbaikan):**
- **P1 (Mendesak):** Harus diperbaiki segera sebelum rilis.  
- **P2 (Tinggi):** Penting, segera diperbaiki.  
- **P3 (Sedang):** Dapat dijadwalkan untuk rilis berikutnya.  
- **P4 (Rendah):** Masalah visual atau minor, tidak mendesak.

---