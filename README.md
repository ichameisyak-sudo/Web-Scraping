# Web & API Scraping Task

Repositori ini berisi notebook Python untuk melakukan pengolahan data berbasis teks menggunakan dua metode ekstraksi data: **Web Scraping via HTTP (HTML Parsing)** dan **API Fetching**.

---

## Deskripsi Proyek

Notebook ini terbagi menjadi dua bagian utama:

### 1. Web Scraping menggunakan HTTP (Detik News)
* **Target:** Artikel berita Detik.com mengenai karhutla di Kalimantan Selatan.
* **Metode:** Ekstraksi HTML menggunakan `requests` dan `BeautifulSoup`.
* **Proses Pembersihan Data:**
  * Menghapus elemen non-isi seperti *SCROLL TO CONTINUE WITH CONTENT*, iklan, video, dan tautan internal (*Baca juga*, *[Gambas:]*).
  * Menghapus header lokasi (*Jakarta -*).
* **Output:** `pandas.DataFrame` berisi daftar paragraf beserta inti teks artikel yang sudah dibersihkan.

### 2. Scraping Data menggunakan API (Spaceflight News API)
* **Target Endpoint:** `https://api.spaceflightnewsapi.net/v4/articles/`
* **Metode:** Mengambil data JSON publik via HTTP Request.
* **Proses Data:** Menyaring atribut penting (`title`, `news_site`, `published_at`, `url`, `summary`).
* **Output:** `pandas.DataFrame` berisi daftar artikel berita antariksa terkini.

---

## Library yang Digunakan

* `requests` — Mengirim HTTP Request ke server/API.
* `beautifulsoup4` — Melakukan parsing struktur HTML.
* `pandas` — Menyusun dan menampilkan data dalam bentuk tabular (DataFrame).
* `re` — *Regular Expression* untuk cleaning teks dari pola iklan/noise.

---

## Cara Menjalankan

1. Clone repositori ini:
   ```bash
   git clone [https://github.com/USERNAME_KAMU/NAMA_REPOSITORI.git](https://github.com/USERNAME_KAMU/NAMA_REPOSITORI.git)
