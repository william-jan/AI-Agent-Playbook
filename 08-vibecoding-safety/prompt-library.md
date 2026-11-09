# Prompt Library untuk Codex / Claude Code

Semua prompt menuntut **read-only audit terlebih dahulu**; edit kode hanya setelah ruang lingkup disetujui.

## 1. General Engineering Audit

```text
Audit repository ini secara read-only. Petakan arsitektur, alur request, state, dependency, dan trust boundary. Prioritaskan masalah yang dapat dibuktikan, sertakan file/line, tingkat risiko, cara reproduce, dan usulan test. Bedakan temuan terverifikasi dari hipotesis. Jangan mengubah file.
```

## 2. Authentication & Authorization

```text
Audit semua API route dan server actions yang memakai identitas pengguna. Periksa login, session, role, dan ownership per resource, termasuk IDOR. Tulis matriks endpoint x role, tunjukkan kontrol server-side, lalu usulkan negative integration tests. Jangan mengubah file.
```

## 3. Database Consistency

```text
Cari read-check-write, perubahan multi-dokumen, webhook retries, dan operasi yang harus idempotent. Tulis invariant, kemungkinan interleaving request, solusi atomic/transaction yang relevan, serta uji concurrent. Jangan mengubah file.
```

## 4. Multiplayer Authority

```text
Petakan alur input multiplayer dari client ke sumber kebenaran. Identifikasi siapa memvalidasi cooldown, mana/stamina, collision, damage dan state update. Jelaskan host-cheat risk dan desync; usulkan pengujian input duplikat, terlambat, dan tidak valid. Jangan mengubah file.
```

## 5. Performance

```text
Identifikasi kandidat masalah performa, tetapi jangan mengklaim bottleneck tanpa metrik. Berikan langkah profiling, lokasi kode terkait, usulan benchmark sebelum/sesudah, serta risiko setiap optimasi. Jangan mengubah file.
```

## 6. Pre-deploy Gate

```text
Susun checklist pre-deploy sesuai arsitektur project ini. Periksa lint/typecheck/tests bila tools tersedia, ringkas hasil sebenarnya, dan laporkan hal yang tidak dapat dijalankan. Evaluasi secrets, database migration, backups, rollback, observability, dan route kritis. Jangan menyatakan production-ready tanpa bukti.
```
