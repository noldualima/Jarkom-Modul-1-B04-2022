# Jarkom-Modul-1-B04-2022

### Praktikum Jaringan Komputer Modul 1 - Crimping dan Wireshark
NRP | Nama
-----------|---------------------------
5025201025 | Dawamul Fikri Aqil
5025201048 | Afril Muzaqqi Arif
5025201165 | Gabriel Solomon Sitanggang
-----------------------------------------------------------------

### SOAL 1
Sebutkan web server yang digunakan pada "monta.if.its.ac.id"!
#### Penjelasan
1. Melakukan filter ```http```
![image](https://user-images.githubusercontent.com/102939348/192096248-8eaee681-2955-404e-ab52-ea2275f72be5.png)
2. Memilih ```http/1.1 200 OK```
![image](https://user-images.githubusercontent.com/102939348/192096296-20ec3b63-8f1e-42fc-9655-18d773dead06.png)
3. Menuju Hypertext Transfer Protokol
![image](https://user-images.githubusercontent.com/102939348/192096353-e0ac1bc2-c5a5-425d-b996-1da9827b1784.png)
4. Diketahui server yang digunakan adalah ```nginx/1.10.3```


### SOAL 2
Ishaq sedang bingung mencari topik ta untuk semester ini, lalu ia datang ke website monta dan menemukan detail topik pada website “monta.if.its.ac.id”, judul TA apa yang dibuka oleh ishaq ?
#### Penjelasan
1. Melakukan ```Export Objects -> HTTP```
![image](https://user-images.githubusercontent.com/102939348/192096539-1d245bf8-5340-40d7-9563-99308834b53a.png)
2. Menyimpan file dengan format html, misal memilih filename ```194``` menjadi ```194.html```
3. Kemudian buka file ```194.html```, dan hasilnya
![image](https://user-images.githubusercontent.com/102939348/192096731-663cd514-2559-4d60-81b8-a594ab541ad7.png)


### SOAL 3
Filter sehingga wireshark hanya menampilkan paket yang menuju port 80! 
#### Penjelasan
```tcp.dstport == 80 || udp.dstport == 80```


### SOAL 4
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 21!
#### Penjelasan
```tcp.srcport == 21 || udp.srcport == 21```


### SOAL 5
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 443!
#### Penjelasan
```tcp.srcport == 443 || udp.srcport == 443```


### SOAL 6
Filter sehingga wireshark hanya menampilkan paket yang menuju ke lipi.go.id !
#### Penjelasan
```ip.dst == 203.160.128.158```


### SOAL 7
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
#### Penjelasan
```ip.src == 192.168.100.131```


### Untuk soal 8-10, silahkan baca cerita di bawah ini!
Di sebuah planet bernama Viltrumite, terdapat Kementerian Komunikasi dan Informatika yang baru saja menetapkan kebijakan baru. Dalam kebijakan baru tersebut, pemerintah dapat mengakses data pribadi masyarakat secara bebas jika memang dibutuhkan, baik dengan maupun tanpa persetujuan pihak yang bersangkutan. Sebagai mahasiswa yang sedang melaksanakan program magang di kementerian tersebut, kalian mendapat tugas berupa penyadapan percakapan mahasiswa yang diduga melakukan tindak kecurangan dalam kegiatan Praktikum Komunikasi Data dan Jaringan Komputer 2022. Selain itu, terdapat sebuah password rahasia (flag) yang diduga merupakan milik sebuah organisasi bawah tanah yang selama ini tidak sejalan dengan pemerintahan Planet Viltrumite. Tunggu apa lagi, segera kerjakan tugas magang tersebut agar kalian bisa mendapatkan pujian serta kenaikan jabatan di kementerian tersebut!

### SOAL 8
Telusuri aliran paket dalam file .pcap yang diberikan, cari informasi berguna berupa percakapan antara dua mahasiswa terkait tindakan kecurangan pada kegiatan praktikum. Percakapan tersebut dilaporkan menggunakan protokol jaringan dengan tingkat keandalan yang tinggi dalam pertukaran datanya sehingga kalian perlu menerapkan filter dengan protokol yang tersebut.
#### Penjelasan
Kita disuruh mencari percakapan antara 2 mahasiswa terkait tukar menukar jawaban atau mencontek, dan kita mencari menggunakan ```tcp contains jawaban``` tetapi tidak harus jawaban menggunakan ```tcp contains file``` juga bisa karena hanya mencari percakapan
![messageImage_1664022128838](https://user-images.githubusercontent.com/91501217/192098571-3fd59bb4-33d8-4681-8f98-6402bcf46ee3.jpg)

Kemudian kita Follow dengan cara klik kanan lalu arahkan ke Follow > TCP
![messageImage_1664022260012](https://user-images.githubusercontent.com/91501217/192098662-f0d90eda-cf88-4258-aff0-29354752891f.jpg)
Maka keluar percakapan antara mereka berdua
![messageImage_1664022260012](https://user-images.githubusercontent.com/91501217/192098730-d5621ee5-a5c3-44e7-9f92-944440d4f177.jpg)

### SOAL 9
Terdapat laporan adanya pertukaran file yang dilakukan oleh kedua mahasiswa dalam percakapan yang diperoleh, carilah file yang dimaksud! Untuk memudahkan laporan kepada atasan, beri nama file yang ditemukan dengan format [nama_kelompok].des3 dan simpan output file dengan nama “flag.txt”.
#### Penjelasan


### SOAL 10
Temukan password rahasia (flag) dari organisasi bawah tanah yang disebutkan di atas!
#### Penjelasan


### KENDALA
