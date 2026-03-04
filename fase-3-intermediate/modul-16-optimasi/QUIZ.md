# 📝 Quiz & Latihan — Modul 16: Database Lanjutan & Optimasi

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

**Soal 1:** Apa itu N+1 query problem?

```
Jawabanmu: ___________________________
```

---

**Soal 2:** Kapan menggunakan select_related vs prefetch_related?

```
Jawabanmu: ___________________________
```

---

**Soal 3:** Apa keuntungan menggunakan database index?

```
Jawabanmu: ___________________________
```

---

**Soal 4:** Apa itu caching dan mengapa berguna?

```
Jawabanmu: ___________________________
```

---

**Soal 5:** Tools apa yang digunakan untuk profiling query Django?

```
Jawabanmu: ___________________________
```

---


## 🔑 Kunci Jawaban

<details>
<summary>👆 Klik untuk lihat jawaban (coba sendiri dulu!)</summary>

**Jawaban Soal 1:** Apa itu N+1 query problem?

> ✅ Mengambil N object dari database, lalu untuk setiap object melakukan 1 query tambahan untuk data related. Total: N+1 queries. Sangat tidak efisien.

---

**Jawaban Soal 2:** Kapan menggunakan select_related vs prefetch_related?

> ✅ select_related: untuk ForeignKey/OneToOne (JOIN query). prefetch_related: untuk ManyToMany atau reverse FK (query terpisah yang efisien).

---

**Jawaban Soal 3:** Apa keuntungan menggunakan database index?

> ✅ Mempercepat pencarian data secara drastis. Seperti indeks buku — langsung ke halaman yang tepat tanpa baca seluruh buku.

---

**Jawaban Soal 4:** Apa itu caching dan mengapa berguna?

> ✅ Menyimpan hasil komputasi/query yang sering diakses di memori. Akses berikutnya dari cache — jauh lebih cepat dari database.

---

**Jawaban Soal 5:** Tools apa yang digunakan untuk profiling query Django?

> ✅ Django Debug Toolbar — menampilkan semua SQL query, durasi, dan lokasi di kode.

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
