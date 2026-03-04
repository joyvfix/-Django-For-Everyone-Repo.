# 🐛 Masalah & Solusi — Modul 17: Testing & Debugging

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

## ❌ Masalah 1: Test database tidak di-reset

**🔴 Gejala / Pesan Error:**
```
Data test tercampur antar test
```

**🟡 Penyebab:**
Ini terjadi karena gunakan testcase (bukan unittest.

**✅ Solusi:**
Gunakan TestCase (bukan unittest.TestCase). Django TestCase otomatis bersihkan database setelah setiap test.

**🛡️ Pencegahan:**
Biasakan untuk selalu cek konfigurasi sebelum menjalankan program. Baca pesan error dari baris pertama — biasanya sudah ada petunjuk solusinya.

---

## ❌ Masalah 2: Test gagal tapi kode benar

**🔴 Gejala / Pesan Error:**
```
Test tidak independen
```

**🟡 Penyebab:**
Ini terjadi karena pastikan test menggunakan data yang disiapkan sendiri (fixtures atau setup).

**✅ Solusi:**
Pastikan test menggunakan data yang disiapkan sendiri (fixtures atau setUp). Jangan bergantung pada data yang sudah ada.

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
