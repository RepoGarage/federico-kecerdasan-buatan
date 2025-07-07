# Generate Hoax News: Penelitian Konten Berita Sintetis

Repositori ini menyajikan implementasi model untuk menghasilkan artikel berita sintetis, dengan fokus pada eksplorasi dan penelitian tentang konten _hoax_. Proyek ini mencakup dua versi generator berita, dari dasar hingga lebih canggih, yang masing-masing memanfaatkan kombinasi model statistik dan bahasa.

## Anggota Kelompok

- Elisa Bayu Hendra
- Yohanes Emmanuel Putra Sutanto
- Federico Matthew Pratama
- Fernando Perry
- Vincentius Johanes Lwie Jaya
- Yohanes Bramanta Adita Saputra

## Struktur Proyek

Proyek ini terdiri dari satu notebook Jupyter:

- `GENERATE_HOAX_AI.ipynb`: Berisi seluruh kode, penjelasan, dan demonstrasi untuk kedua versi generator berita.

## Deskripsi Fungsionalitas

Proyek ini bertujuan untuk menghasilkan artikel berita sintetis, yang dapat digunakan untuk tujuan penelitian, seperti deteksi _hoax_ atau analisis konten.

### Fitur Utama:

1.  **Pengambilan Data Otomatis**: Menggunakan dataset `20 Newsgroups` sebagai korpus dasar untuk melatih model.
2.  **Pemrosesan Teks**: Fungsi pembersihan teks yang komprehensif untuk menghapus _email_, _URL_, karakter non-standar, dan artefak umum dari data _newsgroups_.
3.  **Pembuatan Rantai Markov**:
    - **Versi Dasar**: Membangun rantai Markov tradisional untuk memprediksi kata berikutnya berdasarkan urutan kata sebelumnya.
    - **Versi Lanjutan**: Rantai Markov yang ditingkatkan dengan probabilitas berbobot, deteksi _loop_ (untuk menghindari pengulangan yang berlebihan), serta kemampuan untuk menghasilkan kalimat pembuka dan penutup yang lebih baik.
4.  **Pemodelan Topik (LDA)**: Menggunakan `Latent Dirichlet Allocation` (LDA) untuk mengidentifikasi topik-topik utama dan mengekstrak kata kunci yang relevan dari dataset. Kata kunci ini membantu dalam memberikan konteks dan relevansi tematik pada berita yang dihasilkan.
5.  **Peningkatan Teks dengan LLM**: Mengintegrasikan model bahasa besar ringan (`DistilGPT2`) dari pustaka Hugging Face Transformers untuk:
    - Meningkatkan koherensi dan kualitas teks yang dihasilkan oleh rantai Markov.
    - Menyaring duplikasi kalimat dalam keluaran LLM.
    - Memastikan konten yang dihasilkan sebagian besar dalam bahasa Inggris yang valid.
6.  **Pengendalian Kualitas Konten**:
    - Fungsi validasi kata (`is_valid_english_word`) untuk memastikan kata-kata yang dihasilkan adalah kata dalam bahasa Inggris yang sah.
    - Kontrol jumlah kata minimum untuk memastikan artikel yang dihasilkan memiliki substansi.
    - Ekstraksi entitas (misalnya, nama orang, organisasi, lokasi) menggunakan spaCy untuk menyuntikkan entitas yang realistis ke dalam judul dan kutipan berita.
7.  **Struktur Artikel Berita**: Artikel dihasilkan dengan struktur yang umum, termasuk judul utama, paragraf pembuka, badan artikel (beberapa paragraf), kutipan, transisi, dan kesimpulan.

## Cara Menjalankan Proyek

1.  **Clone Repositori:**

    ```bash
    git clone [URL_REPOS_ANDA]
    cd [nama_folder_repositori]
    ```

2.  **Instal Dependensi:**
    Pastikan Anda memiliki Python yang terinstal. Instal semua pustaka yang diperlukan menggunakan pip:

    ```bash
    pip install pandas numpy scikit-learn spacy transformers torch nltk
    ```

    Untuk spaCy, Anda mungkin perlu mengunduh model bahasa:

    ```bash
    python -m spacy download en_core_web_sm
    ```

    Untuk NLTK, unduh data `punkt`:

    ```bash
    python -m nltk.downloader punkt
    ```

3.  **Jalankan Notebook Jupyter:**
    Buka `GENERATE_HOAX_AI.ipynb` menggunakan Jupyter Notebook atau Google Colab.
    ```bash
    jupyter notebook
    ```
    Jalankan setiap sel secara berurutan. Notebook akan secara otomatis memuat dataset, melatih model, dan menghasilkan artikel berita sintetis.

## Catatan Penting

- **Tujuan Penelitian**: Alat ini dibuat _semata-mata untuk tujuan penelitian_ dalam ranah generasi teks dan deteksi _hoax_.
- **Akurasi Konten**: Artikel yang dihasilkan bersifat _sintetis_ dan _tidak akurat secara faktual_.
- **Etika Penggunaan**: Pengguna _tidak boleh menyebarkan atau membagikan_ konten yang dihasilkan sebagai berita nyata atau informasi yang kredibel. Penyalahgunaan alat ini untuk tujuan yang menyesatkan sangat tidak dianjurkan.

---
