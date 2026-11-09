# Performance Audit

1. Ukur baseline latency p50/p95, ukuran bundle, konsumsi memori dan database query.
2. Profiling sebelum optimasi; catat top bottleneck.
3. Review N+1 query, index, caching dan invalidasi, lazy loading dan client bundles.
4. Tinjau biaya operasi background, queue/backpressure dan concurrency.
5. Load test di lingkungan yang mengizinkan; jangan menguji endpoint pihak lain tanpa izin.
6. Bandingkan setelah perubahan menggunakan skenario dan hardware yang setara.

**Prompt:** `Audit performa project secara read-only. Jangan menebak bottleneck. Usulkan metrik dan prosedur profiling dulu, identifikasi kandidat penyebab dengan file/line, kemudian rangking solusi berdasarkan impact, kompleksitas dan risiko.`

Sumber: [web.dev Performance](https://web.dev/learn/performance).
