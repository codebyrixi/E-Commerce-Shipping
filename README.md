# Final Project - _E-Commerce Shipping_
Project ini merupakan project akhir dari bootcamp saya di Rakamin Academy Batch 42. Project ini dinobatkan sebagai Runner Up Best Final Project Batch 42.

## Daftar Isi
- Overview
- EDA (_Exploratory Data Analysis_) dan Insight
- Data Pre-Processing
- _Feature Engineering_
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
Pemberian diskon ternyata memiliki pengaruh signifikan terhadap ketepatan waktu pengiriman. Berdasarkan analisis data, produk-produk yang dibeli dengan diskon lebih dari 10% cenderung mengalami keterlambatan dalam pengiriman. Hal ini dapat disebabkan oleh beberapa faktor, seperti lonjakan permintaan yang tidak diimbangi dengan kapasitas logistik yang memadai atau penurunan prioritas pengiriman untuk produk dengan harga diskon. Kondisi ini menunjukkan adanya hubungan antara besarnya diskon dan penurunan efisiensi dalam proses pengiriman, yang pada akhirnya dapat memengaruhi kepuasan pelanggan. Dengan demikian, perusahaan perlu mempertimbangkan strategi yang tepat untuk menjaga keseimbangan antara penawaran diskon dan kemampuan untuk memastikan pengiriman tetap berjalan tepat waktu.<br>
Solusi yang dapat diusulkan untuk menjaga kepuasan pelanggan mencakup beberapa langkah strategis sebagai berikut:
1. Untuk memberikan transparansi kepada pelanggan, e-commerce dapat menyediakan informasi yang jelas sejak awal proses pembelian, terutama pada saat pelanggan memilih kurir pengiriman. Informasi ini dapat berupa pemberitahuan bahwa produk yang mendapatkan diskon besar lebih berpotensi mengalami keterlambatan pengiriman. Dengan memberikan informasi ini secara proaktif, pelanggan dapat memiliki ekspektasi yang lebih realistis terkait waktu pengiriman, sehingga mengurangi potensi ketidakpuasan akibat keterlambatan.
2. Menambahkan estimasi waktu pengiriman yang lebih akurat dan spesifik juga merupakan solusi yang penting. E-commerce dapat menyesuaikan estimasi ini berdasarkan faktor-faktor seperti besarnya diskon, volume pemesanan, dan kapasitas pengiriman dari mitra logistik. Dengan memperbarui estimasi waktu secara real-time, pelanggan akan mendapatkan gambaran yang lebih tepat mengenai kapan barang mereka akan tiba, sehingga memungkinkan mereka untuk mengambil keputusan pembelian dengan informasi yang lebih lengkap. Solusi ini tidak hanya meningkatkan transparansi, tetapi juga memperkuat hubungan antara perusahaan dan pelanggan melalui komunikasi yang lebih jujur dan terbuka.

### Hubungan Antara Keterlambatan Pengiriman dengan Berat Paket
![image](https://github.com/user-attachments/assets/b60b6e09-4a03-4676-afc3-570fb215bba4)
Berat paket terbukti memiliki pengaruh yang signifikan terhadap keterlambatan pengiriman. Berdasarkan analisis data pengiriman, paket dengan berat antara 2000 hingga 4000 gram, serta paket yang beratnya melebihi 6000 gram, hampir semuanya mengalami keterlambatan. Faktor ini kemungkinan disebabkan oleh tantangan logistik dalam menangani paket-paket dengan bobot lebih besar, yang memerlukan penanganan khusus atau kapasitas pengangkutan yang lebih besar. Keterlambatan tersebut mungkin juga diakibatkan oleh proses distribusi yang lebih lambat, karena kurir atau jasa pengiriman mungkin memprioritaskan paket yang lebih ringan dan lebih mudah diproses.<br>
Solusi yang dapat diusulkan untuk menjaga kepuasan pelanggan mencakup beberapa langkah strategis sebagai berikut:
1. Pihak e-commerce dapat memberikan notifikasi di awal proses pembelian terkait potensi keterlambatan pengiriman pada paket dengan berat antara 2-4 kg dan lebih dari 6 kg. Notifikasi ini akan membantu pelanggan memahami bahwa produk dengan berat tersebut memiliki risiko keterlambatan yang lebih tinggi, sehingga mereka dapat membuat keputusan yang lebih tepat terkait pengiriman.
2. Pihak e-commerce pun dapat menambahkan estimasi waktu pengiriman yang disesuaikan dengan berat paket. Estimasi ini bisa mencakup tambahan waktu pengiriman untuk paket-paket yang lebih berat, yang disesuaikan dengan kemampuan dan kapasitas mitra logistik. Dengan transparansi yang lebih baik mengenai waktu pengiriman, pelanggan akan memiliki ekspektasi yang lebih akurat dan tidak terkejut jika terjadi keterlambatan, sehingga dapat mengurangi potensi keluhan dan meningkatkan kepercayaan pelanggan terhadap layanan e-commerce.

### Persentase Pengiriman Pesanan Tepat Waktu dan Terlambat oleh _Warehouse_ dan Biaya
![image](https://github.com/user-attachments/assets/f6936c50-6f86-4506-8f5a-70af12d1bd1f)
Warehouse B dan F menunjukkan ketepatan waktu pengiriman sekitar 50% untuk barang dengan harga murah (51-100), mengindikasikan performa yang kurang optimal dalam menangani produk dengan nilai lebih rendah. Sebaliknya, Warehouse A, D, dan F memiliki persentase ketepatan waktu yang lebih tinggi, melebihi 57%, untuk pengiriman barang dengan harga lebih mahal (301-350). Perbedaan ini menunjukkan bahwa beberapa warehouse lebih efisien dalam menangani produk bernilai tinggi, mungkin karena prioritas yang diberikan terhadap barang yang lebih mahal atau alokasi sumber daya yang lebih baik untuk memastikan ketepatan pengiriman pada produk bernilai tinggi. Namun, ini juga membuka peluang untuk meningkatkan performa pengiriman pada barang murah agar tetap kompetitif dan menjaga kepuasan pelanggan.<br>
Solusi yang dapat diusulkan untuk menjaga kepuasan pelanggan mencakup beberapa langkah strategis sebagai berikut:
1. Untuk barang dengan harga dalam rentang 51-100, disarankan agar penanganan pengiriman dilakukan oleh Warehouse B dan F. Kedua warehouse ini memiliki pengalaman dan efisiensi yang lebih cocok dalam menangani produk dengan harga lebih rendah, meskipun ketepatan waktu pengiriman perlu ditingkatkan, mereka masih berada pada level yang memadai untuk kategori ini.
2. Untuk barang yang cenderung lebih mahal, dengan harga dalam kisaran 301-350, disarankan agar pengiriman dikelola oleh Warehouse A, D, dan F. Ketiga warehouse ini telah menunjukkan performa yang lebih unggul dalam hal ketepatan waktu pengiriman untuk produk bernilai tinggi, yang dapat memberikan pelayanan lebih baik serta meminimalkan risiko keterlambatan pengiriman bagi barang mahal.

## Bagian 3: Data Pre-Processing
Selanjutnya adalah tahapan pre-processing data, yang terdiri dari tahapan-tahapan sebagai berikut.

### Menangani Missing Value
   <br>Pada tahap ini, dilakukan pengecekan terhadap data untuk mengidentifikasi apakah terdapat missing value atau nilai yang hilang. Setelah dilakukan pemeriksaan menyeluruh, ditemukan bahwa tidak ada missing value dalam dataset, sehingga data dapat langsung digunakan tanpa perlu proses imputasi atau penghapusan nilai kosong.
   
### Menangani Data Duplikat
   <br>Langkah selanjutnya adalah memeriksa adanya data duplikat dalam dataset. Data duplikat dapat menyebabkan distorsi dalam hasil analisis. Setelah proses pengecekan, tidak ditemukan data yang duplikat, sehingga tidak diperlukan tindakan lebih lanjut terkait penghapusan atau penggabungan entri data.
   
### Menangani Nilai Invalid
   <br>Pada tahap ini, data diperiksa untuk mendeteksi adanya nilai invalid, seperti format yang tidak sesuai, nilai di luar rentang yang diharapkan, atau data yang salah input. Setelah pengecekan, tidak ditemukan nilai invalid dalam dataset, sehingga semua data yang ada dinyatakan valid dan dapat digunakan untuk analisis lebih lanjut.
   
### Menangani Outlier
![image](https://github.com/user-attachments/assets/b4a0035a-05ec-4131-b83f-f82cac3fdab4)
   Pada tahap ini, outlier diidentifikasi menggunakan metode filtering z-score, di mana nilai absolut lebih besar dari 3 dianggap sebagai outlier. Proses ini dilakukan untuk memastikan bahwa data yang terlalu ekstrem tidak memengaruhi hasil analisis. Sebelum memfilter outlier, dataset memiliki 10.999 baris, dan setelah proses penyaringan, jumlah baris berkurang menjadi 10.642.<br>
   Selanjutnya, dilakukan perbandingan distribusi nilai pada kolom 'Late' sebelum dan sesudah filter outlier. Distribusi awal untuk kolom 'Late' menunjukkan bahwa 59,67% data bernilai 'Yes' (pengiriman terlambat) dan 40,33% bernilai 'No' (pengiriman tepat waktu). Setelah outlier dihapus, distribusi berubah sedikit menjadi 59,03% 'Yes' dan 40,97% 'No'. Perubahan persentase ini masih tergolong aman dan tidak memengaruhi keseimbangan distribusi secara signifikan. Oleh karena itu, dipertimbangkan untuk tetap mempertahankan outlier yang ada, karena tidak memberikan dampak besar terhadap analisis.

## Bagian 4: _Feature Engineering_
Selanjutnya adalah tahapan _feature engineering_, yang terdiri dari tahapan-tahapan sebagai berikut.

### _Feature Transformation_
   Pada tahap ini, kolom numerik dalam dataset dinormalisasi menggunakan teknik MinMaxScaler. Normalisasi ini bertujuan untuk mengubah nilai-nilai numerik sehingga berada dalam rentang 0 hingga 1, tanpa mengubah distribusi data asli. MinMaxScaler bekerja dengan menggeser dan menskalakan nilai setiap kolom berdasarkan minimum dan maksimum yang ada, sehingga fitur yang memiliki rentang nilai yang berbeda-beda dapat dibandingkan secara adil dan tidak mendominasi fitur lain dalam model analisis.<br>
   ![image](https://github.com/user-attachments/assets/d32ba1e6-89fd-4f14-9133-4bb33ce1a7bd)

### _Feature Encoding_
![image](https://github.com/user-attachments/assets/18455025-338b-4a81-bd9b-54265aadd487)
   Pada tahap ini, dilakukan **feature encoding** pada kolom-kolom kategori agar dapat digunakan dalam analisis atau model machine learning. Proses encoding ini bertujuan untuk mengubah data kategori menjadi format numerik yang dapat dipahami oleh algoritma.<br>
   - **Kolom 'Importance'**<br>
     Kolom ini mewakili kategori ordinal, di mana terdapat tingkatan atau urutan tertentu antar kategori. Oleh karena itu, diterapkan **Label Encoding** pada kolom ini. Label Encoding akan mengubah setiap kategori menjadi nilai numerik sesuai dengan tingkatannya, misalnya "Low" menjadi 0, "Medium" menjadi 1, dan "High" menjadi 2. Teknik ini cocok digunakan karena pentingnya urutan antar kategori yang mewakili prioritas atau level tertentu.
   - **Kolom 'Shipment' dan 'Warehouse'**<br>
     Kolom-kolom ini mewakili kategori nominal, di mana setiap kategori tidak memiliki urutan tertentu. Oleh karena itu, digunakan **One-Hot Encoding**. One-Hot Encoding akan mengonversi setiap kategori dalam kolom 'Shipment' dan 'Warehouse' menjadi kolom baru yang mewakili kategori tersebut dengan nilai biner (0 atau 1). Dengan metode ini, setiap kategori diperlakukan secara independen, tanpa mempengaruhi hubungan antar kategori lain. Hal ini penting agar model tidak salah menafsirkan bahwa ada hubungan hierarki di antara kategori yang seharusnya tidak ada.

### _Feature Selection_
   Pada tahap ini, dilakukan proses pemilihan fitur (feature selection) untuk menghapus fitur yang dianggap tidak relevan atau tidak memberikan kontribusi signifikan terhadap proses modeling. Fitur-fitur yang dihapus antara lain:
- ID: Fitur ini merupakan identifikasi unik untuk setiap entri, namun tidak memiliki hubungan langsung dengan variabel target dan tidak memberikan informasi yang berguna untuk prediksi.
- Gender: Setelah dianalisis, fitur 'Gender' tidak menunjukkan pengaruh yang signifikan terhadap ketepatan waktu pengiriman produk dan dianggap tidak relevan dalam konteks analisis ini.
- Rating: Meskipun 'Rating' mungkin berguna dalam konteks lain, dalam kasus ini fitur ini tidak memiliki pengaruh terhadap variabel yang sedang diprediksi, yaitu ketepatan waktu pengiriman. Oleh karena itu, fitur ini juga dihapus.

### _Feature Extraction_
Pada tahap ini, dilakukan proses ekstraksi fitur (feature extraction) untuk menambahkan informasi baru yang relevan ke dalam dataset. Fitur yang diekstraksi adalah Reorder_purchases, berdasarkan jumlah pembelian sebelumnya. Fitur ini memberikan informasi tambahan tentang perilaku pelanggan, khususnya apakah mereka termasuk pelanggan yang sering melakukan pembelian ulang. Data ini berguna dalam analisis untuk melihat apakah ada hubungan antara kebiasaan pelanggan melakukan reorder dan ketepatan waktu pengiriman.
- Jika jumlah pembelian sebelumnya (prior purchases) >= 3, maka dikategorikan sebagai Yes dengan nilai 1. Ini menunjukkan bahwa pelanggan cenderung melakukan pembelian ulang setelah tiga atau lebih transaksi sebelumnya.
- Jika jumlah pembelian sebelumnya < 3, maka dikategorikan sebagai No dengan nilai 0. Ini mengindikasikan bahwa pelanggan cenderung belum melakukan pembelian ulang karena riwayat transaksi yang lebih sedikit.

## Data Modelling
Tahapan selanjutnya adalah melakukan pemodelan data dimana pada penelitian ini akan digunakan lima model, yaitu _Logistic Regression_, _Decision Tree_, _Random Forest_, _Gradient Boosting_, dan _XGBoost_. Hasilnya dapat dilihat pada tabel dibawah ini
| Metode Machine Learning | Accuracy | Precision | Recall | F1-Score |
|---|---|---|---|---|
| Logistic Regression | 0.64 | 0.69 | 0.69 | 0.69 |
| Gradient Boosting | 0.68 | 0.91 | 0.51 | 0.65 |
| Decision Tree | 0.66 | 0.74 | 0.65 | 0.69 |
| Random Forest | 0.64 | 0.71 | 0.66 | 0.69 |
| XGBoost | 0.69 | 0.89 | 0.53 | 0.66 |


Dapat terlihat pada tabel bahwa model Decision Tree terbukti menjadi model terbaik dalam analisis yang dilakukan. Model ini menunjukkan performa yang cukup baik dengan nilai Precision sebesar 0.74, yang berarti sebagian besar prediksi pengiriman tepat waktu yang dilakukan oleh model adalah benar. Selain itu, model ini memiliki Recall sebesar 0.65, menunjukkan kemampuan model dalam mendeteksi sebagian besar pengiriman yang terlambat. Nilai F1-score sebesar 0.69 menggambarkan keseimbangan yang baik antara precision dan recall, menjadikan Decision Tree sebagai model yang optimal untuk penelitian ini.
![image](https://github.com/user-attachments/assets/fdcea381-e90f-41aa-ae28-0476af9243b9)

### _Feature Importance_
![image](https://github.com/user-attachments/assets/9e9afd56-24cf-45b5-996a-c84946af377e)<br>
Berdasarkan analisis _feature importance_, fitur-fitur yang paling berpengaruh dalam model ini adalah Weight, Discount, dan Cost. Ketiga fitur ini memberikan insight yang penting untuk memahami faktor-faktor yang memengaruhi keterlambatan pengiriman dalam e-commerce.
- Weight (berat paket) menunjukkan dampak yang signifikan terhadap ketepatan waktu pengiriman, karena paket yang lebih berat cenderung lebih sulit ditangani oleh logistik.
- Discount (diskon) juga memainkan peran penting, di mana produk dengan diskon tinggi sering mengalami keterlambatan pengiriman, mungkin karena lonjakan pesanan.
- Cost (biaya) menunjukkan bahwa harga produk juga memengaruhi ketepatan waktu, di mana barang yang lebih mahal cenderung diprioritaskan dalam pengiriman.

### _Machine Learning Deployment_
![image](https://github.com/user-attachments/assets/51a0019a-899c-4db2-81d6-94cb1f74fd6f)
Pada tahap ini, model machine learning diuji dengan melakukan penerapan pada layanan web (web service). Proses ini melibatkan integrasi model ke dalam sistem yang memungkinkan akses dan pengujian oleh klien secara langsung. Dengan menerapkan model pada web service, klien dapat menguji model secara real-time untuk memvalidasi hasil dan efektivitasnya dalam skenario yang lebih luas. Deployment ini memastikan bahwa model yang telah dikembangkan tidak hanya dapat berfungsi dalam lingkungan pengujian tetapi juga dapat memberikan nilai tambah dalam operasi nyata dan pengambilan keputusan berbasis data. Untuk selengkapnya, dapat dilihat dengan melakukan klik [disini](https://final-project-sigma.onrender.com)
![image](https://github.com/user-attachments/assets/9e0ba532-80ab-4f62-8390-5ac2e4107573)

## Bagian 5: Result & Reccomendation
### _Model Impact_
Penggunaan model machine learning dalam memprediksi keterlambatan pengiriman membawa dampak positif yang signifikan. Dengan kemampuan model untuk mengidentifikasi potensi keterlambatan sebelum terjadi, langkah pencegahan dapat diambil lebih awal. Pencegahan keterlambatan dan penurunan kepuasan pelanggan. Dilakukan dengan penambahan estimasi waktu pengiriman/notifikasi kemungkinan keterlambatan pengiriman. Ini memungkinkan perusahaan untuk mengimplementasikan tindakan proaktif, seperti penyesuaian dalam proses logistik atau komunikasi lebih awal dengan pelanggan.<br>
Sebagai hasilnya, prediksi yang akurat dapat membantu meningkatkan persentase pengiriman tepat waktu (on-time delivery), yang berkontribusi langsung pada peningkatan kepuasan pelanggan. Pelanggan yang menerima barang mereka sesuai jadwal cenderung lebih puas dengan layanan dan lebih mungkin untuk terus bertransaksi. Secara keseluruhan, dampak dari penerapan model machine learning ini mencakup peningkatan efisiensi operasional dan kepuasan pelanggan, yang mendukung pertumbuhan dan reputasi positif perusahaan.

### _Impact Analysis_
Untuk mengevaluasi dampak dari penggunaan model machine learning, dilakukan simulasi yang bertujuan untuk memperkirakan perubahan pada metrik _On-time Delivery_ (OTD) _Rate_. Metrik ini sangat penting karena mencerminkan persentase pengiriman yang dilakukan tepat waktu, yang secara langsung memengaruhi kepuasan pelanggan dan efisiensi operasional.<br>
Pembuatan model machine learning ini mempertimbangkan bahwa akan lebih baik jika produk yang seharusnya terkirim tepat waktu tetapi diprediksi terlambat oleh model, dibandingkan dengan skenario sebaliknya. Hal ini dilakukan untuk mengurangi risiko pengiriman terlambat yang tidak terdeteksi.<br>
Dalam simulasi, fokus utama adalah pada produk yang sebenarnya terlambat tetapi diprediksi oleh model sebagai _on-time_. Dengan mengevaluasi kesalahan ini, analisis dapat mengukur dampak nyata dari model terhadap ketepatan prediksi dan mengidentifikasi area yang memerlukan perbaikan. Pendekatan ini memastikan bahwa model tidak hanya efektif dalam mengidentifikasi pengiriman tepat waktu tetapi juga sensitif terhadap kasus-kasus di mana keterlambatan terjadi namun tidak terdeteksi, memberikan gambaran yang lebih komprehensif tentang kinerja model.<br>
Hasil simulasi model menggunakan data pengiriman yang ada menunjukkan bahwa model memprediksi 2.374 pesanan yang sebenarnya "akan terlambat" sebagai pesanan yang "akan delivered on-time" dari total 10.999 pesanan, menghasilkan False Negative Rate sekitar 21,58%. Ini berarti bahwa model mengalami kesalahan dalam mengidentifikasi keterlambatan pada 21,58% kasus, sementara 78,42% data berhasil diprediksi sesuai dengan ekspektasi. Dengan kata lain, meskipun model cukup efektif, masih ada ruang untuk peningkatan dalam akurasi prediksi untuk mengurangi tingkat kesalahan dan meningkatkan keandalan dalam memprediksi ketepatan waktu pengiriman.<br>
![image](https://github.com/user-attachments/assets/f2ee8132-7a4d-4330-91c3-f34e90138e87)<br>
![image](https://github.com/user-attachments/assets/fc836959-0169-4bac-adc8-c2249eea4d34)<br>
Penggunaan model ML, jika ditindaklanjuti dengan langkah pencegahan keterlambatan yang tepat, dapat meningkatkan OTD rate sebesar 38.09% menjadi 78.42%.

### Actionable Insights dan Business Recommendation
Insight dan Rekomendasi dari Hasil Analisis serta Penggunaan Model Machine Learning yaitu sebagai berikut:
1. **Early Notification untuk Diskon Besar:** Berikan notifikasi lebih awal mengenai potensi keterlambatan pengiriman untuk produk dengan diskon besar. Hal ini akan membantu pelanggan untuk lebih memahami kemungkinan keterlambatan dan mengatur ekspektasi mereka.
2. **Berat Produk dan Keterlambatan:** Produk dengan berat 2-4 kg dan lebih dari 6 kg cenderung mengalami keterlambatan pengiriman. Identifikasi dan manajemen yang lebih baik diperlukan untuk kategori produk ini.
3. **Perpanjangan Estimasi Pengiriman:** Pertimbangkan untuk memperpanjang estimasi durasi pengiriman atau memberikan informasi mengenai kemungkinan keterlambatan untuk produk-produk yang berisiko tinggi. Ini akan membantu dalam mengelola harapan pelanggan dan mengurangi ketidakpuasan.
4. **Penanganan Barang Berdasarkan Harga:** Untuk barang dengan harga dalam rentang 51-100 USD, disarankan untuk dihandle di Warehouse B dan F, yang menunjukkan performa baik dalam menangani produk dengan harga ini.
5. **Penanganan Barang Mahal:** Untuk barang dengan harga cenderung mahal (301-350 USD), sebaiknya dihandle di Warehouse A, D, dan F. Ketiga warehouse ini menunjukkan performa yang lebih baik dalam mengelola produk dengan nilai tinggi.
6. **Estimasi Pengiriman Berdasarkan Prediksi Model:** Pertimbangkan untuk menambah estimasi durasi pengiriman untuk produk yang diprediksi akan terlambat oleh model machine learning. Hal ini akan membantu mengurangi risiko ketidakpuasan pelanggan dan meningkatkan kepuasan keseluruhan dengan akurasi prediksi yang lebih baik.
