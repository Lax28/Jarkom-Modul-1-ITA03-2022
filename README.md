# Jarkom-Modul-1-ITA03-2022
## Anggota Kelompok
1. Muhammad Jovan Adiwijaya Yanuarsyah (5027201025)
2. Muhammad Naufal Pasya (5027201045)
3. Fatchia Farhan (5027201044)

## Descripsi
Laporan ini dibuat dengan tujuan untuk menjelaskan pengerjaan serta permasalahan yang kami alami dalam pengerjaan soal shift Jaringan Komunikasi modul 1 tahun 2022.

## Jawaban

1. Sebutkan web server yang digunakan pada "monta.if.its.ac.id"! 

Untuk mengetahui server yang digunakan pada website tersebut, praktikan menggunakan display filter dengan expression "http.response.code" Karena dengan syntax tersebut praktikan dapat melihat response yang diberikan oleh website tersebut, dan di dalam response tersebut praktikan harus membuka Protokol HTTP dan lihat di bagian header, maka disitu tertera web server apa yang digunakan oleh website tersebut, pada soal ini ditemukan web server yang digunakan adalah "nginx/1.10.3".

![image](https://user-images.githubusercontent.com/90240809/191941994-f2fb35d2-32fc-462d-b3b2-373608936b08.png)

![image](https://user-images.githubusercontent.com/90240809/191942096-7d3f05b4-86b3-48bf-8892-4d819065cfda.png)


2. Ishaq sedang bingung mencari topik ta untuk semester ini , lalu ia datang ke website monta dan menemukan detail topik pada website “monta.if.its.ac.id” , judul TA apa yang dibuka oleh ishaq ?

Untuk soal ini praktikan menggunakan kembali displlay filter menggunakan syntax "http.request.uri contains "detail" " karena pada soal juga diminta mencari detail topik dan apabila syntax tersebut dijalankan akan terlihat packet yang mengandung "detail topik" kemudian praktikan bisa mencopy url nya ke browser dan membuka link tersebut.

![image](https://user-images.githubusercontent.com/90240809/191942793-7ac5eed6-b02b-4b95-abf9-e5da2bdbe8a7.png)

![image](https://user-images.githubusercontent.com/90240809/191942857-c07c0920-afc9-4e21-8160-3908bf4bee1d.png)
