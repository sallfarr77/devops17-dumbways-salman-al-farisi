# SSL w/Certbot

## 1.Tugas ini dimaksudkan untuk nantinta website kita agar merubah http menjadi https dengan bantuan Certbot, Langkah awal hampir sama dengan apt disini kita akan mengupdate terlebih dahulu akan tetapi dengan snapd `sudo snap install core; sudo snap refresh core`, jika sebelumnta kalian pernah install atau memiliki versi lain dari aplikasi certbot bisa kalian uninstall terlebih dahulu dengan `sudo apt-get remove certbot`.

![1](/stage-2/week-1/ssl-certbot/img/1.png)

## 2.Selanjutnya install aplikasi Cerbot dari snapd dengan comand `sudo snap install --classic certbot`, selanjutnya kita bisa memastikan bahwa certbot bisa dijalankan dengan comand `sudo ln -s /snap/bin/certbot /usr/bin/certbot` jika tidak terdapat pesan error maka kita bisa lanjut ketahap berikutnya.

![2](/stage-2/week-1/ssl-certbot/img/2.png)

## 3.Selanjutnya kita akan menjalankan script yang secara otomatis membuat setelan dan configurasi untuk website kita nantinya.

![3](/stage-2/week-1/ssl-certbot/img/3.png)

## 4.Kita juga dapat menjalankan renew certificates secara otomatis dengan `sudo certbot renew --dry-run` tanpa harus menjalankan sricpt lagi, kecuali jika kamu mengubah configurasi.

![4](/stage-2/week-1/ssl-certbot/img/4.png)

## 5.Selanjutnya kalian bisa cek kedalam website dan lihat icon gembok serta alamat url default kalian akan berubah dari http menjadi https.

![5](/stage-2/week-1/ssl-certbot/img/5.png)


