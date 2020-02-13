# Praktikum Teknologi Cloud Computing - Minggu 2

## 1. Perbedaan antara IaaS, SaaS, dan Paas

* **IaaS (infrastructure as a service)** ialah yang termudah dari semua kategori. Ini mengacu pada layanan berbasis cloud, seperti penyimpanan pay-as-you-go, jaringan, dan virtualisasi. Model ini menyediakan teknologi dan ruang lingkup yang sama dengan pusat data tradisional. Perbedaannya adalah kita tidak dapat secara fisik memelihara atau mengelolanya menggunakan solusi offline. IaaS membantu perusahaan membuat dan mengelola data mereka saat mereka berskala, membayar ruang server yang mereka gunakan untuk mengembangkan perangkat keras atau perangkat lunak. Contoh IaaS yaitu Amazon Web Services , Microsoft Azure dll.

* **SaaS (software-as-a-service)** merupakan perangkat lunak berbasis cloud yang tersedia untuk pembelian secara berlangganan. Ini sebagian besar digunakan untuk aplikasi yang membutuhkan akses web dan seluler. Produk SaaS tidak perlu diunduh dan diinstal pada perangkat individu. Sebagian besar dapat dijalankan langsung dari browser web. Harus diperhitungkan bahwa pelanggan tidak bertanggung jawab atas pembaruan perangkat keras dan perangkat lunak. Selain itu, dengan SaaS, vendor mengelola semua masalah teknis potensial, seperti data, middleware, server, dan penyimpanan. Ini memungkinkan bisnis untuk merasionalisasi pemeliharaan dan dukungan mereka. Contoh SaaS yaitu Google App Engine , Dropbox , JIRA dll.

* **PaaS (platform as a service)** mengacu pada layanan platform berbasis cloud yang memberi para pengembang kerangka kerja yang dapat mereka gunakan untuk membuat aplikasi khusus. Model ini menyediakan programmer dengan platform yang digunakan untuk membuat perangkat lunak yang dikirimkan melalui Internet. Semua server, penyimpanan, dan jaringan dapat dikontrol oleh bisnis atau penyedia pihak ketiga. PaaS membuat proses pengembangan, pengujian, dan penyebaran cepat, mudah, dan hemat biaya. Dibandingkan dengan SaaS, PaaS menyediakan platform untuk pembuatan perangkat lunak, bukan perangkat lunaknya. Contoh PaaS ialah Windows Azure & Google App Engine.

* Gambar perbedaan utama antara IaaS, PaaS & SaaS
![diff](different.jpg)
***
## 2. Arsitektur Platform SAAS

**SAAS (Software as a Service)** atau dalam bahasa Indonesia dapat dikatakan sebagai Perangkat Lunak sebagai layanan adalah model lisensi dan pengiriman perangkat lunak di mana perangkat lunak dilisensikan berdasarkan berlangganan dan di-host secara terpusat. Pengguna dapat mengaksesnya dengan bantuan browser web. SaaS adalah model pengiriman umum untuk banyak aplikasi bisnis, termasuk perangkat lunak perkantoran dan pesan, perangkat lunak manajemen, virtualisasi dll. Ini adalah bagian dari nomenklatur komputasi awan, bersama dengan infrastruktur sebagai layanan (IaaS), platform sebagai layanan (PaaS) , desktop sebagai layanan (DaaS).

![arsi](arsiSaaS.jpg)
**Arsitektur SAAS:** <br>
Dengan model ini, satu versi aplikasi, dengan satu konfigurasi digunakan untuk semua pelanggan. Aplikasi ini diinstal pada banyak mesin untuk mendukung skalabilitas (disebut penskalaan horizontal). Dalam beberapa kasus, versi kedua aplikasi diatur untuk menawarkan kelompok pelanggan tertentu dengan akses ke versi pra-rilis aplikasi untuk tujuan pengujian. Dalam model tradisional ini, setiap versi aplikasi didasarkan pada kode unik. Meskipun pengecualian, beberapa solusi SaaS tidak menggunakan multitenancy, untuk mengelola secara efektif sejumlah besar pelanggan di tempat. Apakah multitenancy merupakan komponen yang diperlukan untuk perangkat lunak-sebagai-layanan adalah topik kontroversi.

Terdapat 2 versi utama pada SaaS yaitu :
1. Vertical SaaS
    * Perangkat Lunak yang menjawab kebutuhan industri tertentu (misalnya: Perangkat lunak untuk kesehatan, pertanian, real estat & industri keuangan)
2. Horizontal SaaS
    * Produk-produk yang berfokus pada kategori perangkat lunak (pemasaran, penjualan, alat pengembang, SDM) tetapi agnostik industri.

Ilustrasi SaaS Vertical & Horizontal
![vh](vh.jpg)
**Manfaat SAAS:** <br>
 Secara tradisional, menyebarkan sistem perangkat lunak skala besar telah menjadi tugas utama. Menyebarkan sistem ini di perusahaan besar membutuhkan biaya lebih besar. Waktu, staf, dan persyaratan anggaran untuk penyebaran sebesar ini mewakili risiko yang signifikan bagi organisasi dalam ukuran berapa pun, dan sering kali menempatkan perangkat lunak seperti itu di luar jangkauan organisasi yang lebih kecil yang jika tidak dapat diturunkan darinya banyak utilitas. Model pengiriman berdasarkan permintaan mengubah beberapa hal ini. Aplikasi SaaS tidak memerlukan penyebaran infrastruktur besar di lokasi klien. Integrasi dapat direncanakan dan dilaksanakan dengan upaya minimal, menciptakan salah satu interval waktu-ke-nilai sesingkat mungkin untuk investasi TI utama. Ini juga memungkinkan sejumlah vendor SaaS untuk menawarkan "test drive" bebas risiko (dan seringkali secara harfiah gratis) dari perangkat lunak mereka untuk periode terbatas, seperti 30 hari. Memberi pelanggan kesempatan untuk mencoba perangkat lunak sebelum mereka membelinya membantu menghilangkan banyak risiko seputar pembelian perangkat lunak.

 **Kesimpulan** <br>
 Perusahaan sebaiknya mempertimbangkan fleksibilitas dan implikasi manajemen risiko dalam menambahkan SaaS ke portofolio layanan TI mereka. Integrasi dan komposisi adalah komponen penting dalam strategi arsitektur Anda untuk menggabungkan SaaS dengan sukses sebagai anggota yang berpartisipasi penuh dari infrastruktur TI Anda yang berfokus pada layanan. Kami percaya bahwa masa depan komputasi perusahaan tidak akan murni di tempat. Sebaliknya, mereka akan ada dalam harmoni simbiosis.
 ***
 ## 3. SaaS (Software as a Service) Platform itecture
 **Fitur dan Manfaat Utama dari Platform SaaS**
 1. Kesederhanaan
    * Aplikasi perangkat lunak yang dirancang sebagai solusi SaaS biasanya diakses melalui web melalui berbagai jenis perangkat. Kemajuan dalam bahasa pemrograman sisi klien seperti JavaScript telah menghasilkan antarmuka web yang lebih intuitif dan dengan demikian, membuat penggunaan aplikasi yang dikirim melalui internet mudah digunakan seperti rekan-rekan desktop mereka.

 2. Ekonomis
    * Model pembayaran biaya subskrip bulanan atau tahunan memudahkan bisnis untuk menganggarkan dana, ditambah dengan biaya pemasangan infrastruktur nol, mudah untuk melihat bagaimana memilih menggunakan solusi SaaS dapat menghemat uang bisnis.

 3. Keamanan
    * Keamanan adalah aspek penting dari solusi pengembangan perangkat lunak dan platform SaaS tidak berbeda. Sebagai konsumen aplikasi yang dirancang menggunakan SaaS, kita tidak perlu khawatir dengan bagaimana data kita dikunci. Itu dipegang dengan aman di cloud!

 4. Kesesuaian
    * Dengan penginstalan perangkat lunak tradisional, pembaruan dan tambalan terkadang membutuhkan banyak waktu dan uang. Ini terutama benar dalam perusahaan. Selain itu, perbedaan versi antara anggota tim dari tenaga kerja kita dapat menyebabkan masalah kompatibilitas dan bahkan lebih banyak waktu terbuang. Namun, dengan SaaS, pelanggan dapat log-on ke layanan yang sudah ditingkatkan.