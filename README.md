# Tugas 2 - Natural Language Processing (NLP)
## Eksplorasi Dataset & Text Preprocessing Bahasa Indonesia

Repository ini berisi penyelesaian **Tugas 2 NLP** mengenai tahapan eksplorasi data ulasan *e-commerce* dan implementasi lengkap *pipeline text preprocessing* berbahasa Indonesia.

---

### Identitas Mahasiswa
* **Nama Lengkap:** Ananda Khairatun Nisa
* **NIM:** 24146038
* **Kelas / Program Studi:** Teknik Informatika / Ilmu Komputer
* **Dosen Pengampu:** Teuku Rizky Noviandy
* **URL Repositori GitHub:** https://github.com/anandakhairatunnisa/tugas-2-nlp-preprocessing

---

### Deskripsi Dataset
* **Nama Dataset:** [`dipawidia/ecommerce-product-reviews-sentiment`](https://huggingface.co/datasets/dipawidia/ecommerce-product-reviews-sentiment)
* **Sumber:** Ulasan pelanggan dari berbagai e-commerce Indonesia (Shopee, Tokopedia, Lazada, Bukalapak, Blibli, Zalora).
* **Ukuran Data:** 11.606 baris ulasan.
* **Kolom:** `review` (teks ulasan bahasa Indonesia), `sentimen` (0 = Negatif, 1 = Positif), `translate` (terjemahan bahasa Inggris).

---

### Tahapan Preprocessing Teks
Notebook mengimplementasikan 5 tahapan preprocessing teks standar:
1. **Case Folding:** Mengubah seluruh karakter teks menjadi huruf kecil (*lowercase*).
2. **Cleaning:** Menghapus tautan/URL, tag HTML, mention/hashtag, angka, tanda baca, dan karakter khusus non-alfabet.
3. **Tokenisasi:** Memecah teks menjadi daftar token kata (*tokens list*).
4. **Stopword Removal:** Menghapus kata-kata umum yang tidak membawa bobot sentimen menggunakan pustaka `Sastrawi` ditambah kata slang e-commerce.
5. **Stemming (Teroptimasi):** Mengembalikan kata berimbuhan ke kata dasar menggunakan algoritma Sastrawi dengan teknik *dictionary caching / memoization* sehingga selesai hanya dalam hitungan detik.

---

### Struktur Repositori
```text
├── Tugas_2_NLP_Preprocessing.ipynb   # File Jupyter Notebook lengkap (siap dijalankan di Google Colab)
└── README.md                         # Dokumentasi repository, nama, dan NIM
```

---

### Cara Menjalankan di Google Colab
1. Buka [Google Colaboratory](https://colab.research.google.com/).
2. Pilih tab **Upload** lalu pilih file `Tugas_2_NLP_Preprocessing.ipynb` (atau pilih tab **GitHub** dan masukkan URL repository ini).
3. Jalankan seluruh sel dari atas ke bawah secara berurutan dengan menekan menu **Runtime** > **Run all** (atau shortcut `Ctrl + F9`).
4. Semua library (`datasets`, `Sastrawi`, `nltk`, `tqdm`) akan terpasang otomatis di sel pertama tanpa error.
