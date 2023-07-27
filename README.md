# AlphaGroup_JC_DS_FT_Batam_2_FinalProject
# Hotel Booking Demand
---
![Image](https://cf.bstatic.com/xdata/images/hotel/max1280x900/451160074.jpg?k=9370b6a1c98ecb5b5dea7c3eb1b8b59365b28af4617df57a57fd9f08b22aa084&o=&hp=1)
Data Scource: [kaggle](https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand/code?datasetId=511638&sortBy=voteCount) 
## Created By : 
-   Irfan Ardiana
-   Reza Purnama Adi
-   Muhammad Vito Nurhayat

# Context 
---
__One Hotel__ adalah perusahaan hotel berbasis di Portugal dengan lokasi di kota Lisbon dan area resort Algarve. Seperti banyak hotel lain di industri perhotelan, mereka menghadapi tantangan meningkatnya pembatalan reservasi hotel. Seperti yang disebutkan dalam artikel [Consumers vs. Revenue Managers: The Case of Cancellations and No-Shows](https://www.bu.edu/bhr/2021/06/29/consumers-vs-revenue-managers-the-case-of-cancelations-and-no-shows/), peningkatan pembatalan ini memiliki dampak buruk pada praktik manajemen keuangan dan menyebabkan kerugian yang signifikan.

Pada industri perhotelan, manajemen hotel sangat bergantung pada jumlah pemesanan dan tingkat pembatalan pemesanan untuk mengoptimalkan operasi mereka. Tingkat pembatalan pemesanan hotel dapat memiliki dampak signifikan pada pendapatan dan ketersediaan kamar. Oleh karena itu, memiliki pemahaman yang baik tentang faktor-faktor yang mempengaruhi pembatalan pemesanan dapat membantu manajemen hotel untuk mengambil langkah-langkah yang tepat guna mengurangi dampak negatifnya. __One Hotel__ perlu mempertimbangkan implikasi dari meningkatnya pembatalan dan perlunya menemukan keseimbangan antara memberikan fleksibilitas kepada tamu dan melindungi keuangan hotel, oleh karenanya __One Hotel__ perlu untuk memanfaatkan tools yang dapat digunakan untuk menganalisis data dan melakukan prediksi terhadap customer yangh terindikasi membatalkan pemesanan. Dengan pembuatan model prediksi pembatalan pemesanan hotel adalah untuk mengembangkan algoritma atau model machine learning yang dapat memprediksi kemungkinan pembatalan pemesanan berdasarkan fitur-fitur yang ada dalam dataset. Model ini dapat memberikan wawasan berharga kepada manajemen hotel tentang perilaku pelanggan dan faktor-faktor apa saja yang berkontribusi pada tingkat pembatalan yang tinggi.

Dengan adanya model prediksi ini, manajemen hotel dapat mengambil langkah-langkah strategis untuk mengatasi masalah pembatalan pemesanan, seperti menawarkan insentif kepada pelanggan yang cenderung membatalkan, meningkatkan kebijakan pembatalan, atau mengoptimalkan strategi harga dan promosi. Selain itu, model ini juga dapat membantu manajemen hotel dalam perencanaan ketersediaan kamar, penjadwalan staf, dan manajemen sumber daya lainnya.

# Problem Statement
---
Dalam industri perhotelan yang kompetitif, salah satu tantangan utama yang dihadapi oleh One Hotel adalah bagaimana mengelola pembatalan pemesanan secara efektif untuk mengurangi dampak negatifnya terhadap pendapatan. Menangani pembatalan dengan tepat dapat membantu mengoptimalkan ketersediaan kamar, meningkatkan pemanfaatan sumber daya, dan menghadirkan strategi pemasaran serta penetapan harga yang lebih efisien. Oleh karena itu, pernyataan masalah yang menjadi fokus hotel adalah: __Bagaimana One Hotel dapat mengelola pembatalan pemesanan dengan efektif sehingga dapat memaksimalkan potensial revenue?__

# Goals
---
Berdasarkan pernyataan masalah, __One Hotel perlu mengembangkan alat prediksi yang dapat memprediksi pembatalan dan mengidentifikasi faktor-faktor utama yang mempengaruhi keputusan untuk membatalkan__. Alat ini dapat menggunakan data historis, seperti pola pemesanan, demografi tamu, dan informasi kanal pemesanan, untuk menganalisis dan mengidentifikasi pola dan tren yang terkait dengan pembatalan. Dengan menggunakan data analitik dan algoritma pembelajaran mesin, alat ini akan dapat melakukan analisis mendalam dan mengidentifikasi pola dan tren yang berarti terkait dengan pembatalan. Dengan wawasan berharga ini, One Hotel dapat mengimplementasikan strategi proaktif, mengalokasikan sumber daya dengan bijaksana, dan menyesuaikan pendekatan pemasaran untuk mengelola pembatalan secara efektif dan mengoptimalkan inventaris kamar. Pada akhirnya, alat prediksi ini akan memberdayakan One Hotel untuk mencapai keseimbangan antara fleksibilitas tamu dan stabilitas keuangan, sambil memastikan kepuasan pelanggan yang tinggi dan memaksimalkan potensi pendapatan.

# Analytic Approach
---
Untuk mencapai tujuan akan dilakukan dengan pendekatan dua tahapan. Pertama yaitu dengan menganalisis data untuk mengetahui pola atau tren dari setiap fitur terhadap cancellations rate dan juga korelasinya agar dapat diketahui fitur mana yang terindikasi membuat customer cenderung untuk membatalkan pemesanan. Setelahnya akan dibangun model klasifikasi yang akan membantu hotel dalam memprediksi customer yang terindikasi membatalkan booking hotel sehingga dapat dilakukan strategi penanganan lebih lanjut. 

### Metric Evaluation
---
Type 1 error    : False Positive  
Kondisi         : Model memprediksi customer membatalkan booking hotel namun aktualnya lanjut.
Konsekuensi     : Hotel akan membuang waktu dan biaya untuk menangani hal yang tidak perlu ditangani.

Type 2 error    : False Negative  
Kondisi         : Model memprediksi customer melanjutkan booking hotel namun aktualnya membatalkan.
Konsekuensi     : Hotel akan kehilangan potensial revenue.


# Conlusion & Recommendation
---

### Kesimpulan

Berdasarkan analisa dan pengembangan model yang telah dilakukan, didapatkan sebuah model prediktif yang mampu mengidentifikasi pelanggan yang berpotensi membatalkan pemesanan yang terbilang baik. Model yang didapat menggunakan algortima Catboost dengan RUS sebagai teknik resampling terbaik dan juga dilakukan hyperparameter tuning untuk mendapatkan nilai metriks evaluasi yang maksimal. Model yang didapat memiliki score Recall 89.36%, yang artinya model mampu mengidentifikasi dan menangkap data yang terindikasi pembatalan pemesanan dengan baik sesuai dengan tujuan penelitian dan pengembangan yang dilakukan. Dengan model yang baik ini dapat dimanfaatkan oleh hotel untuk meminimalkan pembatalan sehingga dapat memaksimalkan revenue. Peningkatan potensial revenue yang akan didapat dengan memanfaatkan model digambarkan sebagai berikut.

Dalam konteks ini, dengan fokus tujuan yaitu menangani pelanggan yang terindikasi membatalkan, hotel perlu mengembangkan model yang dapat mengurangi Type 2 error (False Negative). Type 2 error terjadi ketika model memprediksi bahwa pelanggan akan melanjutkan booking hotel, tetapi sebenarnya mereka membatalkannya. Konsekuensinya adalah hotel akan kehilangan potensial pendapatan.

Untuk mengatasi masalah ini, hotel harus memprioritaskan `Recall` sebagai metrik utama. `Recall` mengukur kemampuan model dalam mengidentifikasi sebagian besar kasus positif yang sebenarnya. Dalam hal ini, recall akan mengukur seberapa baik model dapat mengenali pelanggan yang sebenarnya akan membatalkan. Dengan meningkatkan `Recall`, hotel dapat mengurangi jumlah False Negative, sehingga dapat mengidentifikasi lebih banyak pelanggan yang berpotensi membatalkan dan mengambil langkah-langkah yang diperlukan untuk mempertahankan mereka.

### Rekomendasi Bisnis:

- Personalisasi Layanan: Manfaatkan informasi yang diberikan oleh model untuk melakukan personalisasi layanan kepada pelanggan yang berpotensi membatalkan pemesanan. Dengan pemahaman yang lebih baik tentang preferensi dan kebutuhan pelanggan, hotel dapat mengambil langkah-langkah proaktif untuk meningkatkan pengalaman pelanggan dan mengurangi kemungkinan pembatalan.

- Penawaran dan Diskon: Gunakan model untuk mengidentifikasi segmen pelanggan tertentu yang cenderung membatalkan pesanan mereka. Selanjutnya, tawarkan penawaran khusus dan diskon untuk segmentasi ini guna mendorong mereka untuk tetap mempertahankan pemesanan mereka. Diskon khusus dapat meningkatkan keterikatan pelanggan dan mendorong mereka untuk kembali menggunakan layanan hotel.

- Peningkatan Komunikasi: Model dapat membantu dalam menentukan pelanggan mana yang perlu mendapatkan komunikasi lebih lanjut dan lebih efektif untuk mencegah pembatalan. Hotel harus berfokus pada pemberian informasi yang relevan, mengingatkan pelanggan tentang pemesanan mereka, dan menawarkan bantuan jika diperlukan. Pendekatan ini akan memberikan kesan bahwa hotel sangat peduli terhadap kepuasan pelanggan.

- Analisis Pemasaran dan Strategi Harga: Manfaatkan wawasan dari model untuk menilai efektivitas kampanye pemasaran dan strategi harga saat ini. Dengan pemahaman yang lebih baik tentang perilaku pelanggan yang berpotensi membatalkan, hotel dapat mengoptimalkan strategi pemasaran dan harga untuk menciptakan loyalitas pelanggan dan meningkatkan konversi.

- Peningkatan Kualitas Layanan: Evaluasi alasan di balik pembatalan pesanan dan gunakan informasi tersebut untuk meningkatkan kualitas layanan hotel. Dengan mengatasi masalah yang mungkin memicu pembatalan, hotel dapat meningkatkan reputasi dan kepercayaan pelanggan.

- Pelatihan Karyawan: Edukasi dan pelatihan karyawan, terutama yang berhubungan langsung dengan pelanggan, sangat penting. Karyawan yang terlatih dengan baik dapat lebih peka terhadap tanda-tanda pelanggan yang cenderung membatalkan dan dapat mengambil langkah-langkah proaktif untuk mengatasi masalah sebelum mencapai titik pembatalan.

Melalui implementasi strategi di atas dengan memanfaatkan model yang telah dibuat, hotel dapat meminimalkan angka pembatalan pesanan, meningkatkan retensi pelanggan, dan akhirnya meningkatkan keuntungan serta reputasi hotel.
