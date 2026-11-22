# Preprocessing Teks Ulasan E-Commerce Berbahasa Indonesia

## Identitas Mahasiswa
- **Nama:** Mhd Zaki Arkan
- **NIM:** 25146061

## Deskripsi Proyek
Repository ini berisi implementasi tahapan *text preprocessing* pada dataset ulasan produk e-commerce berbahasa Indonesia menggunakan Python. Dataset yang digunakan bersumber dari Hugging Face Datasets:
- **Dataset:** [`dipawidia/ecommerce-product-reviews-sentiment`](https://huggingface.co/datasets/dipawidia/ecommerce-product-reviews-sentiment)

## Struktur Repository
- `preprocessing_ulasan_ecommerce.ipynb` : File Jupyter Notebook berisi pemuatan dataset, eksplorasi informasi dataset (jumlah baris, kolom, dan distribusi label sentimen), pipeline preprocessing 5 tahap, 10 contoh teks sebelum dan sesudah preprocessing, serta analisis pengaruh preprocessing.
- `README.md` : Dokumentasi identitas mahasiswa dan panduan penggunaan repository.

## Tahapan Preprocessing yang Diterapkan
1. **Case Folding** — Mengubah seluruh karakter huruf menjadi huruf kecil (*lowercase*).
2. **Cleaning** — Menghapus URL, angka, tanda baca, emoji, dan karakter khusus.
3. **Tokenisasi** — Memisahkan teks bersih menjadi daftar token kata.
4. **Stopword Removal** — Menghapus kata-kata umum tidak penting menggunakan daftar *stopword* Bahasa Indonesia (`PySastrawi`).
5. **Stemming** — Mengubah kata berimbuhan menjadi bentuk kata dasar menggunakan algoritma Nazief-Adriani (`PySastrawi`).

## Cara Menjalankan Notebook
1. Pastikan Python 3.8+ terpasang pada perangkat atau gunakan Google Colab.
2. Instal dependensi yang diperlukan:
   ```bash
   pip install datasets pandas PySastrawi nltk
   ```
3. Buka dan jalankan seluruh sel pada berkas `preprocessing_ulasan_ecommerce.ipynb`.