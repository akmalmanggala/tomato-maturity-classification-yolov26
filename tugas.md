
Activity!

* Buat kelompok yang terdiri dari 3-4 orang (15 kelompok): kelompokku 3 anggota
* Pilih topik image classification yang dekat dengan kehidupan sehari-hari: Klasifikasi tingkat kematangan buah tomat
* Pilih 1 arsitektur deep leaerning yang mendukung image classification: yolo v26
* 1 arsitektur max dipilih oleh 3 kelompok


Dibagi menjadi 2 pembagian tugas:

A. Mencari problem

1. Task apa? : sudah
2. Menentukan arsitektur x. : sudah
3. Pencarian dataset private
4. Clean up
5. Anotasi: labelStudio

B. Reproduce results

1. Cari related papers/website sumber
2. Image dataset FREE/OPEN
3. Setup environment $\rightarrow$ github
4. Load pretrained model
5. Inference pretrained model untuk data test B2, cek kemiripan dengan klaim di B1
6. Train from scratch dengan B2, cek kemiripan dengan B1


Langkah selanjutnya jika itu udah:

1. Inference data private dengan pretrained model
2. Fine tune $\rightarrow$ ubah hyperparameters, training head only
3. Transfer learning $\rightarrow$ load pretrained, freeze some layers, ...
4. Train from scratch
