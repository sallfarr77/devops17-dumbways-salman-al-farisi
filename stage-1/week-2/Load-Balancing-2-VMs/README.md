# 1.Buat 2 VM untuk penggunaan

1.Langkah awal adalah membuat Vm baru terlebih dahulu baik itu di virtualbox maupun di vmware, disini saya menggunakan ssh untuk menjalankan 2 Vm tersebut dengan dua tab, ditab pertama saya menjalankan Vm pertama yang di awal tadi sudah menginstall nginx dan segala configurasinya, lalu di tab kedua adalah Vm baru yang saya buat dengan nama @server2 berjalan di ip 192.168.1.202.

![1](/stage-1/week-2/Load-Balancing-2-VMs/img/1.png)
<br/>

2.Selanjutnya adalah kita akan mengedit file yang ada di /etc/host dengan menambahkan ip Vm kedua kita beserta nama domainnya dengan cara `sudo nano /etc/hosts`

![2](/stage-1/week-2/Load-Balancing-2-VMs/img/2.png)
<br/>

3.Dan tentu saja kalian juga harus mengedit file host yang ada di windows kalian juga coppy alamat berikut: `C:\Windows\System32\drivers\etc` lalu edit file hostsnya dengan menambahkan ip dan domain dari server2, pastikan menggunakan administrator agar mendapat akses untuk mengedit.

![3](/stage-1/week-2/Load-Balancing-2-VMs/img/3.png)
<br/>

4.Setelah selesai masuk kedalam Vm ke-2 kalian, pastikan tidak ada nginx yang terinstall dengan cara `nginx -v`, karna disini Vm baru jadi kita akan mendapatkan pesan bahwa nginx belum terinstall.

![4](/stage-1/week-2/Load-Balancing-2-VMs/img/4.png)
<br/>

5.Selanjutnya masuk ke folder dumbflix yang ada di Vm2 dua install nvm dan node.js, setelah terinstall jalankan `npm install` dan `npm run build` tunggu saya proses instalasi selesai.

![5](/stage-1/week-2/Load-Balancing-2-VMs/img/5.png)
<br/>

6.Selanjutnya adalah menginstall serve dengan cara `npm install -g serve` dan jangan lupa install pm2 juga yang nantinya akan kita gunakan `npm install -g pm2`.

![6](/stage-1/week-2/Load-Balancing-2-VMs/img/6.png)
<br/>

7.Setelah selesai semuanya kita bisa menjalankan pm2 di Vm2 dengan perintah `pm2 serve build` pm2 akan membuild website dumbflix dan memberikan info seperti status, cpu atau seberapanyak memory yang terpakai, jangan lupa jalankan juga di Vm1.

![7](/stage-1/week-2/Load-Balancing-2-VMs/img/7.png)
<br/>

8.Dilangkah sebelumnya pm2 memberikan informasi bahwa website kita telah berjalan di port 8080 mari kita cek, buka browser dan ketikan ip addres kita disini saya akan mengetikannya jadi `192.168.1.202:8080`, kita juga bisa membukanya dengan alamat domain yang barusan sudah kita buat kalau disaya alamat jadi `dumbflix-salman.xyz`.

![8](/stage-1/week-2/Load-Balancing-2-VMs/img/8.png)
<br/>

9.Disini ada use case menarik saat kita memberhentikan pm2 di Vm1 ternyata website dengan domain `dumbflix-salman.xyz` masih bisa diakses maupun sebaliknya, kesimpulannya tentu saja cara seperti ini bisa sangat berguna saat kita memanage sebuah server yang penting dan harus selalu online setiap saat, disaat nanti satu komputer mati website tidak akan ikut mati karna ada komputer yang lain yang menghandlenya, hal tersebut tentu akan menjadi sebuah keuntungan yang besar bagi perusahaan dan pekerjaan kita.

![9](/stage-1/week-2/Load-Balancing-2-VMs/img/9.png)
<br/>



