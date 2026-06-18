# Planning - Manipulasi Citra Digital

## Identitas
- **Mata Kuliah:** Pengolahan Sinyal Digital
- **Topik:** Manipulasi Citra Digital Menggunakan OpenCV
- **Tools:** Python, OpenCV, NumPy, Matplotlib, Jupyter Notebook

---

## Deliverables
1. Jupyter Notebook `notebooks/image_manipulation.ipynb`
2. Laporan PDF `report/laporan.pdf`
3. File `README.md`
4. Repository GitHub

---

## Struktur Repository
```
manipulasi-citra-digital/
├── notebooks/
│   └── image_manipulation.ipynb
├── images/
│   ├── image1.jpg          # Citra terang/detail
│   └── image2.jpg          # Citra gelap/kontras tinggi
├── report/
│   └── laporan.pdf
├── README.md
├── requirements.txt
├── planning.md
└── agents.md
```

---

## Tahapan Pengerjaan

### Tahap 1: Setup & Persiapan
- [x] Baca tugas dari PDF
- [x] Buat planning.md
- [x] Buat agents.md
- [ ] Buat struktur folder (`images/`, `notebooks/`, `report/`)
- [ ] Cari/download 2 citra berbeda
- [ ] Buat `requirements.txt`
- [ ] Init Git repository

### Tahap 2: Implementasi Notebook - Bagian A (Membaca & Konversi Warna)
- [ ] Setup Jupyter Notebook
- [ ] Baca 2 citra dengan OpenCV
- [ ] Konversi BGR ke RGB
- [ ] Tampilkan: citra sebelum & sesudah konversi, shape, tipe data, min/max pixel
- [ ] Jawab pertanyaan analisis

### Tahap 3: Implementasi Notebook - Bagian B (Resize)
- [ ] Resize 2 citra ke ukuran sama
- [ ] Tampilkan before/after + ukuran
- [ ] Jawab pertanyaan analisis

### Tahap 4: Implementasi Notebook - Bagian C (Image Blending)
- [ ] Blending dengan 3 kombinasi bobot (0.2/0.8, 0.5/0.5, 0.8/0.2)
- [ ] Tampilkan hasil + tabel perbandingan
- [ ] Jawab pertanyaan analisis

### Tahap 5: Implementasi Notebook - Bagian D (Image Negative)
- [ ] Buat citra negatif (255 - I)
- [ ] Tampilkan: citra asli, negatif, histogram keduanya
- [ ] Jawab pertanyaan analisis

### Tahap 6: Implementasi Notebook - Bagian E (Transformasi Logaritmik)
- [ ] Hitung konstanta skala c
- [ ] Terapkan s = c * log(1 + r)
- [ ] Tampilkan: citra asli, hasil, histogram, perbandingan min/max
- [ ] Jawab pertanyaan analisis

### Tahap 7: Implementasi Notebook - Bagian F (Transformasi Gamma)
- [ ] Normalisasi pixel ke [0,1]
- [ ] Coba 4 nilai gamma: 0.5, 1, 2, 2.5
- [ ] Tampilkan: citra asli, hasil tiap gamma, histogram, tabel efek
- [ ] Jawab pertanyaan analisis

### Tahap 8: Implementasi Notebook - Bagian G & H (Analisis & Refleksi)
- [ ] Tabel perbandingan 4 teknik
- [ ] Jawab 5 pertanyaan analisis keputusan
- [ ] Kerjakan 2 studi kasus
- [ ] Jawab 5 pertanyaan refleksi

### Tahap 9: README & Dokumentasi
- [ ] Buat README.md lengkap
- [ ] Isi semua identitas mahasiswa

### Tahap 10: Finalisasi & GitHub
- [ ] Review notebook secara keseluruhan
- [ ] Export ke PDF laporan
- [ ] Push ke GitHub
- [ ] Kumpulkan link ke Moodle

---

## Timeline Target

| Tahap | Target Selesai |
|-------|---------------|
| 1-2   | Hari 1        |
| 3-5   | Hari 2        |
| 6-7   | Hari 3        |
| 8-10  | Hari 4        |

---

## Rubrik Penilaian (Total: 100)
1. Membaca Citra & Konversi Warna: 10
2. Image Blending: 15
3. Image Negative: 10
4. Transformasi Logaritmik: 15
5. Transformasi Gamma: 15
6. Visualisasi & Kerapian Notebook: 10
7. Analisis HOTS & Studi Kasus: 20
8. Dokumentasi & Refleksi: 5

## Catatan Penting
- Kode harus berjalan + mampu menjelaskan efek transformasi
- Minimal 2 citra berbeda
- Fokus: implementasi, pemahaman pixel, pemilihan teknik yang tepat
