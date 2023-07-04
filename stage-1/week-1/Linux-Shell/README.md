## 1. Berikut adalah 3 comand yang tidak saya temui di ebook beserta penjelasannya.

1. man, man adalah singkatan dari "manual". man adalah perintah pada sistem operasi Linux dan Unix yang digunakan untuk menampilkan manual pengguna untuk perintah, program, atau fungsi tertentu pada sistem tersebut.

2.  vim, Vim adalah salah satu text editor yang populer pada sistem operasi Linux dan Unix. Vim (Vi Improved) merupakan pengembangan dari editor teks yang lebih tua yaitu Vi.

3. less, less adalah salah satu comand pada sistem operasi Linux dan Unix yang digunakan untuk membaca isi dari file teks secara bertahap (page by page). less dapat membaca isi dari file yang sangat besar dengan efisien, karena ia hanya memuat sejumlah kecil data pada satu waktu (less is more). 



## 2. Perbedaan antara bash dan shell

1. BASH (Bourne Again Shell) adalah salah satu jenis shell Linux, sedangkan shell secara umum merujuk kepada antarmuka teks untuk berinteraksi dengan sistem operasi Linux. Jadi BASH adalah jenis khusus dari shell.

2. BASH adalah shell default pada sebagian besar distribusi Linux, sedangkan shell lain yang tersedia misalnya zsh, ksh, tcsh.

3. BASH memiliki fitur lebih kompleks dibandingkan shell umum, misalnya memiliki variabel environment, alias, fungsi, ekspansi string, dll.

4. Script BASH memiliki ekstensi .sh, sedangkan shell lain biasanya menggunakan ekstensi lain tergantung jenis shellnya.

5. Perintah dasar BASH misalnya if, for, while, sedangkan shell secara umum juga mengimplementasikan perintah dasar tersebut namun sintaks atau penulisannya bisa berbeda-beda.


Kesimpulannya adalah bahwa BASH dan shell adalah dua hal yang berbeda, BASH adalah jenis shell Linux khusus yang memiliki fitur yang lebih kompleks daripada shell Linux umumnya. BASH sangat populer dan menjadi shell default dalam sebagian besar distribusi Linux.


## 3. Berikut ini adalah cara saya menginstall dan menjalankan apache di ubuntu server


1. Pertama, pastikan server Ubuntu Anda sudah terkoneksi dengan internet, jika sudah Jalankan perintah `sudo apt update` untuk memperbarui daftar paket pada server Ubuntu.


![1](/week-1/Linux-Shell/img/1.png)


2. Setelah proses pembaruan selesai, jalankan perintah `sudo apt install apache2 -y` untuk menginstal Apache2 pada server Ubuntu.

![2](/week-1/Linux-Shell/img/2.png)


3. Setelah proses instalasi selesai, jalankan perintah `sudo systemctl start apache2` untuk memulai Apache2.

![3](/week-1/Linux-Shell/img/3.png)


4.  Untuk mengakses Apache2 melalui IP Address server, buka browser pada komputer Anda dan ketikkan alamat IP Address server di bar URL, note kalian bisa cek ip lewat ubuntu juga dengan 'ifconfig' comand, kemungkinan bakal harus install net-tools terlebih dahulu, dan jika berhasil tampilannya akan seperti ini.


![4](/week-1/Linux-Shell/img/4.png)


5. Untuk memastikan bahwa Apache2 sedang berjalan, jalankan perintah `sudo systemctl status apache2` pada terminal server Ubuntu. Jika Apache2 sedang berjalan, maka statusnya akan ditampilkan sebagai "active (running)".


![5](/week-1/Linux-Shell/img/5.png)





