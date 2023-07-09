# Membuat vm dan meluncurkan website dengan aws

## 1.Pertama kamu harus membuat akun aws terlebih dahulu jika sudak masuk kedalam dahsboard dan kita akan membuat key Pairs agar vm kita bisa login nantinya lewat ssh.

![1](/stage-2/week-1/deploy-using-aws/img/1.png)

## 2.Selanjutnya kalian bisa memasukan rsa.pub yang ada didalam komputer kalian jika sudah punya, jiak sudah jangan lupa save.

![2](/stage-2/week-1/deploy-using-aws/img/2.png)

## 3.Untuk membuat vm masuk kedashboard awal dan klik tulisan launch instance.

![3](/stage-2/week-1/deploy-using-aws/img/3.png)

## 4.Disini kita tinggal memasukan nama vm dan sistem operasi yang ingin kita pilih, karna saya nantinya ingin membuat dua vm app server dan gateway, maka pada vm pertama ini saya berinama salman-appserver menggunakan sistem operasi ubuntu.

![4](/stage-2/week-1/deploy-using-aws/img/4.png)

## 5.Selanjutnya mengkonfigurasi Key-pair login yang nantinya akan kita gunakan untuk masuk lewat terminal/ssh, kalian bisa menggunakan key-pair yang sudah dibuat sebelumnya.

![5](/stage-2/week-1/deploy-using-aws/img/5.png)

## 6.Selanjutnya kita akan menkonfigurasi firewall, didalam settingan defaultnya aws akan memberikan tanda centang hanya di bagian allow ssh traffic, kalian bisa mencentang opsi keduanya yaitu http dan https yang nantinya berguna untuk mengakses website yang sudah kita luncurkan, jiak sudah klik launch instance.

![6](/stage-2/week-1/deploy-using-aws/img/6.png)

## 7.Tunggu prosses pembuatan vm sampai selesai, jika sudah kalian bisa klik tombol connect instance untuk masuk kedalam vm, karna aws memiliki opsi yang sangat banyak untuk login kedalam mesin virtual disini kita akan login lewat ssh, dan untuk caranya aws memberi tahu kita dan gambar dibawah berwarna merah, atau kalian juga bisa login dengan `ssh ubuntu@IpPublicKalian`.

![7](/stage-2/week-1/deploy-using-aws/img/7.png)

## 8.Jika berhasil kalian akan masuk kedalam virtual mechine yang barusan kita buat, jangan lupa untuk meng update repositori dulu dengan `sudo apt update -y`.

![8](/stage-2/week-1/deploy-using-aws/img/8.png)

## 9.Jika kalian tertarik untuk mendeploy website dengan aws bisa kunjungi repo saya [wayshub & nginx](https://github.com/sallfarr77/devops17-dumbways-salman-al-farisi/tree/main/stage-2/week-1/wayshub-%26-nginx), dibawah adalah dokumentasi keti saya menjalankan npm start dengan frontend saja.

![9](/stage-2/week-1/deploy-using-aws/img/9.png)

## 10.Selanjutnya saya akan mendeploy website ini dengan menggunakan aws dengan cara yang hampir sama dengan idcloudhost di tugas sebelumnya dengan menggunakan pm2 serta domain yang ada di cloudflare.

![10](/stage-2/week-1/deploy-using-aws/img/10.png)

## 11.Selanjutnya menggetest website kita dan membuat akun dengan alamat email dan juga password.

![11](/stage-2/week-1/deploy-using-aws/img/11.png)

## 12.Login dengan email yang sudah dibuat dan jika berhasil kalian akan masuk kedalam dashboard wayshub seperti dibawah ini.

![12](/stage-2/week-1/deploy-using-aws/img/12.png)

## 13.Sebagai info tambahan kalian juga dapat mencari tahu info tentang website yang telah dibuat dengan [wmtips](https://www.wmtips.com/tools/info/) contohnya seperti lokasi server, dibuat dengan apa dan di handle menggunakan apa. didalam sini website saya di hosted dengan amazon webservice dengan lokasi server yang ada di australian,website dibuat dengan nodejs, serta di handle menggunakan nginx.

![13](/stage-2/week-1/deploy-using-aws/img/13.png)













