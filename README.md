**Analisis Sentimen & Topic Modeling Ulasan Aplikasi IndiHome Eazy**
Repositori ini berisi kode dan analisis studi kasus untuk menganalisis sentimen dan topik utama dari ulasan pengguna aplikasi IndiHome Eazy di Google Play Store. Analisis ini bertujuan untuk memahami persepsi pengguna, mengidentifikasi keluhan dan pujian utama, serta merumuskan rekomendasi strategis untuk meningkatkan kepuasan pelanggan dan kualitas produk.

Latar Belakang
Aplikasi IndiHome Eazy merupakan platform pengelola perangkat rumah pintar (khususnya CCTV) dari PT Telkom Indonesia. Seperti aplikasi lainnya, IndiHome Eazy menerima beragam ulasan di Google Play Store, mulai dari pujian hingga keluhan teknis. Studi ini menggunakan data ulasan tersebut untuk menggali wawasan mendalam mengenai pengalaman pengguna (UX) dan mengidentifikasi area perbaikan yang paling krusial.

Tujuan Analisis
1. Menganalisis Sentimen Pengguna: Mengklasifikasikan ulasan ke dalam kategori positif, netral, dan negatif untuk mengukur tingkat kepuasan secara umum.
2. Mengidentifikasi Pola Keluhan dan Pujian: Menggunakan Natural Language Processing (NLP) dan Topic Modeling (LDA) untuk menemukan tema-tema utama yang dibicarakan pengguna.
3. Merumuskan Rekomendasi Strategis: Menyusun saran perbaikan produk yang berbasis data untuk tim produk, developer, dan customer support.

Metodologi Analisis
Analisis ini dilakukan melalui beberapa tahapan utama:
1. Data Gathering: Mengambil 5.000 ulasan terbaru dari Google Play Store menggunakan library google-play-scraper.
2. Data Preprocessing: Membersihkan teks ulasan melalui proses case folding, tokenizing, stopword removal (Sastrawi), stemming (Sastrawi), dan normalisasi kata tidak baku.
3. Analisis Sentimen: Memberi label sentimen (positif, netral, negatif) pada setiap ulasan berdasarkan skor rating yang diberikan pengguna.
4. Exploratory Data Analysis (EDA): Melakukan visualisasi data untuk memahami distribusi sentimen, tren ulasan dari waktu ke waktu, dan kata-kata yang paling sering muncul.
5. Topic Modeling: Menerapkan Latent Dirichlet Allocation (LDA) untuk mengekstrak 5 topik utama yang paling sering dibahas dalam ulasan.

Hasil Analisis & Visualisasi Utama
1. Distribusi Sentimen Pengguna
Distribusi menunjukkan bahwa meskipun ulasan positif mendominasi, jumlah ulasan negatif (rating 1-2) sangat signifikan. Ini mengindikasikan adanya masalah serius yang dihadapi oleh sebagian besar pengguna. Ulasan netral (rating 3) memiliki jumlah paling sedikit, menunjukkan polarisasi pengalaman pengguna.
2. Tren Ulasan per Bulan
Terdapat lonjakan jumlah ulasan pada periode tertentu, khususnya pada awal dan pertengahan tahun. Puncak tertinggi terjadi pada November 2022. Lonjakan ini seringkali berkorelasi dengan rilis pembaruan aplikasi, promosi, atau terjadinya gangguan layanan massal.
3. Word Cloud Berdasarkan Sentimen
Word cloud secara visual merangkum kata kunci utama untuk setiap sentimen.
4. Sentimen Positif	Sentimen Negatif
Kata Kunci: bagus, bantu, mudah, mantap, lancar. Menunjukkan kepuasan terhadap fungsi utama dan kemudahan penggunaan.	Kata Kunci: buka, error, update, cctv, rekam. Menyoroti masalah teknis fundamental seperti aplikasi crash, gagal login, dan masalah pada fungsi CCTV setelah pembaruan.
5. Analisis Topik dengan LDA
LDA berhasil mengidentifikasi 5 topik utama dari seluruh ulasan:
Topik 0: Masalah Akses & Stabilitas Aplikasi: Berisi keluhan aplikasi tidak bisa dibuka, error, dan crash. (Kata kunci: buka, bisa, error, login, masuk).
Topik 1: Kepuasan & Fungsi Bantuan: Berisi pujian dan apresiasi terhadap fungsi aplikasi. (Kata kunci: bagus, bantu, mudah, mantap, rumah).
Topik 2: Gangguan Fungsi CCTV & Rekaman: Fokus pada masalah spesifik terkait CCTV yang tidak bisa diakses atau gagal merekam. (Kata kunci: cctv, rekam, lihat, hasil, putar).
Topik 3: Masalah Setelah Pembaruan (Update): Keluhan yang muncul secara spesifik setelah pengguna memperbarui aplikasi. (Kata kunci: update, versi, baru, jelek, parah).
Topik 4: Kinerja & Kelancaran: Membahas performa umum aplikasi, termasuk kelambatan dan koneksi. (Kata kunci: lambat, jaring, koneksi, lama, mohon).

Teknologi & Library yang Digunakan
Bahasa: Python 
Library Utama: pandas & numpy
google-play-scraper: Pengambilan data ulasan
Sastrawi: Stopword removal dan stemming Bahasa Indonesia
scikit-learn: TF-IDF Vectorizer
gensim: Implementasi LDA (Latent Dirichlet Allocation)
matplotlib, seaborn, wordcloud: Visualisasi data

Cara Menjalankan
Clone repositori ini:
Generated bash
git clone https://github.com/rizkamars/IndiHome-Eazy.git
cd IndiHome-Eazy
