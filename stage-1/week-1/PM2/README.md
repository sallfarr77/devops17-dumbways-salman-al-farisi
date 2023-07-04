# 1. Install PM2 secara global

pengertian pm2 : PM2 adalah sebuah alat manajemen proses untuk aplikasi Node.js yang diinstal melalui npm (Node Package Manager). Singkatan dari "Process Manager 2," PM2 dirancang untuk memudahkan pengelolaan aplikasi Node.js dalam lingkungan produksi.

# 2. Menjalankan PM2 dengan node js

1. Instal PM2 melalui npm dengan menjalankan perintah berikut di terminal: `npm install pm2 -g`.

![1](/week-1/PM2/img/1.png/)

2. Kemudian kita akan membuat script sederhana untuk node jsnya yang akan kita beri nama app `nano app.js` lalu tuliskan script kita didalamnya.

![2](/week-1/PM2/img/2.png/)

3. Setelah PM2 terinstal, jalankan aplikasi menggunakan PM2 dengan perintah: `pm2 start app.js`, PM2 akan memulai aplikasi dan menjalankannya sebagai proses latar belakang yang terkelola. Anda akan melihat output yang menampilkan informasi tentang proses yang sedang berjalan.

![3](/week-1/PM2/img/3.png/)

 4. Untuk memantau proses yang dijalankan oleh PM2, jalankan perintah: `pm2 monit`, Perintah ini akan menampilkan informasi pemantauan seperti penggunaan CPU, memori, dan log dari aplikasi.

![4](/week-1/PM2/img/4.png/)

<br/>

# 3. menjalankan PM2 dengan python

1. Buat file baru dengan nama "app.py" dan tambahkan kode berikut.

![5](/week-1/PM2/img/5.png/)

2. Setelah PM2 terinstal, jalankan aplikasi Python menggunakan PM2 dengan perintah berikut: `pm2 start app.py --name app --interpreter python3`
<br/>

![6](/week-1/PM2/img/6.png/)

`start`: Perintah untuk memulai aplikasi menggunakan PM2.
<br/>

`app.py`: Nama file aplikasi Python yang akan dijalankan.
<br/>

`--name app`: Menentukan nama proses yang akan digunakan dalam manajemen PM2. Dalam contoh ini, nama proses diatur sebagai "app".
<br/>

`--interpreter python3`: Menentukan interpreter yang digunakan untuk menjalankan aplikasi Python. Dalam contoh ini, interpreter Python3 akan digunakan.
<br/>

PM2 akan memulai aplikasi dan menjalankannya sebagai proses latar belakang yang terkelola. Anda akan melihat output yang menampilkan informasi tentang proses yang sedang berjalan.

4. Kita juga dapat menggunakan perintah `pm2 monit` untuk memantau proses yang dijalankan oleh PM2 dan melihat output dari aplikasi Python.

![7](/week-1/PM2/img/7.png/)

