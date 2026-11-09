# Database & Concurrency Audit

1. Inventarisasi operasi read/write pada order, saldo, inventori, booking dan game state.
2. Tulis invariant setiap operasi (contoh: `stock >= 0`, satu pembayaran diproses sekali).
3. Cari pola `read → check → write` yang tidak atomic.
4. Tinjau transaction, unique constraint, conditional update, idempotency keys dan webhook retries.
5. Periksa indexing, N+1, limit query, migrasi dan backups.
6. Jalankan concurrent requests terkontrol dan pastikan hasil benar setelah retry.

**Prompt:** `Telusuri mutasi database kritis. Identifikasi race condition, ketidakatomikan dan risiko duplicate processing. Sertakan invariant, file/line, test concurrency yang bisa dijalankan aman, serta trade-off perbaikan.`

Sumber: [MongoDB Atomicity](https://www.mongodb.com/docs/manual/core/write-operations-atomicity/).
