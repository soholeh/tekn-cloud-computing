# Praktikum Teknologi Cloud Computing - Minggu 9 (Docker for Beginners - Linux)

## Login akun Docker

---
![dfb-1](dfb-1.png)

Untuk dapat mengakses terminal linux pada web ini yakni dengan login terlebih dahulu menggunakan akun Docker kita.

---
## Task 0: Prerequisites
---
Meng-clone repo dari github dengan nama linux_tweet_app pada akun dockersamples.

![dfb-2](dfb-2.png)

---
## Task 1: Run some simple Docker containers

**Run a single task in an Alpine Linux container**
1. Memulai container baru dengan image alpine

    ![dfb-3](dfb-3.png)

2. Melihat daftar semua container yang ada

    ![dfb-4](dfb-4.png)

**Run an interactive Ubuntu container**
1. Menjalankan Docker container dan mengakses terminal ubuntu

    ![dfb-5](dfb-5.png)
2. Menjalankan perintah berikut.

    ![dfb-6](dfb-6.png)
    ```
    //Menampilkan daftar folder atau file yang ada
    $ ls /

    //Menampilkan proses container yang sedang berjalan
    $ ps aux

    //Menampilkan distro linux yang container yang digunakan
    $ cat /etc/issue
    ```
3. Keluar dari terminal ubuntu

    ![dfb-7](dfb-7.png)

4. Cek versi host VM

    ![dfb-8](dfb-8.png)

**Run a background MySQL container**

1. Menjalankan MySQL container

    ![dfb-9](dfb-9.png)

2. Melihat daftar container

    ![dfb-10](dfb-10.png)

3. Cek log dan proses yang berjalan didalam container 

    ![dfb-11](dfb-11.png)
    ![dfb-12](dfb-12.png)

4. Melihat versi MySQL yang digunakan

    ![dfb-13](dfb-13.png)

5. Menghubungkan terminal ke sh

    ![dfb-14](dfb-14.png)
---
## Task 2: Package and run a custom app using Docker
---
**Build a simple website image**
1. Berpindah ke direktori repo yang telah di-clone sebelumnya

    ![dfb-15](dfb-15.png)
    ```
    //Melihat isi dari Dockerfile
    $ cat Dockerfile
    ```
2. Mengexport variabel dockerid dengan isian id docker kita

    ![dfb-16](dfb-16.png)
    ```
    //Menampilkan isi dari variabel dockerid
    $ echo $DOCKERID
    ```
3. Membuat docker image

    ![dfb-17](dfb-17.png)
4. Menjalankan container untuk menghosting image yang telah dibuat

    ![dfb-18](dfb-18.png)

5. Mengecek hasilnya dengan menekan link yang telah disediakan

    ![dfb-19](dfb-20.png)
    ![dfb-20](dfb-19.png)

6. Menghentikan dan menghapus container lalu mengeceknya

    ![dfb-21](dfb-40.png)
    ![dfb-22](dfb-21.png)
---
## Task 3: Modify a running website
**Start our web app with a bind mount**
1. Menjalankan container untuk menghosting image yang telah dibuat

    ![dfb-23](dfb-22.png)

2. Mengecek bahwasanya image berhasil di hosting dengan menekan link yang telah disediakan

    ![dfb-24](dfb-23.png)
    ![dfb-25](dfb-24.png)

**Modify the running website**
1. Meng-kopi index.html container dan merefresh web sblmnya untuk melihat hasilnya

    ![dfb-26](dfb-25.png)
    ![dfb-27](dfb-26.png)

2. Menghentikan dan menghapus container dan mengeceknya

    ![dfb-28](dfb-27.png)
    ![dfb-29](dfb-28.png)

**Update the image**
1. Membuat image baru

    ![dfb-30](dfb-29.png)

2. Melihat daftar image yang ada

    ![dfb-31](dfb-30.png)

**Test the new version**
1. Menjalankan container dan melihat hasilnya

    ![dfb-32](dfb-31.png)
    ![dfb-33](dfb-32.png)

2. Menjalankan container lainnya dan melihat hasilnya

    ![dfb-34](dfb-33.png)
    ![dfb-35](dfb-34.png)

**Push your images to Docker Hub**
1. Melihat daftar image yang telah di hosting

    ![dfb-36](dfb-35.png)

2. Sebelumnya login menggunakan akun docker kita agar tepat dan lancar di push atau upload pada akun docker kita

    ![dfb-37](dfb-36.png)

3. Push image versi 1.0 dan 2.0

    ![dfb-38](dfb-37.png)
    ![dfb-39](dfb-38.png)

4. Melihat hasil image yang telah di push pada akun docker hub kita masing-masing

    ![dfb-40](dfb-39.png)
---