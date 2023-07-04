# DEPLOY WAYSHUB VIA IDCLOUD

# Membuat VM

## 1.Membuat Vm Ubuntu di IDCloudHost
  Buatlah akun Idcloudhostnya terlebih dahulu, jika sudah masuk ke console dan pilih Virtual Mechine.
  ![1](/stage-2/week-1/cloud-computing-wayshub/img/1.png)

## 2.Memilih OS, location server, serta spek vm
  Selanjutnya saya akan mmenggunakan OS ubuntu dengan server yang berada di singapure serta spek yang tertera di gambar.
  ![2](/stage-2/week-1/cloud-computing-wayshub/img/2.png)

## 3.Konfigurasi tambahan untuk vm
  Sama seperti di virtualbox/Vmware kita akan membuat username,password dan juga nama Vm, kita bisa melihat estimasi pengeluaran Vm kita berapa rupiah.
  ![3](/stage-2/week-1/cloud-computing-wayshub/img/3.png)

## 4.Membuat VPC baru
  Di dalam idcloud kita akan memndapatkan banyak pilihan salah satunya untuk membeli/membuat jaringan salah satunya adalah VPC, VPC atau Virtual private cloud adalah   layanan cloud computing yang memungkinkan lita untuk membuat jaringan pribadi virtual di lingkungan cloud publik.
  ![4](/stage-2/week-1/cloud-computing-wayshub/img/4.png)

## 5.Cross-check
  Setelah selesai semua harap dilihat dan di pastikan bahwa VM sudah sesuai keinginan dan tujuan dari project serta jangan lupa juga untuk memastikan estimasi cost
  yang tertera, jikalau sudah yakin pilih tombol create.
  ![5](/stage-2/week-1/cloud-computing-wayshub/img/5.png)

## 6.Menunggu prosses
  Setelah VM berhasil dibuat kita akan menunggu prosses building VM kita estimasi waktu 1-2 menit tergantung dari spek serta konfigurasi VM yang kita pilih.
  ![6](/stage-2/week-1/cloud-computing-wayshub/img/6.png)

## 7.Melihat VM yang sudah kita buat
  Setelah menunggu prosses building serta installasi VM kita akan melihat dashboard seperti di bawah ini disini kita akan melihat banyak dari mulai jaringan hingga
  ssh.
  ![7](/stage-2/week-1/cloud-computing-wayshub/img/7.png)

# Deploy Front-end WaysHub

## 1.Login ssh Vm
  Selnajutnya kita bisa langsung masuk dan menjalankan vm kita lewat ssh, disini saya akan menngunakan powershell terminal kita bisa langsung masuk kedalam Vm
  dengan mengetikan format seperti ini "ssh UsernameKamu@AlamatIpKamu" dan ubuntu kita langsung bisa digunakan.
  ![8](/stage-2/week-1/cloud-computing-wayshub/img/8.png)

## 2.Update serta install npm
  jalankan "sudo apt update" untuk mengupdate repositori kita, setelah itu bisa install nginx dengan "sudo apt install nginx, jangan lupa nvm untuk mengatur versi
  npm yang ingin digunakan, setelah nvm di install kita akan gunakan npm versi 14 "nvm use 14". lalu clone repo wayshub dan masuk kedalam foldernya dan install
  dependenci website dengan "npm install".
  ![10](/stage-2/week-1/cloud-computing-wayshub/img/10.png)

## 3.Build and Serve
  setelah selesai jalankan "npm run build" untuk membuat folder build yang nantinya akan kita gunakan untuk meluncurkan website, lalu "npm install -g serve" dan
  install juga pm2 dengan "npm install -g pm2"
  ![11](/stage-2/week-1/cloud-computing-wayshub/img/11.png)

## 4.Serve wayshub with pm2
  Jalankan "pm2 serve build" untuk meluncurkan website WaysHub, disana pm2 akan memberitahu kita bahwa website telah running di port 8080 dan status talah online.
  ![12](/stage-2/week-1/cloud-computing-wayshub/img/12.png)

## 5.Cek Website
  Buka browser dan masukan "Alamat ip kita:8080", disini kita akan melihat website wayshub frond-end telah berjalan dan bisa di akses.
  ![13](/stage-2/week-1/cloud-computing-wayshub/img/13.png)


























