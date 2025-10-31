---
title: "UI/UX Testing"
date: 2025-08-25 08:30:00
categories: [Software Testing and Quality Assurance]
tags: [STQA]
image: /assets/images/STQA/ui-ux-testing.png
---

# UI/UX Testing

Artikel ini merangkum materi *UI & UX Testing* (Slide Kelompok 2) — mencakup perbedaan, area fokus utama, alur kerja, contoh teknik, dan checklist heuristik untuk evaluasi desain. Konten disusun agar mudah dipahami dan dapat langsung dipakai sebagai referensi cepat dalam tugas QA atau latihan.

---

## Perbedaan Fundamental: UI vs UX
- **UI Testing** = berfokus pada elemen antarmuka: warna, ikon, ukuran tombol, tata letak, konsistensi visual, dan responsivitas.  
  *Contoh*: memastikan tombol **Login** muncul di posisi yang benar dan ukuran font dapat terbaca.  
- **UX Testing** = berfokus pada pengalaman pengguna secara keseluruhan: alur tugas, kemudahan mencapai tujuan, dan kepuasan pengguna.  
  *Contoh*: pengguna dapat menemukan produk dan menyelesaikan pembelian tanpa kebingungan.

---

## Area Fokus Utama untuk UI Testing
1. **Konsistensi Visual**  
   - Warna, tipografi, ikonografi, spasi, dan gaya tombol harus seragam di semua halaman.  
   - Teknik: checklist manual & visual regression testing (mis. Percy, Applitools).  
2. **Responsivitas**  
   - UI harus adaptif di berbagai ukuran layar: smartphone → tablet → desktop.  
   - Teknik: pengujian manual + tools (mis. BrowserStack, Responsively App).  
3. **Kompatibilitas**  
   - Lintas-browser & lintas-platform (Chrome, Firefox, Safari, Edge; macOS, Windows, iOS, Android).  
   - Tools: BrowserStack, Sauce Labs, LambdaTest.

---

## Area Fokus Utama untuk UX Testing
1. **Alur Kerja (Workflow)**  
   - Iteratif: perencanaan → rekrut pengguna → pelaksanaan sesi pengujian → analisis → iterasi desain.  
   - Contoh praktik: wawancara generatif → card sorting → tree testing → validasi prototipe.  
2. **Kegunaan (Usability)**  
   - Amati pengguna nyata menyelesaikan tugas, identifikasi hambatan, dan rekomendasikan perbaikan.  
3. **Aksesibilitas**  
   - Patuhi WCAG: kontras warna, navigasi keyboard, dukungan screen reader.  
   - Pengujian: tes kontras, alur keyboard-only, dan alat bantu seperti Axe atau Lighthouse.

---

## Metode & Alat yang Sering Digunakan
- **Heatmaps** (Hotjar, Crazy Egg, Microsoft Clarity) — untuk mengidentifikasi area yang sering diklik/dilihat.  
- **A/B Testing** — membandingkan dua variasi UI untuk metrik tertentu.  
- **Prototype testing** (Maze, Figma user testing) — cepat memvalidasi ide tanpa pengembangan penuh.  
- **Automated visual regression** (Percy, Applitools) — mendeteksi perubahan visual yang tidak disengaja.

---

## Heuristic Evaluation — Checklist Praktis
Gunakan heuristik berikut sebagai checklist saat meninjau desain:

- **Visibility of system status** — sistem memberikan umpan balik yang jelas untuk setiap aksi.  
- **Match between system and the real world** — gunakan bahasa/ikon yang familiar.  
- **User control and freedom** — sediakan opsi undo/keluar yang jelas.  
- **Consistency and standards** — desain seragam di seluruh fitur.  
- **Error prevention** — desain mencegah kesalahan; jangan hanya mengandalkan pesan error.  
- **Recognition rather than recall** — tampilkan affordance; jangan paksa pengguna mengingat.  
- **Flexibility and efficiency of use** — sediakan pintasan untuk pengguna ahli.  
- **Aesthetic and minimalist design** — hindari informasi yang tidak relevan.  
- **Help and documentation** — pesan error jelas dan dokumentasi mudah dicari.

---

## Contoh Checklist QA Praktis (Singkat)
- [ ] Tombol utama (CTA) terlihat dan memiliki kontras yang memadai.  
- [ ] Ukuran font untuk teks badan ≥ 14px (desktop) dan tetap terbaca pada mobile.  
- [ ] Navigasi dapat diakses melalui keyboard (urutan Tab).  
- [ ] Semua gambar memiliki atribut `alt` yang deskriptif.  
- [ ] Kontras teks vs latar memenuhi rasio minimum WCAG.  
- [ ] Form menampilkan pesan error yang jelas dan otomatis memfokuskan pada field bermasalah.  
- [ ] Halaman utama memuat dalam waktu yang wajar (performance smoke test).

---

## Integrasi Alur Kerja ke SDLC (Rekomendasi)
1. **Sebelum pengembangan**: buat desain & definisikan metrik keberhasilan.  
2. **Selama pengembangan**: jalankan unit + component tests, visual regression.  
3. **Sebelum rilis**: lakukan usability testing dengan sample pengguna, audit aksesibilitas, performance smoke test.  
4. **Setelah rilis**: kumpulkan analytics & heatmaps → iterasi berdasarkan data.

---