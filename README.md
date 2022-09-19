# Jarkom-Modul-1-B04-2022

### Praktikum Jaringan Komputer Modul 1 - Crimping dan Wireshark
- 5025201025 - Dawamul Fikri Aqil
- 5025201048 - Afril Muzaqqi Arif
- 5025201165 - Gabriel Solomon Sitanggang
-----------------------------------------------------------------

### SOAL 1
Sebutkan web server yang digunakan pada "monta.if.its.ac.id"! 
ip.src == 103.94.189.5 && http.server

### SOAL 2
Ishaq sedang bingung mencari topik ta untuk semester ini, lalu ia datang ke website monta dan menemukan detail topik pada website “monta.if.its.ac.id”, judul TA apa yang dibuka oleh ishaq ?


### SOAL 3
Filter sehingga wireshark hanya menampilkan paket yang menuju port 80! 
tcp.dstport == 80 || udp.dstport == 80

### SOAL 4
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 21!
tcp.srcport == 21 || udp.srcport == 21

### SOAL 5
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 443!
tcp.srcport == 443 || udp.srcport == 443

### SOAL 6
Filter sehingga wireshark hanya menampilkan paket yang menuju ke lipi.go.id !
ip.dst == 203.160.128.158

### SOAL 7
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
ip.src == 192.168.100.131

### Untuk soal 8-10, silahkan baca cerita di bawah ini!
Di sebuah planet bernama Viltrumite, terdapat Kementerian Komunikasi dan Informatika yang baru saja menetapkan kebijakan baru. Dalam kebijakan baru tersebut, pemerintah dapat mengakses data pribadi masyarakat secara bebas jika memang dibutuhkan, baik dengan maupun tanpa persetujuan pihak yang bersangkutan. Sebagai mahasiswa yang sedang melaksanakan program magang di kementerian tersebut, kalian mendapat tugas berupa penyadapan percakapan mahasiswa yang diduga melakukan tindak kecurangan dalam kegiatan Praktikum Komunikasi Data dan Jaringan Komputer 2022. Selain itu, terdapat sebuah password rahasia (flag) yang diduga merupakan milik sebuah organisasi bawah tanah yang selama ini tidak sejalan dengan pemerintahan Planet Viltrumite. Tunggu apa lagi, segera kerjakan tugas magang tersebut agar kalian bisa mendapatkan pujian serta kenaikan jabatan di kementerian tersebut!

### SOAL 8
Telusuri aliran paket dalam file .pcap yang diberikan, cari informasi berguna berupa percakapan antara dua mahasiswa terkait tindakan kecurangan pada kegiatan praktikum. Percakapan tersebut dilaporkan menggunakan protokol jaringan dengan tingkat keandalan yang tinggi dalam pertukaran datanya sehingga kalian perlu menerapkan filter dengan protokol yang tersebut.


### SOAL 9
Terdapat laporan adanya pertukaran file yang dilakukan oleh kedua mahasiswa dalam percakapan yang diperoleh, carilah file yang dimaksud! Untuk memudahkan laporan kepada atasan, beri nama file yang ditemukan dengan format [nama_kelompok].des3 dan simpan output file dengan nama “flag.txt”.

### SOAL 10
Temukan password rahasia (flag) dari organisasi bawah tanah yang disebutkan di atas!
