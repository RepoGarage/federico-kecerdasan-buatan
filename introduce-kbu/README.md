# Pengenalan Kecerdasan Buatan (AI)

Repositori ini berisi materi pengantar dan implementasi dasar terkait Kecerdasan Buatan (AI), disajikan dalam format _notebook_ Jupyter. Ini adalah panduan praktis untuk memahami konsep-konsep AI fundamental melalui contoh kode.

## Daftar Isi

1.  **Pengenalan**
2.  **Anggota Kelompok**
3.  **Struktur Proyek**
4.  **Fungsionalitas**
    - Algoritma Pencarian (DFS, BFS, UCS)
    - Problem Solving (Water Jug Problem)
    - Constraint Satisfaction Problem (CSP - N-Queens Problem)
5.  **Persiapan dan Instalasi**
6.  **Cara Menjalankan**
7.  **Catatan**

## 1. Pengenalan

Proyek ini mengeksplorasi implementasi fundamental dari algoritma pencarian klasik, teknik penyelesaian masalah, dan konsep _Constraint Satisfaction Problem_ (CSP) dalam konteks Kecerdasan Buatan. Semua implementasi disajikan dalam satu _notebook_ yang mudah dipahami dan dijalankan.

## 2. Anggota Kelompok

- Elisa Bayu Hendra (233401015)
- Yohanes Emmanuel Putra Sutanto (233401017)
- Federico Matthew Pratama (233405001)
- Fernando Perry (233406005)
- Vincentius Johanes Lwie Jaya (233408010)
- Yohanes Bramanta Adita Saputra (233409009)

## 3. Struktur Proyek

- `introduce-kbu.ipynb`: Notebook Jupyter utama yang berisi seluruh kode Python, penjelasan, dan demonstrasi dari setiap bagian.

## 4. Fungsionalitas

### 4.1. Algoritma Pencarian

Implementasi tiga algoritma pencarian graf dasar:

- **Depth-First Search (DFS)**: Mencari solusi dengan menjelajahi sejauh mungkin setiap cabang sebelum melakukan _backtracking_.
- **Breadth-First Search (BFS)**: Mencari solusi dengan menjelajahi simpul-simpul pada tingkat yang sama secara merata sebelum pindah ke tingkat berikutnya.
- **Uniform-Cost Search (UCS)**: Mencari solusi optimal dengan memperluas simpul dengan biaya jalur terendah terlebih dahulu.

### 4.2. Problem Solving (Water Jug Problem)

Penerapan algoritma pencarian untuk menyelesaikan "Water Jug Problem". Masalah ini melibatkan menentukan serangkaian operasi untuk mendapatkan jumlah air tertentu dalam bejana dengan kapasitas yang berbeda.

### 4.3. Constraint Satisfaction Problem (CSP - N-Queens Problem)

Implementasi "N-Queens Problem" sebagai contoh _Constraint Satisfaction Problem_. Tujuannya adalah menempatkan N ratu pada papan catur N×N sedemikian rupa sehingga tidak ada dua ratu yang saling mengancam (yaitu, tidak ada dua ratu yang berbagi baris, kolom, atau diagonal yang sama).

## 5. Persiapan dan Instalasi

1.  **Clone Repositori**:

    ```bash
    git clone [URL_REPOSITORI_ANDA]
    cd introduce-kbu
    ```

2.  **Instal Dependensi**:
    Pastikan Anda memiliki Python (disarankan Python 3.7+) terinstal. Anda dapat menginstal pustaka yang diperlukan menggunakan `pip`:
    ```bash
    pip install numpy pandas matplotlib networkx
    ```

## 6. Cara Menjalankan

1.  **Buka Notebook Jupyter**:

    ```bash
    jupyter notebook introduce-kbu.ipynb
    ```

2.  **Jalankan Setiap Sel**:
    Ikuti instruksi di dalam _notebook_. Jalankan setiap sel secara berurutan untuk melihat implementasi, penjelasan, dan hasil dari setiap algoritma dan masalah yang diselesaikan.

## 7. Catatan

- Notebook ini dirancang untuk pemahaman konseptual dan tidak dioptimalkan untuk kinerja pada skala besar.
- Visualisasi sederhana disertakan untuk membantu pemahaman alur kerja algoritma.
