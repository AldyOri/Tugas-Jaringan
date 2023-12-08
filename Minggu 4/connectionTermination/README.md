## Dosen Pengampu
Tugas ini merupakan tugas mata kuliah Konsep Jaringan yang diampu oleh Dr. Ferry Astika Saputra ST, M.Sc ([@ferryastika](https://github.com/ferryastika)).

# Connection Termination pada Socket Programming
### 1. Quit (Full Close)
```
    if(!bcmp(buffer, "quit", 4))
        break;
```
   - <p>Saat client menerima pesan "quit" dari server, client akan keluar dari loop dan mengakhiri program. Ini berarti client akan menutup koneksi sepenuhnya (full close).</p>
   
   - <p>Penutupan penuh ini mengindikasikan bahwa client tidak akan mengirim atau menerima data lagi melalui koneksi tersebut, dan sumber daya jaringan akan dibebaskan setelah program client berakhir.</p>

   - <p>Ini adalah cara yang umum digunakan untuk mengakhiri koneksi secara aman ketika pengguna memutuskan untuk keluar dari program.</p>

### 2. Close (Half Close)
```
    scanf("%s", buffer);
```
   - <p>Ketika client mengetikkan "close" dan mengirimkannya ke server, client hanya mengirim pesan "close" ke server melalui koneksi. Koneksi itu sendiri tidak akan ditutup sepenuhnya oleh client, tetapi hanya sisi pengiriman data (half close) dari sisi client.</p>

   - <p>Ini berarti client masih dapat menerima respons atau pesan lain dari server melalui koneksi tersebut, tetapi client tidak akan mengirim pesan lebih lanjut ke server melalui koneksi tersebut.</p>
```
    if(buffer == "close"){
        printf("Process %d: ", getpid());
        close(client_fd);
        printf("Closing session with `%d`. Bye!\n", client_fd);
        break;
    }
```
   - <p>Kode di sisi server akan mendeteksi pesan "close" dan menutup koneksi dari sisi server, sehingga koneksi menjadi setengah tertutup (half closed) dari sisi server. Server tidak lagi akan mengirim data ke client melalui koneksi tersebut.</p>
   
   - <p>Koneksi akan tetap terbuka dari sisi client sampai client juga menutupnya secara eksplisit atau sampai terjadi kesalahan pada koneksi.</p>
