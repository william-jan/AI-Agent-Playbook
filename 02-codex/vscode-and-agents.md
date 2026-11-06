# Codex di VS Code dan AGENTS.md

Codex bisa memilih skill berdasarkan deskripsi pekerjaan tanpa harus menyebut namanya. **Syarat: skill terdeteksi dan tool yang diperlukan tersedia dalam sesi.**

## Tes ketersediaan

> Periksa daftar tools dan skills yang tersedia. Bisakah sesi ini membuat atau mengedit gambar raster dengan AI? Jangan buat gambar dulu dan jangan menggunakan API berbayar.

## Instruksi permanen per project

Tambahkan ke `AGENTS.md` di root project game:

```md
# Raster Artwork
- For image or sprite artwork, use an AI image generation tool when available.
- Do not replace requested PNG artwork with HTML/CSS/SVG/Canvas placeholders.
- Use Python for cropping, validation and sprite packing, not as a fake AI illustrator.
- Save outputs without overwriting approved art.
- If the tool is unavailable, report it instead of silently faking the asset.
- Do not use paid API fallback without explicit permission.
```

**AGENTS.md mengarahkan agent; tidak mengaktifkan tool yang belum tersedia.**

## Instalasi skill

Lihat daftar skill pada lingkungan Codex-mu. Katalog OpenAI mendokumentasikan skill sistem dan `$skill-installer` untuk sebagian skill curated. Restart Codex setelah install jika diminta. Periksa versi dokumentasi karena mekanisme distribusi berkembang.

Referensi: https://developers.openai.com/codex/ · https://github.com/openai/skills · https://github.com/openai/plugins
