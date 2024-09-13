# Final Project - _E-Commerce Shipping_
Project ini merupakan project akhir dari bootcamp saya di Rakamin Academy Batch 42. Project ini dinobatkan sebagai Runner Up Best Final Project Batch 42.

## Daftar Isi
- Overview
- EDA (_Exploratory Data Analysis_) dan Insight
- Data Pre-Processing
- Data Modelling
- Result and Reccomendation

## Bagian 0: Fun Facts

Dilansir dari situs iPrice.com, para konsumen di Indonesia harus menunggu hingga 3.8 hari untuk menerima paket tersebut disaat Thailand hanya menunggu 2.5 hari untuk paket mereka.
![image](https://github.com/user-attachments/assets/b351c222-c2c2-4e12-99cf-6d4c0f8740dc)<br>
Hal inilah yang menyebabkan >90% konsumen di Indonesia memberikan keluhan dikarenakan paket mereka terlambat untuk diterima
![image](https://github.com/user-attachments/assets/687cc646-3070-4d2d-b573-a5276c3969f4)

## Bagian 1: Overview

### Problem Statement
Memastikan ketepatan waktu pengiriman produk sangat penting untuk menjaga kepuasan dan loyalitas pelanggan. Namun, saat ini, persentase pengiriman barang yang tepat waktu sangat rendah, hanya mencapai 40%. Hal ini menunjukkan bahwa perusahaan belum memiliki metode yang efektif untuk memprediksi dan mencegah keterlambatan dalam pengiriman. Akibatnya, kinerja pengiriman yang rendah terus berlanjut dan dapat memengaruhi kepuasan pelanggan serta reputasi perusahaan.<br>
![image](https://github.com/user-attachments/assets/c565e135-175a-4350-b04c-c5d71d0cfac1)<br>
Dapat dilihat pada grafik berikut bahwa tersapat lebih banyak paket dengan status _Late (1)_ (bar sebelah kanan) dibandingkan dengan paket yang berstatus _On Time (0)_ (bar sebelah kiri). Kembali lagi, Hal ini menunjukkan bahwa perusahaan belum memiliki metode yang efektif untuk memprediksi dan mencegah keterlambatan dalam pengiriman. Akibatnya, kinerja pengiriman yang rendah terus berlanjut dan dapat memengaruhi kepuasan pelanggan serta reputasi perusahaan.

### Goal and Objectives
#### Goal
Tujuan utama dari penelitian ini adalah untuk meningkatkan persentase ketepatan waktu pengiriman produk. Ketepatan waktu dalam pengiriman merupakan faktor krusial dalam menjaga kepuasan pelanggan dan memastikan kelancaran operasional perusahaan. Dengan memperbaiki ketepatan waktu pengiriman, diharapkan perusahaan dapat meminimalkan keterlambatan yang terjadi serta mengoptimalkan proses logistik secara keseluruhan. Penelitian ini akan mengidentifikasi faktor-faktor penyebab keterlambatan, mengembangkan metode prediktif yang efektif, serta memberikan rekomendasi strategis yang dapat membantu perusahaan meningkatkan efisiensi dan kualitas layanan pengiriman produknya.
#### Objectives
Penelitian ini memiliki tiga tujuan utama yang saling berkaitan untuk meningkatkan ketepatan waktu pengiriman produk, yaitu sebagai berikut.
1. Penelitian ini bertujuan untuk mengidentifikasi faktor-faktor yang mempengaruhi keterlambatan pengiriman produk. Dengan memahami variabel-variabel yang memengaruhi keterlambatan, seperti kondisi cuaca, lokasi pengiriman, atau efisiensi logistik, perusahaan dapat memperoleh wawasan yang lebih dalam tentang penyebab utama dari masalah keterlambatan tersebut.
2. Penelitian ini akan membangun model machine learning yang bertujuan untuk memprediksi apakah sebuah produk akan terdeliver tepat waktu atau tidak. Model ini akan dikembangkan berdasarkan data historis pengiriman dan berbagai faktor yang telah diidentifikasi, sehingga perusahaan dapat memprediksi kemungkinan keterlambatan pengiriman dengan lebih akurat dan dapat mengantisipasinya sebelum terjadi.
3. Berdasarkan hasil analisis data pengiriman dan prediksi dari model machine learning, penelitian ini akan merekomendasikan solusi yang praktis dan efektif untuk mengatasi masalah keterlambatan pengiriman. Solusi ini akan berlandaskan pada wawasan bisnis (_business insight_) yang diperoleh dari analisis data, dan diharapkan dapat membantu perusahaan dalam merancang strategi yang lebih baik untuk meningkatkan efisiensi operasional serta ketepatan waktu pengiriman produk.

### Data Overview
Dataset ini berjumlah 10999 data, dengan terbagi kedalam lima kategori berbeda, tiga mode pengiriman berbeda, serta dua kategori ketepatan pengiriman. Selengkapnya dapat dilihat pada bagan dibawah ini. <br>
![image](https://github.com/user-attachments/assets/dd3e55c5-792d-45f1-8416-70d889889a2c)

## Bagian 2: EDA (_Exploratory Data Analysis_) dan Insight

### Hubungan Antara Keterlambatan Pengiriman dengan Diskon
![image](https://github.com/user-attachments/assets/8f0e75e3-0fa2-4ecd-a81e-ccbb6b6ca313)
Pemberian diskon ternyata memiliki pengaruh signifikan terhadap ketepatan waktu pengiriman. Berdasarkan analisis data, produk-produk yang dibeli dengan diskon lebih dari 10% cenderung mengalami keterlambatan dalam pengiriman. Hal ini dapat disebabkan oleh beberapa faktor, seperti lonjakan permintaan yang tidak diimbangi dengan kapasitas logistik yang memadai atau penurunan prioritas pengiriman untuk produk dengan harga diskon. Kondisi ini menunjukkan adanya hubungan antara besarnya diskon dan penurunan efisiensi dalam proses pengiriman, yang pada akhirnya dapat memengaruhi kepuasan pelanggan. Dengan demikian, perusahaan perlu mempertimbangkan strategi yang tepat untuk menjaga keseimbangan antara penawaran diskon dan kemampuan untuk memastikan pengiriman tetap berjalan tepat waktu.
Solusi yang dapat diusulkan untuk menjaga kepuasan pelanggan mencakup beberapa langkah strategis sebagai berikut:
1. Untuk memberikan transparansi kepada pelanggan, e-commerce dapat menyediakan informasi yang jelas sejak awal proses pembelian, terutama pada saat pelanggan memilih kurir pengiriman. Informasi ini dapat berupa pemberitahuan bahwa produk yang mendapatkan diskon besar lebih berpotensi mengalami keterlambatan pengiriman. Dengan memberikan informasi ini secara proaktif, pelanggan dapat memiliki ekspektasi yang lebih realistis terkait waktu pengiriman, sehingga mengurangi potensi ketidakpuasan akibat keterlambatan.
2. Menambahkan estimasi waktu pengiriman yang lebih akurat dan spesifik juga merupakan solusi yang penting. E-commerce dapat menyesuaikan estimasi ini berdasarkan faktor-faktor seperti besarnya diskon, volume pemesanan, dan kapasitas pengiriman dari mitra logistik. Dengan memperbarui estimasi waktu secara real-time, pelanggan akan mendapatkan gambaran yang lebih tepat mengenai kapan barang mereka akan tiba, sehingga memungkinkan mereka untuk mengambil keputusan pembelian dengan informasi yang lebih lengkap. Solusi ini tidak hanya meningkatkan transparansi, tetapi juga memperkuat hubungan antara perusahaan dan pelanggan melalui komunikasi yang lebih jujur dan terbuka.

### Hubungan Antara Keterlambatan Pengiriman dengan Berat Paket
![image](https://github.com/user-attachments/assets/b60b6e09-4a03-4676-afc3-570fb215bba4)
Berat paket terbukti memiliki pengaruh yang signifikan terhadap keterlambatan pengiriman. Berdasarkan analisis data pengiriman, paket dengan berat antara 2000 hingga 4000 gram, serta paket yang beratnya melebihi 6000 gram, hampir semuanya mengalami keterlambatan. Faktor ini kemungkinan disebabkan oleh tantangan logistik dalam menangani paket-paket dengan bobot lebih besar, yang memerlukan penanganan khusus atau kapasitas pengangkutan yang lebih besar. Keterlambatan tersebut mungkin juga diakibatkan oleh proses distribusi yang lebih lambat, karena kurir atau jasa pengiriman mungkin memprioritaskan paket yang lebih ringan dan lebih mudah diproses.
Solusi yang dapat diusulkan untuk menjaga kepuasan pelanggan mencakup beberapa langkah strategis sebagai berikut:
1. Pihak e-commerce dapat memberikan notifikasi di awal proses pembelian terkait potensi keterlambatan pengiriman pada paket dengan berat antara 2-4 kg dan lebih dari 6 kg. Notifikasi ini akan membantu pelanggan memahami bahwa produk dengan berat tersebut memiliki risiko keterlambatan yang lebih tinggi, sehingga mereka dapat membuat keputusan yang lebih tepat terkait pengiriman.
2. Pihak e-commerce pun dapat menambahkan estimasi waktu pengiriman yang disesuaikan dengan berat paket. Estimasi ini bisa mencakup tambahan waktu pengiriman untuk paket-paket yang lebih berat, yang disesuaikan dengan kemampuan dan kapasitas mitra logistik. Dengan transparansi yang lebih baik mengenai waktu pengiriman, pelanggan akan memiliki ekspektasi yang lebih akurat dan tidak terkejut jika terjadi keterlambatan, sehingga dapat mengurangi potensi keluhan dan meningkatkan kepercayaan pelanggan terhadap layanan e-commerce.

### Persentase Pengiriman Pesanan Tepat Waktu dan Terlambat oleh _Warehouse_ dan Biaya
![image](https://github.com/user-attachments/assets/f6936c50-6f86-4506-8f5a-70af12d1bd1f)

