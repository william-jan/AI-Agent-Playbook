# Practical Deep Dives

[← Handbook](README.md) · [Checklist](../08-vibecoding-safety/production-checklist.md)

Contoh berikut **ilustratif**, bukan potongan kode production-ready yang bisa disalin tanpa menyesuaikan arsitektur.

## 1. Race Condition dan Atomic Update (MongoDB)

**Kasus:** dua request membeli stok terakhir. Pola `findOne → if stock > 0 → update` terpisah rentan karena kedua request dapat membaca stok yang sama.

```ts
// Contoh Mongoose: pengurangan stok bersyarat dan atomik dalam satu dokumen.
const updated = await Product.findOneAndUpdate(
  { _id: productId, stock: { $gte: quantity } },
  { $inc: { stock: -quantity } },
  { new: true },
);
if (!updated) throw new Error("Stok tidak cukup");
```

**Batas:** bila checkout juga membuat order, memproses pembayaran, atau mengubah beberapa dokumen, pertimbangkan transaction dan desain idempotency, bukan menganggap satu update sudah menyelesaikan semuanya.

**Verifikasi:** kirim dua request bersamaan untuk stok 1. Pastikan tepat satu berhasil, tidak ada stok negatif, dan order/pembayaran konsisten.

## 2. Authorization / IDOR

**Kasus:** endpoint `GET /api/orders/:id` memeriksa bahwa user login, tetapi tidak memeriksa pemilik order.

```ts
// Setelah session diverifikasi di server:
const order = await Order.findOne({
  _id: orderId,
  customerId: session.user.id,
});
if (!order) return new Response("Not found", { status: 404 });
```

**Batas:** contoh ini khusus resource milik satu customer. Role admin, mitra, atau kebijakan berbasis atribut memerlukan aturan eksplisit tambahan.

**Verifikasi:** user A harus ditolak ketika memakai ID order milik user B; uji read, update, dan delete secara terpisah.

## 3. Input Validation dan Type Safety

```ts
// TS type tidak memvalidasi JSON runtime:
type Purchase = { quantity: number };
const body = await request.json(); // unknown / data eksternal
// Gunakan runtime schema validation sebelum menggunakan body.
```

**Verifikasi:** uji string, null, array, angka negatif, angka non-integer, angka sangat besar, dan field ekstra. Jangan hanya mengandalkan error TypeScript.

## 4. SQL Injection

```ts
// Salah: interpolasi input pengguna dalam SQL
const bad = `SELECT * FROM users WHERE email = '${email}'`;
// Aman secara struktur: parameter binding (sintaks tergantung driver)
const result = await db.query("SELECT * FROM users WHERE email = $1", [email]);
```

**Verifikasi:** query tak boleh berubah struktur karena input pengguna. Parameter SQL tidak otomatis melindungi identifier dinamis seperti nama kolom; gunakan allowlist.

## 5. XSS, CSRF dan CORS bukan hal yang sama

- **XSS:** penyerang memasukkan script/konten aktif ke halaman korban; gunakan escaping bawaan framework dan sanitasi HTML saat benar-benar diperlukan.
- **CSRF:** browser korban mengirim request yang membawa kredensial otomatis (misalnya cookie); gunakan perlindungan CSRF sesuai alur autentikasi, SameSite, dan pemeriksaan origin.
- **CORS:** kebijakan browser tentang akses respons antar-origin; CORS bukan sistem izin atau pengganti auth.

**Verifikasi:** identifikasi konteks sink HTML, jenis kredensial cookie/bearer token, origin yang diizinkan, dan operasi yang mengubah data.

## 6. JWT: signed ≠ encrypted

JWT bertanda tangan membuktikan integritas setelah signature diverifikasi; payload biasa tetap dapat dibaca. Verifikasi algoritma yang diizinkan, issuer, audience, expiry, dan aturan revocation/rotation bila diperlukan. Jangan menaruh secret atau data pribadi yang tidak perlu di payload.

## 7. Caching dan data privat

Kesalahan umum: cache response profil pelanggan menggunakan key global, lalu memberikannya kepada pengguna lain. Pastikan key mencerminkan scope otorisasi, header cache benar, dan invalidasi terjadi setelah mutasi.

**Verifikasi:** akses halaman sebagai dua akun berbeda; data privat tidak boleh bercampur meskipun request dipicu bergantian atau bersamaan.

## 8. Rate Limiting pada multi-instance

Counter in-memory per-instance tidak konsisten ketika traffic tersebar ke banyak instance atau fungsi serverless. Untuk batas global, pertimbangkan shared store, penentuan identitas yang tepat, dan penanganan kegagalan store.

**Verifikasi:** kirim request melewati batas melalui beberapa instance; uji status 429 dan pesan retry yang sesuai.

## 9. WebSocket multiplayer: client tidak boleh menentukan damage final

Client boleh mengirim **intent aksi**, tetapi host/server otoritatif harus memvalidasi cooldown, resources, range, collision, dan damage. Pada arsitektur *browser-host*, host sendiri tetap dapat memodifikasi simulasi; desain ini tidak setara dengan server tepercaya.

**Verifikasi:** kirim input duplikat, input terlambat, input di luar urutan, serta action yang tidak mungkin menurut state. Amati apakah kedua client akhirnya konsisten.

## 10. WebRTC dan TURN

WebRTC DataChannel dapat menghubungkan peer secara langsung jika negosiasi dan jaringan mengizinkan. Signaling tetap diperlukan; sebagian jaringan membutuhkan relay TURN. Latency tidak dapat dijamin dari jarak geografis saja.

**Verifikasi:** tes dua jaringan nyata, NAT ketat, packet loss, reconnect, dan biaya relay TURN.

## 11. CI/CD dan testing berlapis

**Unit:** aturan bisnis murni. **Integration:** database/API nyata dalam lingkungan test. **E2E:** alur pengguna. Jalankan lint, TypeScript check dan test sebelum merge/deploy; gunakan hasil CI sebagai bukti terbatas, bukan klaim zero-bug.

## 12. Logging, monitoring dan rollback

Catat request ID, operasi, durasi dan error tanpa token atau password. Tentukan indikator error rate dan latency, serta prosedur rollback yang kompatibel dengan perubahan schema. Uji restore backup terpisah dari keberhasilan build.

## Referensi lanjutan

- [MDN Web Docs](https://developer.mozilla.org/)
- [OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/)
- [MongoDB Atomicity and Transactions](https://www.mongodb.com/docs/manual/core/write-operations-atomicity/)
- [WebRTC API](https://developer.mozilla.org/en-US/docs/Web/API/WebRTC_API)
- [OpenTelemetry](https://opentelemetry.io/docs/)
