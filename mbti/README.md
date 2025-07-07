# MBTI - Metode Bayesian

Repositori ini berisi implementasi aplikasi tes kepribadian MBTI (Myers-Briggs Type Indicator) menggunakan pendekatan inferensi Bayesian. Aplikasi ini akan memandu pengguna melalui serangkaian pertanyaan dan menghitung probabilitas setiap tipe MBTI berdasarkan jawaban yang diberikan, pada akhirnya mengidentifikasi tipe MBTI yang paling mungkin.

## Anggota Kelompok

- Elisa Bayu Hendra - 233401015
- Yohanes Emmanuel Putra Sutanto - 233401017
- Federico Matthew Pratama - 233405001
- Fernando Perry - 233406005
- Vincentius Johanes Lwie Jaya - 233408010
- Yohanes Bramanta Adita Saputra - 233409009

## Deskripsi Proyek

Proyek ini mengimplementasikan tes MBTI interaktif yang menggunakan prinsip-prinsip Bayesian Inference. Setiap pertanyaan dalam tes memiliki bobot probabilitas yang terkait dengan setiap aspek kepribadian MBTI (E/I, S/N, T/F, J/P). Saat pengguna menjawab pertanyaan, probabilitas untuk setiap tipe MBTI diperbarui secara iteratif menggunakan Teorema Bayes. Setelah semua pertanyaan dijawab, aplikasi akan menampilkan tipe MBTI yang memiliki probabilitas tertinggi beserta deskripsi singkatnya.

## Struktur Proyek

- `MBTI_BAYESIAN_KECERDASAN_BUATAN.ipynb`: Notebook Jupyter utama yang berisi seluruh kode, penjelasan, dan demonstrasi aplikasi.
- `data.csv`: File CSV yang berisi daftar pertanyaan tes MBTI dan bobot probabilitas terkait untuk setiap pilihan jawaban.
- `data_fetcher.py`: Skrip Python terpisah untuk memuat dan memproses data pertanyaan dari `data.csv`. (Catatan: Dalam notebook, kode `data_fetcher` disertakan langsung untuk kemudahan demonstrasi).

## Bagaimana Metode Bayesian Bekerja di Sini

1.  **Probabilitas Awal (Prior Probability)**: Setiap dari 16 tipe MBTI diinisialisasi dengan probabilitas yang sama (1/16).
2.  **Probabilitas Bukti (Likelihood)**: Setiap pilihan jawaban (dari 1 hingga 5) pada setiap pertanyaan dikaitkan dengan probabilitas tertentu untuk setiap `trait` (misalnya, untuk pertanyaan EI, ada probabilitas untuk E dan I). Ini adalah 'bukti' yang akan kita gunakan.
3.  **Update Probabilitas (Posterior Probability)**: Ketika pengguna memberikan jawaban, Teorema Bayes digunakan untuk memperbarui probabilitas setiap tipe MBTI. Probabilitas tipe MBTI dikalikan dengan _likelihood_ jawaban tersebut untuk _trait_ yang sesuai.
4.  **Normalisasi**: Setelah setiap update, semua probabilitas tipe MBTI dinormalisasi sehingga totalnya kembali menjadi 1.
5.  **Hasil Akhir**: Setelah semua pertanyaan dijawab, tipe MBTI dengan probabilitas tertinggi akan menjadi hasil tes.

## Contoh Data Pertanyaan (`data.csv`)

File `data.csv` berisi pertanyaan-pertanyaan yang terstruktur sebagai berikut:

```csv
type,question,score5,score4,score3,score2,score1
"EI","I feel energized after spending time with a group of people.","0.9|0.3","0.7|0.4","0.5|0.5","0.3|0.7","0.1|0.8"
"SN","I enjoy learning about new abstract concepts.","0.7|0.4","0.6|0.5","0.5|0.5","0.4|0.6","0.3|0.7"
"TF","I value logic and consistency in decision making.","0.9|0.3","0.8|0.4","0.6|0.5","0.4|0.7","0.3|0.8"
"JP","I prefer having a planned schedule.","0.8|0.4","0.7|0.5","0.6|0.6","0.4|0.7","0.3|0.9"
# ... dan seterusnya untuk pertanyaan lain
```
