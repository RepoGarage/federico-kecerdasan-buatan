# Identifikasi Genre Musik dengan Metode Augmentasi Data

Repositori ini berisi implementasi sistem untuk mengidentifikasi genre musik menggunakan metode augmentasi data dan model pembelajaran mesin. Proyek ini bertujuan untuk meningkatkan kinerja klasifikasi genre musik, terutama ketika dihadapkan pada keterbatasan data, dengan memanfaatkan berbagai teknik augmentasi audio.

## Anggota Kelompok

- **Federico Matthew Pratama** - (Cantumkan NIM Anda jika ada)
- **Fernando Perry** - (Cantumkan NIM Anda jika ada)

## Deskripsi Proyek

Proyek ini mengeksplorasi penggunaan augmentasi data untuk melatih model klasifikasi genre musik yang lebih robust dan akurat. Kami akan memproses _file_ audio musik, mengekstraksi fitur-fitur penting, menerapkan teknik augmentasi yang berbeda untuk memperkaya dataset, dan kemudian melatih model pembelajaran mesin untuk mengidentifikasi genre.

**Tujuan Utama:**

- Meningkatkan akurasi identifikasi genre musik.
- Mengatasi masalah _overfitting_ dan generalisasi model pada dataset kecil.
- Mempelajari dampak berbagai teknik augmentasi data pada kinerja model audio.

## Fitur-Fitur Utama

- **Pemrosesan Audio**: Memuat dan memproses _file_ audio.
- **Ekstraksi Fitur**: Mengekstrak fitur-fitur akustik relevan dari audio (misalnya, MFCCs, _Chroma Feature_, _Melspectrogram_).
- **Augmentasi Data**: Menerapkan berbagai teknik augmentasi audio seperti perubahan kecepatan, perubahan _pitch_, penambahan _noise_, _time stretching_, dan _pitch shifting_.
- **Pelatihan Model**: Melatih model pembelajaran mesin (misalnya, CNN, SVM, Random Forest) pada data yang telah diaugmentasi.
- **Evaluasi Model**: Mengevaluasi kinerja model menggunakan metrik klasifikasi standar.

## Persiapan & Instalasi

1.  **Clone Repositori**:

    ```bash
    git clone [URL_REPOSITORI_ANDA]
    cd identifikasi-genre-musik
    ```

2.  **Instal Dependensi**:
    Pastikan Anda memiliki Python (disarankan Python 3.7+) terinstal. Instal pustaka yang diperlukan menggunakan `pip`:

    ```bash
    pip install numpy pandas librosa scikit-learn matplotlib seaborn ipywidgets tqdm
    ```

    Jika Anda berencana untuk menggunakan GPU untuk pelatihan model (misalnya dengan TensorFlow atau PyTorch), pastikan driver yang sesuai terinstal dan instal versi `tensorflow-gpu` atau `pytorch` yang kompatibel.

3.  **Dataset**:
    Proyek ini akan memerlukan dataset audio musik yang sesuai untuk klasifikasi genre. Anda perlu menyediakan dataset Anda sendiri atau mengunduh dataset yang umum digunakan seperti GTZAN Dataset. Pastikan _path_ ke dataset dikonfigurasi dengan benar di dalam _notebook_.

## Cara Menjalankan

1.  **Buka Notebook Jupyter**:

    ```bash
    jupyter notebook identifikasi-genre-musik.ipynb
    ```

2.  **Jalankan Setiap Sel**:
    Ikuti instruksi di dalam _notebook_. Jalankan setiap sel secara berurutan. _Notebook_ akan memandu Anda melalui langkah-langkah berikut:
    - Memuat dan memproses data.
    - Menerapkan augmentasi data.
    - Mengekstraksi fitur.
    - Melatih dan mengevaluasi model.
    - Menganalisis hasil.

## Hasil

Bagian ini akan berisi temuan dan hasil dari eksperimen Anda, termasuk akurasi model, grafik kinerja, dan analisis dampak augmentasi data.

## Kontribusi

Kontribusi disambut baik! Jika Anda memiliki saran atau perbaikan, silakan buat _issue_ atau kirim _pull request_.
