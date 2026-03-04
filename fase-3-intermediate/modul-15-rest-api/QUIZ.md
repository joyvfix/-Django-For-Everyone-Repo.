# 📝 Quiz & Latihan — Modul 15: REST API dengan Django REST Framework

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

**Soal 1:** Apa format data yang paling umum digunakan dalam REST API?

```
Jawabanmu: ___________________________
```

---

**Soal 2:** Apa fungsi Serializer di Django REST Framework?

```
Jawabanmu: ___________________________
```

---

**Soal 3:** Apa perbedaan Token Authentication dan JWT?

```
Jawabanmu: ___________________________
```

---

**Soal 4:** HTTP method apa yang digunakan untuk: ambil data, buat data baru, update seluruh data, hapus data?

```
Jawabanmu: ___________________________
```

---

**Soal 5:** Apa itu ViewSet di DRF?

```
Jawabanmu: ___________________________
```

---


## 🔑 Kunci Jawaban

<details>
<summary>👆 Klik untuk lihat jawaban (coba sendiri dulu!)</summary>

**Jawaban Soal 1:** Apa format data yang paling umum digunakan dalam REST API?

> ✅ JSON (JavaScript Object Notation)

---

**Jawaban Soal 2:** Apa fungsi Serializer di Django REST Framework?

> ✅ Mengkonversi model Python ke JSON (untuk response) dan JSON ke data Python (untuk request). Juga melakukan validasi.

---

**Jawaban Soal 3:** Apa perbedaan Token Authentication dan JWT?

> ✅ Token Auth: token disimpan di database, perlu query DB untuk verifikasi. JWT: token berisi informasi terenkripsi, bisa diverifikasi tanpa DB query — lebih scalable.

---

**Jawaban Soal 4:** HTTP method apa yang digunakan untuk: ambil data, buat data baru, update seluruh data, hapus data?

> ✅ GET (ambil), POST (buat baru), PUT (update penuh)/PATCH (update sebagian), DELETE (hapus)

---

**Jawaban Soal 5:** Apa itu ViewSet di DRF?

> ✅ Class yang menggabungkan logika untuk multiple related views (list, create, retrieve, update, destroy) dalam satu class.

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
