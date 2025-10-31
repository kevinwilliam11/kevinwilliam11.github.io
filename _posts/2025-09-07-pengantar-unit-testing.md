---
title: "Pengantar Unit Testing"
date: 2025-09-07 07:30:00
categories: [Software Testing and Quality Assurance]
tags: [STQA]
image: /assets/images/STQA/pengantar-unit-testing.png
---

## Pengantar Unit Testing

*Unit testing* adalah praktik untuk memverifikasi bagian terkecil yang dapat diuji dari sebuah aplikasi — seperti fungsi, metode, atau kelas — secara terpisah (*isolasi*). Unit test biasanya ditulis dan dijalankan oleh pengembang untuk menemukan bug lebih awal, mendokumentasikan perilaku yang diharapkan, serta membuat proses *refactoring* menjadi lebih aman dan cepat.  
Materi dari **Kelompok 5** menyoroti ide utama, framework umum, serta pola **Arrange–Act–Assert (AAA)** yang digunakan dalam pengujian unit.

---

## Mengapa Unit Testing Penting

- **Menemukan bug lebih awal:** kesalahan yang ditemukan pada tahap unit test lebih murah dan cepat diperbaiki dibandingkan tahap akhir.  
- **Meningkatkan kualitas kode:** pengujian memaksa API lebih jelas dan mendorong desain yang modular.  
- **Memungkinkan refactoring yang aman:** kumpulan test yang baik membuat perubahan kode lebih percaya diri.  
- **Sebagai dokumentasi hidup:** test menggambarkan bagaimana kode *seharusnya* berperilaku.

---

## Pola AAA (Arrange — Act — Assert)

Struktur umum dalam unit test adalah **AAA**, yaitu:

1. **Arrange (Atur):** siapkan kondisi awal dan input (buat objek, setel nilai awal).  
2. **Act (Lakukan):** jalankan fungsi atau metode yang ingin diuji.  
3. **Assert (Verifikasi):** pastikan hasil keluaran atau efek samping sesuai dengan yang diharapkan.

Pola ini membantu menjaga agar test tetap jelas, mudah dibaca, dan mudah dirawat.

---

## Framework Unit Testing Populer (berdasarkan ekosistem)

- **JUnit 5** — untuk Java (dan bahasa berbasis JVM). Sudah matang, berbasis anotasi, dan banyak digunakan.  
- **pytest** — untuk Python. Minim konfigurasi, mendukung *fixtures*, dan laporan error yang informatif.  
- **Jest** — untuk JavaScript/TypeScript. Tanpa konfigurasi rumit, mendukung *snapshot testing* secara bawaan.  

Slide dari Kelompok 5 juga menampilkan contoh langsung (*live coding*) sederhana menggunakan **pytest** dan **JUnit 5**.

---

## Praktik Terbaik (Best Practices)

- Buat test **kecil** dan **terfokus** (satu skenario atau tujuan per test bila memungkinkan).  
- Pastikan test **deterministik** — hindari elemen acak atau ketergantungan pada kondisi eksternal.  
- **Isolasi** dependensi eksternal (gunakan *mock* atau *stub* untuk database, jaringan, atau file).  
- Prioritaskan test yang **cepat** — test lambat mengurangi frekuensi pengujian. Pisahkan test integrasi dari test unit.  
- Gunakan nama test yang **deskriptif** dan sertakan pesan kegagalan yang jelas.  
- Jalankan test **secara otomatis** di sistem CI setiap kali ada *push* atau *pull request*.

---