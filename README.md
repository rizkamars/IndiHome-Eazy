Analisis Sentimen & Topic Modeling: Studi Kasus Aplikasi IndiHome Eazy

Repositori ini berisi analisis studi kasus untuk memahami sentimen dan topik utama dari ulasan pengguna aplikasi IndiHome Eazy di Google Play Store. Analisis ini bertujuan untuk mengubah ribuan ulasan kualitatif menjadi insight bisnis yang actionable, mengidentifikasi pain points pengguna, serta merumuskan rekomendasi strategis untuk peningkatan produk.

📍 Latar Belakang

Aplikasi IndiHome Eazy merupakan platform pengelola perangkat rumah pintar (khususnya CCTV) dari PT Telkom Indonesia. Seperti aplikasi lainnya, IndiHome Eazy menerima beragam ulasan di Google Play Store, mulai dari pujian hingga keluhan teknis. Studi ini menggunakan data ulasan tersebut untuk menggali wawasan mendalam mengenai pengalaman pengguna (UX) dan mengidentifikasi area perbaikan yang paling krusial.

🎯 Tujuan Analisis

Menganalisis Sentimen Pengguna: Mengklasifikasikan ulasan ke dalam kategori positif, netral, dan negatif untuk mengukur tingkat kepuasan secara umum.

Mengidentifikasi Pola Keluhan dan Pujian: Menggunakan Natural Language Processing (NLP) dan Topic Modeling (LDA) untuk menemukan tema-tema utama yang dibicarakan pengguna.

Merumuskan Rekomendasi Strategis: Menyusun saran perbaikan produk yang berbasis data untuk tim produk, developer, dan customer support.

🛠️ Metodologi Analisis

Analisis ini dilakukan melalui beberapa tahapan utama:

Data Gathering: Mengambil 5.000 ulasan terbaru dari Google Play Store menggunakan library google-play-scraper.

Data Preprocessing: Membersihkan teks ulasan melalui proses case folding, tokenizing, stopword removal (Sastrawi), stemming (Sastrawi), dan normalisasi kata tidak baku.

Analisis Sentimen: Memberi label sentimen (positif, netral, negatif) pada setiap ulasan berdasarkan skor rating yang diberikan pengguna.

Exploratory Data Analysis (EDA): Melakukan visualisasi data untuk memahami distribusi sentimen, tren ulasan dari waktu ke waktu, dan kata-kata yang paling sering muncul.

Topic Modeling: Menerapkan Latent Dirichlet Allocation (LDA) untuk mengekstrak 5 topik utama yang paling sering dibahas dalam ulasan.

📊 Hasil Analisis & Visualisasi Utama
1. Distribusi Sentimen Pengguna

Distribusi menunjukkan bahwa meskipun ulasan positif mendominasi, jumlah ulasan negatif (rating 1-2) sangat signifikan. Ini mengindikasikan adanya masalah serius yang dihadapi oleh sebagian besar pengguna. Ulasan netral (rating 3) memiliki jumlah paling sedikit, menunjukkan polarisasi pengalaman pengguna.

2. Tren Ulasan per Bulan

Terdapat lonjakan jumlah ulasan pada periode tertentu, khususnya pada awal dan pertengahan tahun. Puncak tertinggi terjadi pada November 2022. Lonjakan ini seringkali berkorelasi dengan rilis pembaruan aplikasi, promosi, atau terjadinya gangguan layanan massal.

3. Word Cloud Berdasarkan Sentimen

Word cloud secara visual merangkum kata kunci utama untuk setiap sentimen.

Sentimen Positif	Sentimen Negatif
Kata Kunci: bagus, bantu, mudah, mantap, lancar. <br><br> Menunjukkan kepuasan terhadap fungsi utama dan kemudahan penggunaan.	Kata Kunci: buka, error, update, cctv, rekam. <br><br> Menyoroti masalah teknis fundamental seperti aplikasi crash, gagal login, dan masalah pada fungsi CCTV setelah pembaruan.
4. Analisis Topik dengan LDA

LDA berhasil mengidentifikasi 5 topik utama dari seluruh ulasan:

Topik 0: Masalah Akses & Stabilitas Aplikasi

Berisi keluhan aplikasi tidak bisa dibuka, error, dan crash. (Kata kunci: buka, bisa, error, login, masuk).

Topik 1: Kepuasan & Fungsi Bantuan

Berisi pujian dan apresiasi terhadap fungsi aplikasi. (Kata kunci: bagus, bantu, mudah, mantap, rumah).

Topik 2: Gangguan Fungsi CCTV & Rekaman

Fokus pada masalah spesifik terkait CCTV yang tidak bisa diakses atau gagal merekam. (Kata kunci: cctv, rekam, lihat, hasil, putar).

Topik 3: Masalah Setelah Pembaruan (Update)

Keluhan yang muncul secara spesifik setelah pengguna memperbarui aplikasi. (Kata kunci: update, versi, baru, jelek, parah).

Topik 4: Kinerja & Kelancaran

Membahas performa umum aplikasi, termasuk kelambatan dan koneksi. (Kata kunci: lambat, jaring, koneksi, lama, mohon).

🧠 Insight Bisnis & Rekomendasi Strategis
Aspek Strategis	Insight Kunci dari Data	Rekomendasi Aksi
1. Prioritas Produk & QA	Keluhan paling fatal adalah aplikasi tidak bisa dibuka (crash, error), terutama setelah update.	Jadikan Stabilitas sebagai KPI #1. Lakukan regression testing yang ketat sebelum setiap rilis untuk memastikan fungsi inti (login, streaming CCTV) tidak terganggu.
2. Manajemen Rilis	Lonjakan ulasan negatif berkorelasi dengan jadwal update, menandakan pengguna kaget atau menemukan bug baru.	Terapkan Komunikasi Proaktif. Rilis changelog yang jelas di Play Store dan sertakan onboarding pop-up singkat di aplikasi untuk menjelaskan perubahan penting.
3. Manajemen Reputasi	Ulasan negatif yang tidak direspons memperburuk frustrasi dan merusak citra merek.	Alokasikan Tim Respons Cepat. Balas ulasan (terutama yang negatif) di Play Store dalam <24 jam. Tawarkan solusi atau eskalasi, tunjukkan bahwa feedback didengar.
4. Peningkatan Rating	Pengguna yang puas memuji kemudahan (mudah) dan manfaat (bantu) aplikasi.	Implementasikan In-App Rating Prompt Cerdas. Minta rating hanya setelah pengguna berhasil melakukan aksi positif (misal: berhasil melihat rekaman), bukan saat membuka aplikasi.
⚙️ Teknologi & Library yang Digunakan

Bahasa: Python

Library Utama:

pandas & numpy: Manipulasi dan analisis data.

google-play-scraper: Pengambilan data ulasan dari Google Play Store.

Sastrawi: Stopword removal dan stemming untuk Bahasa Indonesia.

scikit-learn: TF-IDF Vectorizer.

gensim: Implementasi LDA (Latent Dirichlet Allocation).

matplotlib, seaborn, wordcloud: Visualisasi data.

🚀 Cara Menjalankan
1. Prasyarat

Python 3.8+

Jupyter Notebook / Jupyter Lab

2. Instalasi

Clone repositori ini ke mesin lokal Anda.

Generated bash
git clone https://github.com/rizkamars/IndiHome-Eazy.git
cd IndiHome-Eazy


Instal semua dependensi yang diperlukan. Direkomendasikan menggunakan virtual environment.

Generated bash
pip install -r requirements.txt
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
Bash
IGNORE_WHEN_COPYING_END

(Catatan: Pastikan Anda telah membuat file requirements.txt di repositori Anda)

3. Eksekusi

Buka dan jalankan notebook IndiHome_Eazy_Analysis.ipynb di Jupyter.

Generated bash
jupyter notebook IndiHome_Eazy_Analysis.ipynb
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
Bash
IGNORE_WHEN_COPYING_END
