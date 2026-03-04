# 📝 Quiz & Latihan — Modul 23: Keamanan & Best Practices

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

**Soal 1:** Apa itu SQL Injection dan bagaimana Django mencegahnya?

```
Jawabanmu: ___________________________
```

---

**Soal 2:** Apa bedanya XSS dan CSRF?

```
Jawabanmu: ___________________________
```

---

**Soal 3:** Di mana sebaiknya menyimpan SECRET_KEY Django?

```
Jawabanmu: ___________________________
```

---

**Soal 4:** Perintah Django apa untuk mengecek konfigurasi keamanan production?

```
Jawabanmu: ___________________________
```

---

**Soal 5:** Apa OWASP Top 10?

```
Jawabanmu: ___________________________
```

---


## 🔑 Kunci Jawaban

<details>
<summary>👆 Klik untuk lihat jawaban (coba sendiri dulu!)</summary>

**Jawaban Soal 1:** Apa itu SQL Injection dan bagaimana Django mencegahnya?

> ✅ Injeksi kode SQL via input user untuk manipulasi database. Django ORM mencegah dengan parameterized queries otomatis.

---

**Jawaban Soal 2:** Apa bedanya XSS dan CSRF?

> ✅ XSS: injeksi JavaScript berbahaya ke halaman web. CSRF: request palsu dari site lain yang berpura-pura jadi user login.

---

**Jawaban Soal 3:** Di mana sebaiknya menyimpan SECRET_KEY Django?

> ✅ Di environment variable atau file .env yang tidak di-commit ke Git. Jangan pernah hardcode di settings.py.

---

**Jawaban Soal 4:** Perintah Django apa untuk mengecek konfigurasi keamanan production?

> ✅ python manage.py check --deploy

---

**Jawaban Soal 5:** Apa OWASP Top 10?

> ✅ Daftar 10 kerentanan keamanan web paling umum dan berbahaya yang diterbitkan OWASP. Standar referensi keamanan web dunia.

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
