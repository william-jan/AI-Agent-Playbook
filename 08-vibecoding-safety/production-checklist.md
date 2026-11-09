# Production Readiness Checklist

Gunakan sebelum deployment penting; tandai **N/A** dengan alasan jika tidak relevan.

## Identity & Security

- [ ] Route privat membuktikan identitas di server.
- [ ] Setiap aksi resource memverifikasi otorisasi pemilik/role.
- [ ] Input eksternal divalidasi saat runtime; output dikodekan sesuai konteks.
- [ ] Proteksi CSRF ditinjau bila browser mengirim kredensial otomatis.
- [ ] Cookies, CORS, TLS dan CSP ditinjau sesuai arsitektur.
- [ ] Password di-hash dengan algoritma adaptif; secret tidak berada di repository atau client bundle.
- [ ] Rate limiting dipasang pada operasi rawan penyalahgunaan, termasuk OTP dan login.
- [ ] Dependencies dan izin pihak ketiga diaudit.

## Data & Concurrency

- [ ] Index sesuai pola query; query kritis diprofilkan.
- [ ] Operasi stok, saldo, pembayaran, atau game state menjaga invariant ketika concurrent.
- [ ] Webhook/pekerjaan retry tidak menggandakan efek penting.
- [ ] Migrasi schema dan rencana rollback disiapkan.
- [ ] Backup tersedia dan proses restore sudah diuji.

## Quality & Operations

- [ ] Lint, typecheck, unit dan integration tests relevan lulus.
- [ ] E2E alur kritis dan unauthorized access telah diuji.
- [ ] Error response tidak membocorkan data internal.
- [ ] Monitoring error rate dan latency tersedia sesuai kebutuhan.
- [ ] Logging mencantumkan correlation ID tanpa rahasia pengguna.
- [ ] Timeout, retry, dan kegagalan dependency ditangani.
- [ ] Prosedur rollback deployment dan penanggung jawab tersedia.
- [ ] Performa diperiksa dengan workload realistis.

**Catatan audit:** fitur/commit: ___; tanggal: ___; reviewer: ___; bukti tes: ___; risiko belum selesai: ___.

[← Vibe Coding Safety](README.md)
