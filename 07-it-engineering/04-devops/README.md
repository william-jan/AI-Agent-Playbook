# DevOps & Deployment

> 14 istilah · Bahasa Indonesia · Terminologi teknis tetap dalam bahasa Inggris.

[← Indeks handbook](../README.md) · [Kamus A–Z](../glossary-a-z.md)

## Isi

- [Git Branching](#git-branching)
- [CI/CD](#cicd) · **prioritas pendalaman**
- [Docker Images](#docker-images)
- [Containers](#containers)
- [Environment Variables](#environment-variables)
- [Reverse Proxy](#reverse-proxy)
- [DNS](#dns)
- [Health Checks](#health-checks) · **prioritas pendalaman**
- [Blue-Green Deployment](#bluegreen-deployment)
- [Canary Release](#canary-release)
- [Rollback](#rollback)
- [Infrastructure as Code](#infrastructure-as-code)
- [Serverless Functions](#serverless-functions)
- [Build Artifacts](#build-artifacts)

## Penjelasan praktis

### Git Branching

**Definisi.** Penggunaan cabang untuk isolasi perubahan kode.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan git branching; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Review diff dan pilih strategi merge.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Git Branching dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### CI/CD

**Definisi.** Otomasi build, test dan pengiriman aplikasi.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan ci/cd; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Pastikan job gagal bila test wajib gagal.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi CI/CD dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Docker Images

**Definisi.** Paket filesystem dan metadata untuk menjalankan container.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan docker images; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Gunakan image minimal dan pin versi.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Docker Images dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Containers

**Definisi.** Isolasi proses dengan lingkungan runtime yang terkemas.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan containers; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Jangan menyamakan container dengan VM.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Containers dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Environment Variables

**Definisi.** Konfigurasi yang diberikan di luar kode sumber.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan environment variables; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Pisahkan konfigurasi publik dan secrets.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Environment Variables dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Reverse Proxy

**Definisi.** Server perantara yang meneruskan request ke backend.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan reverse proxy; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Periksa forwarding headers dan TLS.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Reverse Proxy dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### DNS

**Definisi.** Sistem yang memetakan domain ke record jaringan.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan dns; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Cek TTL dan record saat memindah hosting.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi DNS dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Health Checks

**Definisi.** Endpoint atau probe untuk mengetahui kesiapan dan kesehatan instance.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan health checks; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Bedakan liveness dengan readiness.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Health Checks dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Blue-Green Deployment

**Definisi.** Peralihan traffic antara dua lingkungan deployment.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan blue-green deployment; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Siapkan kompatibilitas skema saat transisi.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Blue-Green Deployment dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Canary Release

**Definisi.** Melepas versi baru kepada sebagian kecil traffic dahulu.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan canary release; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Tentukan metrik dan langkah rollback.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Canary Release dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Rollback

**Definisi.** Mengembalikan versi atau perubahan ke keadaan sebelumnya.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan rollback; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Rancang kompatibilitas data pada rollback.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Rollback dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Infrastructure as Code

**Definisi.** Pengelolaan infrastruktur lewat konfigurasi terversi.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan infrastructure as code; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Review perubahan dan lindungi state/secrets.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Infrastructure as Code dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Serverless Functions

**Definisi.** Eksekusi fungsi sesuai request di infrastruktur terkelola.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan serverless functions; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Cek cold start, timeout dan koneksi database.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Serverless Functions dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Build Artifacts

**Definisi.** Output hasil build yang dideploy atau didistribusikan.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan build artifacts; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Pastikan lingkungan deploy memakai hasil build teruji.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Build Artifacts dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`

## Referensi kategori

- [Dokumentasi teknis terkait](https://docs.docker.com/)

> Referensi adalah titik awal belajar, bukan klaim bahwa setiap contoh telah diuji pada proyek tertentu.
