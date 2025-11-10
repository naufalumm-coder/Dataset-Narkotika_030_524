# ⚖️ Dataset 50 Putusan Pidsus Narkotika & Psikotropika pn jaksel

Kumpulan data ini berisi **50 dokumen putusan** Pengadilan Negeri jakarta selatan terkait tindak pidana khusus (pidsus) narkotika dan psikotropika dipengadilan negri jaksel.

## 📝 Deskripsi

Dataset ini dikumpulkan secara manual untuk tujuan akademis, khususnya sebagai bahan studi kasus untuk mata kuliah temu kembali informasi. Fokus utama dari penggunaan dataset ini adalah untuk menerapkan teknik *Natural Language Processing (NLP)* dan *Information Retrieval (IR)* pada teks hukum berbahasa Indonesia.

Seluruh dokumen dalam dataset ini adalah data publik yang diperoleh dari sumber resmi.

## 📦 Isi Dataset

* **Folder:** `narkotika/`
* **Jumlah Dokumen:** 50 file
* **Format File:** pdf
* **Bahasa:** Indonesia

## 📂 Sumber Data

Dokumen-dokumen ini diunduh dari **Direktori Putusan Mahkamah Agung Republik Indonesia**.
* **URL:** [https://putusan3.mahkamahagung.go.id/](https://putusan3.mahkamahagung.go.id/)

## ⚙️ Proyek Terkait (Penggunaan Dataset)

Dataset ini digunakan dalam sebuah proyek untuk membangun mesin pencari sederhana. Alur kerja utama yang diterapkan pada 50 dokumen ini meliputi:

1.  **Ekstraksi Teks:** Membaca dan mengekstrak seluruh teks dari 50 file dokumen.
2.  **Preprocessing Teks:**
    * *Case Folding*: Mengubah semua teks menjadi huruf kecil.
    * *Punctuation & Number Removal*: Menghapus tanda baca dan angka.
    * *Stopword Removal*: Menghapus kata-kata umum (menggunakan library Sastrawi).
    * *Stemming*: Mengubah kata-kata ke bentuk dasarnya (misal: "menyakinkan" -> "yakin") menggunakan Sastrawi.
3.  **Indexing:**
    * Membangun indeks dokumen menggunakan pembobotan **TF-IDF (Term Frequency-Inverse Document Frequency)**.
    * Menggunakan `TfidfVectorizer` dari library Scikit-learn dengan `ngram_range=(1, 2)` untuk menangkap frasa 2-kata (bigram).
4.  **Pencarian (Search Engine):**
    * Menerapkan **Cosine Similarity** untuk menghitung skor relevansi antara kueri (pertanyaan) pengguna dengan dokumen yang ada di dalam indeks.

## ⚠️ Disclaimer

Dataset ini disediakan untuk tujuan **edukasi dan penelitian non-komersial** semata. Data ini merupakan data publik yang bersumber dari Mahkamah Agung RI. Pengguna dataset ini bertanggung jawab penuh atas penggunaannya dan disarankan untuk selalu merujuk ke sumber asli untuk informasi hukum yang sah dan final.

---
