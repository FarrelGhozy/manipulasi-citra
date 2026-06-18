# Agents.md - Panduan untuk AI Assistant

## Tujuan Proyek
Membantu mahasiswa mengerjakan tugas Manipulasi Citra Digital menggunakan Python, OpenCV, NumPy, dan Matplotlib dalam bentuk Jupyter Notebook.

---

## Aturan Main

1. **BERTAHAP** - Jangan lompat ke tahap berikutnya sebelum tahap sebelumnya selesai.
2. **JANGAN SENTUH KODE** sebelum user menyatakan siap.
3. Setiap selesai satu tahap, TANYA user apakah lanjut atau revisi.
4. Tampilkan hasil visual (plot/histogram) setiap kali memungkinkan.
5. Simpan semua aset (citra) di folder `images/`.

---

## Prompt untuk Setiap Tahap

### Tahap 1: Persiapan
```
Buat struktur folder proyek:
- images/          -> untuk menyimpan citra
- notebooks/       -> untuk menyimpan .ipynb
- report/          -> untuk laporan PDF

Buat requirements.txt berisi:
- opencv-python
- numpy
- matplotlib
- jupyter

Cari 2 citra berbeda dari internet atau minta user upload:
- image1.jpg: citra dengan detail tinggi/pencahayaan bagus
- image2.jpg: citra yang cenderung gelap/kontras rendah
```

### Tahap 2: Bagian A - Membaca & Konversi Warna
```
1. Import library: cv2, numpy, matplotlib
2. Baca 2 citra dengan cv2.imread()
3. Tampilkan citra asli (BGR) - akan terlihat aneh warnanya
4. Konversi ke RGB dengan cv2.cvtColor()
5. Tampilkan citra setelah konversi
6. Print: shape, dtype, min pixel, max pixel
7. Jawab pertanyaan analisis dalam markdown/teks
```

### Tahap 3: Bagian B - Resize
```
1. Resize kedua citra ke ukuran yang sama (contoh: 600x400)
2. Tampilkan before/after + ukuran
3. Jawab pertanyaan analisis
```

### Tahap 4: Bagian C - Image Blending
```
1. Gunakan cv2.addWeighted()
2. Coba 3 bobot: (0.2,0.8), (0.5,0.5), (0.8,0.2)
3. Tampilkan hasil + tabel perbandingan
4. Jawab pertanyaan analisis
```

### Tahap 5: Bagian D - Image Negative
```
1. img_negative = 255 - img
2. Tampilkan: citra asli, negatif
3. Plot histogram asli dan negatif
4. Jawab pertanyaan analisis
```

### Tahap 6: Bagian E - Transformasi Logaritmik
```
1. Hitung c = 255 / np.log10(1 + np.max(img))
2. img_log = c * np.log10(img + 1)
3. Konversi ke uint8
4. Tampilkan: asli, hasil log, histogram, min/max
5. Jawab pertanyaan analisis
```

### Tahap 7: Bagian F - Transformasi Gamma
```
1. Normalisasi: img_norm = img / 255.0
2. Coba gamma: 0.5, 1.0, 2.0, 2.5
3. img_gamma = img_norm ** gamma
4. Kembalikan ke [0,255] dan uint8
5. Tampilkan: asli, hasil tiap gamma, histogram, tabel
6. Jawab pertanyaan analisis
```

### Tahap 8: Bagian G - Analisis HOTS & Studi Kasus
```
1. Buat tabel perbandingan 4 teknik
2. Jawab 5 pertanyaan analisis keputusan
3. Jawab 2 studi kasus (pilih dari 5)
4. Jawab refleksi pribadi
```

### Tahap 9: README
```
Buat README.md dengan:
1. Judul project
2. Nama mahasiswa (isi placeholder)
3. Deskripsi singkat
4. Daftar citra yang digunakan
5. Library yang digunakan
6. Cara menjalankan
7. Struktur folder
8. Ringkasan hasil
9. Kesimpulan
```

### Tahap 10: Finalisasi
```
1. Review semua cell notebook berjalan dengan benar
2. Export notebook ke PDF
3. Init Git, commit, push ke GitHub
4. Siapkan link untuk dikumpulkan
```

---

## Teknik Yang Harus Dikuasai
| Teknik | Fungsi Utama |
|--------|-------------|
| BGR→RGB | cv2.cvtColor(img, cv2.COLOR_BGR2RGB) |
| Resize | cv2.resize(img, (w, h)) |
| Blending | cv2.addWeighted(img1, a, img2, b, g) |
| Negative | 255 - img |
| Log Transform | c * np.log10(1 + img) |
| Gamma Transform | (img/255.0) ** gamma * 255 |

## Format Wajib Output Notebook
- Setiap bagian punya **judul** jelas (# atau ##)
- Ada **penjelasan markdown** tiap langkah
- **Kode** berjalan tanpa error
- **Plot** menggunakan matplotlib (subplot rapi)
- **Tabel perbandingan** untuk blending dan gamma
- **Jawaban analisis** dalam markdown

## Checklist Akhir
- [ ] Notebook bisa di-run dari awal sampai akhir tanpa error
- [ ] 2 citra berbeda digunakan
- [ ] Semua visualisasi tampil (citra + histogram)
- [ ] Analisis HOTS terjawab lengkap
- [ ] README.md lengkap
- [ ] requirements.txt ada
- [ ] Laporan PDF ready
- [ ] GitHub repository siap
