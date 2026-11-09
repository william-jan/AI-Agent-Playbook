# Vibe Coding Safety

Panduan operasional untuk memeriksa aplikasi yang dibuat dengan AI coding tools.

**Tujuan:** meningkatkan kualitas review dan keandalan implementasi. Bukan sertifikasi dan bukan jaminan keamanan.

- [Production Readiness Checklist](production-checklist.md)
- [Security Audit](security-audit.md)
- [Database & Concurrency Audit](database-audit.md)
- [Performance Audit](performance-audit.md)
- [AI Code Review Workflow](ai-code-review.md)
- [Prompt Library](prompt-library.md)
- [Kamus 140 Istilah](../07-it-engineering/README.md)

## Siklus kerja yang dianjurkan

1. Tulis tujuan fitur, acceptance criteria dan batas trust.
2. Minta AI menjelaskan rencana dan trade-off sebelum implementasi.
3. Review diff dan dependencies; pahami data flow dan authorization.
4. Jalankan lint, typecheck, automated tests, serta manual adversarial tests.
5. Verifikasi deployment dan monitoring dengan data nyata yang aman.
6. Catat risiko tersisa dan tindakan lanjut.

> Minta bukti berupa path file, test case, command yang dijalankan, dan output ringkas. Klaim “sudah aman” tanpa pembuktian harus dianggap belum diverifikasi.
