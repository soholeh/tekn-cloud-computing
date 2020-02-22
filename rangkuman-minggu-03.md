# Praktikum Teknologi Cloud Computing - Minggu 3 (LATIHAN)

1. Sign-up heroku
![g0](/minggu-03/g0.png)

* Disini sebelumnya saya telah memiliki akun heroku atau sudah mendaftar namun saya lupa password dan saya ganti password terlebih dahulu lewat konfirmasi email saya dan langsung melakukan login dan berhasil.

2. Membuat aplikasi baru melalui dashboard
![g1](/minggu-03/g1.png)
![g2](/minggu-03/g2.png)
* Pada pembuatan app baru ini saya namai dengan paas-tcc175610047 lalu untuk regionnya saya pilih United States.

3. Menghubungkan account heroku dengan github
![g3](/minggu-03/g3.png)
![g4](/minggu-03/g4.png)

**Getting Started on Heroku with Python**

1. Masuk ke Heroku CLI
![g5](/minggu-03/g5.png)
* Dengan menggunakan perintah "heroku login" kita dapat masuk ke Heroku CLI, lalu diikuti dengan mengklon pada repo python-getting-started yang ada pada akun github heroku, setelah berhasil mengklonnya pindah ke direktori folder tersebut dengan perintah cd.
* Penjelasan perintah pada CLI :

    $ heroku create

    -Untuk membuat aplikasi pada heroku yang akan mendapat nama acak di app kita.

    $ git push heroku master

    -Untuk upload atau deploy app kita.

    $ heroku ps
    $ heroku ps:scale web=0
    $ heroku ps:scale web=1

    -Untuk penskalaan aplikasi dan dino web.

    $ heroku open
    $ heroku local
    $ heroku local web -f Procfile.windows

    -Untuk menguji dan menjalankan app

2. Menambahkan text dan syntax
![g6](/minggu-03/g6.png)
* Untuk file requirements.txt kita menambahkan text berupa "requests" yang sebelumnya telah menginstall modul requests.
* Untuk file views.py kita menambahkan syntax berupa "import requests" dan menambahkan sebuah fungsi baru dengan nama index.

3. Hasil deploy melalui heroku
![g7](/minggu-03/g7.png)

4. Menjalankan lewat Python
![g8](/minggu-03/g8.png)

