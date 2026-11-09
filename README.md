# AI Agent Playbook

Knowledge base berbahasa Indonesia tentang **AI agents, Codex, Agent Skills, tools, MCP, dan workflow pengembangan software**. Dikembangkan agar konsep dan eksperimen dapat dicari, diuji, dan digunakan kembali.

> **Prinsip penting:** Skill berisi instruksi/resources; skill sendiri tidak otomatis menyediakan kemampuan tool baru. Verifikasi fitur yang tersedia pada versi dan sesi Codex-mu.

## Daftar isi

| Kategori | Dokumentasi |
|---|---|
| Fundamentals | [Agent, Skills, Tools & MCP](01-fundamentals/agent-skills-tools.md) |
| Codex VS Code | [Setup & AGENTS.md](02-codex/vscode-and-agents.md) |
| Skills | [ImageGen untuk artwork game](03-skills/imagegen.md) |
| Skills | [Katalog skill dan integrasi menarik](03-skills/catalog.md) |
| Workflows | [Game asset pipeline](04-workflows/game-asset-pipeline.md) |
| Prompts | [Resep prompt siap salin](05-prompts/recipes.md) |
| Troubleshooting | [Masalah umum dan solusinya](06-troubleshooting/common-issues.md) |
| IT Engineering | [Handbook 140 istilah + kamus A–Z](07-it-engineering/README.md) |
| Vibe Coding Safety | [Checklist production & prompt audit](08-vibecoding-safety/README.md) |
| Custom Skills | [Merancang skill sendiri](custom-skills/README.md) |

## Cara memakai repository ini

1. Pelajari konsep di **Fundamentals**.
2. Periksa kemampuan Codex di **Setup**.
3. Pilih workflow lalu adaptasi prompt.
4. Pelajari [IT Engineering Handbook](07-it-engineering/README.md) sesuai kebutuhan proyek; cari istilah di [kamus A–Z](07-it-engineering/glossary-a-z.md).
5. Gunakan [Vibe Coding Safety](08-vibecoding-safety/README.md) untuk mereview, menguji dan mendokumentasikan risiko sebelum deployment.
6. Catat hasil pengujian sendiri; jangan menyamakan contoh dengan fitur yang sudah terbukti di lingkungan lokal.

**Label informasi:** *Verified (documentation)* = didukung dokumentasi; *Needs testing* = perlu diuji di environment; *Example* = rancangan workflow.

> **AI coding bukan jaminan keamanan.** Checklist dan audit AI hanya membantu menemukan risiko; validasi, pengujian, dan review tetap diperlukan.

## Referensi

- [Codex documentation](https://developers.openai.com/codex/)
- [OpenAI Plugins](https://github.com/openai/plugins)
- [OpenAI Skills](https://github.com/openai/skills)
- [ImageGen skill sample](https://github.com/openai/codex/blob/main/codex-rs/skills/src/assets/samples/imagegen/SKILL.md)
- [Agent Skills specification](https://agentskills.io/)
- [MDN Web Docs](https://developer.mozilla.org/)
- [OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/)

Terakhir disusun: **2026-11-09**. Dokumentasi ini berkembang dan perlu ditinjau ulang saat fitur agent berubah.
