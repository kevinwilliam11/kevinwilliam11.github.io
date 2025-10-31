---
title: "Pengantar Selenium WebDriver"
date: 2025-09-14 07:30:00
categories: [Software Testing and Quality Assurance]
tags: [STQA]
image: /assets/images/STQA/pengantar-selenium-webdriver.png
---

# Pengantar Selenium WebDriver

Artikel ini memberikan pengenalan praktis tentang **Selenium WebDriver** — meliputi apa itu Selenium, alasan penggunaannya, cara instalasi dan menjalankan otomatisasi browser dasar, pola umum (selector, wait), contoh implementasi dalam Python / Java / JavaScript, serta tips integrasi CI dan praktik terbaik.  
Sebagian materi diadaptasi dari slide presentasi kelompok.

---

## Apa itu Selenium & WebDriver

- **Selenium** adalah framework *open-source* untuk otomatisasi browser, biasa digunakan untuk pengujian fungsional atau *end-to-end testing*.  
- **WebDriver** merupakan komponen inti Selenium yang mengontrol browser seperti Chrome, Firefox, Edge, dan Safari melalui *driver binaries*.  
  WebDriver menyediakan API lintas bahasa (*language-agnostic*) dengan *bindings* untuk Python, Java, JavaScript, dan C#.  
- Penggunaan umum: validasi UI, *regression testing*, pengecekan kompatibilitas browser, serta otomatisasi alur kerja antarmuka pengguna.

---

## Mengapa Menggunakan Selenium

- Mendukung banyak bahasa pemrograman (Python, Java, JavaScript, C#, dsb).  
- Kompatibel dengan berbagai browser dan platform (Windows, macOS, Linux).  
- Dapat diintegrasikan dengan *test framework* seperti **pytest**, **JUnit**, **TestNG**, atau **Mocha**.  
- Memiliki komunitas besar dan ekosistem kuat (Selenium Grid, layanan cloud, plugin, dll).

---

## Instalasi Cepat & Contoh Pertama

> 💡 **Catatan:** Disarankan menggunakan *driver manager* agar tidak perlu mengunduh driver browser secara manual.

### Contoh Otomatisasi Dasar (Python)

```python
from selenium import webdriver
from selenium.webdriver.common.by import By
from webdriver_manager.chrome import ChromeDriverManager

# Arrange: Siapkan browser
driver = webdriver.Chrome(ChromeDriverManager().install())

# Act: Buka halaman dan cari elemen
driver.get("https://www.google.com")
search_box = driver.find_element(By.NAME, "q")
search_box.send_keys("Selenium WebDriver\n")

# Assert: Pastikan hasil pencarian muncul
assert "Selenium" in driver.title

driver.quit()
```