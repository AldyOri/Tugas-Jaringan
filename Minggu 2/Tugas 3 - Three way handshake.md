Nama : Muhamad Aldy Nugroho
Kelas : D4 IT A
NRP : 3122600020

1. Kenapa 1 port FTP (File Transfer Protocol) bisa menggunakan UDP/TCP
    Port FTP (File Transfer Protocol) umumnya menggunakan protokol TCP (Transmission Control Protocol) daripada UDP (User Datagram Protocol) karena sifat protokol FTP yang membutuhkan handshaking, kontrol akurasi, dan koneksi yang andal, yang lebih sesuai dengan karakteristik TCP.

2. Three way handshake
    Three-Way Handshake, juga dikenal sebagai TCP Three-Way Handshake atau TCP Handshake, adalah proses yang digunakan oleh protokol TCP (Transmission Control Protocol) untuk memastikan koneksi yang andal dan terjalin dengan baik antara pengirim dan penerima sebelum pertukaran data dimulai. Ini adalah langkah awal dalam menginisiasi koneksi TCP.

    Proses Three-Way Handshake terdiri dari tiga langkah yang dilakukan secara berurutan:

    **Langkah 1 - SYN (Synchronize):**
    Pengirim (klien) mengirimkan pesan SYN ke penerima (server) untuk memulai koneksi. Pesan ini berisi nomor urut acak (initial sequence number) yang akan digunakan dalam pengiriman data. Pengirim juga memulai penghitungan jendela (window size) yang menunjukkan seberapa banyak data yang dapat diterima oleh penerima sebelum harus mengirimkan konfirmasi.

    **Langkah 2 - SYN-ACK (Synchronize-Acknowledgment):**
    Penerima menerima pesan SYN dari pengirim dan mengirimkan balasan SYN-ACK. Pesan SYN-ACK berisi nomor urut acak sendiri dan juga mengonfirmasi nomor urut dari pesan SYN yang diterima sebelumnya. Penerima juga menginisiasi penghitungan jendela (window size) untuk mengontrol aliran data.

    **Langkah 3 - ACK (Acknowledgment):**
    Pengirim menerima pesan SYN-ACK dari penerima dan mengirimkan balasan ACK. Dalam pesan ACK ini, pengirim mengonfirmasi nomor urut dari pesan SYN-ACK yang diterima sebelumnya. Koneksi dianggap berhasil terjalin setelah pengirim mengirimkan pesan ACK, dan keduanya siap untuk pertukaran data.

    Setelah Three-Way Handshake selesai, koneksi TCP sudah terbentuk dan data dapat dikirimkan antara klien dan server secara andal. Handshake ini memastikan bahwa keduanya menyadari keberadaan satu sama lain dan bahwa parameter koneksi yang diperlukan sudah dikonfigurasi dengan benar.

    Proses Three-Way Handshake juga penting dalam melindungi jaringan dari kondisi aneh seperti aliran data yang tidak valid atau ancaman serangan, karena pesan-pesan SYN-ACK yang dibalas diharapkan hanya berasal dari koneksi yang sah.