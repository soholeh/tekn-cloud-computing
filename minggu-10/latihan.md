# Praktikum Teknologi Cloud Computing - Minggu 10 (Docker Networking)

## Login akun Docker

---
![dnh-1](dnh-1.png)

Untuk dapat mengakses terminal linux pada web ini yakni dengan login terlebih dahulu menggunakan akun Docker kita.

---
## Section #1 - Networking Basics
---
**Step 1: The Docker Network Command**

![dnh-2](dnh-2.png)
```
//Merupakan perintah utama untuk konfigurasi dan mengelola container networks
$ docker network
```

**Step 2: List networks**

![dnh-3](dnh-3.png)
```
//Menampilkan daftar container networks
$ docker network ls
```
**Step 3: Inspect a network**

![dnh-4](dnh-4.png)
```
//Melihat detail konfigurasi jaringan
$ docker network inspect bridge
```
**Step 4: List network driver plugins**

![dnh-5](dnh-5.png)
```
//Melihat informasi mengenai installasi Docker
$ docker info
```
---
## Section #2 - Bridge Networking
---
**Step 1: The Basics**

![dnh-6](dnh-6.png)
![dnh-7](dnh-7.png)
![dnh-8](dnh-8.png)
![dnh-9](dnh-9.png)
![dnh-10](dnh-10.png)
```
//Menampilkan daftar container networks
$ docker network ls

//Mengupdate dan install packages bridge-utils
$ apk update

//Menambahkan packages bridge-utils
$ apk add bridge

//Menampilkan daftar bridges pada Docker host 
$ brctl show

//Melihat detail bridge
$ ip a
```
**Step 2: Connect a container**

![dnh-11](dnh-11.png)
![dnh-12](dnh-12.png)
![dnh-13](dnh-13.png)
![dnh-14](dnh-14.png)
```
//Membuat container baru
$ docker run -dt ubuntu sleep infinity

//Melihat spek container network
$ docker ps

//Menampilkan daftar bridges pada Docker host 
$ brctl show

//Menampilkan lampiran pada container bridge
$ docker network inspect bridge
```
**Step 3: Test network connectivity**

![dnh-15](dnh-15.png)
![dnh-16](dnh-16.png)
![dnh-17](dnh-17.png)
![dnh-18](dnh-18.png)
![dnh-19](dnh-19.png)
```
//Mengetes jaringan (ping)
$ ping -c5 172.17.0.2

//Melihat spek container network
$ docker ps

//Masuk terminal ubuntu
$ docker exec -it yourcontainerid /bin/bash

//Menginstall program ping
$ apt-get update && apt-get install -y iputils-ping

//Mengetes jaringan (ping)
$ ping -c5 www.github.com

//Keluar dari terminal ubuntu
$ exit

//Menghentikan container yang sedang berjalan
$ docker stop yourcontainerid
```
**Step 4: Configure NAT for external connectivity**

![dnh-20](dnh-20.png)
![dnh-21](dnh-21.png)
![dnh-22](dnh-22.png)
```
//Menjalankan container baru dari official NGINX image
$ docker run --name web1 -d -p 8080:80 nginx

//Melihat spek container network
$ docker ps

//Menghubungkan ke docker host
$ curl 127.0.0.1:8080
```
---
## Section #3 - Overlay Networking
---
**Step 1: The Basics**

![dnh-23](dnh-23.png)
![dnh-24](dnh-24.png)
![dnh-25](dnh-25.png)
```
//Menginisialisasi docker swarm baru
$ docker swarm init --advertise-addr $(hostname -i)

//Menggabungkan node
$ docker swarm join \
>     --token SWMTKN-1-69b2x1u2wtjdmot0oqxjw1r2d27f0lbmhfxhvj83chln1l6es5-37ykdpul0vylenefe2439cqpf \
>     10.0.0.5:2377

//Melihat daftar node
$ docker node ls
```
**Step 2: Create an overlay network**

![dnh-26](dnh-26.png)
![dnh-27](dnh-27.png)
![dnh-28](dnh-28.png)
![dnh-29](dnh-29.png)
```
//Membuat sebuah overlay network
$ docker network create -d overlay overnet

//Mengecek/menampilkan network
$ docker network ls

//Melihat lebih detail informasi mengenai overnet network
$ docker network inspect overnet
```
**Step 3: Create a service**

![dnh-30](dnh-30.png)
![dnh-31](dnh-31.png)
![dnh-32](dnh-32.png)
![dnh-33](dnh-33.png)
```
//Membuat layanan baru
$ docker service create --name myservice \
--network overnet \
--replicas 2 \

//Mengecek/menampilkan daftar layanan
$ docker service ls

//Melihat daftar layanan yang sedang berjalan
$ docker service ps myservice

//Mengecek/menampilkan network
$ docker network ls

//Melihat lebih detail informasi mengenai overnet network
$ docker network inspect overnet
```
**Step 4: Test the network**

![dnh-34](dnh-34.png)
![dnh-35](dnh-35.png)
```
//Melihat lebih detail informasi mengenai overnet network
$ docker network inspect overnet

//Melihat spek container network
$ docker ps
```
---
## Cleaning Up

![dnh-36](dnh-36.png)
![dnh-37](dnh-37.png)
![dnh-38](dnh-38.png)
```
//Menghspus layanan
$ docker service rm myservice

//Melihat spek container network
$ docker ps

//Menghapus node
$ docker swarm leave --force
```
---