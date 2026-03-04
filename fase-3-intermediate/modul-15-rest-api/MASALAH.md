# 🐛 Masalah & Solusi — Modul 15: REST API dengan Django REST Framework

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

## ❌ Masalah 1: 401 Unauthorized di API

**🔴 Gejala / Pesan Error:**
```
Authentication header salah
```

**🟡 Penyebab:**
Ini terjadi karena token tidak dikirim atau format salah.

**✅ Solusi:**
Token tidak dikirim atau format salah. Header: Authorization: Token <token_value> atau Bearer <jwt>.

**🛡️ Pencegahan:**
Biasakan untuk selalu cek konfigurasi sebelum menjalankan program. Baca pesan error dari baris pertama — biasanya sudah ada petunjuk solusinya.

---

## ❌ Masalah 2: Serializer tidak valid

**🔴 Gejala / Pesan Error:**
```
Data tidak sesuai serializer
```

**🟡 Penyebab:**
Ini terjadi karena cek required fields di serializer.

**✅ Solusi:**
Cek required fields di serializer. Print serializer.errors untuk lihat field mana yang bermasalah.

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
