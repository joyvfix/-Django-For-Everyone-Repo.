# 🐛 Masalah & Solusi — Modul 01: Perkenalan & Setup Environment

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

## ❌ Masalah 1: Python tidak ditemukan setelah install

**🔴 Gejala / Pesan Error:**
```
ModuleNotFoundError / 'python' is not recognized
```

**🟡 Penyebab:**
Ini terjadi karena pastikan centang 'add python to path' saat install.

**✅ Solusi:**
Pastikan centang 'Add Python to PATH' saat install. Atau tambahkan manual ke sistem PATH.

**🛡️ Pencegahan:**
Biasakan untuk selalu cek konfigurasi sebelum menjalankan program. Baca pesan error dari baris pertama — biasanya sudah ada petunjuk solusinya.

---

## ❌ Masalah 2: VS Code tidak detect Python

**🔴 Gejala / Pesan Error:**
```
Tidak ada linting/autocomplete di VS Code
```

**🟡 Penyebab:**
Ini terjadi karena tekan ctrl+shift+p → 'python: select interpreter' → pilih python yang terinstall.

**✅ Solusi:**
Tekan Ctrl+Shift+P → 'Python: Select Interpreter' → pilih Python yang terinstall.

**🛡️ Pencegahan:**
Biasakan untuk selalu cek konfigurasi sebelum menjalankan program. Baca pesan error dari baris pertama — biasanya sudah ada petunjuk solusinya.

---

## ❌ Masalah 3: Terminal tidak bisa dibuka

**🔴 Gejala / Pesan Error:**
```
Bingung cara buka terminal
```

**🟡 Penyebab:**
Ini terjadi karena windows: cari 'powershell' di start menu.

**✅ Solusi:**
Windows: cari 'PowerShell' di Start Menu. Mac: Cmd+Space → 'Terminal'. Linux: Ctrl+Alt+T.

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
