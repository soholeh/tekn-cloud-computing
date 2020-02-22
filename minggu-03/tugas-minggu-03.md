# Praktikum Teknologi Cloud Computing - Minggu 3 (TUGAS)

**Deployement ke PaaS di Heroku untuk PHP**

1. Masuk ke Heroku CLI
![g11](/minggu-03/g11.png)
* Dengan menggunakan perintah "heroku login" kita dapat masuk ke Heroku CLI, lalu diikuti dengan mengklon pada repo php-getting-started yang ada pada akun github heroku, setelah berhasil mengklonnya pindah ke direktori folder tersebut dengan perintah cd.

    ![g12](/minggu-03/g13.png)
* Penjelasan perintah pada CLI :

    $ php -v

    -Untuk mengecek versi php

    $ composer -V

    -Untuk mengecek versi composer

    $ git --version

    -Untuk mengecek versi git

    $ composer update

    -Untuk mengupdate atau memperbarui composer

    $ composer require alrik11es/cowsayphp

    -Untuk menambahakan dependensi tambahan atau library Cowsay

    $ heroku open cowsay
    
    -Untuk menjalankan atau membuka hasil app yang di deploy menggunakan php

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

