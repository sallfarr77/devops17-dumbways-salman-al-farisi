# Deploy Wayshub frontend/backend with nginx and cloudflare domain

## 1.Langkah pertama kita akan membuat dua vm terlebih dahulu di idcloudhost, 1 vm untuk deploy frontend dan backend, dan vm satunya lagi berfungsi reverse proxy yang nantinya kita akan install nginx.

![1](/stage-2/week-1/wayshub-&-nginx/img/1.png)

## 2.Langkah kedua saya akan membuat duam vm dengan nama Appserver dengan spesifikasi sebagai berikut : 2 CPU, 2 GB RAM, dan juga Gateway : 2 CPU, 1 GB RAM masing-masing dengan ram sebesar 20GB.

![2](/stage-2/week-1/wayshub-&-nginx/img/2.png)

## 3.Setelah vm telah dibuat selanjutnya kita tinggal masuk kedalam vm cloud kita bisa dengan ssh, disini saya login menggunakan PowerShell7, selanjutnya didalam tugas ini kita di haruskan menggunakan node v14, jika kalian sudah menginstall nvm bisa menggunakan comand `nvm use 14`. Selanjutnya clone repository frontend dan backend: `git clone https://github.com/dumbwaysdev/wayshub-frontend.git' dan `git clone https://github.com/dumbwaysdev/wayshub-backend.git'

![3](/stage-2/week-1/wayshub-&-nginx/img/3.png)

## 4.Selanjutnya menjalankan Mysql secure installation, sebelumnya kita perlu menginstallnya terlebih dahulu dengan `sudo apt install mysql-server` lalu kita bisa membuat username, pertama masuk sebagai root dulu: `sudo mysql -u root -p` setelah masuk buat username dan password dengan `CREATE USER 'UsernameKamu'@'localhost' IDENTIFIED WITH mysql_native_password BY 'PasswordKamu';` setelah itu kita akan memberikan acces kepada user ini dengan `GRANT SELECT, INSERT ON *.* TO 'UsernameKamu'@'%';` setelah itu `FLUSH PRIVILEGES;`.

![4](/stage-2/week-1/wayshub-&-nginx/img/4.png)

## 5.Setelah selesai melakukan secure installation, kita akan masuk kedalam repository frontend di dalam folder src/config/api.js dan kita akan ubah isi BaseURLnya.

![5](/stage-2/week-1/wayshub-&-nginx/img/5.png)

## 6.Tidak lupa kita akan rubah isi konfigurasi database MySQL di config/config.json, ada beberapa hal yang perlu kita perhatikan seperti isi username sama seperti yang sudah kalian buat, password serta nama databese yang akan kita berinama `db-wayshub`.

![6](/stage-2/week-1/wayshub-&-nginx/img/6.png)

## 7.Sekarang tinggal konfigurasi vm2 kita yang berinama gateway, sebelumnya install nginx `sudo apt install nginx` lalu masuk ke /etc/nginx dan buat folder baru dengan nama dumbways.

![7](/stage-2/week-1/wayshub-&-nginx/img/7.png)

## 8.Selanjutnya masuk kedalam folder dumbways yang sudah kita buat dan buat 2 config dengan nama frontend.conf serta backend.conf, selanjutnya kalian bisa edit seperti ini untuk frondendnya.

![8](/stage-2/week-1/wayshub-&-nginx/img/8.png)

## 9.Dan juga untuk backendnya, mohon untuk di perhatikan perihal port karna sangat penting, frontend akan berjalan di port 3000 dan backend akan berjalan di port 5000.

![9](/stage-2/week-1/wayshub-&-nginx/img/9.png)

## 10.Sebelum menjalankan nginx kita akan mengconfigurasi file nginx.conf yang nantinya akan berguna agar nginx bisa membaca file yang ada di folder dumbways.

![10](/stage-2/week-1/wayshub-&-nginx/img/10.png)

## 11.Setelah itu kita akan belakukan test dengan `sudo nginx -t` serta menjalankannya dengan `sudo systemctl reload nginx`.

![11](/stage-2/week-1/wayshub-&-nginx/img/11.png)

## 12.Selanjutnya masuk kedalam repo frontend dan kita akan menginstall module untuk webnya dengan `npm install`, jika kamu menjalankan pm2 start mungkin akan mendapati pesan error karna file ecosystem.config.js belum dibuat.

![12](/stage-2/week-1/wayshub-&-nginx/img/12.png)

## 13.Kalian bisa membuatnya terlebih dahulu dan menuliskannya seperti ini dan lakukan hal yang sama pada repo backendnya, jika sudah kalian bisa menjalankan `pm2 start`

![13](/stage-2/week-1/wayshub-&-nginx/img/13.png)

## 14.Kalian bisa mengecheck web yang sudah dibuat dengan nama domain kalian.

![14](/stage-2/week-1/wayshub-&-nginx/img/14.png)

## 15.Jika kalian mendapati kesulitan saat login dan tidak bisa conect kedatabsae, kita bisa menggunakan `sequelize-cli db:create` untut membuat database db-wayshub, dan juga `squelize-cli db:migrate`.

![15](/stage-2/week-1/wayshub-&-nginx/img/15.png)

## 16.Disini saya akan membuat akun dengan nama sallfarr dan tunggu sampai loading selesai.

![16](/stage-2/week-1/wayshub-&-nginx/img/16.png)

## 17.Jika sudah tinggal login dengan akun yang sudah kita buat, dan jika database kamu sudah benar makan kalian akan bisa masuk kedalam dashboard dengan tampilan seperti ini.

![17](/stage-2/week-1/wayshub-&-nginx/img/17.png)
