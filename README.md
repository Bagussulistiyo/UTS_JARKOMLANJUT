# UTS_JARKOMLANJUT
Nama : Bagus Sulistiyo NIM : 20210801138 Prodi : Teknik Informatika

Jawaban Essay

1. Routing Statis Routing statis merupakan metode di mana rute ditetapkan secara manual oleh administrator jaringan. Dalam jenis routing ini, rute dimasukkan langsung ke dalam tabel routing setiap perangkat (router) tanpa adanya pembaruan otomatis.
2. Routing Dinamis Routing dinamis memanfaatkan protokol routing yang secara otomatis mengidentifikasi dan memperbarui rute dalam jaringan berdasarkan informasi yang dikumpulkan oleh perangkat-perangkat jaringan.
3. Firewall Firewall adalah sistem keamanan jaringan yang berfungsi sebagai penghalang antara jaringan internal (seperti LAN) dan jaringan eksternal (seperti internet), bertujuan untuk melindungi data dan perangkat dari akses yang tidak sah. Firewall melakukan pemantauan, penyaringan, dan pengendalian lalu lintas jaringan berdasarkan aturan keamanan yang telah ditetapkan, sehingga hanya lalu lintas yang aman dan sesuai izin yang diizinkan untuk melewati jaringan.
4. NAT (Network Address Translation) NAT (Network Address Translation) adalah teknik yang digunakan dalam jaringan komputer untuk mengubah alamat IP pada paket data yang melewati router atau perangkat jaringan lainnya. NAT memungkinkan banyak perangkat dalam jaringan lokal (seperti LAN) yang memiliki alamat IP privat untuk terhubung ke internet menggunakan satu atau beberapa alamat IP publik.


# Cased

# Topologi 
![Blank diagram](https://github.com/user-attachments/assets/4192ba03-148a-4d7b-8e69-92be817d128c)

# Konfigurasi 
Topologi jaringan ini terdiri dari tiga router (KCR, KJ, dan KHI), tiga switch, dan tiga PC yang terhubung melalui IP publik dan IP privat dengan koneksi tunnel antar router. Berikut adalah konfigurasi ringkasnya:

1. **Router KCR:**
   - **IP Publik:** 152.167.10.6/24
   - **Tunnel:** 
     - Ke Router KJ: 40.40.40.1/24
     - Ke Router KHI: 60.60.60.1/24
   - **Subnet Lokal:** 192.168.16.1/24
   - **IP PC:** 192.168.16.2/24 (gateway 192.168.16.1)

2. **Router KJ:**
   - **IP Publik:** 152.167.20.4/24
   - **Tunnel:**
     - Ke Router KCR: 40.40.40.2/24
     - Ke Router KHI: 60.60.60.2/24
   - **Subnet Lokal:** 192.168.17.1/24
   - **IP PC:** 192.168.17.2/24 (gateway 192.168.17.1)

3. **Router KHI:**
   - **IP Publik:** 152.167.30.8/24
   - **Tunnel:**
     - Ke Router KCR: 60.60.60.1/24
     - Ke Router KJ: 60.60.60.2/24
   - **Subnet Lokal:** 192.168.18.1/24
   - **IP PC:** 192.168.18.2/24 (gateway 192.168.18.1)

4. **Konfigurasi Routing:**
   - Setiap router perlu rute statis untuk mengakses jaringan pada router lain melalui IP tunnel yang sudah ditentukan.

5. **Testing Konektivitas:**
   - Lakukan ping antar jaringan untuk memastikan semua router dan PC dapat berkomunikasi.

Topologi ini memungkinkan komunikasi antar router dan perangkat pada jaringan lokal melalui konfigurasi tunnel dan routing statis.
