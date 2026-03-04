# 📝 Quiz & Latihan — Modul 22: Django + Celery + Redis

> Test pemahamanmu! Coba jawab dulu sebelum lihat kunci jawaban.

---

## 📌 Petunjuk

1. Baca setiap soal dengan teliti
2. **Jawab sendiri dulu** — jangan langsung lihat jawaban!
3. Cek jawaban di bagian bawah
4. Untuk soal coding — jalankan dan test kodenya!

**Sistem Nilai:**
- 5 soal benar = ⭐⭐⭐ Excellent!
- 4 soal benar = ⭐⭐ Good!  
- 3 soal benar = ⭐ Keep Learning!
- < 3 soal = 📚 Baca ulang materinya dulu

---

## ❓ Soal

**Soal 1:** Apa itu task queue?

```
Jawabanmu: ___________________________
```

---

**Soal 2:** Apa fungsi Redis dalam arsitektur Celery?

```
Jawabanmu: ___________________________
```

---

**Soal 3:** Kapan sebaiknya menggunakan Celery?

```
Jawabanmu: ___________________________
```

---

**Soal 4:** Apa itu Celery Beat?

```
Jawabanmu: ___________________________
```

---


## 🔑 Kunci Jawaban

<details>
<summary>👆 Klik untuk lihat jawaban (coba sendiri dulu!)</summary>

**Jawaban Soal 1:** Apa itu task queue?

> ✅ Sistem antrian untuk menjalankan pekerjaan secara asynchronous di background, tanpa memblokir request utama.

---

**Jawaban Soal 2:** Apa fungsi Redis dalam arsitektur Celery?

> ✅ Sebagai message broker — menyimpan dan mendistribusikan task ke worker. Juga bisa digunakan sebagai result backend.

---

**Jawaban Soal 3:** Kapan sebaiknya menggunakan Celery?

> ✅ Saat ada task yang butuh waktu lama (>2 detik): kirim email, process gambar, generate laporan, scraping data.

---

**Jawaban Soal 4:** Apa itu Celery Beat?

> ✅ Scheduler Celery untuk menjalankan task secara terjadwal (cron job): tiap jam, tiap hari, tiap Senin, dll.

---

</details>

---

## 🚀 Tantangan Ekstra

Sudah selesai quiz? Coba tantangan ini:

1. Buat variasi project modul ini dengan fitur tambahan
2. Jelaskan konsep modul ini kepada teman/anggota keluarga dengan kata-kata sendiri
3. Cari contoh penerapan konsep ini di aplikasi populer (WhatsApp, Instagram, Tokopedia)

---

_Bagian dari [Django for Everyone](../../README.md) oleh Ahmad Faqih_
