# 🐛 Masalah & Solusi — Modul 04: Python Lanjutan — Fungsi & OOP

> Kumpulan error paling umum yang dialami peserta di modul ini, lengkap dengan solusi dan penjelasan mengapa terjadi.

---

## 💡 Cara Membaca Dokumen Ini

Setiap masalah dijelaskan dalam format:
- **Masalah**: Deskripsi error yang terjadi
- **Gejala**: Apa yang terlihat / pesan error
- **Penyebab**: Kenapa ini terjadi
- **Solusi**: Langkah-langkah mengatasi
- **Pencegahan**: Cara agar tidak terjadi lagi

---

## ❌ Masalah 1: TypeError: missing required argument

**🔴 Gejala / Pesan Error:**
```
Lupa kirim argumen saat panggil fungsi
```

**🟡 Penyebab:**
Ini terjadi karena fungsi dipanggil tanpa argumen yang wajib.

**✅ Solusi:**
Fungsi dipanggil tanpa argumen yang wajib. Cek definisi fungsi — berapa parameter yang dibutuhkan?

**🛡️ Pencegahan:**
Biasakan untuk selalu cek konfigurasi sebelum menjalankan program. Baca pesan error dari baris pertama — biasanya sudah ada petunjuk solusinya.

---

## ❌ Masalah 2: AttributeError: object has no attribute

**🔴 Gejala / Pesan Error:**
```
Typo nama method atau lupa definisikan
```

**🟡 Penyebab:**
Ini terjadi karena method atau atribut yang dipanggil tidak ada di class itu.

**✅ Solusi:**
Method atau atribut yang dipanggil tidak ada di class itu. Cek spelling dan pastikan sudah didefinisikan.

**🛡️ Pencegahan:**
Biasakan untuk selalu cek konfigurasi sebelum menjalankan program. Baca pesan error dari baris pertama — biasanya sudah ada petunjuk solusinya.

---

## ❌ Masalah 3: RecursionError: maximum recursion depth exceeded

**🔴 Gejala / Pesan Error:**
```
Lupa base case di fungsi rekursif
```

**🟡 Penyebab:**
Ini terjadi karena fungsi rekursif memanggil dirinya sendiri tanpa batas.

**✅ Solusi:**
Fungsi rekursif memanggil dirinya sendiri tanpa batas. Pastikan ada base case yang menghentikan rekursi.

**🛡️ Pencegahan:**
Biasakan untuk selalu cek konfigurasi sebelum menjalankan program. Baca pesan error dari baris pertama — biasanya sudah ada petunjuk solusinya.

---

## 🆘 Masalah Tidak Ada di Daftar?

1. **Copy pesan error lengkap** → Google → Stack Overflow
2. **Cek Django documentation** → docs.djangoproject.com
3. **Buka Discussion** di repo ini → [Diskusi](../../discussions)
4. **Tanya di komunitas** dengan menyertakan:
   - Pesan error lengkap
   - Kode yang bermasalah
   - Langkah yang sudah dicoba

---

_Temukan solusi baru? Kontribusikan ke repo ini! Lihat [CONTRIBUTING.md](../../CONTRIBUTING.md)_
