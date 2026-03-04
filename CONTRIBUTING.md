# 🤝 Panduan Kontribusi — Django for Everyone

Terima kasih sudah mau berkontribusi! Setiap kontribusi, sekecil apapun, sangat berarti. 🙏

---

## 📋 Apa yang Bisa Dikontribusikan?

| Tipe | Contoh |
|------|--------|
| 📝 **Perbaikan teks** | Typo, kalimat membingungkan, penjelasan kurang jelas |
| 🐛 **Bug pada kode** | Kode yang tidak berjalan, error yang tidak tertangani |
| 💡 **Contoh tambahan** | Alternatif cara penulisan kode |
| 🌐 **Terjemahan** | Konten dalam bahasa lain |
| 📚 **Materi baru** | Penjelasan topik yang belum ada |
| 🔧 **Tools & resources** | Cheatsheet, template baru |

---

## 🚀 Cara Berkontribusi

### 1. Fork & Clone
```bash
# Fork repo di GitHub, lalu:
git clone https://github.com/USERNAME/django-for-everyone.git
cd django-for-everyone
```

### 2. Buat Branch Baru
```bash
# Gunakan nama yang deskriptif
git checkout -b fix/typo-modul-01
git checkout -b feat/tambah-contoh-views
git checkout -b docs/update-quiz-modul-05
```

### 3. Buat Perubahan
- Ikuti format dan gaya yang sudah ada
- Pastikan kode bisa dijalankan
- Tambahkan komentar pada kode yang kompleks

### 4. Commit dengan Pesan yang Jelas
```bash
# Format: type(scope): deskripsi singkat
git commit -m "fix(modul-01): perbaiki typo pada penjelasan variabel"
git commit -m "feat(modul-09): tambah contoh query filter kompleks"
git commit -m "docs(quiz): tambah soal latihan modul 07"
```

**Tipe commit:**
- `fix` — perbaikan bug/error
- `feat` — fitur/konten baru
- `docs` — perubahan dokumentasi
- `style` — format kode (tanpa ubah logika)
- `refactor` — restrukturisasi kode

### 5. Push & Pull Request
```bash
git push origin nama-branch-kamu
```
Lalu buka Pull Request di GitHub dengan:
- **Judul** yang jelas
- **Deskripsi** apa yang diubah dan kenapa
- **Screenshot** jika ada perubahan visual

---

## 📐 Standar Penulisan

### Markdown
- Gunakan heading yang terstruktur (`#`, `##`, `###`)
- Sertakan contoh kode dalam code block dengan bahasa yang tepat
- Gunakan emoji secukupnya untuk visual yang ramah

### Python / Django Code
```python
# ✅ BENAR — kode yang bersih dan terdokumentasi
def hitung_total(harga, pajak=0.11):
    """
    Menghitung total harga termasuk pajak.
    
    Args:
        harga (float): Harga dasar produk
        pajak (float): Persentase pajak (default: 11%)
    
    Returns:
        float: Total harga setelah pajak
    """
    return harga * (1 + pajak)

# ❌ SALAH — kode tanpa penjelasan
def h(x, y=0.11):
    return x * (1 + y)
```

### Penamaan File
- Gunakan huruf kecil dan tanda hubung: `nama-file.md`
- Deskriptif dan singkat: `error-umum.md` bukan `e.md`

---

## 🐛 Melaporkan Bug

Gunakan template issue yang sudah disediakan. Pastikan sertakan:
1. **Modul yang bermasalah** (contoh: Modul 07 - URL & Views)
2. **Langkah untuk mereproduksi** masalah
3. **Pesan error lengkap** (copy-paste dari terminal)
4. **Environment** (OS, Python version, Django version)

---

## ✅ Checklist Sebelum Submit PR

- [ ] Kode bisa dijalankan tanpa error
- [ ] Sudah test di Python 3.11+
- [ ] Mengikuti format yang sudah ada
- [ ] Tidak ada file sensitif (.env, database, dll)
- [ ] Pesan commit jelas dan deskriptif

---

## 💬 Ada Pertanyaan?

Buka [Discussion](../../discussions) atau [Issue](../../issues) — kami senang membantu! 😊

---

_Dibuat dengan ❤️ oleh komunitas Django for Everyone_
