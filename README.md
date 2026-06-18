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
Eksperimen manipulasi citra digital menggunakan Python dan OpenCV yang mencakup: membaca citra, konversi BGR ke RGB, resize, image blending, image negative, transformasi logaritmik, transformasi gamma, serta analisis efek setiap teknik terhadap brightness, contrast, dan detail citra.

## Citra yang Digunakan
1. **image1.jpg** — Citra terang dengan detail tinggi (pemandangan alam, 600×386)
2. **image2.jpg** — Citra gelap dengan kontras rendah (suasana malam, 600×400)

Keduanya dari [Pexels](https://www.pexels.com).

## Library
Python 3, OpenCV, NumPy, Matplotlib, Jupyter Notebook.

## Cara Menjalankan
```bash
pip install -r requirements.txt
jupyter notebook notebooks/image_manipulation.ipynb
```

## Struktur Folder
```
manipulasi-citra-digital/
├── images/
│   ├── image1.jpg
│   └── image2.jpg
├── notebooks/
│   └── image_manipulation.ipynb
├── report/
│   ├── laporan.tex
│   └── laporan.pdf
├── README.md
└── requirements.txt
```

## Hasil Eksperimen
| Bagian | Teknik | Hasil |
|--------|--------|-------|
| A | Baca & Konversi Warna | 2 citra terbaca, BGR→RGB, shape, dtype, min/max pixel |
| B | Resize | Resize ke 600×400, before/after visual |
| C | Image Blending | 3 bobot (0.2/0.8, 0.5/0.5, 0.8/0.2) + tabel perbandingan |
| D | Image Negative | Citra negatif + histogram asli vs negatif |
| E | Transformasi Logaritmik | s = c·log(1+r), konstanta c, histogram, min/max |
| F | Transformasi Gamma | γ = 0.5, 1, 2, 2.5 + histogram + tabel efek |
| G | Analisis HOTS | Tabel 4 teknik, 5 keputusan, 2 studi kasus |
| H | Refleksi Pribadi | 5 pertanyaan refleksi tentang pemahaman |

## Laporan
`report/laporan.pdf` (8 halaman, format LaTeX).

## Kesimpulan
Transformasi gamma adalah teknik paling fleksibel karena bisa mencerahkan (γ<1) maupun menggelapkan (γ>1). Transformasi logaritmik unggul untuk detail di area gelap. Image blending efektif menggabungkan dua citra, dan image negative berguna untuk analisis medis. Tidak ada teknik yang selalu memperbaiki kualitas — pemilihan harus disesuaikan dengan karakteristik citra dan tujuan yang ingin dicapai.
