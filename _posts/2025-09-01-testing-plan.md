---
title: "Testing Plan"
date: 2025-09-01 07:30:00
categories: [Software Testing and Quality Assurance]
tags: [STQA]
image: /assets/images/STQA/testing-plan.png
---

# Rencana Pengujian (Testing Plan)

Artikel ini adalah template dan penjelasan *Test Plan* yang terstruktur dan praktis, yang dapat kamu gunakan kembali atau sesuaikan untuk proyek perangkat lunak apa pun. Dokumen ini merangkum bagian-bagian penting dari rencana pengujian dan menjelaskan apa yang perlu disertakan di setiap bagiannya agar aktivitas pengujian menjadi konsisten, terukur, dan dapat dilacak. Struktur ini mengikuti panduan umum dari standar perencanaan pengujian bergaya **IEEE-829**.

---

## 1. Identifikasi Rencana (Plan Identifier)
Penanda unik atau nomor versi untuk rencana pengujian ini. Gunakan untuk melacak revisi dan membedakan rencana ini dari proyek lain atau versi berikutnya. Sertakan riwayat versi dan nama penulis.

---

## 2. Referensi
Daftar dokumen, standar, dan sumber yang menjadi acuan atau dasar rencana pengujian (seperti dokumen spesifikasi kebutuhan, desain sistem, standar klasifikasi, atau template dokumentasi pengujian IEEE). Referensi memastikan konsistensi dengan artefak proyek lainnya.

---

## 3. Pendahuluan / Tujuan
Ringkasan singkat yang menjelaskan tujuan, sasaran, dan ruang lingkup pengujian. Jelaskan alasan keberadaan rencana ini dan apa yang ingin divalidasi oleh kegiatan pengujian. Bagian ini menetapkan ekspektasi bagi para pemangku kepentingan.

---

## 4. Item Pengujian (Scope)
Sebutkan komponen perangkat lunak, modul, fitur, atau artefak yang akan diuji. Nyatakan secara konkret: daftar modul, halaman, API, atau integrasi yang termasuk dalam ruang lingkup pengujian. Hal ini membantu menghindari ambiguitas saat eksekusi.

---

## 5. Fitur yang Akan Diuji
Jelaskan dari sudut pandang pengguna akhir fitur mana yang akan diverifikasi, beserta kriteria penerimaan umum untuk fitur tersebut. Prioritaskan fitur berdasarkan risiko dan dampak bisnis.

---

## 6. Fitur yang Tidak Akan Diuji
Cantumkan fitur yang dikecualikan beserta alasan pengecualiannya (misalnya di luar ruang lingkup, fitur stabil/legacy, atau ditunda ke rilis berikutnya). Pengecualian yang eksplisit mengurangi kesalahpahaman tentang cakupan pengujian.

---

## 7. Pendekatan / Strategi Pengujian
Jelaskan strategi keseluruhan:
- Jenis pengujian yang akan dilakukan (unit, integrasi, sistem, penerimaan).  
- Teknik pengujian yang digunakan (black-box, white-box, gray-box).  
- Pendekatan manual vs otomatis, alat yang digunakan, dan strategi data uji.  
- Kriteria lulus/gagal untuk item dan keseluruhan fase pengujian.  

Rancang pendekatan sehingga menjawab pertanyaan: *apa yang diuji, bagaimana cara mengujinya, dan mengapa diuji dengan cara tersebut.*

---

## 8. Kriteria Lulus / Gagal
Tentukan aturan terukur untuk menyatakan lulus atau gagal bagi setiap item dan untuk keseluruhan fase pengujian (misalnya: semua alur kritis harus lulus; tidak ada defect kategori blocking; ≥ 95% test case berhasil). Kriteria yang jelas mencegah keputusan go/no-go yang subjektif.

---

## 9. Kriteria Penangguhan & Pelanjutan
Nyatakan kondisi yang akan menunda pengujian (misalnya aplikasi crash, korupsi data, defect kritis) serta persyaratan yang harus dipenuhi untuk melanjutkan kembali (defect diperbaiki dan diverifikasi, lingkungan pengujian dipulihkan). Dokumentasi ini mencegah upaya yang sia-sia saat terjadi kegagalan besar.

---

## 10. Hasil Keluaran Pengujian (Deliverables)
Daftar artefak yang akan dihasilkan oleh tim pengujian: test case, hasil eksekusi, laporan bug dengan langkah reproduksi dan tangkapan layar, laporan ringkasan pengujian, dan dokumen persetujuan akhir.

---

## 11. Tugas yang Belum Selesai
Rinci item pekerjaan yang masih tersisa pada saat pelaporan status (test case yang belum ditulis, retest yang tertunda, tugas persiapan lingkungan). Hal ini membantu melacak progres menuju penyelesaian.

---

## 12. Kebutuhan Lingkungan
Sebutkan perangkat keras, sistem operasi, versi browser, data uji, kredensial, konfigurasi jaringan, serta sistem eksternal apa pun yang harus tersedia agar pengujian berjalan valid. Sertakan versi yang tepat agar hasil pengujian dapat direproduksi.

---

## 13. Tanggung Jawab
Tetapkan peran dan tanggung jawab (Manajer Pengujian, Tester, Developer, Release Manager). Jelaskan siapa yang menulis test case, siapa yang menjalankan, siapa yang meninjau defect, serta jalur eskalasinya.

---

## 14. Kebutuhan Staf dan Pelatihan
Daftar keterampilan yang dibutuhkan dan pelatihan yang direkomendasikan (misalnya pelatihan alat uji, pengetahuan domain). Identifikasi juga tester cadangan untuk mengurangi risiko ketergantungan pada satu orang.

---

## 15. Jadwal
Buat garis waktu untuk perencanaan pengujian, desain test case, siklus eksekusi, retesting, hingga tanda tangan persetujuan akhir. Sertakan tonggak (milestone) dan ketergantungan terhadap build pengembangan.

---

## 16. Risiko, Kontinjensi, dan Mitigasi
Identifikasi risiko yang mungkin terjadi pada kegiatan pengujian (build hilang, kebutuhan tidak jelas, lingkungan tidak stabil) dan solusi mitigasi yang diusulkan (lingkungan cadangan, sumber daya tambahan, sesi klarifikasi).

---

## 17. Glosarium & Singkatan
Definisikan istilah yang digunakan dalam rencana agar semua pemangku kepentingan memiliki pemahaman yang sama (contoh: “Test Plan Identifier”, “Test Items”, “Pass/Fail Criteria”).

---

## 18. Persetujuan
Catat pihak yang harus menyetujui rencana ini, sertakan nama, peran, tanda tangan, dan tanggal sebagai bentuk pelacakan (traceability).

---