# 🔧 Git Cheatsheet — Django for Everyone

> Git adalah skill wajib setiap developer. Kuasai ini!

---

## 🚀 Setup Awal (Sekali saja)

```bash
git config --global user.name "Ahmad Faqih"
git config --global user.email "ahmad@email.com"
git config --global init.defaultBranch main
```

---

## 📅 Workflow Harian

```bash
# Cek status
git status                        # File apa yang berubah?
git diff                          # Apa perubahannya?

# Simpan perubahan
git add .                         # Stage semua perubahan
git add nama_file.py              # Stage satu file saja
git commit -m "feat: tambah fitur login"

# Sync dengan GitHub
git pull origin main              # Ambil update terbaru
git push origin main              # Kirim ke GitHub
```

---

## 🌿 Branch (Cabang)

```bash
git branch                        # Lihat semua branch
git branch nama-fitur             # Buat branch baru
git checkout nama-fitur           # Pindah ke branch
git checkout -b nama-fitur        # Buat + langsung pindah (shortcut)
git merge nama-fitur              # Gabungkan branch ke main
git branch -d nama-fitur          # Hapus branch (sudah di-merge)
```

---

## ⏪ Membatalkan Perubahan

```bash
git restore nama_file.py          # Batalkan perubahan di file (belum di-stage)
git restore --staged nama_file.py # Un-stage file
git revert HEAD                   # Batalkan commit terakhir (aman, buat commit baru)
git log --oneline                 # Lihat history commit
```

---

## 📝 Konvensi Pesan Commit

```bash
# Format: type(scope): deskripsi
feat(auth): tambah fitur login dengan Google
fix(modul-09): perbaiki error migrasi database
docs(readme): update instruksi instalasi
style(template): rapikan indentasi HTML
refactor(views): ubah FBV ke CBV
test(models): tambah unit test untuk model Artikel
chore(deps): update Django ke versi 5.1
```

---

_Cheatsheet ini bagian dari [Django for Everyone](../../README.md) oleh Ahmad Faqih_
