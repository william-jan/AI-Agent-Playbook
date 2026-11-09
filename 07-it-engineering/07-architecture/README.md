# System Architecture

> 14 istilah · Bahasa Indonesia · Terminologi teknis tetap dalam bahasa Inggris.

[← Indeks handbook](../README.md) · [Kamus A–Z](../glossary-a-z.md)

## Isi

- [Monolith](#monolith)
- [Modular Monolith](#modular-monolith)
- [Microservices](#microservices)
- [Horizontal Scaling](#horizontal-scaling) · **prioritas pendalaman**
- [Vertical Scaling](#vertical-scaling)
- [Stateless Services](#stateless-services) · **prioritas pendalaman**
- [Stateful Services](#stateful-services)
- [Event-Driven Architecture](#eventdriven-architecture)
- [Event Sourcing](#event-sourcing)
- [CQRS](#cqrs)
- [CAP Theorem](#cap-theorem)
- [Circuit Breaker](#circuit-breaker)
- [Retry with Backoff](#retry-with-backoff)
- [Fault Tolerance](#fault-tolerance)

## Penjelasan praktis

### Monolith

**Definisi.** Aplikasi dibangun dan dideploy sebagai satu unit utama.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan monolith; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Sering cukup untuk produk tahap awal.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Monolith dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Modular Monolith

**Definisi.** Satu deployment dengan batas modul internal jelas.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan modular monolith; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Pilihan sebelum perlu microservices.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Modular Monolith dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Microservices

**Definisi.** Layanan independen yang berkomunikasi lewat kontrak.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan microservices; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Hitung biaya distribusi dan operasional.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Microservices dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Horizontal Scaling

**Definisi.** Menambah jumlah instance untuk menampung beban.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan horizontal scaling; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Hilangkan asumsi state lokal bersama.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Horizontal Scaling dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Vertical Scaling

**Definisi.** Menambah CPU atau memori pada satu instance.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan vertical scaling; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Periksa batas mesin dan biaya.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Vertical Scaling dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Stateless Services

**Definisi.** Instance tidak mengandalkan state session lokal antarrequest.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan stateless services; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Gunakan store bersama bila diperlukan.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Stateless Services dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Stateful Services

**Definisi.** Layanan menyimpan state penting sepanjang proses berjalan.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan stateful services; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Rancang recovery dan failover.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Stateful Services dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Event-Driven Architecture

**Definisi.** Komponen merespons event tanpa pemanggilan langsung ketat.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan event-driven architecture; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Tentukan urutan dan duplikasi event.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Event-Driven Architecture dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Event Sourcing

**Definisi.** State dibangun dari deretan event yang disimpan.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan event sourcing; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Tidak diperlukan untuk setiap CRUD.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Event Sourcing dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### CQRS

**Definisi.** Memisahkan model operasi baca dan tulis saat bermanfaat.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan cqrs; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Perhatikan konsistensi dan kompleksitas.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi CQRS dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### CAP Theorem

**Definisi.** Dalam partisi jaringan, sistem terdistribusi memilih trade-off consistency atau availability.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan cap theorem; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Jangan mengartikannya sebagai tiga tombol bebas.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi CAP Theorem dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Circuit Breaker

**Definisi.** Menghentikan sementara panggilan layanan yang terus gagal.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan circuit breaker; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Gunakan timeout dan fallback sesuai konteks.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Circuit Breaker dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Retry with Backoff

**Definisi.** Mengulangi operasi gagal dengan jeda meningkat.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan retry with backoff; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Hindari retry tanpa batas dan efek ganda.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Retry with Backoff dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Fault Tolerance

**Definisi.** Kemampuan sistem tetap berguna saat sebagian komponen gagal.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan fault tolerance; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Identifikasi titik kegagalan tunggal.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Fault Tolerance dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`

## Referensi kategori

- [Dokumentasi teknis terkait](https://learn.microsoft.com/en-us/azure/architecture/)

> Referensi adalah titik awal belajar, bukan klaim bahwa setiap contoh telah diuji pada proyek tertentu.
