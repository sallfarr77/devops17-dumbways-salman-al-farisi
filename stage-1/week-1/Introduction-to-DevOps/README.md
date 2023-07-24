## 1. DevOps 
DevOps adalah suatu pendekatan kolaboratif dan berkelanjutan dalam pengembangan software yang mengintegrasikan tim pengembangan (developers) dan tim operasi (operations) dengan tujuan untuk meningkatkan efisiensi, keamanan, kualitas, dan kecepatan pengiriman software. DevOps bertujuan untuk memperpendek siklus pengembangan software dari konsep hingga produksi, dengan mengotomatiskan proses pengujian, pengiriman, dan penerapan.

## 2. lifecycle DevOps ada 4 di antaranya adalah

   1. Continuous Integration, Continuous Integration atau (CI) adalah praktik pengembangan software yang bertujuan untuk secara otomatis menggabungkan dan memverifikasi perubahan kode yang dilakukan oleh para pengembang dalam repositori bersama secara teratur.

   2. Continuous Delivery, Continuous Delivery atau (CD) adalah pendekatan dalam pengembangan perangkat lunak yang memungkinkan tim untuk menghasilkan perubahan kode yang dapat dipasang dan diimplementasikan ke dalam lingkungan produksi secara otomatis dan secara berkala.

   3. Continuous Deployment, Continuous Deployment atau (CD) adalah pendekatan dalam pengembangan software yang secara otomatis dan terus-menerus menerapkan perubahan kode yang lulus melalui proses Continuous Integration (CI) dan Continuous Delivery ke dalam lingkungan produksi secara langsung. Dalam Continuous Deployment, setiap kali perubahan kode dianggap stabil dan siap, perubahan tersebut akan secara otomatis diterapkan ke lingkungan produksi tanpa campur tangan manusia.

   4. Continuous Monitoring, Continuous Monitoring atau (CM) adalah proses pengawasan dan pemantauan terus-menerus terhadap sistem, aplikasi, infrastruktur, atau lingkungan IT secara keseluruhan untuk mendeteksi perubahan, ancaman keamanan, masalah performa, atau ketidaksesuaian dengan kebijakan yang ditetapkan.
   
   
## 3. Berikut adalah langkah-langkah dan cara saya menginstallasi Ubuntu Server menggunakan Virtualbox

1. Langkah pertama adalah membuka software vm yang kita sudah punya terlebih dahulu lalu mengklik tombol 'new' di pojok atas.

![1](/stage-1/week-1/Introduction-to-DevOps/img/1.png)

2. Langkah selanjutnya adalah mengisi username dan password untuk akun vm kita

![2](/stage-1/week-1/Introduction-to-DevOps/img/2.png)

3. Selanjutnya anda bisa menconfigurasi untuk ram, stroge dan core yang anda ingin dedikasikan untuk vm, untuk tugas kali ini saya meng-alokasikan ram sebesar 2GB, 1 core, dan 10 GB stroge, ketika telah yakin klik `finish`

![3](/stage-1/week-1/Introduction-to-DevOps/img/3.png)

4. Jika telah selesai, jangan lupa untuk mengconfigurasi network kita juga lewat setting yang ada di vmnya, saya akan menggunakan bridge adapter.

![4](/stage-1/week-1/Introduction-to-DevOps/img/4.png)

5. Tunggu sampai ubuntu berjalan sampai kita di sambut untuk memilih bahasa, disini saya menyarankan menggunakan bahasa inggris

![5](/stage-1/week-1/Introduction-to-DevOps/img/5.png)

6. Selanjutnya kita bisa memilih ubuntu server, untuk search for third party drivers itu opsional

![6](/stage-1/week-1/Introduction-to-DevOps/img/6.png)

7. Selanjutnya kita akan mengubah ipv4 kita dari dinamis ke statis, pertama-tama kita harus memperhatikan ipconfig kita yang ada di windows dari mulai subnet hingga gateway, lalu selanjutnya kita bisa mengisi sesuai format yang ada.

![7](/stage-1/week-1/Introduction-to-DevOps/img/7.png)

8. berikut adalah configurasi ip statis yang saya gunakan 

![8](/stage-1/week-1/Introduction-to-DevOps/img/8.png)

9. Untuk selanjutnya kita akan dimintai commit untuk menyimpan configurasi yang telah kita pilih, mohon di perhatikan tindakan ini tidak akan bisa di ubah nantinya ( bisa saja di ubah akan tetapi akan lebih sulit ).

![9](/stage-1/week-1/Introduction-to-DevOps/img/9.png)

10. Setelah kita commit langkah terakhir kita akan membuat aku untuk ubuntu kita, mohon di inggat akun ubuntu berbeda dari akun Vm ubuntu yang telah kita buat di awal.

![10](/stage-1/week-1/Introduction-to-DevOps/img/10.png)

11. Langkah selanjutnya  adalah install ssh, disarankan untuk menginstall karna akan sangat berguna untuk projek kita.

![11](/stage-1/week-1/Introduction-to-DevOps/img/11.png)

12. Disini kita akan menunggu instalasi di Vm yang mungkin sangat lama, tergantung dari spec dan device yang kita gunakan, jika berhasil tampilannya akan seperti ini, kita tinggal masukan akun ubuntu yang suda kita buat saat installasi.

![12](/stage-1/week-1/Introduction-to-DevOps/img/12.png)

13. Langkah terakhir kita bisa mengecek koneksi internet kita denga comand `ping google`, dan jika berhasil selamat kita telah berhasil menginstall dan menconfigurasi ubuntu server di mode Vm

![13](/stage-1/week-1/Introduction-to-DevOps/img/13.png)























