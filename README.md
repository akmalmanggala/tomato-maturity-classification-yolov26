# 🍅 Tomato Maturity Classification with YOLOv26

> **Mata Kuliah**: Sains Data Terapan  
> **Tugas**: Kelompok 2  
> **Topik**: Klasifikasi Tingkat Kematangan Buah Tomat  
> **Arsitektur**: YOLOv26 (Image Classification)

---

## 📋 Deskripsi Proyek

Proyek ini mengimplementasikan **klasifikasi tingkat kematangan buah tomat** menggunakan arsitektur deep learning terbaru **YOLOv26** dari Ultralytics. Tomat diklasifikasikan ke dalam 4 kelas:

| Kelas | Deskripsi |
|:---|:---|
| `Unripe` | Tomat mentah (hijau) |
| `Ripe` | Tomat matang (merah) |
| `Old` | Tomat lewat matang / tua |
| `Damaged` | Tomat rusak / cacat |

---

## 📁 Struktur Repository

```
tomato-maturity-classification-yolov26/
│
├── 📓 tomato_yolov26_reproduce.ipynb   # Notebook utama (B3–B6)
├── 📄 README.md                        # Dokumentasi proyek
├── 📄 requirements.txt                 # Daftar library
├── 📄 .gitignore                       # File yang dikecualikan dari git
│
├── 📂 paper/
│   └── 2606.03748v1.pdf               # Paper acuan YOLO26 (arXiv)
│
└── 📂 data/
    └── README.md                       # Panduan download dataset
```

> **Catatan**: Folder `dataset/` tidak di-push ke GitHub karena ukurannya besar.  
> Dataset didownload otomatis saat menjalankan notebook. Lihat [data/README.md](data/README.md).

---

## 🗂️ Dataset

**Dataset Publik (Reproduce Results):**
- **Nama**: VegNet — Vegetable Dataset with Quality
- **Sumber**: Mendeley Data — [doi: 10.17632/6nxnjbn9w6.1](https://data.mendeley.com/datasets/6nxnjbn9w6/1)
- **Penulis**: Suryawanshi, Patil, Chumchu (2022)
- **Subset yang digunakan**: Folder `Tomato` (3.061 foto)
- **Lisensi**: CC BY 4.0 (Gratis untuk riset)

**Dataset Private (Kelompok):**
- Foto tomat diambil sendiri oleh anggota kelompok
- Dianotasi menggunakan **Label Studio**
- Kelas: `mentah`, `setengah_matang`, `matang`

---

## 📄 Paper Acuan

| Komponen | Detail |
|:---|:---|
| **Paper** | Ultralytics YOLO26: Unified Real-Time End-to-End Vision Models |
| **Penulis** | Glenn Jocher et al. (2026) |
| **Publikasi** | arXiv:2606.03748 |
| **Link** | https://arxiv.org/abs/2606.03748 |
| **Klaim Akurasi** | Top-1: 71.4% (yolo26n-cls, ImageNet) |

---

## 🚀 Cara Menjalankan

### Opsi 1: Google Colab (Direkomendasikan)

Klik tombol di bawah untuk langsung membuka notebook di Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/akmalmanggala/tomato-maturity-classification-yolov26/blob/main/tomato_yolov26_reproduce.ipynb)

**Langkah:**
1. Pastikan runtime GPU aktif: `Runtime → Change runtime type → T4 GPU`
2. Jalankan semua cell dari atas ke bawah (`Runtime → Run all`)
3. Saat diminta upload, upload file `Tomato.zip` (lihat [data/README.md](data/README.md))

### Opsi 2: Lokal

```bash
git clone https://github.com/akmalmanggala/tomato-maturity-classification-yolov26.git
cd tomato-maturity-classification-yolov26
pip install -r requirements.txt
jupyter notebook tomato_yolov26_reproduce.ipynb
```

---

## 🧪 Alur Eksperimen

```
B1. Paper YOLO26 (arXiv:2606.03748) → Klaim: Top-1 = 71.4% di ImageNet
         │
B2. Dataset Tomat VegNet (3.061 foto, 4 kelas)
         │
B3. Setup environment (ultralytics, torch)
         │
B4. Load pretrained model → yolo26n-cls.pt (bawaan paper YOLO26)
         │
B5. Inference pretrained → data test tomat
    → Bandingkan hasil dengan klaim 71.4% di paper
         │
B6. Train from scratch → yolo26n-cls.yaml + data tomat
    → Buktikan arsitektur YOLO26 efektif untuk kematangan tomat
```

---

## 📊 Hasil Eksperimen

| Eksperimen | Keterangan | Top-1 Accuracy |
|:---|:---|:---|
| Klaim Paper B1 | ImageNet (1.000 kelas umum) | 71.4% |
| B5: Pretrained → Tomat | Tanpa training ulang | *(isi setelah dijalankan)* |
| B6: Train From Scratch | Dilatih khusus data tomat | *(isi setelah dijalankan)* |

---

## 🔖 Sitasi

```bibtex
@article{jocher2026yolo26,
  title={Ultralytics YOLO26: Unified Real-Time End-to-End Vision Models},
  author={Jocher, Glenn and others},
  journal={arXiv preprint arXiv:2606.03748},
  year={2026}
}

@article{suryawanshi2022vegnet,
  title={VegNet: Dataset of vegetable quality images for machine learning applications},
  author={Suryawanshi, Yogesh and Patil, Kailas and Chumchu, Prawit},
  journal={Data in Brief},
  volume={45},
  pages={108657},
  year={2022},
  doi={10.1016/j.dib.2022.108657}
}
```
