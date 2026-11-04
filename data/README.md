# Panduan Dataset (VegNet Tomato)

Dataset citra buah tomat tidak disimpan langsung di repository GitHub ini untuk mematuhi batas ukuran file GitHub dan menjaga repository tetap efisien.

---

## Sumber Dataset Resmi
- Nama Dataset: VegNet: Vegetable Dataset with quality (Unripe, Ripe, Old, Dried and Damaged)
- Penulis: Yogesh Suryawanshi, Kailas Patil, Prawit Chumchu (2022)
- Repositori: Mendeley Data
- DOI: 10.17632/6nxnjbn9w6.1
- Tautan: https://data.mendeley.com/datasets/6nxnjbn9w6/1
- Lisensi: Creative Commons Attribution 4.0 International (CC BY 4.0)

---

## Pembagian Kategori Citra
Hanya subset direktori `Tomato` (atau `4. Tomato`) yang digunakan dalam eksperimen klasifikasi kematangan:

| Kategori | Kondisi Buah | Keterangan |
|:---|:---|:---:|
| `Unripe` | Mentah (hijau) | Termasuk dalam pengujian |
| `Ripe` | Matang (merah) | Termasuk dalam pengujian |
| `Old` | Lewat matang / tua | Termasuk dalam pengujian |
| `Damaged` | Rusak / cacat / busuk | Termasuk dalam pengujian |
| `Dried` | Kering (0 sampel pada tomat) | Diabaikan otomatis |

---

## Cara Penggunaan di Google Colab
1. Unduh arsip ZIP dari Mendeley Data (atau ambil folder `4. Tomato`).
2. Kompres folder tomat menjadi `Tomato.zip` atau `4. Tomato.zip`.
3. Buka dan jalankan notebook `tomato_yolov26_reproduce.ipynb`.
4. Unggah berkas ZIP tersebut pada cell penyiapan dataset. Sistem akan membagi data menjadi:
   - Train: 80%
   - Validation: 10%
   - Test: 10%
