---
title: "Pengantar Cypress"
date: 2025-09-14 08:30:00
categories: [Software Testing and Quality Assurance]
tags: [STQA]
image: /assets/images/STQA/pengantar-cypress.png
---

# Pengantar Cypress — Modern End-to-End Testing for Web Apps

**Cypress** adalah framework modern untuk *end-to-end (E2E) testing* aplikasi web (React, Vue, Angular, atau bahkan HTML/JS biasa).  
Cypress menawarkan *interactive Test Runner*, *automatic waiting*, *time-travel debugging*, *network stubbing*, dan API yang sangat ramah bagi developer — memungkinkan penulisan skrip uji yang terasa seperti mendeskripsikan perilaku pengguna sebenarnya.

Artikel ini menjelaskan cara instalasi, perintah dasar, contoh pengujian praktis, penggunaan *fixtures* & *network stubbing*, integrasi dengan CI, praktik terbaik, serta contoh *test case* yang bisa langsung digunakan.

---

## Mengapa Cypress?

- **Umpan balik cepat:** melalui *interactive Test Runner* yang menampilkan setiap langkah uji dan status aplikasi (fitur *time-travel*).  
- **Menunggu otomatis:** Cypress secara otomatis menunggu elemen, *assertion*, dan respon jaringan tanpa harus menggunakan `sleep()`.  
- **Berjalan dalam konteks browser:** memungkinkan akses langsung ke `window`, `localStorage`, dan DOM.  
- **Mendukung screenshot & rekaman video otomatis** saat pengujian gagal.  
- **Mudah melakukan stubbing & mocking** menggunakan `cy.intercept()` serta *fixtures* untuk membuat tes deterministik.  

---

### Contoh Tes Sederhana

1. Tes untuk halaman login
```java
describe("Login Page", () => {
  it("should login successfully with valid credentials", () => {
    cy.visit("/login");
    cy.get("#username").type("user123");
    cy.get("#password").type("password123");
    cy.get("button[type="submit"]").click();

    cy.url().should("include", "/dashboard");
    cy.contains("Welcome, user123").should("be.visible");
  });
});
```

2. Tes untuk validasi form
```java
it("should show error for empty input", () => {
  cy.visit("/login");
  cy.get("button[type="submit"]").click();
  cy.contains("Username is required").should("be.visible");
});
```