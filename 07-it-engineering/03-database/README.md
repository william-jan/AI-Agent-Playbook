# Database & Data Integrity

> 16 istilah · Bahasa Indonesia · Terminologi teknis tetap dalam bahasa Inggris.

[← Indeks handbook](../README.md) · [Kamus A–Z](../glossary-a-z.md)

## Isi

- [Database Index](#database-index) · **prioritas pendalaman**
- [Query Execution Plan](#query-execution-plan)
- [N+1 Queries](#n1-queries)
- [ACID Transactions](#acid-transactions) · **prioritas pendalaman**
- [Atomic Operations](#atomic-operations) · **prioritas pendalaman**
- [Race Conditions](#race-conditions) · **prioritas pendalaman**
- [Optimistic Concurrency](#optimistic-concurrency)
- [Pessimistic Locking](#pessimistic-locking)
- [Database Schema](#database-schema)
- [Schema Migration](#schema-migration) · **prioritas pendalaman**
- [Data Normalization](#data-normalization)
- [Denormalization](#denormalization)
- [Referential Integrity](#referential-integrity)
- [Database Connection Pool](#database-connection-pool)
- [Backups & Restore](#backups-restore)
- [Eventual Consistency](#eventual-consistency)

## Penjelasan praktis

### Database Index

**Definisi.** Struktur akses yang mempercepat pencarian tertentu dengan biaya write dan storage.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan database index; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Uji query plan sebelum menambah index.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Database Index dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Query Execution Plan

**Definisi.** Rencana eksekusi yang dipilih database untuk sebuah query.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan query execution plan; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Periksa scan, filter dan jumlah dokumen diproses.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Query Execution Plan dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### N+1 Queries

**Definisi.** Satu query awal memicu banyak query lanjutan per item.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan n+1 queries; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Gunakan batching atau eager loading yang sesuai.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi N+1 Queries dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### ACID Transactions

**Definisi.** Sifat atomicity, consistency, isolation dan durability pada transaksi.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan acid transactions; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Pastikan beberapa perubahan penting atomik.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi ACID Transactions dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Atomic Operations

**Definisi.** Perubahan yang berlaku sebagai satu tindakan indivisible menurut database.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan atomic operations; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Gunakan conditional update untuk stok atau saldo.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Atomic Operations dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Race Conditions

**Definisi.** Hasil operasi bergantung pada timing konkurensi.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan race conditions; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Simulasikan request bersamaan dan cek invariant.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Race Conditions dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Optimistic Concurrency

**Definisi.** Strategi menolak update jika versi data sudah berubah.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan optimistic concurrency; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Gunakan version field dan retry terkontrol.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Optimistic Concurrency dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Pessimistic Locking

**Definisi.** Strategi mengunci data sebelum perubahan untuk mencegah konflik.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan pessimistic locking; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Periksa contention dan deadlock.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Pessimistic Locking dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Database Schema

**Definisi.** Aturan struktur, tipe dan relasi data.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan database schema; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Validasi skema dan rencanakan evolusinya.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Database Schema dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Schema Migration

**Definisi.** Perubahan terkontrol pada struktur data antarversi.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan schema migration; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Siapkan migrasi, rollback dan backup.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Schema Migration dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Data Normalization

**Definisi.** Memisahkan fakta agar redundansi dan anomali berkurang.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan data normalization; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Pertimbangkan kebutuhan query dan konsistensi.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Data Normalization dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Denormalization

**Definisi.** Menduplikasi sebagian data demi pembacaan yang lebih murah.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan denormalization; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Tetapkan cara sinkronisasi salinan.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Denormalization dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Referential Integrity

**Definisi.** Konsistensi hubungan antarentitas atau dokumen.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan referential integrity; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Pastikan foreign key atau invariant aplikasi terjaga.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Referential Integrity dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Database Connection Pool

**Definisi.** Kumpulan koneksi yang digunakan ulang oleh aplikasi.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan database connection pool; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Periksa limit pada serverless atau banyak instance.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Database Connection Pool dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Backups & Restore

**Definisi.** Salinan data dan prosedur memulihkan layanan.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan backups & restore; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Uji restore, bukan hanya membuat backup.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Backups & Restore dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Eventual Consistency

**Definisi.** Keadaan salinan data dapat sementara berbeda lalu berkonvergensi.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan eventual consistency; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Jangan mengandalkan pembacaan yang langsung terbaru.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Eventual Consistency dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`

## Referensi kategori

- [Dokumentasi teknis terkait](https://www.mongodb.com/docs/manual/)

> Referensi adalah titik awal belajar, bukan klaim bahwa setiap contoh telah diuji pada proyek tertentu.
