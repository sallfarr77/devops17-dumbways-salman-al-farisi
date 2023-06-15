# 1.Berikut adalah cara instal nginx dari apt beserta mengaktifkannya
<br/>

 1.`sudo apt install nginx` comand tersebut akan menginstall nginx kedalam os ubuntu kita, setelah selesai install jika nginx kita belum aktif kita dapat mengaktifkannya dengan comand `sudo systemctl enable nginx && sudo systemctl start nginx` perintah tersebut akan mengaktifkan dan menjalankan nginx di sistem operasi kita.

![1](/week-2/Web-Server-and-Load-Balancing/img/1.png)
<br/>

2.Untuk lebih memastikan bahwa nginx sudah berjalan di sistem kita dapat pengecek status nginx dengan comand `sudo systemctl status nginx` , indikator warna hijau menandakan bahwa nginx kita sedang berjalan.

![2](/week-2/Web-Server-and-Load-Balancing/img/2.png)
<br/>

# 2.menjalankan aplikasi dumbflix menggunakan PM2

<br/>
1.Selanjutnya masuk ke dalam folder dumbflix dan jalankan `npm install` ini akan memasang semua dependensi dan module yang di perlukan untuk mendeploy si website dumblix, lalu jalankan `npm run build` ini akan membangun dan membuat folder build yang nantinya bisa kita gunakan untuk deploy website, terakhir jalankan `npm install -g serve` comand tersebut akan memasang serve secara global.

![3](/week-2/Web-Server-and-Load-Balancing/img/3.png)
<br/>

2.Selanjutnya kita akan memasang pm2 jalankan perintah `npm install -g pm2` npm akan menginstall pm2 secara global yang nantinya sangat berguna.

![4](/week-2/Web-Server-and-Load-Balancing/img/4.png)
<br/>

3.Setelah pm2 telah berhasil terinstall maka selanjutnya kita bisa langsung mendeploy website kita dengan comand `pm2 serve build` disini kita menjankannya dengan pm2 dari pada dengan npm, dan disana kita bisa melihat status dan informasti yang sangat bermanfaat dari pm2.

![5](/week-2/Web-Server-and-Load-Balancing/img/5.png)
<br/>

4.Terkahir kita bisa mengecek kedalam browser bahwa website kita telah berhasil di jalanlan disini kita akan mengetikan alamat ip computer kita beserta portnya yaitu 8080

![6](/week-2/Web-Server-and-Load-Balancing/img/6.png)
<br/>

# 3.Membuat konfigurasi reverse proxy menguunakan 2 server didalam Vm
<br/>

1.Masuk kedalam folder nginx dengan cara `cd /etc/nginx` lalu kita akan membuat folder didalam folder nginx `sudo mkdir dumbways && cd dumbways` kita harus menggunakan sudo jika ingin berinteraksi didalam folder etc karna folder etc sendiri masuk kedalam folder sistem root di linux, setelah masuk ke dalam folder dumbways kita akan membuat proxy dengan cara `sudo nano reverse-proxy.conf`.

![7](/week-2/Web-Server-and-Load-Balancing/img/7.png)
<br/>

2.Kalian bisa mengikuti tulisan seperti saya yang ada di bawah ini, dengan catatan menggunakan ip komputer kalian sendiri beserta menggunakan port 8080.

![8](/week-2/Web-Server-and-Load-Balancing/img/8.png)
<br/>

3.Selanjutnya kita akan mengedit file config di nginx yang kita punya dengan menggunakan `sudo nano /etc/nginx/nginx.conf`.

![9](/week-2/Web-Server-and-Load-Balancing/img/9.png)
<br/>

4.Kalian bisa menambahkan include seperti gambar yang ada di bawah ini, tulisan tersebut berfungsi sebagai akan memberitahu nginx bahwa akan membaca semua yang ada didalam folder dumbways termasuk config proxy yang sudah kita buat sebelumnya.

![10](/week-2/Web-Server-and-Load-Balancing/img/10.png)
<br/>

5.Setelah selesai mengedit file nginx.conf kita bisa mengecek bahwa systanx yang sudah kita tulis aman dan tidak ada eror dengan menulisakn `sudo nginx -t` dan jika mendapatkan pesan OK succesfull kita dapat melanjutkan ketahap berikutnya yaitu me reload nginx dengan cara `sudo systemctl reload nginx`.

![11](/week-2/Web-Server-and-Load-Balancing/img/11.png)
<br/>

6.Langkah selanjutnya kita harus mengedit file host yang ada di windows kita disini kalian bisa mengcopy path untuk masuk kedalam foldernya `C:\Windows\System32\drivers\etc` disana akan ada folder hosts dan buka dengan notedpad, pastikan menjalankannya dengan administrator agar kalian dapat mendedit file tersebut, selanjutnya masukan alamat ip kalian beserta nama webnya.

![12](/week-2/Web-Server-and-Load-Balancing/img/12.png)
<br/>

7.Untuk langkah terakhir kalian bisa masuk kedalam browser dan memasukan alamat domain disini karna saya membuatnya dengan nama dumbflix-salman maka saya mengetikan dumbflix-salman.xyz, dan jika berhasil kalian bisa melihat website dumbflix dengan custom domain yang telah kalian buat.

![13](/week-2/Web-Server-and-Load-Balancing/img/13.png)
<br/>

8.Edit reverse-proxy untuk mengarahkan lalu lintas ke server backend yang terdaftar dalam blok upstream seperti gambar dibawah

![14](/week-2/Web-Server-and-Load-Balancing/img/14.png)
<br/>













