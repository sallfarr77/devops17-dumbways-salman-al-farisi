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

1.






