# Troubleshooting

## Codex menggambar dengan CSS/SVG, bukan ImageGen

**Kemungkinan:** skill/tool tidak ada, tidak dipilih atau request dianggap tugas coding. Periksa tools tersedia, minta raster artwork yang eksplisit dan larang placeholder. Jangan menganggap AGENTS.md dapat mengaktifkan tool.

## Skill sudah terpasang tapi image tool tidak ada

Skill adalah workflow, bukan akses tool. Periksa versi Codex, sesi, fitur dan izin. Jangan mengganti ke API berbayar tanpa persetujuan.

## Repair mengubah seluruh karakter

Batasi edit dengan invariants yang jelas; sertakan original; simpan hasil non-destructive; bandingkan kedua versi.

## Sprite sheet salah frame

Validasi jumlah grid, dimensi, penempatan, dan preview frame. Image generator tidak menjamin angka tepat hanya dari prompt.

## PNG latar tidak transparan

Pastikan alpha=0 di background, bukan pola checkerboard yang dilukis.

## Klaim AI 'sudah dites' tapi belum jelas

Minta path output, command test, log validasi, dan bukti screenshot. Bedakan pemeriksaan otomatis dan review visual.
