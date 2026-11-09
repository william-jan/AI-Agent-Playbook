# Performance & Optimization

> 14 istilah · Bahasa Indonesia · Terminologi teknis tetap dalam bahasa Inggris.

[← Indeks handbook](../README.md) · [Kamus A–Z](../glossary-a-z.md)

## Isi

- [Caching](#caching) · **prioritas pendalaman**
- [Cache Invalidation](#cache-invalidation)
- [CDN](#cdn)
- [Lazy Loading](#lazy-loading)
- [Code Splitting](#code-splitting)
- [Debouncing](#debouncing)
- [Throttling](#throttling)
- [Memory Leaks](#memory-leaks) · **prioritas pendalaman**
- [Profiling](#profiling)
- [Core Web Vitals](#core-web-vitals)
- [Time Complexity](#time-complexity)
- [Database Query Optimization](#database-query-optimization)
- [Concurrency vs Parallelism](#concurrency-vs-parallelism)
- [Backpressure](#backpressure)

## Penjelasan praktis

### Caching

**Definisi.** Menyimpan hasil komputasi agar penggunaan ulang lebih cepat.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan caching; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Tetapkan TTL dan invalidasi.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Caching dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Cache Invalidation

**Definisi.** Menghapus atau memperbarui cache saat data sumber berubah.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan cache invalidation; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Tes perubahan data setelah update.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Cache Invalidation dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### CDN

**Definisi.** Jaringan server edge untuk mempercepat distribusi konten.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan cdn; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Periksa aturan cache konten privat.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi CDN dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Lazy Loading

**Definisi.** Memuat modul atau resource hanya saat dibutuhkan.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan lazy loading; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Ukur dampak pada UX dan waktu interaksi.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Lazy Loading dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Code Splitting

**Definisi.** Memecah bundle menjadi bagian yang dimuat terpisah.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan code splitting; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Periksa ukuran bundle dan waterfall request.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Code Splitting dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Debouncing

**Definisi.** Menunda eksekusi sampai aktivitas berhenti sejenak.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan debouncing; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Cocok untuk pencarian saat mengetik.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Debouncing dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Throttling

**Definisi.** Membatasi frekuensi eksekusi secara berkala.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan throttling; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Cocok untuk scroll atau input berulang.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Throttling dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Memory Leaks

**Definisi.** Memori tetap tertahan walau tidak lagi dibutuhkan.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan memory leaks; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Periksa listener, timer dan cache yang tumbuh.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Memory Leaks dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Profiling

**Definisi.** Pengukuran bagian program yang mengonsumsi waktu atau resource.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan profiling; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Optimalkan berdasarkan bukti profiler.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Profiling dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Core Web Vitals

**Definisi.** Metrik pengalaman web termasuk LCP, INP dan CLS.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan core web vitals; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Uji perangkat nyata dan data pengguna bila ada.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Core Web Vitals dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Time Complexity

**Definisi.** Hubungan pertumbuhan input dengan jumlah pekerjaan algoritma.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan time complexity; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Cari loop kuadratik pada data besar.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Time Complexity dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Database Query Optimization

**Definisi.** Perubahan query dan index untuk mengurangi beban akses data.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan database query optimization; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Bandingkan execution plan dan latensi.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Database Query Optimization dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Concurrency vs Parallelism

**Definisi.** Concurrency mengelola beberapa pekerjaan; parallelism mengeksekusi bersama.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan concurrency vs parallelism; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Pahami bottleneck I/O atau CPU.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Concurrency vs Parallelism dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Backpressure

**Definisi.** Mekanisme memperlambat produsen agar konsumen tidak kewalahan.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan backpressure; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Batasi antrean, buffer dan pemakaian memori.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Backpressure dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`

## Referensi kategori

- [Dokumentasi teknis terkait](https://web.dev/learn/performance)

> Referensi adalah titik awal belajar, bukan klaim bahwa setiap contoh telah diuji pada proyek tertentu.
