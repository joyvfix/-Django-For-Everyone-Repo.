# 🐍 Python Cheatsheet — Django for Everyone

> Referensi cepat Python yang dipakai di kursus ini.

---

## 📦 Tipe Data

```python
# String
nama = "Ahmad Faqih"
nama = 'Ahmad Faqih'
nama = f"Halo, {nama}!"           # f-string (paling modern)
nama.upper()   # AHMAD FAQIH
nama.lower()   # ahmad faqih
nama.split()   # ['Ahmad', 'Faqih']
len(nama)      # 11

# Integer & Float
umur = 25
harga = 99.99
total = int("42")      # Konversi string ke int
desimal = float("3.14")

# Boolean
aktif = True
nonaktif = False
not True       # False
True and False # False
True or False  # True

# List (urutan, bisa diubah)
buah = ["apel", "mangga", "jeruk"]
buah[0]           # "apel" (index dari 0)
buah[-1]          # "jeruk" (dari belakang)
buah.append("anggur")  # tambah di akhir
buah.insert(1, "pisang")  # tambah di index 1
buah.remove("mangga")     # hapus by nilai
buah.pop()                # hapus terakhir
len(buah)                 # jumlah item

# Dictionary (pasangan kunci-nilai)
user = {
    "nama": "Ahmad",
    "umur": 25,
    "aktif": True
}
user["nama"]              # "Ahmad"
user.get("email", "N/A")  # "N/A" (default jika tidak ada)
user["email"] = "ahmad@email.com"  # tambah/ubah
user.keys()               # semua key
user.values()             # semua value
user.items()              # semua pasangan (key, value)
```

---

## 🔀 Kontrol Alur

```python
# If / elif / else
nilai = 85
if nilai >= 90:
    print("A")
elif nilai >= 75:
    print("B")
elif nilai >= 60:
    print("C")
else:
    print("D")

# For loop
for i in range(5):          # 0, 1, 2, 3, 4
    print(i)

for i in range(1, 6):       # 1, 2, 3, 4, 5
    print(i)

for buah in ["apel", "mangga"]:
    print(buah)

for key, value in user.items():
    print(f"{key}: {value}")

# While loop
hitung = 0
while hitung < 5:
    print(hitung)
    hitung += 1

# List Comprehension (cara elegan membuat list)
angka_genap = [x for x in range(10) if x % 2 == 0]
# [0, 2, 4, 6, 8]

kuadrat = [x**2 for x in range(5)]
# [0, 1, 4, 9, 16]
```

---

## 🔧 Fungsi

```python
# Fungsi dasar
def sapa(nama):
    return f"Halo, {nama}!"

# Default parameter
def sapa(nama, salam="Halo"):
    return f"{salam}, {nama}!"

sapa("Ahmad")           # "Halo, Ahmad!"
sapa("Ahmad", "Hai")   # "Hai, Ahmad!"

# *args dan **kwargs
def jumlahkan(*angka):
    return sum(angka)

jumlahkan(1, 2, 3, 4)  # 10

def buat_profil(**info):
    for key, value in info.items():
        print(f"{key}: {value}")

buat_profil(nama="Ahmad", umur=25, kota="Jakarta")

# Lambda (fungsi singkat)
kuadrat = lambda x: x**2
kuadrat(5)  # 25

# sorted dengan key
data = [{"nama": "Budi", "umur": 30}, {"nama": "Ahmad", "umur": 25}]
sorted(data, key=lambda x: x["umur"])  # urut by umur
```

---

## 🏛️ OOP — Class

```python
class Hewan:
    # Class attribute (shared semua instance)
    kingdom = "Animalia"

    def __init__(self, nama, suara):
        # Instance attribute
        self.nama = nama
        self.suara = suara

    def bersuara(self):
        return f"{self.nama} berkata: {self.suara}"

    def __str__(self):
        return f"Hewan({self.nama})"

    def __repr__(self):
        return f"Hewan(nama='{self.nama}', suara='{self.suara}')"


class Kucing(Hewan):  # Inheritance
    def __init__(self, nama, warna):
        super().__init__(nama, "Meow")  # Panggil __init__ parent
        self.warna = warna

    def bersuara(self):  # Override method
        return f"{self.nama} si kucing {self.warna} berkata: {self.suara}!"


# Penggunaan
kucing = Kucing("Mimi", "oranye")
print(kucing.bersuara())    # "Mimi si kucing oranye berkata: Meow!"
print(isinstance(kucing, Hewan))   # True
print(issubclass(Kucing, Hewan))   # True
```

---

## 🛡️ Error Handling

```python
try:
    hasil = 10 / 0
except ZeroDivisionError:
    print("Tidak bisa dibagi nol!")
except ValueError as e:
    print(f"ValueError: {e}")
except Exception as e:
    print(f"Error tidak terduga: {e}")
else:
    print("Berhasil!")      # Jalan jika tidak ada exception
finally:
    print("Selalu jalan")   # Selalu dijalankan

# Raise custom exception
class UmurTidakValidError(Exception):
    pass

def set_umur(umur):
    if umur < 0 or umur > 150:
        raise UmurTidakValidError(f"Umur {umur} tidak valid!")
    return umur
```

---

## 📁 File & Module

```python
# Baca file
with open('file.txt', 'r', encoding='utf-8') as f:
    konten = f.read()

# Tulis file
with open('output.txt', 'w', encoding='utf-8') as f:
    f.write("Halo Dunia!")

# Import
import os
import json
from datetime import datetime, timedelta
from pathlib import Path

# Virtual environment
# python -m venv venv
# source venv/bin/activate    # Mac/Linux
# venv\Scripts\activate       # Windows
# pip install nama-package
# pip freeze > requirements.txt
# pip install -r requirements.txt
```

---

_Cheatsheet ini bagian dari [Django for Everyone](../../README.md) oleh Ahmad Faqih_
