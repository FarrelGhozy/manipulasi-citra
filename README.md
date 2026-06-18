# Manipulasi Citra Digital Menggunakan OpenCV

**Mata Kuliah:** Pengolahan Sinyal Digital

## Identitas Mahasiswa
- **Nama:** Farrel Ghozy Affifudin
- **NIM:** 452024611053
- **Kelas:** TI5 A2
- **Program Studi:** Teknik Informatika
- **Fakultas:** Sains dan Teknologi
- **Universitas:** Universitas Darussalam Gontor

## Deskripsi
Proyek ini berisi eksperimen manipulasi citra digital menggunakan Python dan OpenCV. Tugas ini mencakup 8 teknik manipulasi citra: membaca dan menampilkan citra, konversi warna BGR ke RGB, resize, image blending, image negative, transformasi logaritmik, transformasi gamma, serta analisis efek setiap transformasi terhadap kualitas citra.

## Citra yang Digunakan
1. **image1.jpg** - Citra terang dengan detail tinggi (pemandangan alam)
2. **image2.jpg** - Citra gelap dengan kontras rendah (suasana malam)

Kedua citra diambil dari [Pexels](https://www.pexels.com) (sumber gambar gratis).

## Library yang Digunakan
- Python 3.x
- OpenCV (cv2)
- NumPy
- Matplotlib
- Jupyter Notebook

## Cara Menjalankan Notebook
1. Clone repository ini
2. Install dependensi: `pip install -r requirements.txt`
3. Jalankan Jupyter Notebook: `jupyter notebook`
4. Buka file `notebooks/image_manipulation.ipynb`
5. Jalankan semua cell (Run All)

## Struktur Folder
```
manipulasi-citra-digital/
├── images/
│   ├── image1.jpg
│   └── image2.jpg
├── notebooks/
│   └── image_manipulation.ipynb
├── report/
│   └── laporan.pdf
├── README.md
├── requirements.txt
├── planning.md
└── agents.md
```

## Ringkasan Hasil Eksperimen
| Bagian | Teknik | Hasil Utama |
|--------|--------|-------------|
| A | Baca & Konversi Warna | Berhasil membaca 2 citra, mengkonversi BGR ke RGB, menampilkan shape, dtype, min/max pixel |
| B | Resize | Kedua citra di-resize ke ukuran 600x400 agar bisa di-blending |
| C | Image Blending | 3 variasi bobot diuji: (0.2,0.8), (0.5,0.5), (0.8,0.2) - semakin besar α, semakin dominan citra 1 |
| D | Image Negative | Citra negatif berhasil dibuat, histogram tercermin (mirror) pada sumbu horizontal |
| E | Transformasi Logaritmik | Area gelap diperkuat, area terang dikompresi - efektif untuk detail di area gelap |
| F | Transformasi Gamma | 4 nilai gamma (0.5, 1, 2, 2.5) diuji: γ<1 terang, γ=1 identik, γ>1 gelap |

## Laporan
Laporan PDF tersedia di `report/laporan.pdf` (8 halaman, format LaTeX).

## Kesimpulan
Setiap teknik manipulasi citra memiliki kelebihan dan kekurangan masing-masing. Transformasi gamma adalah teknik yang paling fleksibel karena dapat digunakan untuk mencerahkan (γ<1) maupun menggelapkan (γ>1) citra. Transformasi logaritmik sangat efektif untuk meningkatkan detail pada area gelap. Image blending berguna untuk menggabungkan dua citra, dan image negative bermanfaat untuk analisis medis dan efek kreatif. Pemilihan teknik yang tepat bergantung pada karakteristik citra dan tujuan yang ingin dicapai.
