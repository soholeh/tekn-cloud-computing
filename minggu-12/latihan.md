# Praktikum Teknologi Cloud Computing - Minggu 12 (Docker Orchestration Hands-on Lab)

1. Membuat container baru pada terminal node1.

    ![doh-1](doh-1.png)
    ![doh-2](doh-2.png)
    ```
    Disini menggunakan container terbaru dari ubuntu.
    ```

2. Melihat daftar container untuk memastikan bahwa container telah berhasil dibuat.

    ![doh-3](doh-3.png)

3. Menginisialisasi docker swarm.

    ![doh-4](doh-4.png)
    ![doh-5](doh-5.png)
    ```
    Disini kita mendapatkan token untuk menggabungkan dengan node lain nantinya.
    ```

4. Melihat informasi docker swarm pada node1.

    ![doh-6](doh-6.png)
    ![doh-7](doh-7.png)
    ![doh-8](doh-8.png)
    ```
    Node1 merupakan node untuk memanajemen node lainnya.
    ```

5. Menggabungkan node2 dan node3 kedalam swarm node1 dengan menggunakan token yang telah didapatkan sebelumnya.

    ![doh-9](doh-9.png)
    ![doh-10](doh-10.png)
    ```
    Disini node2 dan node3 telah bergabung dengan swarm node1 sebagai Worker nodes.
    ```

6. Melihat daftar node yang ada beserta keterangannya.

    ![doh-11](doh-11.png)
    ![doh-12](doh-12.png)

7. Mendeploy container.

    ![doh-13](doh-13.png)

8. Memastikan bahwa container telah berhasil di deploy.

    ![doh-14](doh-14.png)

9. Menjalankan layanan yang sama dengan skala 7.

    ![doh-15](doh-15.png)
    ![doh-16](doh-16.png)

10. Melihat layanan yang sedang berjalan.

    ![doh-17](doh-17.png)
    ![doh-18](doh-18.png)
    ![doh-19](doh-19.png)

11. Menjalankan kembali layanan yang sama namun dengan skala 4.

    ![doh-20](doh-20.png)
    ![doh-21](doh-21.png)

12. Melihat kembali layanan yang sedang berjalan.

    ![doh-22](doh-22.png)
    ![doh-23](doh-23.png)

13. Melihat daftar node yang ada.

    ![doh-24](doh-24.png)
    ![doh-25](doh-25.png)

14. Melihat daftar container.

    ![doh-26](doh-26.png)
    ![doh-27](doh-27.png)

15. Melihat kembali daftar node yang ada.

    ![doh-28](doh-28.png)
    ![doh-29](doh-29.png)

16. Mengubah availability node 2 menjadi drain.

    ![doh-30](doh-30.png)

17. Mengecek hasilnya.

    ![doh-31](doh-31.png)
    ![doh-32](doh-32.png)

18. Melihat container yang sedang berjalan pada node2.

    ![doh-33](doh-33.png)
    ```
    Disini kosong karena node2 availability sebelumnya telah diubah menjadi drain.
    ```

19. Melihat layanan yang sedang berjalan.

    ![doh-34](doh-34.png)
    ![doh-35](doh-35.png)
    ![doh-36](doh-36.png)
    ```
    Disini terlihat bahwasanya layanan yang menggunakan node2 terhenti karena sama seperti sebelumnya tadi.
    ```

20. Menghapus layanan.

    ![doh-37](doh-37.png)

21. Melihat daftar container yang ada.

    ![doh-38](doh-38.png)
    ![doh-39](doh-39.png)

22. Menghapus container.

    ![doh-40](doh-40.png)

23. Menhapus swarm pada node1, 2 dan 3.
    ![doh-41](doh-41.png)
