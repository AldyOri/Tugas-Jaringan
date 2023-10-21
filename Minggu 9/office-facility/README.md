    Nama            : Dukhaan Kamimpangan
    NRP             : 3122600003
    Kelas           : 2 D4 IT A
    Mata Kuliah     : Konsep Jaringan
    Dosen Pengampu  : Dr. Ferry Astika Saputra S.T., M.Sc
    Pertemuan       : Minggu 9

## OFFICE FACILITY

### A. OFFICE FACILITY DENGAN PUBLIC IP : 12.0.0.0/8 & 6 SUBNET 

<div align="center">
<img src="./assets/main.png">
<p><strong>Gambar :</strong> konfigurasi jaringan</p>
</div>

Pada percobaan konfigurasi jaringan fasilitas kantor dengan Packet Tracer yang pertama, digunakan 1 router, 6s switch dan 6 PC.
Berikut adalah konfigurasi dari peragkat yang digunakan :

1. Menggunakan Router-PT, dimana terdapat  konfigurasi :

   - FastEthernet(Fa) 0/0 : 12.32.0.1
   - FastEthernet(Fa) 1/0 : 12.64.0.1
   - FastEthernet(Fa) 6/0 : 12.96.0.1
   - FastEthernet(Fa) 7/0 : 12.128.0.1
   - FastEthernet(Fa) 8/0 : 12.160.0.1
   - FastEthernet(Fa) 9/0 : 12.192.0.1

2. Lakukan konfigurasi pada keempat PC dengan IP Address sebagai berikut :

<div align="center">
<img src="./assets/pc0.png">
<p><strong>Gambar :</strong> konfigurasi ip PC0 : 12.33.0.2</p>
</div>

<div align="center">
<img src="./assets/pc1.png">
<p><strong>Gambar :</strong> konfigurasi ip PC1 : 12.65.0.2</p>
</div>

<div align="center">
<img src="./assets/pc2.png">
<p><strong>Gambar :</strong> konfigurasi ip PC2 : 12.97.0.2</p>
</div>

<div align="center">
<img src="./assets/pc3.png">
<p><strong>Gambar :</strong> konfigurasi ip PC3 : 12.129.0.2</p>
</div>

<div align="center">
<img src="./assets/pc4.png">
<p><strong>Gambar :</strong> konfigurasi ip PC4 : 12.161.0.2</p>
</div>

<div align="center">
<img src="./assets/pc5.png">
<p><strong>Gambar :</strong> konfigurasi ip PC5 : 12.193.0.2</p>
</div>


1. Hubungkan seluruh komponen jaringan yang ada dengan menggunakan kabel tipe straight seperti yang terlihat pada gambar di atas. Jangan lupa meng-onkan seluruh jaringan hingga ada tanda segitiga warna hijau. Pastikan subnet mask diganti dengan 255.224.0.0

**Melakukuan Ping Test**
Setelah selesai melakukan konfigurasi, selanjutnya adalah melakukan Ping test.

**1. Ping 12.33.0.2 -> 12.65.0.2**

<div align="center">
<img src="./assets/ping1.png">
<p><strong>Gambar :</strong> Ping 1</p>
</div>

Ketika perintah ping pertama kali dijalankan, maka akan terjadi broadcast dimana jika menggunakan switch broadcast hanya akan dijalankan sekali di awal ketika ingin menghubungkan suatu perangkat yang mana berfungsi untuk mencari dimana ip address yang dituju, setelah mendapatkan address yang dituju perangkat pengirim ping akan mendapatkan konfirmasi dan selanjutnya akan mengirim sebanyak 4 packets ke address yang dituju.

**2. Ping 12.65.0.2 -> 12.97.0.2**

<div align="center">
<img src="./assets/ping2.png">
<p><strong>Gambar :</strong> Ping 2</p>
</div>

**3. Ping 12.97.0.2 -> 12.129.0.2**

<div align="center">
<img src="./assets/ping3.png">
<p><strong>Gambar :</strong> Ping 3</p>
</div>

**4. Ping 12.129.0.2 -> 12.161.0.2**

<div align="center">
<img src="./assets/ping4.png">
<p><strong>Gambar :</strong> Ping 4</p>
</div>

**5. Ping 12.161.0.2 -> 12.193.0.2 (PT-Hub)**

<div align="center">
<img src="./assets/ping5.png">
<p><strong>Gambar :</strong> Ping 5</p>
</div>