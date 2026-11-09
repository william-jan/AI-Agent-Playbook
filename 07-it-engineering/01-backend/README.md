# Backend & API

> 18 istilah · Bahasa Indonesia · Terminologi teknis tetap dalam bahasa Inggris.

[← Indeks handbook](../README.md) · [Kamus A–Z](../glossary-a-z.md)

## Isi

- [HTTP Request Lifecycle](#http-request-lifecycle)
- [REST API](#rest-api)
- [HTTP Methods](#http-methods)
- [HTTP Status Codes](#http-status-codes)
- [API Contract](#api-contract)
- [Input Validation](#input-validation)
- [Middleware](#middleware)
- [Authentication](#authentication) · **prioritas pendalaman**
- [Authorization](#authorization) · **prioritas pendalaman**
- [Pagination](#pagination)
- [Rate Limiting](#rate-limiting) · **prioritas pendalaman**
- [Idempotency](#idempotency)
- [Caching API](#caching-api)
- [Webhooks](#webhooks)
- [Background Jobs](#background-jobs)
- [Message Queues](#message-queues)
- [API Gateway](#api-gateway)
- [Load Balancing](#load-balancing)

## Penjelasan praktis

### HTTP Request Lifecycle

**Definisi.** Urutan proses request dari browser, jaringan, server hingga response.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan http request lifecycle; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Telusuri middleware, handler, status dan error response.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi HTTP Request Lifecycle dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### REST API

**Definisi.** Gaya desain endpoint berbasis resource dan operasi HTTP.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan rest api; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Periksa method, status code dan kontrak respons.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi REST API dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### HTTP Methods

**Definisi.** GET, POST, PUT, PATCH dan DELETE menunjukkan maksud operasi.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan http methods; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** GET tidak boleh mengubah state penting.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi HTTP Methods dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### HTTP Status Codes

**Definisi.** Kode 2xx, 3xx, 4xx dan 5xx mengkomunikasikan hasil request.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan http status codes; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Bedakan invalid input, unauthorized dan kegagalan server.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi HTTP Status Codes dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### API Contract

**Definisi.** Kesepakatan struktur request, response, status dan error.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan api contract; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Validasi schema serta kompatibilitas client.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi API Contract dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Input Validation

**Definisi.** Pemeriksaan bentuk dan batas data dari sumber tak tepercaya.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan input validation; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Validasi di server meskipun form sudah divalidasi.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Input Validation dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Middleware

**Definisi.** Lapisan fungsi sebelum atau sesudah route handler.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan middleware; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Cek urutan auth, logging dan penanganan error.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Middleware dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Authentication

**Definisi.** Proses membuktikan identitas pengguna atau layanan.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan authentication; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Periksa session dan verifikasi token pada server.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Authentication dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Authorization

**Definisi.** Proses menentukan izin identitas terhadap resource atau operasi.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan authorization; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Uji akses antar akun dan role.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Authorization dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Pagination

**Definisi.** Membagi daftar hasil menjadi halaman atau cursor.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan pagination; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Cek batas maksimum page size dan urutan stabil.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Pagination dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Rate Limiting

**Definisi.** Pembatasan jumlah aksi atau request per periode dan identitas.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan rate limiting; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Tinjau endpoint login, OTP dan API mahal.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Rate Limiting dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Idempotency

**Definisi.** Pengulangan operasi menghasilkan efek akhir yang setara dengan sekali eksekusi.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan idempotency; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Gunakan idempotency key pada aksi pembayaran yang sesuai.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Idempotency dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Caching API

**Definisi.** Penyimpanan sementara hasil API agar tidak selalu dihitung ulang.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan caching api; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Periksa invalidasi dan kebocoran data privat.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Caching API dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Webhooks

**Definisi.** Notifikasi HTTP dari layanan lain saat event terjadi.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan webhooks; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Verifikasi signature, retry dan duplikasi.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Webhooks dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Background Jobs

**Definisi.** Pekerjaan diproses di luar alur request utama.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan background jobs; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Pastikan retry aman dan status dapat dilacak.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Background Jobs dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Message Queues

**Definisi.** Antrean pesan yang memisahkan produsen dan pemroses tugas.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan message queues; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Periksa duplicate delivery dan kegagalan consumer.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Message Queues dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### API Gateway

**Definisi.** Titik masuk terpusat untuk routing dan kebijakan API.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan api gateway; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Jangan menambahkan gateway jika satu app sudah cukup.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi API Gateway dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Load Balancing

**Definisi.** Distribusi traffic ke beberapa instance server.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan load balancing; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Periksa sesi dan state pada beberapa instance.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Load Balancing dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`

## Referensi kategori

- [Dokumentasi teknis terkait](https://developer.mozilla.org/en-US/docs/Web/HTTP)

> Referensi adalah titik awal belajar, bukan klaim bahwa setiap contoh telah diuji pada proyek tertentu.
