# 📝 Quiz & Latihan — Modul 18: Deployment ke Server

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

**Soal 1:** Mengapa DEBUG harus False di production?

```
Jawabanmu: ___________________________
```

---

**Soal 2:** Apa itu environment variable dan mengapa penting untuk keamanan?

```
Jawabanmu: ___________________________
```

---

**Soal 3:** Apa perbedaan SQLite dan PostgreSQL untuk production?

```
Jawabanmu: ___________________________
```

---

**Soal 4:** Platform cloud mana yang direkomendasikan untuk deploy Django gratis/murah?

```
Jawabanmu: ___________________________
```

---

**Soal 5:** Apa yang dimaksud ALLOWED_HOSTS dan mengapa perlu diisi?

```
Jawabanmu: ___________________________
```

---


## 🔑 Kunci Jawaban

<details>
<summary>👆 Klik untuk lihat jawaban (coba sendiri dulu!)</summary>

**Jawaban Soal 1:** Mengapa DEBUG harus False di production?

> ✅ DEBUG=True menampilkan error detail termasuk kode sumber dan variable values — sangat berbahaya jika terlihat publik.

---

**Jawaban Soal 2:** Apa itu environment variable dan mengapa penting untuk keamanan?

> ✅ Variable yang disimpan di sistem operasi (bukan di kode). Menyimpan credentials di sini mencegah bocor ke version control.

---

**Jawaban Soal 3:** Apa perbedaan SQLite dan PostgreSQL untuk production?

> ✅ SQLite: file-based, cocok development, tidak support concurrent writes dengan baik. PostgreSQL: production-grade, scalable, reliable, mendukung banyak user bersamaan.

---

**Jawaban Soal 4:** Platform cloud mana yang direkomendasikan untuk deploy Django gratis/murah?

> ✅ Railway, Render, Fly.io, PythonAnywhere, Heroku (berbayar)

---

**Jawaban Soal 5:** Apa yang dimaksud ALLOWED_HOSTS dan mengapa perlu diisi?

> ✅ Daftar domain/IP yang boleh serve aplikasi Django. Mencegah HTTP Host header attacks.

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
