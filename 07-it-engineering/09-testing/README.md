# Testing & Quality Assurance

> 10 istilah · Bahasa Indonesia · Terminologi teknis tetap dalam bahasa Inggris.

[← Indeks handbook](../README.md) · [Kamus A–Z](../glossary-a-z.md)

## Isi

- [Unit Testing](#unit-testing) · **prioritas pendalaman**
- [Integration Testing](#integration-testing) · **prioritas pendalaman**
- [End-to-End Testing](#endtoend-testing) · **prioritas pendalaman**
- [Regression Testing](#regression-testing)
- [Test Coverage](#test-coverage)
- [Mocking](#mocking)
- [Contract Testing](#contract-testing)
- [Load Testing](#load-testing)
- [Property-Based Testing](#propertybased-testing)
- [Static Analysis](#static-analysis)

## Penjelasan praktis

### Unit Testing

**Definisi.** Pengujian satu unit logika secara terisolasi.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan unit testing; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Uji edge cases dan invariant.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Unit Testing dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Integration Testing

**Definisi.** Pengujian beberapa komponen saat bekerja bersama.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan integration testing; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Gunakan database atau service test yang realistis.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Integration Testing dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### End-to-End Testing

**Definisi.** Pengujian alur pengguna dari antarmuka hingga backend.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan end-to-end testing; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Periksa login, pembayaran dan checkout.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi End-to-End Testing dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Regression Testing

**Definisi.** Pengujian agar perubahan tidak merusak perilaku sebelumnya.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan regression testing; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Jalankan kembali skenario bug yang diperbaiki.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Regression Testing dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Test Coverage

**Definisi.** Ukuran bagian kode yang dieksekusi pengujian.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan test coverage; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Coverage tinggi bukan jaminan kualitas.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Test Coverage dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Mocking

**Definisi.** Penggantian dependency dengan perilaku buatan dalam test.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan mocking; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Jangan mock sampai bug integrasi tersembunyi.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Mocking dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Contract Testing

**Definisi.** Pemeriksaan kesepakatan format antarconsumer dan provider.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan contract testing; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Deteksi perubahan API yang merusak.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Contract Testing dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Load Testing

**Definisi.** Simulasi beban untuk mengukur kapasitas atau latensi.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan load testing; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Gunakan lingkungan dan batas aman.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Load Testing dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Property-Based Testing

**Definisi.** Uji sifat umum dengan beragam input yang digenerasikan.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan property-based testing; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Cocok untuk rules dan fungsi murni.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Property-Based Testing dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Static Analysis

**Definisi.** Analisis kode tanpa menjalankan seluruh program.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan static analysis; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Gabungkan lint, typecheck dan security scanner.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Static Analysis dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`

## Referensi kategori

- [Dokumentasi teknis terkait](https://playwright.dev/docs/intro)

> Referensi adalah titik awal belajar, bukan klaim bahwa setiap contoh telah diuji pada proyek tertentu.
