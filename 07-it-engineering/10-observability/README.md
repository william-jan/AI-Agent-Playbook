# Observability & Reliability

> 8 istilah · Bahasa Indonesia · Terminologi teknis tetap dalam bahasa Inggris.

[← Indeks handbook](../README.md) · [Kamus A–Z](../glossary-a-z.md)

## Isi

- [Structured Logging](#structured-logging) · **prioritas pendalaman**
- [Metrics](#metrics)
- [Distributed Tracing](#distributed-tracing)
- [Monitoring & Alerting](#monitoring-alerting)
- [SLO & SLI](#slo-sli)
- [Error Budgets](#error-budgets)
- [Incident Response](#incident-response)
- [Disaster Recovery](#disaster-recovery)

## Penjelasan praktis

### Structured Logging

**Definisi.** Log berformat konsisten dengan field yang dapat ditelusuri.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan structured logging; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Sertakan request ID tanpa bocorkan secrets.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Structured Logging dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Metrics

**Definisi.** Pengukuran numerik seperti error rate dan latency.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan metrics; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Ukur service-level indicators penting.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Metrics dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Distributed Tracing

**Definisi.** Pelacakan satu request melintasi beberapa komponen.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan distributed tracing; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Sambungkan trace ID lintas layanan.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Distributed Tracing dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Monitoring & Alerting

**Definisi.** Pemantauan kondisi sistem dan notifikasi jika ambang terlampaui.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan monitoring & alerting; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Hindari alarm yang terlalu bising.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Monitoring & Alerting dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### SLO & SLI

**Definisi.** Target reliabilitas dan metrik untuk mengukurnya.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan slo & sli; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Gunakan target berdasarkan pengalaman pengguna.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi SLO & SLI dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Error Budgets

**Definisi.** Batas toleransi kegagalan terhadap target SLO.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan error budgets; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Seimbangkan rilis cepat dengan reliabilitas.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Error Budgets dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Incident Response

**Definisi.** Prosedur mendeteksi, membatasi dan memulihkan gangguan.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan incident response; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Catat peran, komunikasi dan rollback.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Incident Response dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`


### Disaster Recovery

**Definisi.** Strategi memulihkan layanan setelah gangguan berat.

**Kapan dipakai.** Pelajari konsep ini saat keputusan teknis aplikasi berkaitan dengan disaster recovery; tidak semua proyek membutuhkannya pada tahap awal.

**Yang harus diperiksa saat vibe coding.** Definisikan RPO, RTO dan uji pemulihan.

**Pertanyaan untuk AI.** `Tunjukkan lokasi implementasi Disaster Recovery dalam repository ini (atau jelaskan jika belum ada). Apa asumsi, risiko, dan bukti pengujian yang mendukung pilihan tersebut? Jangan mengubah kode dulu.`

## Referensi kategori

- [Dokumentasi teknis terkait](https://opentelemetry.io/docs/)

> Referensi adalah titik awal belajar, bukan klaim bahwa setiap contoh telah diuji pada proyek tertentu.
