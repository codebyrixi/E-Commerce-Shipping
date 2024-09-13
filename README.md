# Final Project - E-Commerce Shipping
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
