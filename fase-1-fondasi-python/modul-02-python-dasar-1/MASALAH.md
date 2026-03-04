# 🐛 Masalah & Solusi — Modul 02: Python Dasar — Bagian 1

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

## ❌ Masalah 1: SyntaxError: invalid syntax

**🔴 Gejala / Pesan Error:**
```
Sering muncul saat belajar sintaks baru
```

**🟡 Penyebab:**
Ini terjadi karena cek tanda kurung, kutip, dan titik dua.

**✅ Solusi:**
Cek tanda kurung, kutip, dan titik dua. Python sensitif terhadap indentasi dan tanda baca.

**🛡️ Pencegahan:**
Biasakan untuk selalu cek konfigurasi sebelum menjalankan program. Baca pesan error dari baris pertama — biasanya sudah ada petunjuk solusinya.

---

## ❌ Masalah 2: NameError: name 'x' is not defined

**🔴 Gejala / Pesan Error:**
```
Lupa assign nilai ke variabel
```

**🟡 Penyebab:**
Ini terjadi karena variabel harus didefinisikan sebelum digunakan.

**✅ Solusi:**
Variabel harus didefinisikan sebelum digunakan. Cek ejaan nama variabel — Python case-sensitive.

**🛡️ Pencegahan:**
Biasakan untuk selalu cek konfigurasi sebelum menjalankan program. Baca pesan error dari baris pertama — biasanya sudah ada petunjuk solusinya.

---

## ❌ Masalah 3: TypeError: unsupported operand type

**🔴 Gejala / Pesan Error:**
```
Mencampur tipe data tanpa konversi
```

**🟡 Penyebab:**
Ini terjadi karena tidak bisa langsung jumlahkan string dan angka.

**✅ Solusi:**
Tidak bisa langsung jumlahkan string dan angka. Konversi dulu: int('5') atau str(5).

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
