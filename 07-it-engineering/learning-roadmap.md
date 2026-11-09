# Learning Roadmap

[← Handbook](README.md)

Baca konsep sesuai kebutuhan proyek, bukan urutan alfabetis. Untuk setiap langkah: **jelaskan konsep → telusuri kode → rumuskan invariant → jalankan test → catat hasil**.

## A. Full-stack Web (Next.js, Node.js, MongoDB)

1. HTTP Request Lifecycle → HTTP Methods → HTTP Status Codes → REST API → API Contract.
2. Input Validation → Authentication → Authorization / IDOR → Secure Cookies → CSRF dan XSS.
3. Database Schema → Database Index → Query Execution Plan → ACID Transactions → Atomic Operations → Race Conditions.
4. Unit Testing → Integration Testing → End-to-End Testing → CI/CD → Monitoring & Alerting.
5. Rate Limiting → Caching → Schema Migration → Backups & Restore.

**Latihan:** buat endpoint untuk mengubah resource milik user. Uji input tidak valid, akses user lain, dua request bersamaan, dan response ketika database gagal.

## B. Browser Multiplayer (Arcana Clash / Kagefall)

1. TCP → UDP → WebSocket → WebRTC → NAT Traversal / TURN.
2. Latency → Jitter → Packet Loss → State Synchronization → Authoritative Server.
3. Client-Side Prediction → Interpolation → Race Conditions → Atomic Operations.
4. Structured Logging → Metrics → Load Testing → Incident Response.

**Latihan:** simulasikan 2 client mengirim aksi pada tick yang sama. Definisikan sumber kebenaran, cara mengurutkan input, dan cara mereproduksi desync. Host-as-authority tidak sama dengan anti-cheat.

## C. AI-Assisted Software Engineer

1. Git Branching → Code Review → Separation of Concerns → Type Safety → Error Handling.
2. KISS → YAGNI → DRY → Technical Debt → Refactoring.
3. Threat Modeling → OWASP Top 10 → Static Analysis → Regression Testing.
4. Structured Logging → Performance Profiling → Health Checks → Rollback.

**Latihan:** minta AI menjelaskan 3 keputusan teknis dan alternatifnya; periksa diff, jalankan test yang relevan, dan tolak klaim yang belum dibuktikan.

## Kapan berhenti belajar lalu membangun?

Ketika mampu menjelaskan risiko utama suatu fitur, menulis acceptance criteria, dan membuktikan hasil implementasi dengan test yang tepat. Pembelajaran berlanjut selama implementasi.
