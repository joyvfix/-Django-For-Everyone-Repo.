# 🐛 Masalah & Solusi — Modul 18: Deployment ke Server

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

## ❌ Masalah 1: 500 Internal Server Error di production

**🔴 Gejala / Pesan Error:**
```
Error tersembunyi di production
```

**🟡 Penyebab:**
Ini terjadi karena cek log server.

**✅ Solusi:**
Cek log server. Aktifkan logging di settings.py. Pastikan DEBUG=False dan ALLOWED_HOSTS sudah diset.

**🛡️ Pencegahan:**
Biasakan untuk selalu cek konfigurasi sebelum menjalankan program. Baca pesan error dari baris pertama — biasanya sudah ada petunjuk solusinya.

---

## ❌ Masalah 2: Static files tidak muncul setelah deploy

**🔴 Gejala / Pesan Error:**
```
Static files di production
```

**🟡 Penyebab:**
Ini terjadi karena jalankan collectstatic sebelum deploy.

**✅ Solusi:**
Jalankan collectstatic sebelum deploy. Konfigurasi WhiteNoise atau web server untuk serve static files.

**🛡️ Pencegahan:**
Biasakan untuk selalu cek konfigurasi sebelum menjalankan program. Baca pesan error dari baris pertama — biasanya sudah ada petunjuk solusinya.

---

## ❌ Masalah 3: Database tidak terhubung

**🔴 Gejala / Pesan Error:**
```
Konfigurasi database production
```

**🟡 Penyebab:**
Ini terjadi karena cek database_url environment variable.

**✅ Solusi:**
Cek DATABASE_URL environment variable. Pastikan PostgreSQL running dan credentials benar.

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
