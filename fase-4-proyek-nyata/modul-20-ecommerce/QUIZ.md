# 📝 Quiz & Latihan — Modul 20: Studi Kasus: E-Commerce

> Test pemahamanmu! Coba jawab dulu sebelum lihat kunci jawaban.

---

## 📌 Petunjuk

1. Baca setiap soal dengan teliti
2. **Jawab sendiri dulu** — jangan langsung lihat jawaban!
3. Cek jawaban di bagian bawah
4. Untuk soal coding — jalankan dan test kodenya!

**Sistem Nilai:**
- 5 soal benar = ⭐⭐⭐ Excellent!
- 4 soal benar = ⭐⭐ Good!  
- 3 soal benar = ⭐ Keep Learning!
- < 3 soal = 📚 Baca ulang materinya dulu

---

## ❓ Soal

**Soal 1:** Bagaimana cara menyimpan cart untuk user yang belum login?

```
Jawabanmu: ___________________________
```

---

**Soal 2:** Apa itu payment webhook?

```
Jawabanmu: ___________________________
```

---

**Soal 3:** Mengapa validasi transaksi wajib di server-side?

```
Jawabanmu: ___________________________
```

---

**Soal 4:** Apa yang harus dilakukan jika payment gateway timeout?

```
Jawabanmu: ___________________________
```

---


## 🔑 Kunci Jawaban

<details>
<summary>👆 Klik untuk lihat jawaban (coba sendiri dulu!)</summary>

**Jawaban Soal 1:** Bagaimana cara menyimpan cart untuk user yang belum login?

> ✅ Menggunakan Django session (request.session) — data tersimpan di server, user diidentifikasi via session cookie.

---

**Jawaban Soal 2:** Apa itu payment webhook?

> ✅ HTTP endpoint yang menerima notifikasi dari payment gateway saat status pembayaran berubah. Penting untuk konfirmasi otomatis.

---

**Jawaban Soal 3:** Mengapa validasi transaksi wajib di server-side?

> ✅ Client-side bisa dimanipulasi. Server harus selalu verifikasi dengan payment gateway sebelum konfirmasi pesanan.

---

**Jawaban Soal 4:** Apa yang harus dilakukan jika payment gateway timeout?

> ✅ Cek status ke payment gateway sebelum tampilkan error. Implementasi idempotency key untuk mencegah double charge.

---

</details>

---

## 🚀 Tantangan Ekstra

Sudah selesai quiz? Coba tantangan ini:

1. Buat variasi project modul ini dengan fitur tambahan
2. Jelaskan konsep modul ini kepada teman/anggota keluarga dengan kata-kata sendiri
3. Cari contoh penerapan konsep ini di aplikasi populer (WhatsApp, Instagram, Tokopedia)

---

_Bagian dari [Django for Everyone](../../README.md) oleh Ahmad Faqih_
