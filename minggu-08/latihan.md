# Praktikum Teknologi Cloud Computing - Minggu 7 (LATIHAN)

## Installasi Docker 

---
![insdock](install-docker.png) 
```
Pastikan telah mendownload Docker Desktop Installer melalui link yang telah disediakan.
Install Docker seperti terlihat pada gambar diatas.
```
---
## Setup dan Orientasi Docker

![set](gs-docker-01.png)
```
//cek versi docker
$ docker --version

//menjalankan docker image hello-world
$ docker run hello-world

//menampilkan seluruh struktur daftar image hello-world
$ docker container ls --all
```
---
## Build and run image

![bri](gs-docker-02.png)
```
//mengcloning repo berdasarkan url
$ git clone https://github.com/dockersamples/node-bulletin-board

//berpindah direktori
$ cd node-bulletin-board/bulletin-board-app

//build image docker
$ docker image build -t bulletinboard:1.0 .

//menjalankan container untuk melihat docker image nantinya secara local yakni pada localhost:8000
$ docker container run --publish 8000:8080 --detach --name bb bulletinboard:1.0

//menghapus container image
$ docker container rm --force bb
```
---
## Share image on Docker Hub

![share](gs-docker-03.png)
```
Sebelumnya kita harus membuat akun docker hub terlebih dahulu, jika sudah kita membuat repo baru dengan nama bulletinboard.

//share image kita ke docker hub
$docker image tag bulletinboard:1.0 soholeh/bulletinboard:1.0

//push image kita ke docker hub
$docker image push soholeh/bulletinboard:1.0

Untuk soholeh dapat disesuaikan dengan username dockerhub kita masing-masing.
Untuk bulletinboard:1.0 dapat disesuaikan juga pada image yg kita buat.

Untuk melihat hasilnya kita dapat membuka tab baru dan isikan url dengan localhost:8000
```
---

