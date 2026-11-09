# Networking & Real-Time

> 12 istilah · Bahasa Indonesia · Terminologi teknis tetap dalam bahasa Inggris.

[← Indeks handbook](../README.md) · [Kamus A–Z](../glossary-a-z.md)

## Isi

- [TCP](#tcp)
- [UDP](#udp)
- [WebSocket](#websocket) · **prioritas pendalaman**
- [WebRTC](#webrtc) · **prioritas pendalaman**
- [Latency](#latency)
- [Jitter](#jitter)
- [Packet Loss](#packet-loss)
- [State Synchronization](#state-synchronization) · **prioritas pendalaman**
- [Client-Side Prediction](#clientside-prediction)
- [Interpolation](#interpolation)
- [Authoritative Server](#authoritative-server) · **prioritas pendalaman**
- [NAT Traversal / TURN](#nat-traversal-turn)

## Penjelasan praktis

### TCP

**Definisi.** Protokol koneksi yang menyediakan stream byte andal dan berurutan.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan tcp; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Pahami head-of-line blocking.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi TCP dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### UDP

**Definisi.** Protokol datagram tanpa jaminan delivery atau ordering bawaan.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan udp; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Tambahkan reliabilitas pada lapisan aplikasi bila perlu.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi UDP dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### WebSocket

**Definisi.** Koneksi dua arah berkelanjutan antara browser dan server.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan websocket; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Uji reconnect, heartbeat dan otorisasi.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi WebSocket dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### WebRTC

**Definisi.** Teknologi peer-to-peer untuk media dan data di browser.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan webrtc; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Periksa signaling, NAT dan TURN fallback.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi WebRTC dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Latency

**Definisi.** Waktu yang dibutuhkan informasi untuk mencapai tujuan.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan latency; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Ukur RTT dan waktu end-to-end.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Latency dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Jitter

**Definisi.** Variasi waktu kedatangan packet atau pesan.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan jitter; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Gunakan buffering atau interpolation yang sesuai.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Jitter dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Packet Loss

**Definisi.** Hilangnya packet sepanjang jalur jaringan.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan packet loss; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Tentukan strategi retransmission atau toleransi.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Packet Loss dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### State Synchronization

**Definisi.** Penyamaan state simulasi di beberapa client atau server.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan state synchronization; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Tetapkan sumber kebenaran dan versi update.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi State Synchronization dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Client-Side Prediction

**Definisi.** Client memperkirakan hasil input sebelum konfirmasi server.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan client-side prediction; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Siapkan reconciliation saat prediksi berbeda.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Client-Side Prediction dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Interpolation

**Definisi.** Menghaluskan gerak di antara snapshot yang diterima.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan interpolation; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Atur buffer delay versus kelancaran.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Interpolation dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Authoritative Server

**Definisi.** Server menjadi penentu sah hasil simulasi permainan.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan authoritative server; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Jangan percaya angka damage dari client.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Authoritative Server dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### NAT Traversal / TURN

**Definisi.** Teknik dan relay untuk menghubungkan peer di balik NAT.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan nat traversal / turn; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Perhitungkan koneksi yang perlu relay.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi NAT Traversal / TURN dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`

## Referensi kategori

- [Dokumentasi teknis terkait](https://developer.mozilla.org/en-US/docs/Web/API/WebRTC_API)

> Referensi adalah titik awal belajar, bukan klaim bahwa setiap contoh telah diuji pada proyek tertentu.
