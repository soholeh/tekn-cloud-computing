# Praktikum Teknologi Cloud Computing - Minggu 11 (Application Containerization & Microservice Orchestration)

## Setup

![acmo-1](acmo-1.png)
```
//Mengclone repository dari url github
$ git clone https://github.com/ibnesayeed/linkextractor.git

//Berpindah ke direktori linkextractor
$ cd linkextractor

//Berpindah ke branch demo
$ git checkout demo
```
---
## Step 0: Basic Link Extractor Script

![acmo-4](acmo-4.png)
```
//Berpindah ke branch step0
$ git checkout step0

//Menampilkan struktur folder
$ tree
```
![acmo-5](acmo-5.png)
```
//Menampilkan isi file linkextractor.py
$ cat linkextractor.py

//Menjalankan file linkextractor.py
$ ./linkextractor.py http://example.com/
```
![acmo-6](acmo-6.png)
```
//Melihat hak/izin akses file linkextractor.py
$ ls -l linkextractor.py

//Menjalankan file linkextractor.py
$ python linkextractor.py
```
---
## Step 1: Containerized Link Extractor Script

![acmo-7](acmo-7.png)
```
//Berpindah ke branch step1
$ git checkout step1

//Menampilkan struktur folder
$ tree
```
![acmo-8](acmo-8.png)
![acmo-9](acmo-9.png)
![acmo-10](acmo-10.png)
```
//Menampilkan isi file Dockerfile
$ cat Dockerfile

//Membuat image
$ docker image build -t linkextractor:step1 .

//Menampilkan daftar image
$ docker image ls

//Menjalankan container
$ docker container run -it --rm linkextractor:step1 http://example.com/
```
![acmo-11](acmo-11.png)
```
//Menjalankan container
$ docker container run -it --rm linkextractor:step1 https://training.play-with-docker.com/
```
---
## Step 2: Link Extractor Module with Full URI and Anchor Text

![acmo-12](acmo-12.png)
```
//Berpindah ke branch step2
$ git checkout step2

//Menampilkan struktur folder
$ tree
```
![acmo-13](acmo-13.png)
```
//Menampilkan isi file linkextractor.py
$ cat linkextractor.py
```
![acmo-14](acmo-14.png)
```
//Membuat image
$ docker image build -t linkextractor:step2 .
```
![acmo-15](acmo-15.png)
```
//Menampilkan daftar image
$ docker image ls
```
![acmo-16](acmo-16.png)
```
//Menjalankan container
$ docker container run -it --rm linkextractor:step2 https://training.play-with-docker.com/
```
![acmo-17](acmo-17.png)
```
//Menjalankan container
$ docker container run -it --rm linkextractor:step1 https://training.play-with-docker.com/
```
---
## Step 3: Link Extractor API Service
![acmo-18](acmo-18.png)
```
//Berpindah ke branch step3
$ git checkout step3

//Menampilkan struktur folder
$ tree
```
![acmo-19](acmo-19.png)
```
//Menampilkan isi file Dockerfile
$ cat Dockerfile
```
![acmo-20](acmo-20.png)
```
//Menampilkan isi file main.py
$ cat main.py
```
![acmo-21](acmo-21.png)
```
//Membuat image
$ docker image build -t linkextractor:step3 .
```
![acmo-22](acmo-22.png)
```
//Menjalankan container
$ docker container run -d -p 5000:5000 --name=linkextractor linkextractor:step3

//Menampilkan daftar container
$ docker container ls
```
![acmo-23](acmo-23.png)
```
//Membuat permintaan HTTP
$ curl -i http://localhost:5000/api/http://example.com/
```
![acmo-24](acmo-24.png)
```
//Melihat catatan container
$ docker container logs linkextractor

//Menghapus container
$ docker container rm -f linkextractor
```
---
## Step 4: Link Extractor API and Web Front End Services

![acmo-25](acmo-25.png)
```
//Berpindah ke branch step4
$ git checkout step4

//Menampilkan struktur folder
$ tree
```
![acmo-26](acmo-26.png)
```
//Menampilkan isi file docker-compose.yml
$ cat docker-compose.yml
```
![acmo-27](acmo-27.png)
```
//Menampilkan isi file www/index.php
$ cat www/index.php
```
![acmo-28](acmo-28.png)
```
//Menjalankan layanan docker compose
$ docker-compose up -d --build
```
![acmo-29](acmo-29.png)
```
//Menampilkan daftar container
$ docker container ls
```
![acmo-30](acmo-30.png)
```
//Menghubungakan dengan layanan API
$ curl -i http://localhost:5000/api/http://example.com/
```
Mengakses web Link Extractor

![acmo-31](acmo-31.png)
![acmo-32](acmo-32.png)
```
//Memodifikasi index file link extractor
$ sed -i 's/Link Extractor/Super Link Extractor/g' www/index.php
```
Mengakses web Link Extractor yang telah di ubah

![acmo-33](acmo-33.png)
![acmo-34](acmo-34.png)
```
//Mereset atau mengembalikan perubahan
$ git reset --hard

//Menghentikan layanan
$ docker-compose down
```
---
## Step 5: Redis Service for Caching

![acmo-35](acmo-35.png)
```
//Berpindah ke branch step5
$ git checkout step5

//Menampilkan struktur folder
$ tree
```
![acmo-36](acmo-36.png)
```
//Menampilkan isi file www/Dockerfile
$ cat www/Dockerfile
```
![acmo-37](acmo-37.png)
```
//Menampilkan isi file api/main.py
$ cat api/main.py
```
![acmo-38](acmo-38.png)
```
//Menampilkan isi file docker-compose.yml
$ cat docker-compose.yml
```
![acmo-39](acmo-39.png)
```
//Menjalankan layanan
$ docker-compose up -d --build
```
Mengakses web Link Extractor

![acmo-40](acmo-40.png)
![acmo-41](acmo-41.png)
![acmo-42](acmo-42.png)
```
//Membuaka client redis
$ docker-compose exec redis redis-cli monitor

//Memodifikasi index file link extractor
$ sed -i 's/Link Extractor/Super Link Extractor/g' www/index.php

//Mereset atau mengembalikan perubahan
$ git reset --hard

//Menghentikan layanan
$ docker-compose down
```
---
## Step 6: Swap Python API Service with Ruby

![acmo-43](acmo-43.png)
```
//Berpindah ke branch step6
$ git checkout step6

//Menampilkan struktur folder
$ tree
```
![acmo-44](acmo-44.png)
```
//Menampilkan isi file api/linkextractor.rb
$ cat api/linkextractor.rb
```
![acmo-45](acmo-45.png)
```
//Menampilkan isi file api/Dockerfile
$ cat api/Dockerfile
```
![acmo-46](acmo-46.png)
```
//Menampilkan isi file docker-compose.yml
$ cat docker-compose.yml
```
![acmo-47](acmo-47.png)
```
//Menjalankan layanana
$ docker-compose up -d --build
```
![acmo-48](acmo-48.png)
```
//Menghubungkan layananan
$ curl -i http://localhost:4567/api/http://example.com/
```
Mengakses web link extractor
![acmo-49](acmo-49.png)

Menguji sebuah url untuk di extract
![acmo-50](acmo-50.png)
![acmo-51](acmo-51.png)
```
//Menghentikan layanan
$ docker-compose down

//Melihat catatan sebuah web yang telah di extract
$ cat logs/extraction.log
```
---