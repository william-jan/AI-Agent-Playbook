# AI Code Review Workflow

## Sebelum AI mengedit

Tulis kebutuhan, file yang diizinkan berubah, constraint, serta acceptance criteria. Minta ringkasan rencana dan risiko.

## Setelah AI mengedit

1. Periksa diff, dependency, file konfigurasi dan secret yang mungkin ikut berubah.
2. Tinjau asumsi input, role, state dan error handling.
3. Cocokkan implementasi dengan acceptance criteria dan contract.
4. Jalankan typecheck/lint/tests; jangan percaya output yang tidak diperlihatkan.
5. Buat negative tests untuk unauthorized, malformed input dan concurrency.
6. Perbaiki hanya temuan terverifikasi dan jalankan regression tests.
7. Dokumentasikan apa yang belum diuji dan alasan.

## Format laporan wajib

| Item | Isi |
|---|---|
| Temuan | Perilaku yang bermasalah |
| Bukti | Path/line, reproduksi/test |
| Dampak | Skenario pengguna yang terpengaruh |
| Keyakinan | Terbukti / perlu verifikasi |
| Solusi | Perubahan minimum dan trade-off |
| Hasil | Perintah test dan output ringkas |

**Aturan:** hasil reviewer AI adalah masukan, bukan pengganti ownership developer.
