## Dosen Pengampu
Tugas ini merupakan tugas mata kuliah Konsep Jaringan yang diampu oleh Dr. Ferry Astika Saputra ST, M.Sc ([@ferryastika](https://github.com/ferryastika)).

# Dynamic Routing

## A. Pengertian
<p>Routing dynamic adalah routing yang dilakukan oleh router dengan cara membuat jalur  komunikasi data secara otomatis sesuai dengan pengaturan yang dibuat. Jika ada  perubahan topologi di dalam jaringan, maka router akan otomatis membuat jalur  routing yang baru. Routing dynamic ini lebih mudah dilakukan daripada menggunakan  routing static dan default. 

Routing dynamic ini berada pada lapisan network layer jaringan komputer dalam  TCP/IP Protocol Suites. Routing dynamic juga merupakan routing protocol yang  digunakan untuk menemukan network serta untuk melakukan update routing table pada  router. Meskipun begitu, routing jenis ini terdapat perbedaan dalam pemrosesan data di  CPU router dan penggunaan bandwith dari link jaringan. </p>

## B. Kelebihan dari Dynamic Routing
1. Hanya mengenalkan alamat yang terhubung langsung dengan routernya (jaringan  yang berada di bawah kendali router tersebut). 

2. Tidak perlu mengetahui semua alamat network yang ada. 

3. Jika terdapat penambahan suatu network baru, maka semua router tidak perlu  mengkonfigurasi. Hanya router-router yang berkaitan yang akan mengkonfigurasi  ulang. 

## C. Kekurangan dari Dynamic Routing
1. Kecepatan pengenalan dan kelengkapan IP table memakan waktu lama karena  router akan melakukan broadcast ke semua router sampai ada IP table yang cocok.  Setelah konfigurasi selesai, router harus menunggu beberapa saat agar setiap router  mendapat semua alamat IP yang tersedia.

2. Beban kerja router menjadi lebih berat karena selalu memperbarui IP table pada  setiap waktu tertentu. 

## D. Macam-Macam Protokol Routing Dynamic

### 1. RIP (Routing Information Protocol) 
<p>RIP (Routing Information Protocol) merupakan protokol yang memberikan routing  table berdasarkan router yang terhubung langsung. Lalu, router selanjutnya akan  memberikan informasi ke router berikutnya yang terhubung langsung dengan router  tersebut. </p>

RIP terbagi menjadi dua bagian, yaitu: 

• RIPv1 (RIP versi 1) 

1. Hanya mendukung routing class-full 

2. Tidak ada info subnet yang di masukkan dalam data perbaikan routing 3. Tidak mendukung VLSM (Variabel Length Subnet Mask) 

4. Adanya fitur perbaikan routing broadcast 

• RIPv2 (RIP versi 2) 

1. Mendukung adanya routing class-full dan class-less 

2. Info subnet dimasukkan dalam data perbaikan routing 

3. Mendukung adanya VLSM (Variabel Length Subnet Mask) 

4. Perbaikan routing multicast 

Sebenarnya secara umum, RIPv2 tidak berbeda jauh dengan RIPv1.  Perbedaan yang ada terlihat pada informasi yang diberikan antar router.  Pada RIPv2, informasi yang dipertukarkan terdapat autentifikasi. 

__Kelebihan RIP__ 

1. Menggunakan metode “Triggered Update” 

2. Memiliki timer untuk mengetahui kapan router harus kembali  memberikan informasi 

3. Mengatur routing menggunakan RIP tidak rumit dan memberikan hasil  yang cukup dapat diterima, terlebih jika jarang terjadi kegagalan link  pada jaringan.

### 2. IGRP (Interior Gateway Routing Protocol)
<p>IGRP adalah sebuah routing protocol yang dikembangkan pada pertengahan tahun  1980-an oleh Cisco Systems Inc. Tujuan utama penciptaan IGRP adalah untuk  menyediakan protokol yang kuat untuk routing dalam sistem otonomi. IGRP  menggunakan bandwith dan garis menunda secara default untuk menentukan rute  terbaik dalam sebuah internetwork (Composite Metrik). 

Protokol routing ini menggunakan algoritma distance vector. IGRP menggunakan  composite metric yang terdiri atas bandwidth, load, delay dan reliability. Update  routing dilakukan secara broadcast setiap 90 detik. Pada IGRP, routing dilakukan  secara matematik berdasarkan jarak. Untuk itu, sistem IGRP sudah  mempertimbangkan beberapa hal sebelum mengambil keputusan jalur mana yang  akan ditempuh. Karena protocol ini diciptakan oleh Cisco, maka di dalam kumpulan  perintah dasar Cisco terdapat perintah untuk mengatur protokol ini. </p>

__Kelebihan IGRP__

1. Mendukung sampai 255 hop count 

### 3. OSPF (Open Short Path First) 
<p>OSPF adalah sebuah routing protocol standar terbuka yang telah diaplikasikan oleh  sejumlah vendor jaringan. Jika jaringan yang dikelola adalah jaringan besar, maka  OSPF adalah pilihan satu-satunya. OSPF ini adalah sesuatu yang disebut route  redistribution, yaitu sebuah layanan penerjemah antar routing protocol. OSPF  hanya mendukung routing IP saja, update routing akan dilakukan secara floaded  saat terjadi perubahan topologi jaringan. </p>

__Kelebihan OSPF__
1. Tidak menghasilkan routing loop 

2. Mendukung penggunaan beberapa metrik sekaligus 

3. Bisa menghasilkan banyak jalur ke tujuan untuk membagi jaringan yang  besar menjadi beberapa area 

4. Waktu yang di perlukan untuk konvergen lebih cepat 

### 4. EIGRP (Enhanced Interior Gateway Routing Protocol) 
<p>Protokol routing ini menggunakan algoritma advanced distance vector dan  menggunakan cost load balancing yang tidak sama. Algoritma yang dipakai adalah  kombinasi antara distance vector dan link-state, serta menggunakan Diffusing 

Update Algorithm (DUAL) untuk menghitung jalur terpendek. Broadcast-broadcast  EIGRP di update setiap 90 detik ke semua router EIGRP yang berdekatan. Setiap  update hanya memasukkan perubahan jaringan. 

EIGRP sangat cocok untuk diterapkan pada jaringan komputer yang besar. IGRP  dan EIGRP sama-sama sudah mempertimbangkan masalah bandwith yang ada dan  delay yang terjadi. </p>

__Kelebihan EIGRP__
1. Melakukan konvergensi secara tepat ketika menghindari loop 

2. Memerlukan lebih sedikit memori dan proses 

3. Adanya fitur “Loop Avoidance” 

### 5. BGP (Border Gateway Protocol) 
<p>Sebagai routing protocol, BGP memiliki kemampuan untuk melakukan  pengumpulan rute, pertukaran rute dan menentukan rute terbaik menuju ke sebuah  lokasi dalam sebuah jaringan. Yang membedakan BGP dengan routing protocol lain  adalah BGP termasuk ke dalam kategori routing protocol jenis Exterior Gateway  Protocol (EGP). BGP merupakan “distance vector exterior gateway protocol” yang  bekerja secara cerdas untuk merawat path-path ke jaringan lainnya. 

Update – update akan dikirim melalui koneksi TCP. Protokol ini biasa digunakan  antara ISP dengan ISP dan atau antara client dengan client lainnya. Dalam  implementasinya, protokol ini digunakan untuk membuat rute dari trafik internet  antar autonomous system. </p>

__Kelebihan BGP__

1. Sangat sederhana dalam proses instalasi 

## E. Cara Kerja Routing Dynamic 
<p>Cara kerja routing dynamic yaitu Protokol Routing mengatur tiap Router sehingga  dapat berkomunikasi antar Router satu dengan Router lainnya dan saling memberikan  informasi dan juga tentunya informasi Routing yang dapat mengubah isi dari routing  table, dengan kata lain Dynamic Routing adalah proses pengisian data pada Routing  table secara otomatis. Secara khusus, dynamic routing merupakan jenis routing yang  paling mudah dikonfigurasikan dan lebih efektif dalam memiliki rute terbaik untuk  sebuah tujuan jaringan serta dapat menemukan jaringan terluar.</p>