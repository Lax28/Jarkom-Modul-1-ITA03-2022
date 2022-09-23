# Jarkom-Modul-1-ITA03-2022
## Anggota Kelompok
1. Muhammad Jovan Adiwijaya Yanuarsyah (5027201025)
2. Muhammad Naufal Pasya (5027201045)
3. Fatchia Farhan (5027201044)

## Deskripsi
Laporan ini dibuat dengan tujuan untuk menjelaskan pengerjaan serta permasalahan yang kami alami dalam pengerjaan soal shift Jaringan Komunikasi modul 1 tahun 2022.

## Jawaban

## 1. Sebutkan web server yang digunakan pada "monta.if.its.ac.id"! 

Untuk mengetahui server yang digunakan pada website tersebut, praktikan menggunakan display filter dengan expression "http.response.code" Karena dengan syntax tersebut praktikan dapat melihat response yang diberikan oleh website tersebut, dan di dalam response tersebut praktikan harus membuka Protokol HTTP dan lihat di bagian header, maka disitu tertera web server apa yang digunakan oleh website tersebut, pada soal ini ditemukan web server yang digunakan adalah "nginx/1.10.3".

![image](https://user-images.githubusercontent.com/90240809/191941994-f2fb35d2-32fc-462d-b3b2-373608936b08.png)

![image](https://user-images.githubusercontent.com/90240809/191942096-7d3f05b4-86b3-48bf-8892-4d819065cfda.png)


## 2. Ishaq sedang bingung mencari topik ta untuk semester ini , lalu ia datang ke website monta dan menemukan detail topik pada website “monta.if.its.ac.id” , judul TA apa yang dibuka oleh ishaq ?

Untuk soal ini praktikan menggunakan kembali displlay filter menggunakan syntax "http.request.uri contains "detail" " karena pada soal juga diminta mencari detail topik dan apabila syntax tersebut dijalankan akan terlihat packet yang mengandung "detail topik" kemudian praktikan bisa mencopy url nya ke browser dan membuka link tersebut.

![image](https://user-images.githubusercontent.com/90240809/191942793-7ac5eed6-b02b-4b95-abf9-e5da2bdbe8a7.png)

![image](https://user-images.githubusercontent.com/90240809/191942857-c07c0920-afc9-4e21-8160-3908bf4bee1d.png)


## 3. Filter sehingga wireshark hanya menampilkan paket yang menuju port 80!

Untuk soal ini praktikan menggunakan display filter dengan syntax `tcp.dstport==80` karena pada port 80 lebih sering menggunakan protokol TCP dan pada soal yang ditanyakan adalah paket yang **menuju** maka digunakan `dst` pada syntaxnya.

![image](https://user-images.githubusercontent.com/90241858/191947285-b260b866-5e81-4981-a823-46cf7ce2e6d5.png)


## 4. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 21!

Untuk soal ini praktikan menggunakan display filter dengan syntax `tcp.srcport==21` karena pada port 21 lebih sering menggunakan protokol TCP atau FTP dan pada soal yang ditanyakan adalah paket yang **berasal** maka digunakan `src` pada syntaxnya.

![image](https://user-images.githubusercontent.com/90241858/191947613-3655ab73-1495-4ceb-a439-39601ac32c30.png)


## 5. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 443!

Untuk soal ini praktikan menggunakan display filter dengan syntax `tcp.srcport == 443 || udp.srcport ==443` karena pada port 443 menggunakan protokol TCP dan protokol UDP dan pada soal yang ditanyakan adalah paket yang **berasal** maka digunakan `src` pada syntaxnya dengan `||` sebaga constaintnya.

![image](https://user-images.githubusercontent.com/90241858/191947981-1683addb-3cd6-43b0-bda1-6a305c188f29.png)


## 6. Filter sehingga wireshark hanya menampilkan paket yang menuju ke lipi.go.id !

Untuk soal ini praktikan mencari ip address dari `lipi.go.id` terlebih dahulu. Disini praktikan menggunakan fitur `export` di wireshark dengan hasilnya seperi gambar berikut.

![image](https://user-images.githubusercontent.com/90241858/191948468-f14b1ad0-9aa5-4866-ae1d-2828f2f2a0cf.png)
![image](https://user-images.githubusercontent.com/90241858/191948399-f128ad42-7956-412d-befd-fb947774220d.png)

pada gambar kedua terlihat ip address sourcenya adalah '203.160.128.158', setelah didapatkan ip address dari 'lipi.go.id' kita dapat menggunakan display filter dengan syntax `ip.dst == 203.160.128.158` dan pada soal yang ditanyakan adalah paket yang **menuju** maka digunakan `dst` pada syntaxnya.

![image](https://user-images.githubusercontent.com/90241858/191949015-be242832-9a34-44e4-8c57-78edda85c108.png)


## 7. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

Untuk soal ini praktikan mencari ip address dari praktikan sendiri. Hal ini dapat dilakukan dengan menggunakan command `ipconfig` pada terminal OS praktikan dimana pada soal ini praktikan menggunakan OS Windows. Jadi, hasil dari command `ipconfig` adlaah seperti gambar

![image](https://user-images.githubusercontent.com/90241858/191949387-373d671f-76ff-4125-b92f-9ff08674378e.png)

Pada gambar karena praktikan menggunakan WI-FI untuk mengakses internet maka ip address-nya adalah `192.168.0.196` sehingga dapat kita gunakan capture filter `src host 192.168.0.196` sehingga menghasilkan hasil yang ada pada gambar berikut:

![image](https://user-images.githubusercontent.com/90241858/191949820-923e40da-43be-42f6-8c23-b6d92ec39f5e.png)
![image](https://user-images.githubusercontent.com/90241858/191949863-c8f152f0-838b-4974-90a5-1cf1faaa0761.png)




