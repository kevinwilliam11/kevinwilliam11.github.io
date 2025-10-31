---
title: "API Testing"
date: 2025-09-07 08:30:00
categories: [Software Testing and Quality Assurance]
tags: [STQA]
image: /assets/images/STQA/api-testing.png
---

# API Testing — Konsep, Alat, dan Contoh Praktis

Artikel ini menyajikan panduan ringkas dan praktis tentang **pengujian API (API Testing)** — mencakup pengertian, tujuan, alat yang umum digunakan (Postman, SoapUI, Newman, RestAssured, JMeter), anatomi permintaan dan respons, contoh permintaan GET/POST, teknik otomatisasi, pemeriksaan keamanan, serta contoh daftar uji (*test-case checklist*).

---

## Apa itu API Testing?

*API Testing* adalah proses untuk memverifikasi perilaku, keandalan, kinerja, dan keamanan dari *Application Programming Interface (API)*.  
Berbeda dengan pengujian antarmuka pengguna (*UI testing*), API testing berinteraksi langsung dengan lapisan logika bisnis aplikasi melalui protokol seperti HTTP, lalu memvalidasi respons, header, kode status, dan format data.

**Mengapa perlu menguji API?**
- Memastikan setiap *endpoint* berfungsi sesuai spesifikasi.  
- Menemukan bug lebih awal di lapisan integrasi.  
- Mendukung pengujian cepat tanpa UI (*headless testing*).  
- Menjadi dasar integrasi yang andal antar sistem.

---

## Manfaat Utama Pengujian API

- **Cepat & Cakupan Luas:** pengujian dapat dijalankan dengan cepat dan mencakup banyak skenario ekstrem.  
- **Mudah Diotomatisasi:** mudah diintegrasikan ke dalam *Continuous Integration (CI)*.  
- **Keamanan & Stabilitas:** membantu mendeteksi kesalahan kontrak, otentikasi, serta hambatan kinerja.  
- **Menguji logika bisnis secara langsung** tanpa bergantung pada tampilan UI.

---

## Alat Pengujian API yang Umum Digunakan

- **Postman** — antarmuka pengguna yang mudah, mendukung *collection*, *environment*, skrip uji, serta otomatisasi dengan Newman.  
- **SoapUI** — mendukung pengujian SOAP dan REST lanjutan (keamanan, skenario berbasis data).  
- **Newman** — *command-line runner* untuk menjalankan *Postman collections* (integrasi CI/CD).  
- **RestAssured** (Java) — pustaka Java yang elegan untuk menguji REST API.  
- **JMeter** — alat pengujian beban (*load testing*) dan performa untuk API.  
- **Insomnia** — klien REST ringan dengan dukungan *environment*.  
- **curl** — alat baris perintah cepat untuk mengirim permintaan dan debugging.

---

## Anatomi Permintaan (Request) dan Respons (Response)

### **Bagian dari Request**
- **HTTP Method (Verb):** GET, POST, PUT, PATCH, DELETE, OPTIONS.  
- **URL / Endpoint:** `/api/v1/users/123`.  
- **Headers:** `Content-Type`, `Authorization`, `Accept`.  
- **Query Params / Path Params:** `?page=2`, `/users/{id}`.  
- **Body (untuk POST/PUT/PATCH):** JSON, XML, atau *form data*.

### **Bagian dari Response**
- **Status Code:** 200, 201, 400, 401, 404, 500 — menunjukkan hasil dari permintaan.  
- **Headers:** informasi cache, tipe konten, atau otentikasi.  
- **Body:** data JSON/XML atau pesan kesalahan (*error details*).  
- **Timing:** waktu respons untuk pengujian performa.

---