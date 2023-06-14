# Deploy Application with Localtunnel
<br/>

<br/>

## 1. Menjalankan apache agar bisa di akses melalui localtunnel
<br/>

1. Pertama-tama kita akan membutuhkan curl atau wget untuk mendownload nvm (node version manager), untuk tutorial kali ini saya akan menggunakan curl, unduh curl terlebih dahulu `sudo apt install curl`

![1](/week-1/Localtunnel/img/1.png)

<br/>

2. Setelah curl terinstall kita akan mendownload dan menjalankan script installasi untuk nvm dengan menjalankan `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash`

![2](/week-1/Localtunnel/img/2.png)

<br/>

3. Selanjutnya kita menjalankan comand `source ~/.bashrc` atau kita juga bisa mengetikan `exec bash` comand tersebut berfungsi seperti me refresh terminal kita dan memperbaharui path yang ada di file bashrc, disini kita akan bisa langsung menjalankan nvm, disini saya akan mendownload node.js versi 14 `nvm install 14` dan `nvm use 14`

![3](/week-1/Localtunnel/img/3.png)

<br/>

4. Selanjutnya install apche2 `sudo apt install apache2`

![4](/week-1/Localtunnel/img/4.png)

<br/>

5. Setelah terinstall coba cek apakah apache telah running, jika belum kita bisa mengetikan `sudo systemctl start apache2`

![5](/week-1/Localtunnel/img/5.png)

<br/>

6. Selanjutnya kita akan memasang localtunnel `npm install -g localtunnel` -g tersebut global, dan langkah terakhir tinggal menjalankan localtunnelnya `lt --port 80 --subdomain dumbways-awesome` kalian bisa memasukan alamat domain sesuka hati kalian.

![6](/week-1/Localtunnel/img/6.png)

<br/>

7. Masukan alamat domain yang ada di terminal kedalam web browser.

![7](/week-1/Localtunnel/img/7.png)

<br/>

8. Dan berikut tampilannya ketika saya mengaksesnya lewat smartphone/android.

![8](/week-1/Localtunnel/img/8.png)

<br/>

<br/>

## 2. Deploy website dumbflix dan bisa di akses melalui localtunnel

<br/>

1. Clone repositori dumbflix dengan comand `https://github.com/dumbwaysdev/dumbflix-frontend.git`

![1](/week-1/Localtunnel/img1/1.png)

<br/>

2. Selanjutnya masuk kedalam folder dumbflix dan `nano src/config/api.js` ubah portnya ke 3000

![2](/week-1/Localtunnel/img1/2.png)

<br/>

3. Ubah node.js ke versi 10 `nvm use 10` lalu jalankan `npm install`

![3](/week-1/Localtunnel/img1/3.png)

<br/>

4. Selanjutnya `npm run build` dan tunggu sampai selesai

![4](/week-1/Localtunnel/img1/4.png)

<br/>

5. Setelah selesai jalankan `npm install -g serve`

![5](/week-1/Localtunnel/img1/5.png)

<br/>

6. Setelah selesai ubah lagi versi node.js ke versi 14 lalu jalankan `serve -s build`

![6](/week-1/Localtunnel/img1/6.png)

<br/>

7. Setelah website telah di serving buka tab baru di shell dan login dengan ssh yang sama lalu masuk ke folder dumbflix, gunakan node.js versi 14 lalu jalankan `npm install -g localtunnel` untuk menginstall local tunnel secara global

![7](/week-1/Localtunnel/img1/7.png)

<br/>

8. lalu jalankan `lt --port 3000 --subdomain dumbflix` kita bebas ingin menggunakan domain apa saja disini saya menggunakan subdomain dumbflix.loca.lt

![8](/week-1/Localtunnel/img1/8.png)

<br/>

9. Selanjutnya buka browser dan masukan alamat subdomain localtunnel kita, saat pertama kali membuka kita akan disuruh memasukan end point, disini kita akan memasukan ip addres public kita lalu pencet submit

![9](/week-1/Localtunnel/img1/9.png)

<br/>

10. Setelah memasukan end point, kita akan di bawa masuk kedalam landing page halam dumbflix dengan menggunakan node.js dan juga localtunnel

![10](/week-1/Localtunnel/img1/10.png)
