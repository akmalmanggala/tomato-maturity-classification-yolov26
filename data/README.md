# 🍅 Panduan Dataset (VegNet Tomato)

Dataset citra buah tomat **tidak disimpan langsung di repository GitHub ini** demi mematuhi batas ukuran file GitHub dan menjaga repository tetap ringan serta teratur.

---

## Sumber Dataset Resmi
* **Nama Dataset**: VegNet: Vegetable Dataset with quality (Unripe, Ripe, Old, Dried and Damaged)
* **Penulis**: Yogesh Suryawanshi, Kailas Patil, Prawit Chumchu (2022)
* **Repositori Resmi**: Mendeley Data
* **DOI**: [10.17632/6nxnjbn9w6.1](https://doi.org/10.17632/6nxnjbn9w6.1)
* **Link Akses**: [https://data.mendeley.com/datasets/6nxnjbn9w6/1](https://data.mendeley.com/datasets/6nxnjbn9w6/1)
* **Lisensi**: Creative Commons Attribution 4.0 International (CC BY 4.0)

---

## Pembagian Kelas Citra Tomat
Hanya subset folder **`Tomato`** (atau `4. Tomato`) yang digunakan dalam eksperimen klasifikasi kematangan:

| Kelas | Kondisi / Kematangan | Jumlah Citra |
|:---|:---|:---:|
| `Unripe` | Buah tomat mentah berwarna hijau | 145 - 845 |
| `Ripe` | Buah tomat matang berwarna merah | 955 |
| `Old` | Buah tomat lewat matang / tua | 1.234 |
| `Damaged` | Buah tomat cacat, rusak, atau busuk | 27 |
| `Dried` | *(Dilewati / 0 citra pada kategori tomat)* | 0 |

---

## Cara Penggunaan di Google Colab
1. Download file ZIP dari Mendeley Data (atau ambil folder `4. Tomato`).
2. Kompres folder tomat menjadi `4. Tomato.zip` atau `Tomato.zip`.
3. Jalankan notebook [`tomato_yolov26_reproduce.ipynb`](../tomato_yolov26_reproduce.ipynb).
4. Saat cell Upload dijalankan, pilih file `.zip` tersebut. Script akan otomatis membagi data menjadi:
   * **Train**: 80%
   * **Val**: 10%
   * **Test**: 10%
