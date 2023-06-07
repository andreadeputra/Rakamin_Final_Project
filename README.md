# Rakamin Final Project
## About Project
Repository ini dibuat sebagai Final Project Bootcamp Data Science Batch 32 yang diadakan oleh [Rakamin Academy](https://www.rakamin.com/). Final project ini mencakup praktik studi kasus penerapan hasil belajar selama bootcamp dengan memanfaatkan dataset dari Kaggle mengenai [Paket Liburan](https://www.kaggle.com/datasets/susant4learning/holiday-package-purchase-prediction). Output dari final project ini adalah untuk membuat simulasi bisnis beserta simulasi alur kerja data scientist.

## Latar Belakang
lorem ipsum

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

## About Infinity
Kelompok final project kami terdiri dari 8 orang, yaitu:
- [Andre Adeputra S](https://github.com/andreadeputra)
- [Gilang Muhammad Risky](https://github.com/gilangrizky67)
- [Jomas Sekar Pawestri](https://github.com/jomassekar)
- [M Nurkholis Fauzi](https://github.com/nurkholisfz)
- [Muhammad Syarif U](https://github.com/sveell)
- [Naomi Florenata Damanik](https://github.com/naomidmnk)
- [Sakinah Nurul R](https://github.com/sakinahnr11)
- [Vanesa](https://github.com/vanesanesa)
