# Praktikum Teknologi Cloud Computing - Minggu 14 (Kubernetes for Beginners)

1. Menjalankan perintah ls.

    ![kfb-1](kfb-1.png)

2. Inisialisasi cluster.

    ![kfb-2](kfb-2.png)
    ```
    Terlihat bahwasanya cluster telah berhasil di inisialisasi.
    ```
3. Menjalankan perintah kubectl apply -n kube-system -f \
    "https://cloud.weave.works/k8s/net?k8s-version=$(kubectl version | base64 |tr -d '\n')".

    ![kfb-3](kfb-3.png)

4. Mengcloning repository dockercoins.

    ![kfb-4](kfb-4.png)

5. Berpindah ke direktori hasil repo yang telah berhasil di clone dan menjalankan perintah docker-compose up.

    ![kfb-5](kfb-5.png)

6. Menjalankan perintah kubectl get node.

    ![kfb-6](kfb-6.png)
    ```
    Terlihat bahwasanya terdapat 1 buah node yang siap digunakan.
    ```
7. Menjalankan perintah kubectl get nodes -o wide.

    ![kfb-7](kfb-7.png)
    ```
    Terlihat bahwasanya terdapat 1 buah node yang siap digunakan.
    ```
8. Menjalankan perintah kubectl get no -o yaml.

    ![kfb-8](kfb-8.png)
    ![kfb-9](kfb-9.png)
    ```
    Terlihat bahwasanya menampilkan informasi yang lebih detail.
    ```
9. Menjalankan perintah kubectl get nodes -o json |
      jq ".items[] | {name:.metadata.name} + .status.capacity".

    ![kfb-10](kfb-10.png)
    ![kfb-11](kfb-11.png)
    ```
    Terlihat bahwasanya menampilkan informasi node dengan format JSON.
    ```
10. Menjalankan perintah kubectl get services.
    ![kfb-12](kfb-12.png)
    ```
    Terlihat bahwasanya menampilkan service kubernetes yang sedang berjalan.
    ```

