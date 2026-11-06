# Pipeline AI Game Asset

1. **Specify:** tetapkan reference, ukuran, grid, urutan facing, palet, alpha, bagian yang wajib konsisten.
2. **Generate:** buat PNG raster dengan image tool bila tersedia, simpan terpisah dari aset approved.
3. **Review:** cek siluet, anatomi, arah, senjata, posisi, kostum, dan frame cacat.
4. **Repair:** lakukan edit terfokus, dengan invariants eksplisit dan non-destructive output.
5. **Validate:** dengan Pillow cek PNG RGBA, ukuran kanvas, cell grid, alpha background, frame yang kosong/terpotong.
6. **Integrate:** masukkan ke game engine, perbaiki loader/animation map, lalu screenshot gameplay dan cek visual.

## Khusus sprite sheet 8×8

64 cell tidak selalu berarti 64 sprite yang benar. Beri preview berlabel nomor dan bandingkan posisi origin antar-frame. Tes animasi dalam konteks game sungguhan. Validasi Python **tidak dapat memastikan** konsistensi anatomi secara sempurna.

## Artefak yang disimpan

- Original/reference
- Prompt dan batasan edit
- Hasil PNG dan versi sebelumnya
- Metadata grid/direction
- Laporan validasi dan screenshot gameplay

Skill custom untuk pipeline ini merupakan **ide yang dapat dibuat**, bukan tool siap pakai yang dijamin ada.
