# Rakamin Final Project
## About Project
Repository ini dibuat sebagai Final Project Bootcamp Data Science Batch 32 yang diadakan oleh [Rakamin Academy](https://www.rakamin.com/). Final project ini mencakup praktik studi kasus penerapan hasil belajar selama bootcamp dengan memanfaatkan dataset dari Kaggle mengenai [Paket Liburan](https://www.kaggle.com/datasets/susant4learning/holiday-package-purchase-prediction). Output dari final project ini adalah untuk membuat simulasi bisnis beserta simulasi alur kerja data scientist.

## Latar Belakang
Dari dataset yang digunakan, kami menempatkan diri sebagai sebuah agensi yang bergerak di bidang data dengan nama Infinity Solutions. Pada masalah ini, klien kami "Trips&Travel" adalah sebuah perusahaan travel yang ingin membuat paket liburan baru. Masalah yang dihadapi oleh klien kami adalah bahwa pada marketing sebelumnya mereka tidak memiliki target customer yang jelas sehingga total pembelian atau conversion rate mereka rendah.

![Grafik conversion rate](assets\TargetPie.png)

Conversion rate yang rendah tersebut menyebabkan biaya yang dikeluarkan dirasa mahal. Sehingga pada masalah ini, tujuan yang ingin dicapai adalah untuk membuat model machine learning untuk mengidentifikasi target customer yang tepat sehingga conversion rate meningkat.

## EDA, Insights & Visualization
1. Pada fitur Passport, sebesar 34% pelanggan dengan paspor memutuskan untuk membeli produk, dan hanya 12% pelanggan tanpa paspor yang memutuskan untuk membeli produk yang ditawarkan.
2. Pada fitur PreferredPropertyStar, sebesar 26% pelanggan yang memilih properti bintang 5 memutuskan untuk membeli produk yang ditawarkan.
3. Pada fitur ProductPitched, sebesar hampir 30% pelanggan yang memilih Basic memutuskan untuk membeli produk yang ditawarkan.
4. Pada fitur MaritalStatus, 33% dari pelanggan yang masih single dan 24% pelanggan Unmarried memutuskan untuk membeli produk yang ditawarkan
5. Pada fitur Designation, conversion rate tertinggi pada jabatan executive sebesar hampir 30%
6. Pada fitur Age, pelanggan yang memutuskan untuk membeli produk yang ditawarkan cukup banyak yang berumur sekitar 26-40 tahun 
7. Pada fitur DurationOfPitch, pelanggan yang membeli produk lebih banyak berasal dari pelanggan yang diberikan penawaran selama kurang dari 20 menit
8. Pada fitur MonthlyIncome, pelanggan yang membeli produk lebih banyak berasal dari pelanggan dengan kisaran gaji 15,000–25,000 rupee

## Data Pre-Processing
Pada bagian ini, dilakukan beberapa penanganan terhadap kebersihan data diantaranya yaitu:
1. Penyesuaian terhadap beberapa nilai pada kolom tertentu untuk membersihkan salah ketik dan menyederhanakan beberapa nilai ordinal
2. Pengisian kolom yang bernilai kosong
3. Penghapusan terhadap nilai duplikat dan pencilan
4. Transformasi beberapa kolom numerik untuk mengubah skala

Kemudian dilakukan pemilihan fitur dengan menggunakan nilai anova untuk melihat korelasi fitur numerik terhadap target ProdTaken. Mayoritas fitur, baik numerik maupun kategorikal, akan digunakan dengan pengecualian nilai NumberOfTrips dan NumberOfChildrenVisiting yang akan dibuang. Dari NumberOfChildrenVisiting diturunkan sebuah fitur baru bernilai biner yaitu fitur HasKids untuk melihat perilaku customer berdasarkan adanya anak atau tidak ketika mengambil paket liburan.

## Modelling & Evaluation
Dalam menentukan metrics yang digunakan oleh algoritma model, dilakukan analisa terhadap arti dari hasil prediksi yaitu:
- True Positive: terprediksi akan membeli, terbukti akan membeli
- True Negative: terprediksi tidak membeli, terbukti tidak membeli
- False Positive: terprediksi akan membeli, padahal tidak membeli, sehingga ada usaha marketing yang terbuang sia-sia (tidak tepat sasaran)
- False Negative: terprediksi tidak membeli, padahal akan membeli, sehingga ada kesempatan bisnis yang hilang (revenue loss)

Berdasarkan tujuan awal untuk meningkatkan efisiensi marketing, fokus dari model prediksi ini adalah **menekan False Positive**. Metrics yang akan digunakan yaitu metrics **Precision**, semakin tinggi nilai Precision maka semakin tepat sasaran marketing yang dilakukan sesuai prediksi model.

Beberapa algoritma model yang digunakan dalam memprediksi antara lain:

![Tabel evaluasi model machine learning](assets\EvalTable.png)

Berdasarkan tabel di atas, kami menggunakan algoritma AdaBoost yang memberi nilai precision 96%. Dari model AdaBoost tersebut, berikut adalah fitur yang dianggap penting:

![Feature importance AdaBoost](assets\FeatureImportance.png)

Dari feature importance tersebut, kami melakukan analisa lebih lanjut pada data sebagai dasar dari rekomendasi bisnis yang kami berikan.

## Business Recommendations
Berikut adalah rekomendasi yang bisa kami berikan:
- MonthlyIncome
![Grafik sebaran customer berdasar pendapatan per bulan](assets\MonthlyIncome.png)
Menawarkan opsi paket dengan harga yang sesuai dengan penghasilan perbulan customer. Misalnya pada range harga produk seperti Basic dan Standard yang lebih sering dibeli. Harga yang sesuai dengan selera customers pada range income tersebut berkemungkinan lebih besar untuk mendorong pembelian.

- Age
![Grafik sebaran customer berdasar umur](assets\Age.png)
Karena mayoritas customer sebelumnya berada pada rentang usia aktif bekerja, sebaiknya buat jenis paket yang fleksibel dari segi durasi. Paket yang fleksibel akan lebih menarik bagi customer yang sibuk dan ingin menggunakan liburan yang sesuai dengan jadwal kesibukan mereka.

- DurationOfPitch
![Grafik sebaran customer berdasar durasi penawaran](assets\DurationOfPitch.png)
Gunakan 10-minutes rule dalam melakukan penawaran. Sampaikan poin utama produk dan jawab pertanyaan mengenai produk secara padat. Informasi yang cukup akan mempermudah customer dalam mengambil keputusan.

## About Infinity
Kelompok final project kami terdiri dari 8 orang, yaitu:
- [Andre Adeputra S](https://github.com/andreadeputra)
- [Gilang Muhammad Risky](https://github.com/gilangrizky67)
- [Jomas Sekar Pawestri](https://github.com/jomassekar)
- [M Nurkholis Fauzi](https://github.com/nurkholisfz)
- [Naomi Florenata Damanik](https://github.com/naomidmnk)
- [Sakinah Nurul R](https://github.com/sakinahnr11)
- [Vanesa](https://github.com/vanesanesa)
