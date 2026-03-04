# 🐛 Masalah & Solusi — Modul 16: Database Lanjutan & Optimasi

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

## ❌ Masalah 1: Query sangat lambat

**🔴 Gejala / Pesan Error:**
```
N+1 query problem
```

**🟡 Penyebab:**
Ini terjadi karena gunakan django debug toolbar untuk identifikasi.

**✅ Solusi:**
Gunakan Django Debug Toolbar untuk identifikasi. Kemungkinan N+1 problem — tambahkan select_related() atau prefetch_related().

**🛡️ Pencegahan:**
Biasakan untuk selalu cek konfigurasi sebelum menjalankan program. Baca pesan error dari baris pertama — biasanya sudah ada petunjuk solusinya.

---

## ❌ Masalah 2: Cache tidak bekerja

**🔴 Gejala / Pesan Error:**
```
Redis tidak terhubung
```

**🟡 Penyebab:**
Ini terjadi karena pastikan redis running.

**✅ Solusi:**
Pastikan Redis running. Cek konfigurasi CACHES di settings.py dan koneksi Redis.

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
