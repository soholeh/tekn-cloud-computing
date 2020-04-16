# Praktikum Teknologi Cloud Computing - Minggu 8 (LATIHAN)

## Step 1: Setup

---
1. Membuat folder proyek

    ![gs1](gs-1.png)
    ```
    //Membuat folder baru dengan nama composetest
    $ mkdir composetest

    //Berpindah ke folder composetest
    $ cd composetest/

    //Membuka code editor vscode
    $ code .
    ```
2. Membuat file app.py

    ![gs2](gs-2.png)
    >[File app.py](app.py)
3. Membuat file requirements.txt

    ![gs3](gs-3.png)
    >[File requirements.txt](requirements.txt)

---
## Step 2: Create a Dockerfile
---
![gs4](gs-4.png)
>[File Dockerfile](Dockerfile)
---
## Step 3: Define services in a Compose file

![gs5](gs-5.png)
>[File docker-compose.yml](docker-compose.yml)
---
## Step 4: Build and run your app with Compose
---
1. Menjalankan perintah docker-compose up

    ![gs6](gs-6.png)
    ```
    //Mulai menjalankan aplikasi
    $ docker-compose up
    ```
2. Membuka url http://localhost:5000/ untuk melihat hasilnya

    ![gs7](gs-7.png)
3. Merefresh halaman

    ![gs8](gs-8.png)
4. Membuka terminal lain dan menjalankan perintah docker image ls

    ![gs9](gs-9.png)
    ```
    //Melihat daftar lokal image
    $ docker image ls
    ```
---
## Step 5: Edit the Compose file to add a bind mount

![gs10](gs-10.png)
>[File docker-compose.yml](docker-compose.yml)
---
## Step 6: Re-build and run the app with Compose
1. Menjalankan perintah docker-compose up

    ![gs11](gs-11.png)
    ```
    //Mulai menjalankan aplikasi
    $ docker-compose up
    ```
2. Mengecek pada browser

    ![gs12](gs-12.png)

---
## Step 7: Update the application
1. Merubah file app.py
    ![gs13](gs-13.png)
    >[File app.py](app.py)

2. Mengecek hasilnya pada browser

    ![gs14](gs-14.png)
---
## Step 8: Experiment with some other commands
1. Menjalankan perintah docker lainnya

    ![gs15](gs-15.png)
    ```
    //Menjalankan aplikasi pada latar belakang
    $ docker-compose up -d

    //Melihat aplikasi yang sedang berjalan
    $ docker-compose ps
    ```
2. Menjalankan perintah docker lainnya

    ![gs16](gs-16.png)
    ```
    //Menjalankan dan melihat variabel yang tersedia
    $ docker-compose run web env

    //Menghentikan aplikasi
    $ docker-compose stop

    //Menghapus containers
    $ docker-compose down --volumes
    ```