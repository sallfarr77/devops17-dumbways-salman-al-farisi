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

<br/>

## 2. Deploy website dumbflix dan bisa di akses melalui localtunnel

<br/>

1. Clone repositori dumbflix dengan comand `https://github.com/dumbwaysdev/dumbflix-frontend.git`

![1](/week-1/Localtunnel/img1/1.png)

<br/>

2. Selanjutnya masuk kedalam folder ways
