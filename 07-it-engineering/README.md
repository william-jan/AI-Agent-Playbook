# IT Engineering Handbook for AI-Assisted Development

**140 istilah IT dalam 10 kategori**, untuk membangun *engineering judgment* ketika memakai Codex, Claude Code, atau alat AI coding lain.

> AI menulis kode; developer memahami sistem dan memverifikasi hasil. Kamus, prompt, dan checklist **tidak menjamin keamanan**.

## Pilih cara belajar

- [Kamus A–Z](glossary-a-z.md) — mencari istilah dengan cepat.
- [Learning Roadmap](learning-roadmap.md) — urutan belajar sesuai jenis proyek.
- [Practical Deep Dives](deep-dives.md) — contoh TypeScript, SQL, MongoDB, dan game real-time yang memperlihatkan kegagalan serta mitigasi.
- [Vibe Coding Safety](../08-vibecoding-safety/README.md) — checklist dan prompt audit.
- [Pedoman Kontribusi](contributing.md) — cara memperluas dan memverifikasi dokumentasi.

## Semua kategori

| Kategori | Istilah | Dokumentasi |
|---|---:|---|
| Backend & API | 18 | [Baca](01-backend/README.md) |
| Security | 18 | [Baca](02-security/README.md) |
| Database & Data Integrity | 16 | [Baca](03-database/README.md) |
| DevOps & Deployment | 14 | [Baca](04-devops/README.md) |
| Performance & Optimization | 14 | [Baca](05-performance/README.md) |
| Software Engineering Principles | 16 | [Baca](06-engineering-principles/README.md) |
| System Architecture | 14 | [Baca](07-architecture/README.md) |
| Networking & Real-Time | 12 | [Baca](08-networking-realtime/README.md) |
| Testing & Quality Assurance | 10 | [Baca](09-testing/README.md) |
| Observability & Reliability | 8 | [Baca](10-observability/README.md) |
| **Total** | **140** | |

## Cara membaca entri

Setiap istilah memuat **definisi**, **kapan relevan**, **pemeriksaan saat vibe coding**, dan **pertanyaan audit untuk AI**. Sebagian istilah penting ditandai prioritas pendalaman; lihat [deep dives](deep-dives.md). Tingkat prioritas tidak sama dengan tingkat kesulitan.

## Prinsip

1. Jangan menerapkan seluruh teknologi sekaligus; mulai dari kebutuhan dan ancaman yang nyata.
2. Server harus memverifikasi otorisasi dan input; TypeScript hanya memeriksa tipe saat development, bukan validasi runtime.
3. Audit AI menghasilkan hipotesis, bukan bukti; selalu uji perilaku dan edge case.
4. Pengamanan dan pengujian harus mengikuti arsitektur nyata proyek.
5. Bahasa penjelasan Indonesia; istilah teknis dan identifier kode Inggris.
