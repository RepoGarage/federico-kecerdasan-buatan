# Tugas FGD: Implementasi dan Visualisasi AI

Repositori ini berisi implementasi dari beberapa konsep dan model AI, termasuk Finite State Automata, Naive Bayes untuk Analisis Sentimen, dan visualisasi Word2Vec, serta demonstrasi model Transformer (DistilBERT).

## Anggota Kelompok

- Federico Matthew Pratama (233405001)
- Fernando Perry (233406005)

## Struktur Proyek

Proyek ini terdiri dari satu notebook Jupyter:

- `FGD_AI.ipynb`: Berisi seluruh kode dan penjelasan untuk setiap bagian tugas.

## Deskripsi Tugas

### 1. Finite State Automata (FSA) untuk Pengenalan Tanggal

Implementasi Finite State Automata (FSA) dalam Python untuk mengenali format tanggal yang fleksibel (misalnya, `dd/mm/yyyy`, `dd-mm-yyyy`, `dd/mm/yy`, `dd-mm-yy`). FSA ini dapat memvalidasi apakah sebuah string adalah tanggal yang valid berdasarkan aturan transisi antar state.

### 2. Probabilitas Analisis Sentimen (Naive Bayes)

Implementasi model Naive Bayes dari awal untuk melakukan analisis sentimen. Model ini dilatih menggunakan dataset komentar berbahasa Indonesia (bahasa umum sehari-hari) untuk mengklasifikasikan sentimen sebagai "positif" atau "negatif". Bagian ini juga mencakup fungsi untuk melihat probabilitas kata dan mode interaktif untuk pengujian sentimen.

### 3. Visualisasi Vektor Kata (Word2Vec)

Visualisasi embedding kata tanpa menggunakan library Gensim (implementasi kustom). Bagian ini mendemonstrasikan cara membuat embedding kata, menghitung kesamaan kata (cosine similarity), dan memvisualisasikan vektor kata dalam ruang 2D dan 3D menggunakan PCA dan t-SNE. Embedding contoh dibuat dengan kategori semantik untuk menunjukkan pengelompokan kata yang serupa.

### 4. Transformer Model (DistilBERT)

Demonstrasi penggunaan model Transformer DistilBERT dari Hugging Face untuk tugas `fill-mask`. Bagian ini menunjukkan cara memuat model dan tokenizer `distilbert-base-uncased` dan menggunakannya untuk memprediksi kata yang hilang dalam sebuah kalimat. Dilengkapi dengan contoh penggunaan CPU (raw pipeline) dan GPU (detail PyTorch).

## Cara Menjalankan

1.  **Clone repositori:**

    ```bash
    git clone [URL_REPOSITORI_ANDA]
    cd [nama_folder_repositori]
    ```

2.  **Instal dependensi:**
    Pastikan Anda memiliki Python terinstal. Anda dapat menginstal library yang diperlukan menggunakan pip:

    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn plotly transformers torch
    ```

3.  **Buka dan Jalankan Notebook:**
    Anda dapat membuka `FGD_AI.ipynb` menggunakan Jupyter Notebook atau Google Colab.
    ```bash
    jupyter notebook
    ```
    Kemudian, navigasikan ke file `FGD_AI.ipynb` dan jalankan setiap sel untuk melihat output dan demonstrasi dari masing-masing bagian.

## Diskusi dengan Asisten AI

Diskusi dengan GitHub Copilot yang relevan dengan tugas ini dapat diakses melalui tautan berikut:

- [CHAT 1](https://github.com/copilot/share/0809129e-0040-84d5-8903-380784520161)
- [CHAT 2](https://github.com/copilot/share/c87a0108-09a0-88c3-a912-d20a040c0061)

---
