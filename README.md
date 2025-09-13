# Tugas-2-Social-Media-Analysis

### Tugas 2: Scraping Keyword "Prabowo" dari Media Sosial
# Latar Belakang Pemilihan Keyword "Prabowo" 

Untuk tugas kedua, saya memilih kata kunci **"Prabowo"** karena:

* **Signifikansi dan Relevansi Publik:** Sebagai Presiden Indonesia, Prabowo Subianto adalah figur publik yang selalu menjadi pusat perhatian dan perbincangan. Hal ini menjamin aliran data yang sangat besar dan konstan di media sosial.
* **Memenuhi Kebutuhan Volume Data:** Popularitas topik ini memudahkan pencapaian target minimal **1.000 baris data** seperti yang disyaratkan tugas.
* **Potensi Analisis yang Kaya:** Data percakapan publik ini sangat kaya akan opini. Ini membuka peluang besar untuk analisis lanjutan seperti analisis sentimen (positif, negatif, netral) atau pemetaan isu-isu kebijakan yang sedang ramai dibicarakan.

# Cara Kerja Menggunakan `Tweet Harvest` di Google Colab
Tugas kedua dieksekusi menggunakan *tool* **Tweet Harvest** di dalam lingkungan **Google Colaboratory**. Pendekatan ini dipilih karena praktis dan tidak memerlukan instalasi di komputer pribadi. Berikut alur kerjanya sesuai *notebook* yang dibuat:

1.  **Instalasi dan Setup:**
    Langkah pertama di dalam Colab adalah menginstal `Tweet Harvest` menggunakan perintah `npx`. Ini memastikan kita selalu menggunakan versi terbaru dari *tool* tersebut.

2.  **Konfigurasi Parameter Scraping:**
    Sebelum eksekusi, semua parameter yang dibutuhkan diatur dalam variabel Python agar mudah diubah:
    * **`filename`**: Nama file output diatur menjadi `'prabowo.csv'`.
    * **`search_keyword`**: Kata kunci pencarian utama diatur menjadi `'prabowo'`.
    * **`limit`**: Batas jumlah tweet yang ingin diambil diatur menjadi `1200` untuk memastikan target 1000 data terlampaui.
    * **`auth_token`**: Token autentikasi dimasukkan di sini. Token ini berfungsi sebagai kunci akses aman untuk masuk ke akun X (Twitter) tanpa harus menggunakan *username* dan *password* secara langsung di dalam kode.

3.  **Eksekusi Perintah Scraping:**
    Perintah inti dijalankan menggunakan `os.system()`. Kode ini secara dinamis menggabungkan semua variabel yang sudah diatur sebelumnya menjadi satu perintah terminal yang lengkap. Perintah inilah yang menyuruh `Tweet Harvest` untuk mulai bekerja: membuka browser virtual, melakukan pencarian, men-*scroll* halaman, dan "memanen" data.

4.  **Hasil Akhir:**
    Setelah proses selesai, `Tweet Harvest` secara otomatis menghasilkan file `prabowo.csv` di dalam lingkungan penyimpanan Google Colab. File ini berisi ribuan baris data tweet, lengkap dengan berbagai metadata berharga seperti isi tweet, *username*, waktu posting, jumlah *likes*, jumlah *retweet*, dan lainnya, yang siap untuk diunduh dan dianalisis.
