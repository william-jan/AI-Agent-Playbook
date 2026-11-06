# Prompt siap pakai

## Audit akses tool

```text
Periksa apakah skill imagegen dan tool image_gen tersedia di sesi ini.
Jangan menghasilkan gambar dan jangan gunakan API berbayar.
```

## Generate raster artwork

```text
Buat pixel art ninja full body dengan background transparan.
Output wajib file PNG artwork AI asli, bukan CSS/SVG/Canvas/Python drawing.
Simpan ke public/assets/characters/ sebagai file baru.
Jika generator gambar tidak tersedia, laporkan, jangan buat placeholder.
```

## Edit anomali

```text
Perbaiki hanya tangan pada sprite yang diberikan. Pertahankan semua
bagian lain termasuk kostum, pose, palet, shading, outline dan ukuran.
Simpan hasil terpisah dari original dan inspeksi perubahannya.
```

## Sprite sheet QA

```text
Validasi file PNG sebagai grid 8x8 (64 cell). Periksa dimensi,
transparansi alpha, framing dan frame terpotong. Bedakan laporan
kesalahan terukur dari masalah visual yang perlu review manusia.
```

## Browser QA

```text
Jalankan aplikasi lokal, uji flow utama dengan browser automation
jika tersedia, screenshot hasil, dan buat laporan reproduksi bug.
Jangan modifikasi data production.
```
