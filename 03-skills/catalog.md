# Katalog skill & integrasi menarik

> Tidak semuanya termasuk skill built-in Codex. Beberapa merupakan plugin, MCP integration, atau workflow custom; cek prasyarat dan kompatibilitas versi.

| Skill / integrasi | Potensi penggunaan | Syarat / catatan |
|---|---|---|
| ImageGen | Art, texture, sprite, image repair | Tool gambar harus tersedia |
| Playwright / browser automation | Menguji UI, mengambil screenshot, mengklik flow | Browser dan dependensi |
| Figma | Membaca design dan implementasi React/Tailwind | Koneksi MCP/plugin dan izin |
| GitHub CI helpers | Membaca error Actions dan memperbaiki workflow | Akses repo dan logs |
| Security threat modeling | Mengidentifikasi attack surface auth/API | Analisis, bukan audit absolut |
| Speech / transcription | Voice-over, transkrip | Model/API, kemungkinan biaya |
| Remotion | Animasi video berbasis React | Render melalui code, bukan otomatis text-to-video |
| Vercel / Cloudflare deployment | Deploy web dari agent | Hak akses platform |
| Skill creator | Membantu menyusun skill sendiri | Tidak menciptakan tool baru |

Untuk pengembangan game: ImageGen + validasi Pillow + Playwright/browser QA. Untuk fullstack: browser testing, CI, threat-model dan deployment.

**Keamanan:** review `SKILL.md` dan semua scripts pihak ketiga sebelum menjalankannya.

Referensi: https://github.com/openai/plugins · https://github.com/openai/skills · https://developers.openai.com/codex/ · https://github.com/remotion-dev/skills
