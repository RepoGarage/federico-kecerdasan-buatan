# Sistem Pakar (Expert System) Sederhana: Deteksi Penyakit Tanaman

Repositori ini berisi implementasi sistem pakar (expert system) sederhana yang dirancang untuk mendeteksi penyakit pada tanaman berdasarkan gejala yang diberikan. Sistem ini dibangun menggunakan konsep _rule-based system_ dan disajikan dalam format _notebook_ Jupyter untuk kemudahan pemahaman dan eksekusi.

## Daftar Isi

1.  **Pengenalan**
2.  **Anggota Kelompok**
3.  **Struktur Proyek**
4.  **Fungsionalitas**
5.  **Data Pengetahuan (Knowledge Base)**
6.  **Persiapan dan Instalasi**
7.  **Cara Menjalankan**
8.  **Catatan**

## 1. Pengenalan

Sistem pakar adalah program komputer yang meniru kemampuan pengambilan keputusan seorang ahli manusia. Dalam proyek ini, kami membangun sistem pakar berbasis aturan untuk membantu mengidentifikasi kemungkinan penyakit tanaman berdasarkan gejala yang diamati pengguna. Sistem ini akan mengajukan serangkaian pertanyaan tentang gejala, dan berdasarkan jawaban, akan memberikan diagnosis.

## 2. Anggota Kelompok

- Elisa Bayu Hendra (233401015)
- Yohanes Emmanuel Putra Sutanto (233401017)
- Federico Matthew Pratama (233405001)
- Fernando Perry (233406005)
- Vincentius Johanes Lwie Jaya (233408010)
- Yohanes Bramanta Adita Saputra (233409009)

## 3. Struktur Proyek

- `EXAMPLE_EXPERT_SYSTEM.ipynb`: Notebook Jupyter utama yang berisi seluruh kode Python, penjelasan, dan demonstrasi sistem pakar.

## 4. Fungsionalitas

Sistem pakar ini memiliki fungsionalitas inti sebagai berikut:

- **Basis Pengetahuan (Knowledge Base)**: Kumpulan aturan (`rules`) dan fakta (`facts`) yang mendefinisikan hubungan antara gejala dan penyakit tanaman.
- **Inferensi Berbasis Aturan (Rule-based Inference)**: Sistem akan memproses gejala yang dimasukkan pengguna dan mencocokkannya dengan aturan dalam basis pengetahuan untuk mencapai kesimpulan (diagnosis).
- **Antarmuka Pengguna Sederhana**: Menggunakan input konsol untuk berinteraksi dengan pengguna, mengajukan pertanyaan gejala.
- **Deteksi Penyakit**: Berdasarkan gejala yang dikonfirmasi, sistem akan mengidentifikasi satu atau lebih penyakit yang mungkin.

## 5. Data Pengetahuan (Knowledge Base)

Basis pengetahuan sistem pakar ini didefinisikan secara langsung dalam kode Python sebagai daftar aturan. Setiap aturan terdiri dari:

- **Kondisi (Conditions)**: Daftar gejala yang harus ada (atau tidak ada) agar aturan ini diaktifkan.
- **Kesimpulan (Conclusion)**: Penyakit yang didiagnosis jika semua kondisi terpenuhi.

Contoh struktur aturan:

```python
rules = [
    {
        "conditions": ["gejala_daun_kuning", "gejala_batang_layu"],
        "conclusion": "Penyakit X"
    },
    # ... aturan lainnya
]
```
