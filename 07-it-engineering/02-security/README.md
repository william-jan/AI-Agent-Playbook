# Security

> 18 istilah · Bahasa Indonesia · Terminologi teknis tetap dalam bahasa Inggris.

[← Indeks handbook](../README.md) · [Kamus A–Z](../glossary-a-z.md)

## Isi

- [Threat Modeling](#threat-modeling)
- [OWASP Top 10](#owasp-top-10)
- [Authentication Sessions](#authentication-sessions)
- [Authorization / IDOR](#authorization-idor)
- [JWT](#jwt) · **prioritas pendalaman**
- [Password Hashing](#password-hashing)
- [SQL Injection](#sql-injection) · **prioritas pendalaman**
- [NoSQL Injection](#nosql-injection) · **prioritas pendalaman**
- [Cross-Site Scripting (XSS)](#crosssite-scripting-xss) · **prioritas pendalaman**
- [Cross-Site Request Forgery (CSRF)](#crosssite-request-forgery-csrf) · **prioritas pendalaman**
- [CORS](#cors)
- [Content Security Policy](#content-security-policy)
- [Secret Management](#secret-management)
- [Least Privilege](#least-privilege)
- [HTTPS / TLS](#https-tls)
- [Secure Cookies](#secure-cookies)
- [Dependency Vulnerabilities](#dependency-vulnerabilities)
- [Replay Attacks](#replay-attacks)

## Penjelasan praktis

### Threat Modeling

**Definisi.** Identifikasi aset, pelaku ancaman, jalur serangan dan mitigasi.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan threat modeling; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Tentukan trust boundary sebelum coding.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Threat Modeling dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### OWASP Top 10

**Definisi.** Referensi kategori risiko keamanan web yang umum.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan owasp top 10; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Gunakan sebagai awal audit bukan jaminan lengkap.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi OWASP Top 10 dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Authentication Sessions

**Definisi.** Pengelolaan identitas login melalui session yang berlaku sementara.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan authentication sessions; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Periksa expiry, logout dan rotasi.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Authentication Sessions dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Authorization / IDOR

**Definisi.** Pemeriksaan hak akses ke object tertentu, bukan hanya login.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan authorization / idor; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Coba akses resource milik user lain.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Authorization / IDOR dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### JWT

**Definisi.** Format token bertanda tangan berisi klaim yang harus diverifikasi.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan jwt; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Periksa signature, issuer, audience dan expiry.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi JWT dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Password Hashing

**Definisi.** Penyimpanan password memakai algoritma hash adaptif dengan salt.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan password hashing; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Gunakan Argon2id atau bcrypt yang dikonfigurasi benar.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Password Hashing dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### SQL Injection

**Definisi.** Input disisipkan sebagai perintah SQL ketika query tidak aman.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan sql injection; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Gunakan parameterized query.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi SQL Injection dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### NoSQL Injection

**Definisi.** Manipulasi operator atau struktur query pada database NoSQL.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan nosql injection; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Validasi bentuk input dan larang operator tak terduga.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi NoSQL Injection dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Cross-Site Scripting (XSS)

**Definisi.** Eksekusi script penyerang di konteks halaman korban.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan cross-site scripting (xss); tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Hindari render HTML mentah tanpa sanitasi sesuai konteks.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Cross-Site Scripting (XSS) dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Cross-Site Request Forgery (CSRF)

**Definisi.** Browser korban dibujuk mengirim request berotoritas tanpa niatnya.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan cross-site request forgery (csrf); tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Periksa SameSite dan token CSRF sesuai arsitektur sesi.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Cross-Site Request Forgery (CSRF) dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### CORS

**Definisi.** Kebijakan browser terhadap akses respons cross-origin.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan cors; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Jangan mengira CORS menggantikan authentication.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi CORS dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Content Security Policy

**Definisi.** Header yang membatasi sumber script dan konten yang boleh dijalankan.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan content security policy; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Audit inline scripts dan sumber eksternal.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Content Security Policy dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Secret Management

**Definisi.** Pengelolaan API key dan kredensial agar tidak bocor.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan secret management; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Jangan simpan secrets di client bundle atau Git.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Secret Management dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Least Privilege

**Definisi.** Setiap identitas memperoleh izin minimum yang diperlukan.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan least privilege; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Tinjau role, database user dan token scope.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Least Privilege dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### HTTPS / TLS

**Definisi.** Enkripsi transport dan autentikasi koneksi melalui sertifikat.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan https / tls; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Wajib untuk kredensial dan traffic sensitif.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi HTTPS / TLS dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Secure Cookies

**Definisi.** Atribut HttpOnly, Secure dan SameSite membatasi risiko tertentu.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan secure cookies; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Setel sesuai kebutuhan session dan HTTPS.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Secure Cookies dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Dependency Vulnerabilities

**Definisi.** Celah pada library maupun dependensi transitive.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan dependency vulnerabilities; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Audit versi, lockfile dan patch berisiko.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Dependency Vulnerabilities dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Replay Attacks

**Definisi.** Permintaan valid ditangkap lalu dikirim ulang untuk efek tambahan.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan replay attacks; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Gunakan nonce, timestamp dan deduplikasi bila perlu.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Replay Attacks dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`

## Referensi kategori

- [Dokumentasi teknis terkait](https://owasp.org/www-project-top-ten/)

> Referensi adalah titik awal belajar, bukan klaim bahwa setiap contoh telah diuji pada proyek tertentu.
