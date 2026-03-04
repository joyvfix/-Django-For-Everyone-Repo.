# 🐛 Masalah & Solusi — Modul 03: Python Dasar — Bagian 2

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

## ❌ Masalah 1: IndentationError: unexpected indent

**🔴 Gejala / Pesan Error:**
```
Error paling umum untuk pemula
```

**🟡 Penyebab:**
Ini terjadi karena python menggunakan indentasi (spasi/tab) untuk blok kode.

**✅ Solusi:**
Python menggunakan indentasi (spasi/tab) untuk blok kode. Jangan campur spasi dan tab. Gunakan 4 spasi konsisten.

**🛡️ Pencegahan:**
Biasakan untuk selalu cek konfigurasi sebelum menjalankan program. Baca pesan error dari baris pertama — biasanya sudah ada petunjuk solusinya.

---

## ❌ Masalah 2: Infinite loop (program tidak berhenti)

**🔴 Gejala / Pesan Error:**
```
Lupa update variabel kondisi di while loop
```

**🟡 Penyebab:**
Ini terjadi karena pastikan kondisi while akan false di suatu saat.

**✅ Solusi:**
Pastikan kondisi while akan False di suatu saat. Gunakan Ctrl+C untuk menghentikan program yang stuck.

**🛡️ Pencegahan:**
Biasakan untuk selalu cek konfigurasi sebelum menjalankan program. Baca pesan error dari baris pertama — biasanya sudah ada petunjuk solusinya.

---

## ❌ Masalah 3: IndexError: list index out of range

**🔴 Gejala / Pesan Error:**
```
Mengakses index yang tidak ada
```

**🟡 Penyebab:**
Ini terjadi karena index list dimulai dari 0.

**✅ Solusi:**
Index list dimulai dari 0. List dengan 3 item: index 0, 1, 2. Index 3 akan error.

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
