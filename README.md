# E-commerce-Sentiment-Analysis-Granite-AI
Analisis sentimen dan ekstraksi topik ulasan e-commerce menggunakan model fondasi IBM Granite. Proyek ini mengolah data teks tidak terstruktur menjadi wawasan bisnis yang dapat ditindaklanjuti.

# Analisis Sentimen dan Ekstraksi Topik Ulasan Produk E-commerce Menggunakan IBM Granite

## Gambaran Umum Proyek (Project Overview)
Proyek ini melakukan analisis sentimen dan ekstraksi topik dari ulasan pelanggan produk e-commerce. Dengan memanfaatkan kecerdasan buatan, khususnya model fondasi **IBM Granite** melalui Replicate API, kami mengolah data ulasan teks yang tidak terstruktur menjadi wawasan yang terstruktur dan dapat ditindaklanjuti. Tujuan utamanya adalah untuk mengidentifikasi sentimen pelanggan (positif, negatif, campuran) dan topik-topik utama yang dibahas, yang dapat digunakan untuk meningkatkan kualitas produk, layanan, dan strategi bisnis.

## Link Dataset Mentah (Raw Dataset Link)
Dataset yang digunakan dalam proyek ini adalah **"E-commerce Customer Reviews"** yang tersedia secara publik di Kaggle.
* **Link Dataset:** [https://www.kaggle.com/datasets/nicapotato/womens-ecommerce-clothing-reviews](https://www.kaggle.com/datasets/nicapotato/womens-ecommerce-clothing-reviews)

## Wawasan dan Temuan (Insight & Findings)
Berdasarkan analisis terhadap 100 sampel ulasan pelanggan, kami menemukan beberapa wawasan kunci:

* **Distribusi Sentimen**: [Deskripsikan distribusi sentimen dari grafik Anda. Contoh: "Sebagian besar ulasan (sekitar 70%) memiliki sentimen positif, menunjukkan kepuasan umum pelanggan. Sisanya terbagi antara sentimen negatif (15%) dan campuran (15%)."]
    [Sertakan gambar grafik distribusi sentimen Anda di sini]
    ![Distribusi Sentimen](images/distribusi_sentimen_keseluruhan.png)

* **Topik Paling Sering Dibahas**: [Sebutkan topik-topik teratas yang muncul dari grafik Anda. Contoh: "Topik yang paling sering dibahas meliputi 'Ukuran', 'Kualitas Bahan', 'Kesesuaian (Fit)', 'Gaya', dan 'Pengiriman'."]
    [Sertakan gambar grafik topik teratas Anda di sini]
    ![Topik Paling Sering Dibahas](images/topik.png)

* **Sentimen per Topik**: [Jelaskan sentimen positif/negatif untuk topik-topik kunci. Contoh: "Analisis lebih dalam menunjukkan bahwa topik 'Ukuran' dan 'Kesesuaian (Fit)' memiliki proporsi sentimen negatif yang tinggi, mengindikasikan area masalah. Sebaliknya, 'Kualitas Bahan' dan 'Gaya' didominasi oleh sentimen positif, menunjukkan kekuatan produk."]
    [Sertakan gambar grafik sentimen per topik Anda di sini]
    ![Sentimen per Topik](images/sentimen_per_topik.png)

## Penjelasan Dukungan AI (AI Support Explanation)
Proyek ini secara ekstensif menggunakan **IBM Granite 3.2-8b-instruct** sebagai model Large Language Model (LLM) utama. Model ini diakses melalui **Replicate API**.

* **Peran AI**: IBM Granite berfungsi sebagai inti analitis, mampu memahami konteks ulasan, mengklasifikasikan sentimen, dan mengekstrak entitas kunci (topik) tanpa memerlukan pelabelan data manual yang ekstensif atau pelatihan model kustom. Hal ini mempercepat proses analisis secara signifikan dan memungkinkan skala yang lebih besar.
* **Teknik Prompt Engineering**: Kami menggunakan *prompt* yang dirancang dengan cermat untuk memandu model agar menghasilkan output dalam format JSON yang terstruktur. Ini memastikan hasil yang konsisten dan mudah diproses secara otomatis.
* **Penanganan Tantangan AI**: Kami mengimplementasikan logika coba ulang (*retry logic*) dan jeda waktu (`time.sleep()`) untuk mengatasi batasan *rate limiting* dari API, serta penanganan kesalahan untuk output JSON yang tidak valid dari model. Ini memastikan proses analisis yang tangguh dan andal.
