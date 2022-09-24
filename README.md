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
```tcp contains "lipi.go.id"```


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
![messageImage_1664022255810](https://user-images.githubusercontent.com/91501217/192098791-6b2e90f4-9038-4c0c-bc48-d7d7caa1fe7f.jpg)
Maka keluar percakapan antara mereka berdua
![messageImage_1664022260012](https://user-images.githubusercontent.com/91501217/192098730-d5621ee5-a5c3-44e7-9f92-944440d4f177.jpg)

### SOAL 9
Terdapat laporan adanya pertukaran file yang dilakukan oleh kedua mahasiswa dalam percakapan yang diperoleh, carilah file yang dimaksud! Untuk memudahkan laporan kepada atasan, beri nama file yang ditemukan dengan format [nama_kelompok].des3 dan simpan output file dengan nama “flag.txt”.
#### Penjelasan
Lalu kita di suruh mencari file yang ada di dalam percakapan tersebut kedua mahasiswa tersebut bertukar jawaban melalui file. dan mereka mengirim file melewati ```port 9002```. kita cari port 9002 tersebut di display packet untuk mencari file nya, kemudian di follow untuk melihat file yang masih dalam bentuk decrypt des3. Sebelum kita save harus kita ubah dalam bentuk raw agar bisa diberi format ```.des3"``` dengan nama file ```B04.des3```

Cari menggunakan ```tcp contains jawaban```
![messageImage_1664022326590](https://user-images.githubusercontent.com/91501217/192098889-bec11e71-97d8-497e-99e3-815cfb4d9d9a.jpg)

Lalu kemudian Follow > TCP
![messageImage_1664022347965](https://user-images.githubusercontent.com/91501217/192098952-147b643d-89e8-4161-b4ac-8b9c5ae89490.jpg)

Setelah itu muncul seperti ini file yang berbentuk encrypt lalu kita ubah ke raw
![messageImage_1664022358722](https://user-images.githubusercontent.com/91501217/192099006-9ad79a9c-9eba-4e1b-a626-ec298b26ef0f.jpg)
setelah itu berubah seperti ini lalu save dengan nama file B04.des3 karena nama kelompok
![messageImage_1664022370189](https://user-images.githubusercontent.com/91501217/192099048-b1c862f6-b183-4772-a160-6abc5621c2e3.jpg)

Lalu buka WSL Ubuntu untuk mendecrypt file des3 tersebut dengan menggunakan syntax ```openssl des3 -d -salt -in namafile -out keluaran file yang ingin di ekstrak```.
Kemudian kita di minta password pada file tersebut dengan clue 5 anime kembar yaitu passwordnya nakano
![messageImage_1664022660258](https://user-images.githubusercontent.com/91501217/192099095-52f2367b-a96f-4448-8b7b-6e5240f9267a.jpg)
Akan muncul notif seperti ini berarti decrypt des3 nya telah berhasil
![messageImage_1664024186987](https://user-images.githubusercontent.com/91501217/192099171-a6a6eafa-fb42-48b8-9549-7d0ac71d69b9.jpg)
Dan isi dari file tersebut adalah
![messageImage_1664022806599](https://user-images.githubusercontent.com/91501217/192099200-6422b25e-fbd2-45ac-8069-75782f63fb01.jpg)


### SOAL 10
Temukan password rahasia (flag) dari organisasi bawah tanah yang disebutkan di atas!
#### Penjelasan
Kita di beri clue oleh kedua mahasiswa tersebut terkait passwordnya yang tertera di percakapan mereka
![messageImage_1664024303231](https://user-images.githubusercontent.com/91501217/192099284-e7f055e8-61cc-4b71-9af8-16ace9060e27.jpg)
password dari file tersebut adalah ```nakano```

### KENDALA
Untuk kendala yang dialami adalah soal di nomor 9 untuk decrypt file nya karena penjelasan dari soal kurang jelas jadi sempat bingung membuang waktu disitu. karena di seslab tidak diberi clue untuk menggunakan linux/WSL
