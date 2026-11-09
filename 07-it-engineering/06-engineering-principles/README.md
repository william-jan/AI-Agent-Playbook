# Software Engineering Principles

> 16 istilah · Bahasa Indonesia · Terminologi teknis tetap dalam bahasa Inggris.

[← Indeks handbook](../README.md) · [Kamus A–Z](../glossary-a-z.md)

## Isi

- [Separation of Concerns](#separation-of-concerns) · **prioritas pendalaman**
- [Single Responsibility Principle](#single-responsibility-principle)
- [DRY](#dry)
- [KISS](#kiss)
- [YAGNI](#yagni)
- [SOLID](#solid)
- [Dependency Injection](#dependency-injection)
- [Modularity](#modularity)
- [Technical Debt](#technical-debt)
- [Code Review](#code-review)
- [Refactoring](#refactoring)
- [Error Handling](#error-handling)
- [Type Safety](#type-safety) · **prioritas pendalaman**
- [Design Patterns](#design-patterns)
- [Domain Modeling](#domain-modeling)
- [API Versioning](#api-versioning)

## Penjelasan praktis

### Separation of Concerns

**Definisi.** Memisahkan tanggung jawab yang berbeda antarbagian kode.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan separation of concerns; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Pisahkan UI, rules dan akses data saat berguna.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Separation of Concerns dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Single Responsibility Principle

**Definisi.** Modul memiliki satu alasan utama untuk berubah.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan single responsibility principle; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Hindari modul serba bisa.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Single Responsibility Principle dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### DRY

**Definisi.** Menghindari duplikasi pengetahuan atau aturan penting.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan dry; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Jangan abstraksi terlalu dini.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi DRY dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### KISS

**Definisi.** Mengutamakan rancangan sederhana yang memenuhi kebutuhan.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan kiss; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Pilih solusi termudah yang dapat diuji.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi KISS dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### YAGNI

**Definisi.** Jangan membangun fitur yang belum benar-benar dibutuhkan.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan yagni; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Tolak abstraksi spekulatif.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi YAGNI dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### SOLID

**Definisi.** Lima pedoman desain object-oriented yang membantu maintainability.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan solid; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Terapkan seperlunya bukan sebagai ritual.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi SOLID dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Dependency Injection

**Definisi.** Penyediaan dependency dari luar modul.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan dependency injection; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Memudahkan substitusi pada test.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Dependency Injection dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Modularity

**Definisi.** Pemecahan sistem menjadi bagian dengan antarmuka jelas.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan modularity; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Jaga batas domain dan dependensi.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Modularity dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Technical Debt

**Definisi.** Biaya masa depan dari keputusan teknis yang mempercepat masa kini.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan technical debt; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Catat trade-off dan rencana perbaikan.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Technical Debt dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Code Review

**Definisi.** Peninjauan perubahan kode oleh manusia atau alat bantu.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan code review; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Tinjau perilaku, keamanan dan test.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Code Review dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Refactoring

**Definisi.** Memperbaiki struktur internal tanpa mengubah perilaku yang dimaksud.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan refactoring; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Amankan dengan regression tests.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Refactoring dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Error Handling

**Definisi.** Penanganan kegagalan dan penyampaian error yang dapat dipahami.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan error handling; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Jangan telan exception secara diam-diam.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Error Handling dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Type Safety

**Definisi.** Pencegahan sebagian kesalahan melalui kontrak tipe.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan type safety; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Ingat TypeScript tidak memvalidasi runtime.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Type Safety dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Design Patterns

**Definisi.** Solusi desain berulang untuk masalah umum.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan design patterns; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Pilih pola setelah masalahnya jelas.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Design Patterns dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Domain Modeling

**Definisi.** Memetakan aturan bisnis ke entitas, state dan invariant.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan domain modeling; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Jangan menaruh semua aturan di UI.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Domain Modeling dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### API Versioning

**Definisi.** Pengelolaan perubahan kontrak agar consumer lama tidak rusak.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan api versioning; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Rencanakan compatibility dan deprecation.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi API Versioning dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`

## Referensi kategori

- [Dokumentasi teknis terkait](https://www.typescriptlang.org/docs/)

> Referensi adalah titik awal belajar, bukan klaim bahwa setiap contoh telah diuji pada proyek tertentu.
